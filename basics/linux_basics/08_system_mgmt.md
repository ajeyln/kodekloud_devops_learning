<h1 align="center"> Storage </h1>

### SYSTEMD Service

* creation of service<p>
	ExecStart = /etc/systemd/system/project.service
* systemctl start project.service - to run the service in background
* systemctl status project.service - to check status of the service
* systemctl stop project.service - to stop the service
* systemctl daemon-reload - to reload the service

### SYSTEMD Tools

* Systemctl 
	+ Manage system state
	+ Start/Stop/Restart/Reload
	+ Enable/Disable
	+ List and Manage Unit
	+ List and Update Targets

##### commands under systemctl

* systemctl start <service name> -  start the service
* systemctl stop <service name> -  stop the service
* systemctl restart <service name> -  restartstart the service
* systemctl reload <service name> -  reload the service
* systemctl enable <service name> -  enable the service
* systemctl disable <service name> -  disable the service
* systemctl status <service name> -  info(status) the service
* systemctl edit <service name> - to edit configuration service file

* Journalctl 
	+ Query SYSTEMD Journal
	
##### commands under Journalctl

* journalctl - log file of running services
* journal -b - log file with current boot
* journal -u <service name> - log file particular service.

### Labs

1. usage of SYSTEMD tool for services as follows
	* systemctl start <service name> -  start the service
	* systemctl stop <service name> -  stop the service
	* systemctl restart <service name> -  restartstart the service
	* systemctl reload <service name> -  reload the service
	* systemctl enable <service name> -  enable the service
	* systemctl disable <service name> -  disable the service
	* systemctl status <service name> -  info(status) the service
	* systemctl edit <service name> - to edit configuration service file
	
2. To generate log files using the following commands 
	* journalctl - log file of running services
	* journal -b - log file with current boot
	* journal -u <service name> - log file particular service.


