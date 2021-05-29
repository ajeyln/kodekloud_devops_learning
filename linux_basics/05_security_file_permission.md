<h1 align="center"> Security & File Permission </h1>

### Linux Security
+ Access Controls - to determine who can access the system.
+ PAM(Plugable Authentication Model) - used authenticate users to program and service linux
+ Network Security - Restrict or allow access to services on server 
+ SSH(Secure Shell) hardening - Only autherised user have access remote server
+ SeLinux - using security policies, isolating applicationone the system.

### Account Types

+ User Account - maintain information about user (UID,username, password)
	* cat /etc/passwd - info about user account
	* each user has unique identifier - UID
	* User can have access for multiple groups, but has only one UID
	* id username - to find the information about user details such as UID, GID etc.
	
+ Group account - Based on common attribute such as role or function
	* cat /etc/group - info about user group
	* each group has unique identifier - GID

+ Super User - has unrestricted access over the system and his UID is 0
	* cat /etc/sudoers - to check information who can switch to super user
	* only users listed in the /etc/sodoers can make use of sudo command
	
### Managing User

* useradd username - to create a local user account in Linux
* grep -i username /etc/passwd - to check info about user
* passwd username - to set password
* passwd - to change password
* userdel username - to delete user
* groupadd groupname - to add group
* groupdel groupname - to delete group

#### coments during creation of user or group

+ -c - custom comments
+ -d - to specify home directory path
+ -e - to specify the account expiration date
+ -u  - to customize UID
+ -g - to customize GID

### Access Contols

* grep -i ^username /etc/passwd - info about user <br />
  Output of the command shows in the following sequence
  username:password:UID:GID:GECOS:homedir:shell
  
* grep -i ^username /etc/shadow - info about user with password <br />
  Output of the command shows in the following sequence
  username:password:lastchange:minage:maxage:warn:inactive:expdate
  
* grep -i ^username /etc/group - group info about user <br />
  Output of the command shows in the following sequence
  groupname:password:GID:members

### File Permission & ownership

* ls -l filename - to check the userpermission <p>

|Bit| Purpose| Octal Value|
|----|------| -------|
| r| read| 4|
|w| write| 2|
|x| execute | 1|
|| no permission| -|

#### Modifying permission

* chmod <permssion> file - to change the mode of the permission
* chmod u+rwx filename - to give full access to the user
* chmod ugo+r-x filename - to give read and execute permission to all
* chmod o-rwx filename - to remove all access to other
* chmod u+rwx,go-w- - to give full access and read and execute permission to group and others
* chmod 777 filename - to give full access to all

#### Modifying ownership and group

* chown owner:groupname filename - to change the owner and group
* chown owner filename - change ownership
* chgrp gropuname filename - to change group



	
