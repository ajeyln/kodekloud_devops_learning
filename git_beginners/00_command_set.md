<h1 align="center"> Command Sets </h1>

This file contains all the commands, which are used in Git operations.

## Git Introduction

+ **Git information and installation** <br />
	* cat /etc/*release* - to find the working operating system.
	* sudo apt update - system updation before installation of any application in linux based system.
	* sudo apt-get install git -y - to install git in linux based system.
	* brew install git - to install Git
	* git --version - to find the version of git (only if git is installed)
	* git help - to get information about git commands
	
+ **git initialization, commit and status** <br />
	* git init - Initialises a Git repository in that directory
	* git config user.name "username" - Setting up user name for Git 
	* git config user.email "email address" - setting up email address 
	* git add file_name - the files moves to the staging area and which will soon to be commited
	* git commit -m <message> - to commit the file with meaningful message so that other user can understand 
	* git log - Shows a log of past commits information with commit-id author, date and time commit, commit messages etc 
	* git log --oneline - shows the commit with commit-id and commit messages
	* git log --name-only -  shows the log  of past commits with file name 
	* git log --max-count 3 or git log -n 3 - lists the last 3 commits 
	* git status - Shows status, including what branch you are on and what changes are staged 
	* git restore file_name - discard changes in working area
	* git restore --stages file_name - to move back to working area from staging area 
	* git rm --cached file_name -  move back to working area from staging area 
	* git rm --f file_name - force delete the file from staging area 
	* .gitignore  - this file contains the file_name which should be ignored
	* echo ".gitignore" >> .gitignore - this command makes .gitignore file should be ignored.

## Git Branch & Merging

+ **Git commands related branches** <br />
	* git branch <branch name> - creation of new branch.
	* git checkout <branch name> - to switch the branch to branch.
	* git checkout -b <branch name> - creation of new branch and switching to it.
	* git checkout -d <branch name> - to delete the branch.
	* git branch - Check the list of branches in directory.


