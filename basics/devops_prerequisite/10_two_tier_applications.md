<h1 align="center"> 2-Tier Applications </h1>

## Seting-up Lab Enviornment 

Steps to be followed for Setting-up Lab enviornment

1. Identifying a System on which we will deploy the application. Installing firewall, enable and start the firewalld services.
	* sudo yum install firewalld
	* sudo service firewalld start
	* sudo systemctl enable firewalld
	
2. Installing and Configuring the Web Server (Apche httpd) Server, enable and start the service.
	* sudo yum install -y httpd
	* sudo vi /etc/httpd/conf/httpd.conf # configure DirectoryIndex to use index.php instead of index.html
	* sudo service httpd start
	* sudo systemctl enable httpd
	
3. Installing and Configuring the Databases (My SQL, MariaDB etc.), enable and start the database services.
	* sudo yum install mariadb-server
	* sudo vi /etc/my.cnf # configure the file with the right port
	* sudo service mariadb start
	* sudo systemctl enable mariadb
	* sudo firewall-cmd --permanent --zone=public --add-port=3306/tcp
	* sudo firewall --cmd  --reload
	* mysql # configuring the database
	* CREATE DATABASE <DATABASE_NAME>;
	* CREATE USER '<USER_NAME>'@'<HOST_ADDRESS>' IDENTIFIED By '<PASSWORD>';
	* GRANT <PERMISSION> ON <DATABASE_NAME.TABLE_NAME> TO '<USER_NAME>'@'<HOST_ADDRESS>;
	* FLUSH PREVILEGES;
	* db-load-<SCRIPT>.sql
	
4. Installing and configuring the application (php, java, python etc.) on the server.
	* sudo yum install -y php php-mysql
	* sudo firewall-cmd --permanent --zone=public --add-port=80/tcp
	* sudo firewall --cmd  --reload
	
5. Any other requirement or dependencies such as firewall on server to create the necessary rule 
to enable communication between server and applications or databases etc.


### Labs

1. Setup E-Comerce application - Installing and configuring the 2-Tier Lab enviornment, Testing.
