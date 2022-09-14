# Topic: BRANCHES in GIT

### what is a branch in terms of GIT?
>In Git, branches are a part of your everyday development process. Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes.

### How it works?
>A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

>The **git branch** command lets you create, list, rename, and delete branches. It doesn’t let you switch between branches or put a forked history back together again. For this reason, git branch is tightly integrated with the git checkout and git merge commands.

### Some of the commands related to this:
#### To create a new branch:
```
git branch <branch-name>
```
### To List out all the branches:
```
git branch --list
```
### To Delete the specific branch:
```
git branch -d <branch-name>
```
### Force Delete:
```
git branch -D <branch-name>
```
### To List all the remote branches:
```
git branch -a
```
### To Switch another branch from main:
```
git checkout <branch-name>
```

