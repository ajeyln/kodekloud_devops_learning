<h1 align="center"> Command Sets </h1>

This file contains all the commands, which are used in Git operations.

## Git Introduction

+ **Git information and installation** 
	* cat /etc/*release* : to find the working operating system.
	* sudo apt update : system updation before installation of any application in linux based system.
	* sudo apt-get install git -y : to install git in linux based system.
	* brew install git : to install Git
	* git --version : to find the version of git (only if git is installed)
	* git help : to get information about git commands
	
+ **Git initialization, commit and status** 
	* git init : Initialises a Git repository in that directory
	* git config user.name "<USER_NAME>" : Setting up user name for Git 
	* git config user.email "<EMAIL ADDRESS>" : setting up email address 
	* git add <FILE_NAME> : the files moves to the staging area and which will soon to be commited
	* git commit -m "<MESSAGE>" : to commit the file with meaningful message so that other user can understand 
	* git log : Shows a log of past commits information with commit:id author, date and time commit, commit messages etc 
	* git log --oneline : shows the commit with commit:id and commit messages
	* git log --name-only :  shows the log  of past commits with file name 
	* git log --max-count 3 or git log -n 3 : lists the last 3 commits 
	* git status : Shows status, including what branch you are on and what changes are staged 
	* git restore <FILE_NAME> : discard changes in working area
	* git restore --stages <FILE_NAME> : to move back to working area from staging area 
	* git rm --cached <FILE_NAME> :  move back to working area from staging area 
	* git rm --f <FILE_NAME> : force delete the file from staging area 
	* .gitignore  : this file contains the <FILE_NAME> which should be ignored
	* echo ".gitignore" >> .gitignore : this command makes .gitignore file should be ignored.

## Git Branch & Merging

+ **Git commands related branches & merging**
	* git branch <BRANCH_NAME> : creation of new branch.
	* git checkout <BRANCH_NAME> : to switch the branch to branch.
	* git checkout -b <BRANCH_NAME> : creation of new branch and switching to it.
	* git checkout -d <BRANCH_NAME> : to delete the branch.
	* git branch : Check the list of branches in directory.
	* git fetch : Download objects and refs from another repository
	* git merge <BRANCH_NAME> - merging the branch with master

## Initialize Remote Repository 

+ **Connection of Remote Repository & Cloning**
	* git remote add origin <URL> : to connect the remote repository from local directory.
	* git remote -v : to list all remote repository
	* git push origin master : to push data to remote repository, Here origin is alias of remote repository and master is branch.
	* git clone <SSH_LINK> - to clone the remote repository, where ssh link is the URL of the remote repository.

+ **Fetching and Merging**
	* git fetch origin master : to update the origin master branch in local repository
	* gir merge origin/master : to merge origin master with local master
	* git pull origin master : to fetch the origin master branch and merge origin master with local master.

## Rebasing

+ **Rebasing and Interactive Rebase**
	* git rebase master :  Reapply commits on top of another(master branch) base tip.
	* git rebase -i Head~<No.of COMMITS> : modifying the git history of multiple commits, Where no.of commits is number of lastest commits
	* git cherry-picking <COMMIT_ID> - to copy the commit onto the branch, where commit-hash is hash id of commit that we are using current branch.

## Resetting & Revert

+ **Resetting & Revert**
	* git revert <COMMIT_ID> : this command creates the new commit, which reverse all changes were made in <COMMIT ID>
	* git reset --soft HEAD~<No.of COMMITS> : to keep all the changes that were made on no.of commits after reset operation, Where no.of commits are the latest commits.
	* git reset --hard HEAD~<No.of COMMITS> : to lose all the changes that were made on no.of commits after reset operation, Where no.of commits is number of latest commits.

+ **Stashing** 
	* git stash : to clear the files in working area and moving the file in temporary location.
	* git stash pop : to retrieve the files from tempoary location which already stashed.
	* git stash list : to list out the no.of stash file in temporarylocation
	* git stash show <STASH No.> : to show the content of file for specific stash
	* git stash pop <STASH No.> : to retrieve the specific stash file.

+ **Refolg**
	* git refolg : to show the all actions have taken on repository (merge, resets, reverts or any alternation.)

