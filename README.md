
<h1 align="center"><b>NetPractice</b></h1>

> **The goal from this project to discover networking.**    


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

### **PAN :**  
PAN stand for **Personal Area Network** and it is just a few meters like the Bluetooth, syncing a phone to a laptop.   
<p align="center">
	<img src="assets/PAN.webp" width="400">
</p>

### **LAN :**
LAN stand for Local Area Network for a single room, home, office, building or campus. A typical home Wi-Fi network or all computers in a school library.   
<p align="center">
	<img src="assets/LAN.webp" width="400">
</p>

### **MAN :** 
MAN is Metropolitan Area Network used on the large cities or large geographical area covering several buildings. Connecting multiple university campuses across city.  
<p align="center">
	<img src="assets/MAN.webp" width="400">
</p>

### **CAN :**  
CAN stand for Campus Area Network, it is a fixed area like a corporate or university campus, often consider a larger type of LAN or a small MAN.  
<p align="center">
	<img src="assets/CAN.webp" width="400">
</p>

### **WAN :**  
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

## Bridge
The bridge purpose is to filter, segment and connect two disparate LANs. The bridge contain only two ports.  
<p align="center">
	<img src="assets/bridge2.webp" width="150">
	<br>
	<img src="assets/bridge.webp" width="350">
</p>

