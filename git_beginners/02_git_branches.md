<h1 align="center"> GIT Branches </h1>

### Branches
	+ Master is the default branch in Git.
	+ Branches provide an isolated environment for every changes of codes
	+ Also, it ensure the master branch always contains production-quality code.

### Git commands related branches

| Command | Description |
|------|-------|
| git branch <branch name> | creation of new branch  |
| git checkout <branch name> | to switch the branch to branch |
| git checkout -b <branch name> | creation of new branch and switching to it |
| git checkout -d <branch name> | to delete the branch |
| git branch | Check the list of branches in directory |

* HEAD point to the last commit in the branch that we are working on.

### Git Merging

After the testing has done in branch and want to merge with master, we can use merge method to do it.

Steps:
1. Switch to master using **git checkout master**
2. git merge <branch name> :  to merge the branch with master


### Labs

1. Branches - checkout, push branches, switch branches etc.
2. Merging - Merging branches
