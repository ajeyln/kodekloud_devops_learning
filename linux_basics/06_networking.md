<h1 align="center"> Networking </h1>

### DNS

* /etc/hosts - stores the ip address with host name of the remote system (Name Resolution)
* /etc/resolv.conf - DNS stores all the hostnames and their ip address
* /etc/nsswitch.conf - if we want to prefer DNS server host file over local host file
* 8.8.8.8 - is global DNS server
* nslookup - to query a hostname from DNS server (ping)

### Switching and Routing

* ip link - list and modify interfaces on the host
* route - kernel's routing table
* ip route add <dest. network> vi <current network> - to connect current network to destination network
* ip route add default via <current network> - to connect current network to all newtork
* traceroute <dest.ipaddress> - to trace the networks between current and destination devices.
* ip link set dev <dest.device> up

### Labs

1. DNS - Updated local host file (/etc/host), DNS server(/etc/resolv.conf) etc.
2. Network basic - connecting the current network to other network using ip route add , all network using ip route add default via etc. 