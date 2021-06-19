<h1 align="center"> Command Sets </h1>

This file contains all the commands, which are used in Git operations.

## Git Introduction

+ **Git information and installation** <br />
	* cat /etc/*release* : to find the working operating system.
	* sudo apt update : system updation before installation of any application in linux based system.
	* sudo apt-get install git -y : to install git in linux based system.
	* brew install git : to install Git
	* git --version : to find the version of git (only if git is installed)
	* git help : to get information about git commands
	
+ **Git initialization, commit and status** <br />
	* git init : Initialises a Git repository in that directory
	* git config user.name <"username"> : Setting up user name for Git 
	* git config user.email <"email address"> : setting up email address 
	* git add <file name> : the files moves to the staging area and which will soon to be commited
	* git commit -m <message> : to commit the file with meaningful message so that other user can understand 
	* git log : Shows a log of past commits information with commit:id author, date and time commit, commit messages etc 
	* git log --oneline : shows the commit with commit:id and commit messages
	* git log --name-only :  shows the log  of past commits with file name 
	* git log --max-count 3 or git log -n 3 : lists the last 3 commits 
	* git status : Shows status, including what branch you are on and what changes are staged 
	* git restore <file name> : discard changes in working area
	* git restore --stages <file name> : to move back to working area from staging area 
	* git rm --cached <file name> :  move back to working area from staging area 
	* git rm --f <file name> : force delete the file from staging area 
	* .gitignore  : this file contains the <file name> which should be ignored
	* echo ".gitignore" >> .gitignore : this command makes .gitignore file should be ignored.

## Git Branch & Merging

+ **Git commands related branches & merging** <br />
	* git branch <branch name> : creation of new branch.
	* git checkout <branch name> : to switch the branch to branch.
	* git checkout -b <branch name> : creation of new branch and switching to it.
	* git checkout -d <branch name> : to delete the branch.
	* git branch : Check the list of branches in directory.
	* git fetch : Download objects and refs from another repository
	* git merge <branch name> - merging the branch with master

## Initialize Remote Repository 

+ **Connection of Remote Repository & Cloning**** <br />
	* git remote add origin <URL> : to connect the remote repository from local directory.
	* git remote -v : to list all remote repository
	* git push origin master : to push data to remote repository, Here origin is alias of remote repository and master is branch.
	* git clone <ssh link> - to clone the remote repository, where ssh link is the URL of the remote repository.

+ **Fetching and Merging** <br />
	* git fetch origin master : to update the origin master branch in local repository
	* gir merge origin/master : to merge origin master with local master
	* git pull origin master : to fetch the origin master branch and merge origin master with local master. 


