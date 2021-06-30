<h1 align="center"> Networking basics </h1>

### Switching and Routing

Switching is process to forward packets coming in from one system to leading towards the destination system.

Routing is the process of transffering packets between multiple switches or multiple networks

* ip link : list and modify interfaces on the host
* ip addr add <IP Address > dev <Interface > : assigning ip address to the system and interface
* route - kernel's routing table
* ip route add <dest. network> vi <current network> - to connect current network to destination network
* ip route add default via <current network> - to connect current network to all newtork
* traceroute <dest.ipaddress> - to trace the networks between current and destination devices.
* ip link set dev <dest.device> up

### DNS

DNS is domain naming service, These enabled servers stores the ip addresses with host names.

* /etc/hosts - stores the ip address with host name of the remote system (Name Resolution)
* /etc/resolv.conf - DNS stores all the hostnames and their ip address
* /etc/nsswitch.conf - if we want to prefer DNS server host file over local host file
* 8.8.8.8 - is global DNS server
* nslookup - to query a hostname from DNS server (ping)


### Labs

1. Network basic - Swicthing, routing maintaining routing table etc.
2. DNS - Configuring DNS, Updating host file on local as well in server etc.