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

#### Multiple VMs & Networking

One way to create Multiple VMs is to clone the existing VM.

There are two types of cloning in Virtual Box

1. Full Clone : It creates a full copy of the disk used by existing VM, consuming equal amount of new space.
2. Linked Clone : It uses the disk of the existing VM and only consumes spacefor the changes made in new VM.

##### Steps to creating network the Multiple VMs

+ Host-only network configure by clicking File (Virtual box) --> Host Network Manager --> Create a new network by clicking enable button.
+ If already NAT is already configured, Select the VM --> Network -->  Adpter 2 and select respective Host-only network

Network Option for Multiple VMs.

| VM can reach internet/other systems in the network | VMs can reach each other | Host can reach VM (without port forwarding | Other system in network can reach VM | Solution |
|-------------------------| -----------------| --------------------- | ----------------- | --------------- |
| Yes | No | No | No | NAT|
| Yes | Yes | No | No | NAT Network |
| No | Yes | Yes | No | Host Network |
| Yes | Yes | Yes| No | Host Network + NAT |
| Yes | Yes | Yes | yes| Bridged |

###### Backup and retrieve the data of VM

+ Snapshot feature  : This feature is used to backup of VMs state at particular point of time and then restore to that at later point of time.
+ Using snapshot feature, can clone new VM.

##### Vagrant

Vagrant is a tool for building and managing virtual machine environments in a single workflow with an easy-to-use workflow and focus on automation.

|Commands | Description |
| -------------- | --------------- |
| vagrant init  |  Initialize Vagrant with a Vagrantfile |
| vagrant up  | starts vagrant environment  |
| vagrant resume  | resume a suspended machine |
| vagrant reload | restarts vagrant machine, loads new Vagrantfile configuration |
| vagrant ssh  | connects to machine via SSH |
| vagrant halt  |  stops the vagrant machine |
| vagrant suspend | suspends a virtual machine |
| vagrant destroy | stops and deletes all traces of the vagrant machine |
| vagrant box list  | see a list of all installed boxes on your computer |
| vagrant box add <name> <url> | download a box image to your computer |
| vagrant box outdated | check for updates vagrant box update |
| vagrant boxes remove <name> | deletes a box from the machine |
| vagrant package |  packages a running virtualbox env in a reusable box |

+ Vagrant file

Vagrantfile is to described the virtual machines required for a project as well as how to configure and provision these machines.

### Reference

1. Download - Oracle Virtual Box : https://www.virtualbox.org/wiki/Downloads
2. Download the pre-configured images for VM from - https://www.osboxes.org/

