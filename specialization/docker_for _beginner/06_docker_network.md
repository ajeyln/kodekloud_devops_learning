<h1 align="center"> Docker Networking </h1>

### Docker Network

Docker creates 3 types network while installation

* Bridge - Default network of a container. It is a private internal network created by docker on the host. All container <br />
atatched to this network by default and they get internal IP address and the container can access each other using this <br />
internal IP if required. We can connect the container externally associate to the container by host network, i.e if we are <br/>
to run a web server on Port 5000 in a web container it is automatically as accessible on the same port externally without <br />
requiring any port mapping as the web container uses the host network.

* None - The containers are not a test to any network and doesn't have any access to the external network or other containers <br />
as they run in an isolated network. <br />

* Host(User defined) Network - By default Docker will create only one internal bridge network and  If we want to create a isolate <br />
container within docker host. <br />
	+ we can create internal network using the command ```docker network create ``` and specify the driver(bridge), subnet of the network <br />
and custom isolated network name. <br />
	+ We can find the list of all networks using command ```docker network ls```
	+ To ckeck the ip address of the container using command ```docker inspect <Container ID/NAME>````

### Embedded Docker

We should connect the container using container name or id as IP address will get changed after rebooting and Docker has built in <br />
DNS server that helps the containers to resolve each other using the container name and DNS server always runs at address 127.0.0.11.

### Labs

1. Docker Networking