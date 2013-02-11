Git Basics
============

### Prerequisites

* git
* cygwin or other terminal
* an ssh key


### Getting started

First, make an account on [bitbucket] and send me your new account name via Facebook. I'll then add you to the bitbucket repository. You'll need to add your ssh key to your bitbucket account under Account Settings. You should now be able to view the [UnityGame] respository. You should see a link for it when you're logged in to bitbucket.

To download the project, open up cygwin, navigate to an appropriate directory, and type:

`git clone git@bitbucket.org:devinabbott/unitygame.git`

NOTE: this will create a new directory called `unitygame` in your current working directory. The project will be downloaded from bitbucket into this directory.

### Basic Commands

There are 5 main commands you'll use with git.

`git pull` - download any new changes made by other people from the shared repository on bitbucket

`git push` - upload any new changes that you made on your local repository to the shared repository

`git add` - tell git which files are important (you must do this before each commit)

`git commit` - permanently save any changes to files added with `git add`. You can only `git push` after you `git commit`.

`git status` - get info on the current status of your local repository (which files have been modified, commited, etc)


### Using Git

When you `git clone` a project, git downloads the most up-to-date version of the project. Any time you're going to start making changes, you should `git pull` to download recent updates made by other people. This ensures that you're working with the latest version of every file.

If you're not sure about the status of your current repository, you can check on the details with `git status`. You can also use `git log -5` (or any other number) to view the 5 most recent commits. They should match the most recent commits on bitbucket. If you're missing a commit, then your copy of the project is out of date.

When you're going to make a change, it's usually best to follow these 5 steps:

1. `git status` - make sure git says you have uncommitted changes
2. `git add .` - tell git you want to commit every file. NOTE: if git asks you if you would like to force it to add files with -f, do not do this!
3. `git commit -m "Briefly explain the changes you made."`
4. `git pull` - check for new changes made since you started working. Resolve any conflicts if they arrise (best to discuss this with whoever made the conflicting commit)
5. `git push` - upload your commit to the shared repository.


### Other Useful Commands

* `git stash` - Sometimes when you try to `git pull`, git will say that you've made changes even when you haven't (this can happen when you open Unity, which automatically makes a few changes). Use `git stash` to 'erase' any local changes so that you can successfully `git pull`. Changes 'erased' with `git stash` can be recovered later, if necessary.

[bitbucket]: https://bitbucket.org/
[UnityGame]: https://bitbucket.org/devinabbott/unitygame
