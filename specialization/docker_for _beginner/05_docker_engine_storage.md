<h1 align="center"> Docker Engine, Storage </h1>

## Docker Engine

Docker Engine is a host where Docker is installed. When we install Docker on Linux host, it is actually <br />
mean installing three different components.

* Docker Deamon - It is background process that manages Docker objects such as images, containers, volumes and networks.

* Rest API server - It is the API interference that programs can use to talk to the deamon and provide instructions.

* Docker CLI - It is command line interface, to perform actions such as running , stoppiong containers, destroying <br />
images etc. It uses the rest API to insteract with docker deamon. Docker CLI need not necessary be on the same host <br />
can still work with remote DOkcer engine using the command ```docker -H <Docker engine address>:<Port>```

### Docker containerization

Docker uses namespace to isolate workspace Process IDS, Network, Inter process communication, Mounts and Unix time sharing <br />
systems are careated in their own namespace thereby providing isolation between containers. 

Process IDs are unique and processes cannot have the same process ID. Whenever Linux system boots up it starts with <br/>
just one process with Process ID, it is root process and kicks off all the other processes in the system by time the system boots up <br />
completely, we have handful of processes running this can be seen by running the PS command to list all the running processes. <br />

Now if we create a container, which is basically like a child system within the current system. The child system needs to think that <br />
it is an independent system on its own and it has its own set of processes originating from the root process with process ID, but we  <br />
know that there is no isolation between the conatiners and the host.So the processes running inside the container are the fact process <br />
running on the host and so two process cannot have the same process IDs.

## Docker Storage

when we install Docker on a system it creates folders structure as follows

* var/lib/docker
	+ aufs or zfs or device mapper etc.  - storage drivers, auf is storage drivers for ubuntu
	+ conatiners - stores the files related to containers in this folder.
	+ images - stores the files related to images in this folder.
	+ volumes - Any volume created docker containers are created under this folder.
	
In layered architecture , once build is completed we cannot modify the content of those layer and so they were ready only and we can only <br />
modify them by modify them by initiating a new build when we run a container based off the image.

#### Container layer 

Using docker run command Docker creates a container based off of these layer and creates a new writable layer on the top of the layer. <br />
The writable layer is used to store data created by the container such as log files by the applications. Any temporary files generated <br />
by the container or just any file modified by the user on that container and the life of this layer is only long as the container alive.

In order to save the persit the data of container, we need to create a volume using ```docker volume create <Volume_Name>```  <br />
when we run this command, it creates folder called <Volume_Name> under Volume directory. Then we run the docker container using the docker run  <br />
command , we could mount this volume inside the docker container using command ```docker run -v <Volume_Name>:/var/lib/<DB NAME> DB_IMAGE``` <br />
evenif, the container destroyed the data stored in this volume and this method is called Volume Mounting.

If we want to store externally like external devices. In this case we can mount the device using the command <br/> 
```docker run -v <External_device_directory>:/var/lib/<DB NAME> DB_IMAGE```  and this method is called as Bind mounting.<br /> 

Storage drivers is responsible for Maintaining the layered architecture, creating writable layer moving files accross layers to enable copy and write etc. 

### Labs

1. Docker Storage