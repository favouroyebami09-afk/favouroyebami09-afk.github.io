<h1> Networking Basics </h1>

<h3> LAN, Switch, Router, WAN, Gateway </h3>

```console
LAN: Local Area Netowrk is collection of devices connected together in one 
physical location. Could be a home or office network 
Each device has a unique IP address

IP address consist of:
    32 bit value
    1 bit = 1 or 0
    every 8 bit is grouped into an octet
    172.16.0.0
    10101100.00010000.00000000.00000000
    octet 1   octet 2  octet 3  octet 4 

Switch: sits within the LAN 
        Facilitates the connection between all the devices within the LAN

Router: helps with communication outside local network 
        sits between LAN & outide networks (WAN)
        connect devices on LAN & WAN
        connect us to the internet
IP address of the router is called a 'Gateway'
    'Gateway' is bascially the same as router 
```

<h3> Subnet </h3>

```console
How to know, whether the other device is inside/outside the LAN?
Devices in the LAN belong to the same IP address range 

Subnet= logical subdivision of an IP network
Subnetting= process of dividing a network into two or more networks 

Example of IP addrss range: 192.168.0.0 255.255.255.0
        255.255.255.0 is the subnet mask
        192.168.0.0 is IP address
        subnets sets the IP range
        all IP address starting with 192.168.0.x belongs to a LAN


255.255.0.0 - means the 16 bits are fixed
255.255.255.0 - means 24 bits are fixed 
value 0 means free range

192.168.0.0 255.255.255.0 means first 3 octets cannot changed 
    [fixed].[fixed].[fixed].[canchange]
    hence 192.168.0.[thiscanchange]

192.168.0.0 255.255.0.0 means half of the octet are fixated
    [fixed].[fixed].[canchange].[canchange]
    192.168.[canchange].[canchange]
    
CIDR Block 
CIDR = Classless Inter-Domain Routing
subnet mask dictates how many bits are fixed
192.168.0.0/16 or 192.168.0.0/24
    /16 bits are fixed
    /24 bits are fixed

Overall: when we send a request to an IP address within our LAN, request willgo to the 'switch' and it will be forwarded to the device within the LAN. If the IP address is external, it will go to the 'Internet' through the 'router/gateway'.
Any device needs 3 pieces of data for communication within/outisde its network:
    IP address
    Subnet
    Gateway
```

<h3> Network Address Translation (NAT) </h3>

```console
IP address range chosen by an administrator
Each device gets a unique IP from that range
IP address within LAN are not visible to the outisde network or internet
    -private IP
When you send a request to Facebook from your laptop, the laptop private IP address from the LAN is replaced by the router
    -this is called 'Network Address Translation' (NAT)

Benefits of NAT:
-security and protection of devices within LAN
-reuse IP address 
```

<h3> Firewall </h3>

```console
Firewall: sets of rules that prevents unauthorized access from entering a private network
Using firewall rules you can define, which requests are allowed 
```

<h3> Ports </h3>

```console
What is a Port? are doors to the same building 
every device has a set of ports 
you can allow specific ports (doors)
you can allow specific ports (doors) AND specific IP address (guests)
Different applications listen on specific ports 
```

<h3> Domain Name System </h3>

```console
Mapping IP address to names 
DNS = translates domain names to IP address
its the yellow pages of the Internet
Root Domains and Top Level Domains
.mil = for military 
.edu = for educational institutions 
.com = general purposes and business
.org = non profit organizations
.net = for networking technologies 
.gov = for government 

Subdomains
can be used for different applications that belongs to the top level domain organization

DNS Entries are cached for efficicency
```

<h3> Networking Commands </h3>

```console 
ifconfig: gives computer IP address, subnet mask, gateway(router)

netstat: shows active connections on machines

ps aux: check current running processess and programs 

nslookup: can get IP address of any domain name
          also displays the IP address of the DNS server 

ping: checks if a service/application is accessible 
```

