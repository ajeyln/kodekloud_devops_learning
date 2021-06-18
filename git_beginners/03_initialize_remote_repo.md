<h1 align="center"> Initialize Remote Repositories </h1>

Images used in this file are downloaded from internet. These are used only for learning purpose.

### Connection of Remote Repository

Remote repository is centralized server and it is optional. Data can be pushed to remote server after got commited. 
We can push code to this remote repository that is hosted somewhere else and get this code again in local machines. 

We can connect the remote repository using connection string. It is a URL that we can use in order to let Git know where the remote repository is located.

+ git remote add origin <URL> - to connect the remote repository from local directory.
+ git remote -v - to list all remote repository
+ git push origin master - to push data to remote repository, Here origin is alias of remote repository and master is branch.

### Cloning of Remote repository

User having access remote repository can clone the repository in order to get all the data to local machines.

+ git clone <ssh link> - to clone the remote repository, where ssh link is the URL of the remote repository.

![SSH LINK](./images/ssh_link.jpg)

### Pull Request

When Team member created and pushed the data to branches in Remote repository. <br />
We can to merge these branches with master  using **Pull Request**

#### Steps to be followed to merge branch  with master file in remote repository.

 1. git push origin <branch_name> - which pushes the data to branches in remote repository. 
 2. login to remote repository and it shows "This branch is 1 commit to <branch_name>
 3. In order to merge <branch_name> with master, we need to click on the pull request.
 ![PULL REQUEST 01 ](./images/pr_01.jpg)
 ![PULL REQUEST 02 ](./images/pr_02.jpg)
 4. We can add the reviewers, labels and description.
 5. Once pull request is done, other team memeber can check the changes.
 6. Lastly, can merge with master by clicking on merge pull request.
  ![PULL REQUEST 03 ](./images/pr_03.jpg)



### Labs

1. Remote Repository - connection, push the data, deletion of repository
2. Cloning remote repository - cloning, check commits etc.