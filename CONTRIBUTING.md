# How do I contribute?

## What needs to be done?


All issues related to the 3T project are on the 
[TopRanker Project Management Page](https://github.com/Outige/foo/projects/1).

If you would like to add an issue, first make sure that no similar issue already exists. If one exists then simply add any
useful findings. When creating a new issue you will be given a template - please make use of these as they enforce 
descriptive and well thought out solutions/fixes.

## What do I need to know before making changes?
This application aims to satisfy the full delevopment stack. The three layers can be found in their respective directories:
* `api`: Python + Flask
* `client`: React.js
* `db`: PostgreSQL
Further layer-specific instructions will be added in their respective directories, TBD.

## Making changes / Branching

Before making a change, create a branch off of `master` with one of the following prefixes to describe it's purpose:
* `feat/`: For adding a new feature.
* `fix/`: For fixing a bug.
* `refactor/`: For any architectural changes, moving or renaming files/directories.
* `docs/`: For any purely documentation related changes
* `ci/`: For any continuous integration additions or changes.

Remember to check your project branches to make sure that your branch is up to date with `master`. If you are a number of commits behind then you should rebase.The following steps are how you can do this:
```
git fetch
git checkout master
git pull
git checkout <your branch>
git rebase -i master
# Your commits will be applied to the tip of master and you
# may need to resolve conflicts with:
git commit <resolved files>
git rebase --continue
```

## Git Commits

The following [emojis](https://gitmoji.carloscuesta.me/) are to be prefixed with a short and concise commit title:
* :art: `:art:` Improving structure / format of the code.
* :zap: `:zap:` Improving performance.
* :fire: `:fire:` Removing code or files.
* :bug: `:bug:` Fixing a bug.
* :ambulance: `:ambulance:` Critical hotfix.
* :sparkles: `:sparkles:` Introducing new features.
* :pencil: `:pencil:` Writing docs.
* :lipstick: `:lipstick:` Updating the UI and style files.
* :tada: `:tada:` Initial commit.
* :white_check_mark: `:white_check_mark:` Updating tests.
* :lock: `:lock:` Fixing security issues.
* :construction: `:construction:` Work in progress.
* :green_heart: `:green_heart:` Fixing CI Build.
* :arrow_down: `:arrow_down:` Downgrading dependencies.
* :arrow_up: `:arrow_up:` Upgrading dependencies.
* :recycle: `:recycle:` Refactoring code.
* :chart_with_upwards_trend: `:chart_with_upwards_trend:` Adding analytics or tracking code.
* :heavy_plus_sign: `:heavy_plus_sign:` Adding a dependency.
* :heavy_minus_sign: `:heavy_minus_sign:` Removing a dependency.
* :wrench: `:wrench:` Changing configuration files.
* :globe_with_meridians: `:globe_with_meridians:` Internationalization and localization.
* :pencil2: `:pencil2:` Fixing typos.
* :twisted_rightwards_arrows: `:twisted_rightwards_arrows:` Merging branches.
* :truck: `:truck:` Moving or renaming files.
* :page_facing_up: `:page_facing_up:` Adding or updating license.
* :bento: `:bento:` Adding or updating assets.
* :card_file_box: `:card_file_box:` Performing database related changes.
* :building_construction: `:building_construction:` Making architectural changes.
* :see_no_evil: `:see_no_evil:` Adding or updating .gitignore file.
* :goal_net: `:goal_net:` Catching errors.
* :dizzy: `:dizzy:` Adding or updating animations and transitions

Anything beyond 50 characters needs to be placed in the description in bullet form.

## Pull requests

Pull requests are to be used when merging your branch into `master`. If your branch is behind use the "Rebase and commit" 
option or simply "Merge and commit". We will use "Squash and commit" if the commits are strictly concerned with a single 
changes.
You should squash your commits into a 1-3 meaningful ones if there are any superfluous or excessively large number of commits
in your branch. This is how you can squash your commits
```
git rebase -i HEAD~N
```
N refers to the amount of commits from head you want to squash e.g. If you want to squash the last two then use `HEAD~2`.
You will then get prompted by a text editor twice. The first time to pick and squash commits, the second to resolve commit
messages. For a more in-depth tutorial see [this link](https://medium.com/@slamflipstrom/a-beginners-guide-to-squashing-commits-with-git-rebase-8185cf6e62ec).

When making a pull request, please make use of the templates in each repository.
