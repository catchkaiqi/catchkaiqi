---
title: GitHub Commands Summary
tags: [GitHub, Git, Terminal, Commands]
style: fill
color: primary
description: for macOS terminal
---
## Commonly-used commands

git log

git diff (commit id) (commit id)

git diff: give u difference of staging area and the working directory

git diff --staged: give u difference between the staging area and the repository

To get colored diff output, run git config --global color.ui auto

git log –stat: give some statistics about which files have changed in each commit.

git clone http://github.com/udacity/asteroids.git

git checkout commit id

To restore a previous version

git reset --hard: discards any changes in either the working directory or the staging area


mv from_directory to_directory

## creating a repository
first go to a file directory

git init

git status: show which files have changed since the last commit

git add filename.txt: add a file to the staging area

git reset filename.txt: the file will be removed from the staging area, but it will still be in your working directory


## Git commit
A commit is a snapshot of a Git repository


git commit -m "Commit message - write a commit message

first git checkout master, then commit, then the HEAD isn’t detached, and commit goes directly to the master branch

## Branch

git branch: list all branches

git branch new_branch_name: create a new branch with the new name

git checkout new_branch_name: goes to new branch

git log --graph --oneline master coins: see the visual representation of the commit history of master branch and coins branch

git checkout –b new_branch_name: create a branch and checkout there

git gc: manual garbage collection (automatical)

## Merge

git merge branch_1 branch_2: merge branch_2 into branch_1

git show commit_id: show difference of the commit and its parent commit

git branch –d coins: delete the branch “coins”

git branch –a: show all branches, including origin/HEAD 

## What is a README?
Many projects contain a file named "README" that gives a general description of what the project does and how to use it.
Initialize this repository with a README: when creating a repository before I had created any content


## Remote
git remote: show current remote

git remote add origin https://github.com/catchcheng/reflections.git

add the url repository as a remote, with the name “origin”

git remote –v: output more info, shows both the url where I’d fetch data from, and the url I’d push data to

git remote set-url origin https://github.com/catchcheng/reflections.git: change remote to

git push origin master: push the master branch to the remote, so in the url, u’ll find a master branch there

git pull origin master: pull the master branch of the remote to the current branch

the local master will change, however, the working directory and staging area will also update when you run git pull

git fetch: if there are changes locally and remotely, then this will update origin master branch to the remote repository, instead of the local master branch.

git pull origin master = git fetch origin + git merge master origin/master

Fast-forward merges, merge b into a is a fast-forward merge if a is b’s ancestor.


### Git Errors and Warnings Solution
##### Should not be doing an octopus

Octopus is a strategy Git uses to combine many different versions of code together. This message can appear if you try to use this strategy in an inappropriate situation.

##### You are in 'detached HEAD' state
HEAD is what Git calls the commit you are currently on. You can “detach” the HEAD by switching to a previous commit, which we’ll see in the next video. Despite what it sounds like, it’s actually not a bad thing to detach the HEAD. Git just warns you so that you’ll realize you’re doing it.

#### Panic! (the 'impossible' happened)
This is a real error message, but it’s not output by Git. Instead it’s output by GHC, the compiler for a programming language called Haskell. It’s reserved for particularly surprising errors!

