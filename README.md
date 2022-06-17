# python-learning-project

Let's get started with some Git.

This project has a master branch and a staging branch.  The master branch can be considered the production branch.  When the application is deployed, the deployed production code should always match the master branch.  The staging branch can be considered a testing environment. Staging closely matches master except what code changes are being tested.

## Getting Started
the first thing you will do, assuming you have git installed and set up is clone down the project.  This can be done with git clone.  

**git clone https://github.com/Havko/python-learning-project.git**

The above command will clone the repository down to your local machine.  Git does not require github, git exists to track all code changes through commits.  Github simply serves as a remote repository to enable sharing and collaborating on code bases.  You will use git locally to track your code changes and then push these changes to the remote repository in github.

## Feature Branches
Feature Branches are what you will develop your code in.  When ever you start developing you will ensure that you are developing from the most recent version of master or staging(we will work off of staging).  Make sure you are using the staging branch with the following command
**git fetch**
**git pull**

Git fetch will get all changes from the remote repository in github.  Git pull will pull any new changes into your currently checked out local branch.

Next you will run 
**git branch {branch_name}**(branch_name being whatever you want to call the branch.)
Git branch will simply create the new branch but it will not check it out.  Next you will use 
**Git checkout {new_branch}**(whatever you just named the branch)
You should now be on your new branch.  You can verify this by typing git branch

**Git Status**
Git status will tell you what branch you are one and what code changes you have made.  

Whenever you change existing files or add new files, you have to add them to a commit to be tracked by git.  git status will show you all changes that are not being tracked in a commit.  Commits are what make git so powerful.  We will dig deeper in to commits later. To stage a change to be commited simply type
**git add {path_to_file}**
This will "stage" the change to be committed.  
**git commit -m "{your commit message}"**
Git commit will add all of your staged changes to a commit.  You can think of a commit as a snapshot of the code at a given point in time.  As you make changes you will continue to capture them in commits.  It is wise to keep commits small so that you have a better picture of how the code changes over time.  Finally, it is time for you to share your changes with your team on git hub.  Git Push is how you send your changes to the remote repository on github.  

**git push origin {branch_name}**

assuming you have commits that do not exist on the remote repository this command will push the commits to the remote branch.  You can push directly to staging or master, but in shared development environment this will not likely be the case.  

## Pull Requests
Once the code is up into git hub and you feel good about the code, you will open a pull request to merge the code changes in to staging/master.  A pull request gives an opportunity for the team to review the code changes before they are merged into the main branches.

## Summary of important commands
**git clone** - git clone copies the repository to your local system.  You will generally only have to do this once.
**git checkout** - git checkout will checkout a branh.
**git status** - tells you what branch you are on and what files you have changed.
**git add {path_to_file}** - stages changes for a commit 
**git commit -m "Commit message"** - adds changes to a commit.  the -m flag adds a commit message that should describe the changes.
**git push origin {branch_name}** - pushes local commits to branch on github.  Creates the remote branch if it does not exist.

These commands are really only the basic commands needed to start using git but they are only a small subset of git commands that are available.

## Challenges
Go ahead and clone the repository.  Make a new branch with whatever name you would like.  Make sure to check out the branch.  Go ahead and add a new text file with some text and commit this change.  Then modify the text file and commit that change.  Then push these commits to this project in github.  When you are done there should be a new branch on this github that contains 2 new commits.  Once this is completed we will talk about opening a pull request.
