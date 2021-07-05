<h1 align="center"> Databases Basics </h1>

### Database

+ Database are a key component of System Design.
+ Operations engineers deploy and manage databases
+ Applications read and write these databases. 

There are mainly 2 types of databases

+ SQL or relation based databases : Databases have been in a tabular format and they stored data in <br />
the form of rows and columns.

+ Non SQL based databases : These databases store information in the form of documnets or pages. These files <br />
can be in any format or structure and changes to one file does not affect the others.

### MySQLSQL Database

+ MySQL is an open-source database, that is fast and realiable.
+ It stores data in Sequel format.

* Use the MySQL client utility to connect the database and it need password
* When the database is installed, it generates a temporary password and that password is logged in log file (/var/log/mysqld.log)
* Using that password in MySQL command-line uility to connect to the database **mysqld -u root -p<PASSWORD>**
* To change the default password **ALTER USER 'root'@'localhost' IDENTIFIED By '<PASSWORD>';**
* To see all the databases on the server **SHOW DATABASES;**
* To create a database **CREATE DATABASE <DATABASE_NAME>;**
* At a time, can use only one database
* To switch database ** USE <DATABASE_NAME>;**
* To create a table **CREATE TABLE <TABLE_NAME> 
					{ 
						<FIELD 1> TYPE[SIZE], 
						<FIELD 2> TYPE[SIZE],
						.,
						.,
						.,
						<FIELD N> TYPE[SIZE]}; **
* To see all the tabless in the database **SHOW TABLES;**
* To add users and restrict the permission to specific action on databases** <br />
**CREATE USER '<USER_NAME>'@'<HOST_ADDRESS>' IDENTIFIED By '<PASSWORD>';** <br />
where if <HOST_ADDRESS> is localhost , then user can access only the databases, which there in local system <br/>
To access databases from all system, use % in <HOST_ADDRESS> . 
* To grant permission to users xon the table in a database <br />
**GRANT <PERMISSION> ON <DATABASE_NAME.TABLE_NAME> TO '<USER_NAME>'@'<HOST_ADDRESS>;**

The following permission can be provided

| Privileges|Description|
|-------|-------|
| ALL PRIVILEGES | Grant all accesses |
| CREATE | Create Databases |
| DROP | Delete Databases |
| DELETE | Delete rows from tables|
| INSERT | Insert rows into table|
| SELECT | Read/Query tables|
| UPDATE | Update rows in tables |

* To check the grants for user 
**SHOW GRANTS FOR '<USER_NAME>'@'<HOST_ADDRESS>'**

### MongoDB Database
+ MongoDB is an open-source, no sequel database.
+ Also known as document database as it stores data in JSON like document format.
+ It is high-performance scalable database.

* MongoDB is no sequel database and stores data as a document.
* Multiple document together form a collection.
* Multiple collection together form a database.
* These multiple database forms a MongoDB server.
* The logs are stores in Logs file (/var/log/mongodb/mongodb.log)
* Can change the configuration for mongodb server in conf file(/etc/mongodb.conf) 
* To switch database ** USE <DATABASE_NAME>;**
* To check the current working database **db**
* To create collection **db.createcollection("<COLLECTION_NAME>")**
* To collection **SHOW COLLECTIONS**
* to retreive data from the database **<DATABASE_NAME>.<COLLECTION_NAME> find()**

### Labs

1. MySQL - Installlation, Create DB,TABLES, connect the database and grant permission to the user.
2. MongoDB - Create Collection, create documents, retreieve data etc.