<h1 align="center"> GIT Introduction </h1>

### Repository types

There are two types repositories in git

#### 1. Local Repository

+ The local repository is own local machine which we have direct access.

It consists of three stages 

a. **Working area** - In this stage,the files are not handled by git and these files are also referred to as "untracked files". <br /> 
It is where we can add new content or modify/delete content in file. 
	
b. **Staging area** - The files in this stage will soon be commited. Git knows what is going to change between the current commit and the next one. <br />
	
c. **commited file** - We can commit our changes in order to add version control to the project.

![Local Repository stages](./images/local_repo.jpg)
	

#### 2. Remote Repository :- 
	+ Remote repository is centralized server and it is optional. Data can be pushed to remote server after got commited.
	+ As servers are centralized, Teammates can initilize their own local repository and pull/push  the data from/to server.
	+ In order to keep local and remote repository in sync, can pull the changes from remote server to local repository.
	+ Data can be retrieve from Remote repository, if local system got crashed or unavailable.
	
![Remote Repository stages](./images/remote_repo.jpg)

