<h1 align="center"> Source Control Management (GIT) </h1>

Version control systems is the practice of tracking and managing changes to software code. <br />
Git is the one of Version control systems that help software teams manage changes to source code over time.

#### Local Repository

+ The local repository is own local machine which we have direct access.

It consists of three stages 

a. **Working area** - In this stage,the files are not handled by git and these files are also referred to as "untracked files". <br /> 
It is where we can add new content or modify/delete content in file. 
	
b. **Staging area** - The files in this stage will soon be commited. Git knows what is going to change between the current commit and the next one. <br />
	
c. **Commited file** - We can commit our changes in order to add version control to the project.

#### Remote Repository

+ Remote repository is centralized server and it is optional. Data can be pushed to remote server after got commited.
+ As servers are centralized, Teammates can initilize their own local repository and pull/push  the data from/to server.
+ In order to keep local and remote repository in sync, can pull the changes from remote server to local repository.
+ Data can be retrieve from Remote repository, if local system got crashed or unavailable.

### Some of the git commands

| Command | Description |
|------|-------|
| git init | Initialises a Git repository in that directory|
| git config user.name "<USER_NAME>" | setting up user name for Git |
| git config user.email "<EMAIL ADDRESS>" | setting up email address |
| git add <FILE_NAME>  | the files moves to the staging area and which will soon to be commited|
| git commit -m "<MESSAGE>" | to commit the file with meaningful message so that other user can understand |
| git log | Shows a log of past commits information with commit-id author, date and time commit, commit messages etc |
| git log --oneline |  shows the commit with commit-id and commit messages |
| git log --name-only |  shows the log  of past commits with file name |
| git log --max-count 3 or git log -n 3 | lists the last 3 commits |
| git status | Shows status, including what branch you are on and what changes are staged |
| git restore <FILE_NAME>  | discard changes in working area|
| git restore --stages file_name | to move back to working area from staging area |
| git rm --cached <FILE_NAME>  |  move back to working area from staging area |
| git rm --f <FILE_NAME>  | force delete the file from staging area |

+ .gitignore  - this file contains the <FILE_NAME>  which should be ignored
+ echo ".gitignore" >> .gitignore - this command makes .gitignore file should be ignored.

### Labs

1. GIT - basic configuration such as initiating, commit and push the source code to Git Hub
2. GIT Repository - configuration of remote repositories, pull and cloning the data from Git hub to local system.