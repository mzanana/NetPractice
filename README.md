
<h1 align="center"><b>NetPractice</b></h1>

> **As ALWAYS, we won't just work the project! We will explain everything you need to know about Networking. Of course you can go deeper if you want**    

# Definitions

## Network & Computer Network

### Network in general 

A **network** is a system of **interconnected** elements (nodes, points or people, ...etc) designed to facilitate the movement or exchange of resources, information or communication between them.  

<p align="center">
	<img src="assets/Network.webp" width="400">
</p>

### Computer Network

A **Computer Network** is a group of two or more interconnected computing devices (such as computers, servers, printers and other peripherals) that are linked together to **share resources, exchange files, and allow electronic communication**.  

<p align="center">
	<img src="assets/Computer-Network.webp" width="300">
</p>

## Client-Server Model

Most modern computer networks including the internet use the **client-server model** :  
### Server

Is a hardware or a software system that stores, manages and provides resources, services or data to other devices (clients) on a network;  
The server role is to listen for a requests and then fulfill those requests.  

**Examples of servers :**  
+ Web Server : Stores and delivers web pages(HTML, images ...etc);  
+ Email Server : Send, receive and store electronic mail;  
+ DataBase Server : Hosts and manages a structured collection of data;  

### Client

Is a device or a software that **initiates communication** by **requesting** a service, resource or data from a **server**.  It can be from any end-user device, like desktop, laptop, smartphone or tablet, ...etc.  

<p align="center">
	<img src="assets/Client-server.webp" width="400">
</p>

# Network Types 

## Types by Scale

### PAN
PAN stand for **Personal Area Network** and it is just a few meters like the Bluetooth, syncing a phone to a laptop.   
<p align="center">
	<img src="assets/PAN.webp" width="400">
</p>

### LAN
LAN stand for Local Area Network for a single room, home, office, building or campus. A typical home Wi-Fi network or all computers in a school library.   
<p align="center">
	<img src="assets/LAN.webp" width="400">
</p>

### MAN
MAN is Metropolitan Area Network used on the large cities or large geographical area covering several buildings. Connecting multiple university campuses across city.  
<p align="center">
	<img src="assets/MAN.webp" width="400">
</p>

### CAN
CAN stand for Campus Area Network, it is a fixed area like a corporate or university campus, often consider a larger type of LAN or a small MAN.  
<p align="center">
	<img src="assets/CAN.webp" width="400">
</p>

### WAN   
WAN is the Wide Area Network for the large indefinite area, connecting cities, countries or continents. The **internet** is the largest public WAN corporate network connecting branch office globally.  
<p align="center">
	<img src="assets/WAN.webp" width="400">
</p>


## Network types by Topology (Structure)

Topology refers to the physical or logical arrangement of nodes (devices) and the connections (cables/links) between them.  
<p align="center">
	<img src="assets/Topology.webp" width="400">
</p>

## Network Traffic Types
Network traffic define the relationship between the sender and the receiver(s) on a **network**.  
There is three main traffic types that a network switch handles :   
+ **Unicast :**  It is one-to-one transmission from a single source to a single specific destination;  
+ **Multicast :**  Sending a message to a specific **group** of devices;   
+ **Broadcast :**  Send a message fro one device to **all** the other devices on the same local network, the frame uses a specific destination MAC address : `FF:FF:FF:FF:FF:FF`;  

<p align="center">
	<img src="assets/traffic-types.webp" width="350">
</p>


# Network Equipment 

## Repeater 
Its role is to regenerates the weakened network signals to extend the signal's reach over longer distances, the repeater contain only two ports.    
<p align="center">
	<img src="assets/repeater.webp" width="500">
</p>

## Hub  
Is a multi ports repeater, that broadcasts **any** incoming signal to **all** other ports, without exceptions, so if the sender want to send a message to RECEIVER-3, the Hub send this message to all the RECEIVERS connected to the HUB.

<p align="center">
	<img src="assets/h-hub.webp" width="200">
	<br>
	<img src="assets/HUB.webp" width="400">
</p>

## Switch
A multi ports RJ45, which connect devices within a single network (LAN). Intelligently forwards data frames based on **mac addresses**, so if a sender want to send a message to RECEIVER-3, even if there is 52 other device plugged in to the switch, only the RECEIVER-3 which gonna get the message.  
So the Switch is much more secure the HUB!  
<p align="center">
	<img src="assets/switch-b.webp" width="200">
	<br>
	<img src="assets/switch.webp" width="500">
</p>

**What is MAC address ?**  
Each end-device has it's own **mac address** which stand for Media Access Control and it is a **unique hardware identifier** assigned to a network interface controller (NIC) the physical component that allow a device to connect to a network;  
<p align="center">
	<img src="assets/mac-address.webp" width="400">
</p>

Unlike the **IP** address which is used for global routing, the MAC address is only used for **local communication** within a single LAN segment;  
### How the Switch Works
The internal memory of the switch is called **MAC Address Table** which contain two rows, the port number and the MAC address of the connected device. When the switch powered on the table been empty.   
<p align="center">
	<img src="assets/mac-table.webp" width="250">
</p>

When a frame arrives on a switch port, the switch reads the **MAC addresses** from the frame's header and fill the table with this **MAC** address and the specific ports the frame was received on, so it knows the port and the MAC address of the source and the destination from the frame.    
<p align="center">
	<img src="assets/mac-table2.webp" width="250">
</p>

Over time, as devices communicate, the switch fills the entire table.   

## Router 
The router is a networking device that connect **different Networks** together, it acts as a gateway, connecting **LAN** to **WAN** for example connecting the home network with the internet .  
**Hubs & Switches** are used to **create** networks. while **Routers** are used to **connect** networks.  

<p align="center">
	<img src="assets/router2.webp" width="150">
	<br>
	<img src="assets/router3.webp" width="550">
</p>
### Routing Table

**Routers** use **Internet Protocol (IP)** for routing process.  Routers route data by using the routing table which is like a road map of a car, so the data can travel across the internet and reach its destination it needs **directions** to determine how to get there.  
<p align="center">
	<img src="assets/destination.webp" width="450">
</p>
There are three routing types :  
+ **Directly Connected :**  Lets say we connect two networks separated by a router, each one with a specific **IP** address, the router will create automatically the router table with the directly connected routes.  
  When a computer on a `192` network want to connect with a computer on a `10` network, the computer sent a data packet to the router, and the router looks for the destination IP address of the packet, the router looks at the routing table and decide to forward the data out the interface  `Eth1` then to the intended computer.  
<p align="center">
	<img src="assets/directly-connected.webp" width="550">
</p>

+ **Static route :** Static routes are manually configured by a network administrator. 
  Lets say the router is connected to another network with the IP `174`, if a computer from the `192` want to connect with a computer from the `174` the router gonna search on the routing table for the interface with this IP address and gonna fail, that when the administrator add the new network `174` to the routing table so the computers of the network `192` could connect with the computers on the network `174`. So to connect back an administrator should add the interface at the other router so the computers on the `174` network could connect to the `192` network computers.  
	<p align="center">
		<img src="assets/static.webp" width="550">
	</p>
+ **Dynamic routes :** Are similar to the static routes the way it works, the difference is how the routing table is filled, on static routes we fill the table manually but on the dynamic routes we use some protocols so the routing table fill itself automatically, some protocols are : `RIP, OSPF, BGP, IS-IS and EIGPR`.
  So what happen is the routers talk with each other and share their routing tables with each other.  
### How the Router works
+ **Determining the best path :**  When a data packet arrives, the router gets the destination IP address from the header of the packet, then it consult the **routing table** which is a map of network paths to determine the most efficient route and to forward the packet closer to its final destination.  

+ **Forwarding the packet :**  Once the router knows the best route, the router sends the data packet out through the appropriate network interface.  

## wireless access point
A wireless access point **relays** data between a wired network and wireless devices
	<p align="center">
		<img src="assets/wap1.webp" width="450">
	</p>
**Wireless APs** are used primarily by medium and large organisations, they have multiple APs to make sure it covers the entire building

## Bridge
The bridge purpose is to filter, segment and connect two disparate LANs. The bridge contain only two ports.  
<p align="center">
	<img src="assets/bridge2.webp" width="150">
	<br>
	<img src="assets/bridge.webp" width="350">
</p>

## Bandwidth & Throughput
+ **Bandwidth :** Is the theoretical maximum capacity of a network connection, the upper limit of the amount of data that could potentially be transferred over a connection in a specific amount of time.  
  It is measured in **bits per second**, Mbps or Gbps.
+ **Throughput :** The actual amount of data **successfully** transmitted over a network connection in a specific amount of time.  

<p align="center">
	<img src="assets/bandwidth.webp" width="450">
</p>

# Computer Network Models 

There are two main computer network models that serve as reference for understanding and designing how data flows : the **OSI Model** and the **TCP/IP Model**.  

The **TCP/IP Model** is the one actually used for the internet and modern networks, while the **OSI Model** is more detailed, **theoretical** model primarily used for teaching and troubleshooting purposes.  

## Problem the models solved
Between 1960s and 1970s, computer networks were often closed, for example **IBM** networks could only talk to other IBM networks. If a business bought hardware from different manufactures, those systems **could not** communicate with each other, so they are **forced** to buy all their networking equipment from a single company.   

To solve this problem, the **ISO** (International Organisation for Standardization) developed the **OSI** model in 1984 to create a universal blueprint that all the hardware and software manufacturers could follow. By defining **Seven Layers**.  

### Protocol  
Protocol is a standardized set of rules between two or more devices so they could communicate with each other,  just as humans speaks a specific language to communicate, also the computers needs protocols to ensure they can correctly format, transmit, receive and interpret the data they exchange. 

Most used protocols :  
+ **HTTP/HTTPS :** Used by web browsers to request and display web pages (Application Layer); 
+ **IP (Internet Protocol) :** Define the addressing system and routes data packets across the entire internet ( Network Layer);  
+ **TCP :** Ensure data is delivered in accurate way, checking errors, resending lost data and ensuring packets arrive in the **correct** order (Transport Layer);   
+ **DNS, FTP, SSH, SMTP ...etc**

# OSI Model

**OSI** Stand for Open System Interconnecting, the purpose of this model to allow different systems to communicate smoothly regardless of their internal architecture, hardware or software.  

The **OSI** model standardize the functions of communication system into **Seven Layers :**  
<p align="center">
	<img src="assets/osilayers.webp" width="350">
</p>

Each layer of the OSI model encapsulate the data by adding a part to the header of the data so when the data arrive to the server it decapsulate  it 
<p align="center">
	<img src="assets/datapacket.webp" width="550">
</p>

## Application Layer
### Definition
The **application layer** is the primary interface between the user's software application and the network services required to exchange data, it contain the protocols that define the rules for application-level communication, for example when browsing google chrome we use the HTTP protocol to talk across the network.  
<p align="center">
	<img src="assets/application.webp" width="550">
</p>

### header
The application layer encapsulates the data and add to it a header that contain the protocol and information used, still named **data**.    

## Presentation Layer
### Definition
On this Layer we have three steps :  
+ **Translation :**  Converting the data from an application-specific format into a common, **standard** format.
+ **Compression;**
+ **Encryption & Decryption :** 
<p align="center">
	<img src="assets/presentationlayer.webp" width="450">
</p>

### header
 Contain the information specifying the **data format** used like JPEG, MP4, PDF ... also metadata necessary to correctly decrypt the incoming data, and then information about the compression algorithm used allowing the receiver to decompress the data correctly.
 Still named by data.  
## Session Layer
This layer determine the transmission mode :
+ **Simplex mode :** The communication is fixed in one direction, from a sender to the receiver. Example of the keyboard sending input to a monitor;  
+ **Half-duplex mode :**  Data can flow in both directions but not simultaneously. Example of the walkie-talkie;  
+ **Full-duplex mode :**  Also bidirectional but simultaneously. Example of a phone call.  
<p align="center">
	<img src="assets/mode.webp" width="450">
</p>
This layer also manage the authentication and the authorization.  
The most important feature it inserts **checkpoints** into the data stream in case the connection fails, the session layer allow the transfer to resume from the last successful checkpoint instead of restarting from scratch.  
<p align="center">
	<img src="assets/checkpointing.webp" width="450">
</p>
### Header
Contain the numbers indicating where checkpoints are placed, bits defining the communication mode and which device currently hold the right to transmit.  
Still named by data.  

## Transport Layer
This Layer is responsible for data transfer, choosing between **Connection-Oriented** service like **TCP**, and **Connectionless** services like **UDP**.  

### Port Addressing
The Transport Layer is the one responsible for getting the data to the **correct** application on the destination computer, using the **Port Numbers** which are a 16-bit numbers (0 to 65535) added to the header to identify the specific application process
<p align="center">
	<img src="assets/ports.webp" width="350">
</p>

### TCP
#### Segmentation
Happens only on the TCP! Since the physical networks have a limit on the maximum size of data unit, and we don't want any **data lost**, this layer break the data into smaller chunks suitable for transmission as **segments**.
<p align="center">
	<img src="assets/T1.webp" width="550">
</p>
#### Header (Segment)
Each segment is tagged with :  
+ **Source and Destination Ports, data offset, header length ...**  
<p align="center">
	<img src="assets/tcpheader.webp" width="350">
</p>
+ **Sequence Number** Indicate the position of the first byte of data carried by the current segment; Helps also to put the segments back together to build the original data before sending it to the Session Layer.    
+ **Acknowledgment Number** Indicate the next expected byte the receiver wait from the sender;  
#### Handshake
Before any data is transferred, TCP make sure both hosts are ready for connection :   
+ **Synchronize :** The client sent the segment proposing the initial sequence number **X** to start communication;  
+ **SYN Acknowledge :** The server reply with a segment includes its own sequence number **Y** and the acknowledge number that equal **X + 1**, so it means am waiting for the next segment.  
+ **Acknowledge :** The client sends a final segment acknowledging the server's sequence number **Y + 1**
 At this point the connection is established and data transfer can begin!  
<p align="center">
	<img src="assets/tranportheader.webp" width="400">
</p>

**TCP** guarantees that all data arrives in order and without errors using the system of sequence numbers and acknowledgments.  
The client send a segment and wait the confirmation of the server then continue.  
If the sender does not receive an **ACK** for a segment within a calculated time period, it assumes the segment was **lost** and **retransmits** it again.  
After finishing the data transfer the **TCP** gracefully closes the connection using **FIN (Finish)** and **ACK** segments, ensuring both sides agree to stop sending data.  
<p align="center">
	<img src="assets/tcpdiagram.webp" width="300">
</p>

### UDP
#### Definition
**UDP**  stands for User Datagram Protocol, described as "fire-and-forget", provides a connectionless transport service, it doesn't care about the connection with the server, it just send the data even is some is lost it continue sending the rest.  
We use UDP when speed is important than absolute accuracy, UDP is much faster than TCP because it avoid the handshakes, sequence numbering and making sure that the data is received well or not.
#### Header (Datagram)
The UDP header is extremely simple, it contain only four fields :  
+ **Source Port Number;**  
+ **Destination Port Number;**  
+ **Length** (of the entire datagram) **;**  
+ **Checksum** (optional but used for basic error detection) **;**  
<p align="center">
	<img src="assets/udpheader.webp" width="400">
</p>

