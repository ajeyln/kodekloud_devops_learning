<h1 align="center"> Lab Enviornment </h1>

### Virtual Machine

The Virtual Machine (VM) is the virtualization of a computer system. These are based on computer architectures and provide functionality of a physical computer.

There are two types of virtualization softwares which helps to virtualize machines

+  Type 1 Hypervisors - These softwares are installed directly on bare metal such as a laptop or server <br />
	Eg : vmwareESXi, Microsoft Hyper-v etc.

+  Type 2 Hypervisors - They are hypervisors that runs on existing operating system <br />
	Eg: Oracle virtual-Box, VMware workstation etc.

####  Oracle Virtual Box

+ Oracle Virtual box is open source and it is free.
+ Supports wondows, linux, Mac os x, Solaris.
+ It supports backup and recovery with snapshots and clone features.
+ It lets to run Multiple VM's.
+ Helps to create separate networks with laptop for different group of VM's.

##### Creating Virtual Machines.

+ Should enable the virtualization Technology in Bios.
+ Install virtual Box and select New Button.
+ Configuration of virtual machine such as name, space of disk to be allocated etc.
+ Change adapter1 to bridge network in order to get IP address for virtual machines.

##### Virtual Box Connectivity

We can start VM either in normal mode or headless mode

+ Normal Mode 
	* Which gives a console to the VM 
	* When the console  is closed, VM must be shutdown or suspended.

+ Headless Mode
	* Console window will not open and VM can only access through remotely using SSH or remote desktop tools for Windows.

+ ip addr add <IP_ADDRESS> dev eth0 - to set the ip address to VM using console.
+ In MAC or in Linux if want to connect the VM from Host os need to start SSH Services (Service sshd start)
+ In MAC or in Linux, as VM doesn't have ip address, need to setup port forwarding(using port)

#### Virtual Box Networking

There are mainly three types of networking in Virtual Box

+ Host-only Network : In this network method, All the VM can reach each other but cannot reach outside world <br />
or no other can outside reach this VM's.
+ Network Address Translation (NAT)Network : A private network within the physical system and all VM gets <br />
ip addresses so that that can connect each other and also with outside world, but outside system cannot access VM's.
+ Bridge Network : When all VM connected to the Bridge network, all the VM gets same ip addresses as that of external LAN network.

+ Port forwarding : It allows to map a port on the host to a port on the guest.
	Eg: port 80 on the host could be mapped to port 80 on the guest so that any traffic on port 80 on the host is fowarded to 80 on the guest.

### Reference

1. Download - Oracle Virtual Box : https://www.virtualbox.org/wiki/Downloads
2. Download the pre-configured images for VM from - https://www.osboxes.org/

