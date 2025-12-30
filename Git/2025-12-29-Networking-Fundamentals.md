<h1> Networking Fundamentals </h1>


```console
What is a Network? Group of connected devices that can share resources.
Networks can be local only or connected to the internet 
***Networks arent always online


Types of Network

1. PANs (Personal Area Network)- designed for short range communication btwn devices with close proximity to a single user
2. LANs (Local Area Network)- connects multiple devices across a home, office, or school. Often wired and sometimes wireless but all within one physical space
3. WANs (Wide Area Network)- connects entire LANs across cities or countries. Needs dedicated infrastructure
WLANs are simply LANS w/o cables. Roaming while connected 
4. Internet

WLANs use Wi-Fi (wireless) while LANs are often wired

Latency-Delay between sending and receiving information

Smaller networks are faster, simplier, and easier to secure but limited in range
Large networks cover more distance but at latency cost and complexcity

2 Ways Devices can share Data
Peer-to-peer: ideal for small, informal setups
Client-server model: offers central control and scalability but relies on a stable core

In reality most systems uses P2P or client server model


The Internet
Data is split into packets which is easier to send 
Each packet travels with a header, payload, and checksum




Computer use DNS (internet address book)

IP address: internet protocol address
private and public IP (router has a public IP)
MAC address: unique identifier assigned to a network interface ona device like a phone, or laptop-locally

Analogy
MAC address: its a device name tag
IP address: device mailing address
name tag stays the same, but mailing address can change

Packet switching happens locally using a MAC address

How Routers forward data across networks? routers refer to destination IP add for the next hop. Packets take different routes based on network conditions

How switches move data within a local network? Switching uses MAC-addresses to move packets inside a LAN. Modern switching doesnt lock the path


| Networking Core

Devices connect to network using NICS. 

NIC stands for Network Interface Card

NIC: is the hardware component that allows a device to connect to a network. Can be wired (ethernet) or wireless (Wi-Fi). 

Most devices today have NICs built in (on the motherboard)

NICs sends and receives data on a network

Routers distribute internet access and assign IP addresses WHILE Switches expand wired capacity; WAPs on wireless connections

Network Topology: Topologies shape how data moves-star is common and mesh is growing
Hyvrid designs mix wired and wireless for balance


|Network Protocols|

TCP/IP Model
TCP: Transmission Control Protocol
IP: Internet Protocol

TCP ensures reliable delivery while IP handles addressing and routing. it defines a universal structure for sending and receiving data reliably 


Encapsulation Explained-How message travel

Application: just the message/writing a letter
Transport: It becomes a segment with delivery instructions added. Like sealing an envelope
Network: Turns into a packet and now addressed for global travel. Like adding a label destination
Data Link: its a frame waiting for the next local hop. Like packing into a van with a driver
Physical: converted to bits, the actual movement. Like the wheels turning

Decapsulation: whole process in reverse. It is the process of unwrapping the data layer by layer 

OSI Model
Application
Transport
Network
Data Link
Physical
Session
Presentation

TCP & UDP
tcp guarantees every packet arrives in order and w/o erros while UDP skips error checking for speed. UDP is used in terms of calls, streaming, and gaming.

DHCP: a protocol that provides a device with its private IP address within a local network 

IP address & port numbers
IP get you to the location while port numbers get you to the right room. it direct data to the correct application/service on a device

ARP (Address Resolution Protocol)- finds the MAC address associated with a specific IP address




|Network Troubleshooting|
ipconfig/ifconfig
ping

```






