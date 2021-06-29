<h1 align="center"> Linux basics </h1>

### Basic commands

+ PWD : present working directory, which prints the present directory currently working on <br/>
+ ls:  list, which the content of the directory <br/>
+ mkdir -p <FILE_PATH> : to create new directory, -p make directory hiearchy <br/>
+ mv <CURRENT_WORKING_PATH> <DESTINATION_PATH>: to move directory/file from current directory to destination <br/>
+ cp -r <CURRENT_WORKING_PATH> <DESTINATION_PATH>: to copy the file from current directory to destination <br/>
+ rm <FILE_NAME> : to remove file/s <br/>
+ touch <FILE_NAME> : to create a file  <br/>
+ cat <FILE_NAME> : to view the content in the file <br />

### vi Editor

* vi directory/filename - to create file

**Operation Modes**

* command Mode(esc): enter "esc" to go to command mode
* Insert Mode(i): enter "i" before insert/delete value
* Last line Mode(:) : enter ":" before save/discard file

+ yy : copy the line
+ p : paste copied line
+ dd : to delete line
+ d"n"d : to delete n no. of lines
+ u : undo
+ r :redo
+ /word : to find the word 
+ n : move next line
+ N : move previous line
+ :w : to save
+ :wq : to save and quit
+ :q! : quit without saving

### Package Management

### RPM(RedHat Package manager) - Low level package manager

+ Installation : **rpm -ivh packagename.rpm**
+ Uninstallation : **rpm -e packagename.rpm**
+ Upgradation : **rpm -Uvh packagename.rpm**
+ Query : **rpm -q packagename.rpm**
+ Verify : **rpm -Vf <path to file>**

### YUM(Yellowdog Update Modified) - Due to dependency issues

+ RPM based distribution
+ Software Repositories (Collection of packages -/etc/yum.repos.d/package)
+ High level package manager
+ Automatic Dependency Resolution

* yum install package
* yum reporlist - repolists
* yum provide package - to check dependency of package
* yum remove package
* yum update package

### Services

A service is a process or group of processes running continuously in the background.

##### commands under systemctl

* systemctl start <SERVICE_NAME> :  start the service
* systemctl stop <SERVICE_NAME> :  stop the service
* systemctl restart <SERVICE_NAME> :  restartstart the service
* systemctl reload <SERVICE_NAME> :  reload the service
* systemctl enable <SERVICE_NAME> :  enable the service
* systemctl disable <SERVICE_NAME> :  disable the service
* systemctl status <SERVICE_NAME> :  info(status) the service
* systemctl edit <SERVICE_NAME> : to edit configuration service file

### Labs

1. Working with the shell : basic command such as mkdir, cp ls etc.
2. vi editor : editing, copy , delet in vi editor
3. Package Management : Installed packages using YUM and RPM , eg: YUM Install, rpm -ivh etc.
4. Services : Service start,stop, enable, disable, status etc.
