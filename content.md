# Networking for Cybersecurity/Ethical Hacking/Pen-tasting

### Table of contents:

*	What is networking actually?
*	Physical devices in a network/Networking
*	OSI & TCP/IP Model
*	IP addressing
*	Sub-netting
*	Broadcast address & Host Range
*	MAC address
*	Routing
*	Switching
*	Ports, services, and protocols
*	DNS
*	VLANS
*	Subnet Mask and CIDR Notation
*	ARP
*	NAT & PAT
*	Network Monitoring Systems
*	VPN's
*	Firewalls
*	IDS & IPS
*	Cloud Security

# What is Network/Networking?
While studying networking, let's first discuss the term' network' or networking. 
A network means at least two or more devices connected with each other to share information and process data. Here, devices connected with each other are called a network.
The process of communication between two or more devices is called networking.
In technical terms, every single device that is present in a network is called a node.
###	Types of Networks:
1.	**LAN:** LAN stands for Local Area Network, which works between nodes that are present in a particular network and connected with wires. No outsiders are allowed to access communication or data from this type of network. e.g., a network of your university lab.
2.	**WAN:** WAN stands for Wide Area Network, which means the Internet we use nowadays to access information or data worldwide. It can also be used to connect two or more LANs
3.	**MAN:** MAN stands for Metropolitan Area Network, which means a network that covers a city, a town, or a particular area that can be from 5 kilometres to 50 kilometres. This is larger than LAN and smaller than WAN
4.	**PAN:** Stands for Personal Area Network, which is used to establish a connection between a single person. e.g., a Bluetooth or NFC connection between a single device or person.
5.	**WLAN:** Stands for Wireless LAN, which is similar to LAN, but connects each node without a wired connection.
Sometimes, a VPN (virtual private network) is also considered a type of network because it allows us to connect to our destination by creating a virtual and private network connection by masks our IP (Internet Protocol) to keep everything private.

#	Network Devices:
In this session, I will discuss the types of physical devices we use to establish our network, enabling nodes to communicate with each other effectively.
For a cybersecurity or ethical hacker, Lerner, it is very important to know how data travels between different devices or networks
1. **Router:** A physical device that routes our traffic to access data from outside (from other LA parts or the Internet) of the network. It decides the best way for data to travel efficiently. e.g., We use a router in a LAN to access the WAN.
2. **NIC:** (Network Interface Card) This is a device or card that gives a system a particular address (assigned during manufacturing), which is used to get data from other devices and send data to other devices or nodes using this address. Modern devices have built-in NICs.
3. **HUB:** This particular device is used to send and receive data between different nodes within a network. The drawback of this device is that when we send a data segment to a particular node, it sends this same data to each node in the network; we get a, huge amount of traffic between devices, causing a slowdown in the network. To control this traffic, we use switches nowadays.
4. **Switch:** This is actually a HUB, but it sends and receives data between nodes or hosts intelligently. A switch has the address of each node in the network. When we send data to a particular node, it will match the address and only allow the corresponding device to receive data. This feature will help us to keep the traffic controlled within a network.

### There are further types of switches.
*	**Circuit Switching:** In Circuit Switching, we turn a full circuit into a path for sending data between just the sender and receiver. During this process, a dedicated path has been established between the sender and the destination address. No one else uses this path until they cut their connection.
*	**Message Switching:** In this type, a network uses a store-and-forward technique in which the whole data set is first stored in the switch and then sent to the destination address entirely at a time.
*	**Packet Switching:** In this technique, data travels between the sender and receiver by creating small segments of data. Each data packet receives the destination address and begins moving without considering the other data packets. 

    ### There are two types of packet switching: 
*	**Connectionless or datagram approach:** In this method, data packets start to move just by receiving the destination address. Every packet of data uses a different path in the network to reach the destination address. 
*	**Connection-oriented or virtual circuit:** During this, a connection has been established between sender and receiver. A virtual path has been created, and each data packet should follow this exact path to reach the destination address.
5. **Bridge:** This is used to connect two different LANs so they can also send and receive data within two or more networks. We usually use it to connect two LAN networks.
6. **Firewalls:** This acts as a security element for our network. This decides which device is allowed to connect to a network and which is not. We use it to establish secure communication within a network. 
7. **Repeaters:** These are used to keep the signal as it is within a network. This acts as a signal booster, which means when we want to increase our wireless LAN range, so when the signals get weak, the repeaters catch these signals and boost them again so the other far devices get the same speed or data Transfer Rate.
8. **APs:** Stands for Access Points, which means when we want to connect our main devices like computers, servers, and printers with wires, but we also want the other devices to access the same network using wireless technology, then we use the APs with our wired router or switch. This creates a wireless broadcast that allows the other devices to connect to the same network.
9. **Modem:** For modulation and demodulation. Modulation is used to convert the computer signals into readable analogue signals for our ISP (internet service provider) so we can access the Internet. Similarly, the incoming analogue signals from our ISP are translated through demodulation. 
10. **Gateways:** This is the entrance point for each network, which is used to translate the protocols. This is most important when we connect our network to another network, which is based on a communication protocol that is entirely different. We can also say this as a translator that translates the traffic of a network according to other network communication protocols. It can be a dedicated physical device or software that is installed on a computer.

# OSI & TCP/IP model:
Now, I will cover the most important topic in networking: 
The **OSI** and **TCP/IP** models.
While studying these two models, it's essential to understand why we examine them in networks.
So today, the modern Internet works according to these models. The OSI model is actually a conceptual model. We just study it to create large networks and know how these networks and nodes are connected, including today's Internet. This provides us with knowledge about the actual functionality of a network. Through this, it is also easy to troubleshoot a network. 
On the other hand, the TCP/IP model is a theoretical and actually implemented model that allows the different nodes in a network to exchange information with each other wirelessly or with wires or even across the globe. 
If we want to understand these two models in one line, then we simply say that the OSI model is for the logical understanding, and the TCP/IP model is for the actual implementation.

In the OSI model, we cover the different **7** layers that interconnect with each other and do their own duty so the next layers receive the data and understand it. 
The TCP/IP model divides the whole network into **4** different layers. Same as the **OSI** model, in the TCP/IP model, each layer can talk with its next layer and the previous one.

##	1\. OSI model:
OSI means Open Systems Interconnection. The word "open" means any device or node in a network that is capable of accessing information or data from anywhere. The word "interconnect" means that the devices or nodes are connected.
In this model, we will study the 7 layers of data processing.
We studied it from bottom to top, which means we talked about the 7th layer first and then the 6th, 5th, and so on. The reason is that, when we send data or a request to a device or something, it starts to proceed in the sender device from layer **7 to 1**, and when the receiver receives the data, the data proceeds from layer **1 to 7**.
The seven layers are:

7\. **Application layer:** This is where the user directly interacts with the application interface to send data or a request. For example, we send an **HTTP** or **HTTPS** request to a web server; here, the interface of the web and our action to send a request and to work on related protocols- all this is handled in this layer. Similarly, for the SMTP request for the email server, the DNS request for domain resolution, etc.

6\. **Presentation Layer:** This layer is responsible for receiving data from the application layer and translating it for understanding between the network. It translates the data according to the application standard. It also handles the formatting of data, compression if data is large, and encryption/decryption of data for security purposes. The common protocols used by these layers are: **SSL** for website security, **JPEG** for conversions, etc.

5\. **Session Layer:** After the data is ready to send, we need to establish a session between the sending point and the destination. The session layer establishes, maintains, and terminates the session. This layer uses the NetBIOS, **PPTP**, RPC, etc., protocols. 

4\. **Transport Layer:** When everything is ready, we need to transport the data or request. The transport layer decides the reliable delivery path and breaks data into packets for safe and faster delivery. This layer also controls the flow of data, error checking and retransmission, and packet assembly. This layer uses two important protocols: **TCP** (Transmission Control Protocol) and UDP (User Datagram Protocol). **TCP** is more reliable than **UDP** because it ensures the data is safe and sent without errors or loss of packets, but it is slower than **UDP**. **UDP** just provides us with fast speed and doesn't care about errors in data, loss of packets, etc. **UDP** is mostly used in live streaming and video calling.

   <p align="center">
  <img src="OSI_model.png" alt="How OSI model process data">
</p>
   
3\. **Network layer:** This is where the data's logical addresses (IP addresses) are assigned to the data for exact distinction. It also handles the best routes for data. The IPv4, IPv6, ARP, and BGP protocols are used in this layer.

2\. **Data Link Layer:** This layer uses the physical addresses of the device for identification or destination. The data here is broken into frames, and frames contain the physical address of the data and the sequence of the data. This layer removes all the errors from the data and makes it ready for final delivery. In this layer, the connection for the physical layer is also managed.

1\. **Physical layer:** Now, it is time to transfer the raw bit stream of data over the physical media. The data is ready to travel through the physical transmission methods. Here, data conversion is also performed: if the transmission medium is a wire, then the data is converted into electrical signals; for WI-FI and fibre optic, the data is converted into waves and light signals.

<p align="center">
  <img src="Camp_OSI&TCPIP.png" alt="Camparison between OSI and TCP/IP model">
</p>

# IP Addressing:
Now, we are going to cover another important topic: IP addresses. 
This is also important for discussion, as well as for our device security and the way communication between devices is established, which determines the range within which devices or nodes can send or receive data. 

 **Definition:** 
IP stands for Internet Protocol. Think of an IP address like the return address of your computer that decides how data is sent and how your device or the devices receive data. This is the logical address of your device or each node on the network that is able to communicate with other devices or nodes. When a device tries to connect to a network or device, an IP is assigned to this device so that it can communicate with other devices, and after this, the device will be able to send and receive data. These IP addresses are assigned by an ISP (Internet Service Provider) when we connect to a WAN network, and when we connect to a local network, this task is handled by **DHCP (Dynamic Host Configuration Protocol)**. 
There are 2 versions of IP addresses:
  1.	**IPv4:** 
Internet Protocol version four (v4) is an IP address that is written in **4 parts** and separated by dots or periods, like **198.165.21.3** or **0.0.0.0**. It is a 32-bit number and provides almost **4.3 million** combinations. This version uses a subnet mask that decides the range of this IP address. After some time, with the repeated increase in IoT devices, the world feels the shortage of IP addresses. Then, we need another method of assigning IP addresses with a large number of IP addresses, which is **IPv6**.
  2.	**IPv6:** 
An IPv6 address is written in hexadecimal 128 bit numbers. This is a combination of letters and numbers separated by colons. e.g. **2001:0db8:85a3:0000:0000:8a2e:0370:7334**. It has an infinite number of combinations for human needs.

### There are two types of IP addresses for the IOT devices on the networks:
  1.	**Public IP:** 
When we connect directly to the Internet, the IP address assigned by the ISP is called our public IP address. The ISP has a larger number of IPs, and these are used to communicate and identify different devices on the Internet. When we connect with LAN networks, this address is provided to our router, and then this way, we will also be able to access global information even on a local area network.
  2.	**Private IP:** 
When we connect to a LAN network, we get an IP address which is managed by DHCP. For example, mobile phones, laptops, printers, etc., get an IP address from DHCP. This system works on this process: **DORA**, where **D** means discover, **O** means offer, **R** means request, and **A** means acknowledge.
The system first discovers and checks for the availability of IP addresses within its ranges and then offers them to the devices with an acknowledgement action. This enhances the security and reliability of a network. This is normally best for an office, a university, or a small network. But again, to access the information or data from outside of the network, we need a public IP address, and here, we use gateways and routers, which are used to decide the best path and manage the traffic according to protocols for a network to communicate outside our **LAN** network.

### There are two further types of IP addresses in public IPs.
   1. **Static IP:** An IP address that does not change when we connect again and again to a WAN network. These IPs are normally for servers when we want to host our website personally. This is a permanent IP when it is assigned; Google's IP address is an example of a static IP.
   2. **Dynamic IP:** Our ISP has a large number of IPs. When a device connects to the Internet, an IP is assigned by the ISP, and when the device is disconnected, this IP will be reserved for another device. This IP provides us with another benefit too, by providing an extra layer of security, which means when our IP changes frequently, it is very hard for an attacker when he is trying to track our online activities.

### There are two types of websites' IP addresses:
   1. **Shared IP:** Websites that run on shared hosting plans and get a shared IP address. This means a server that runs multiple websites simultaneously; the websites hosted on this server share a single IP address. This technique is cost-saving and also beneficial for security purposes. But the traffic of a site and the number of pages are limited and manageable.
  2. **Dedicated IP:** Websites that are hosted on a personal hosting server get a dedicated IP address. This is a static IP address and never changes once it is allocated. After getting a dedicated IP, a website is also able to run its own FTP for communication.

### Broadcast Address: 
This is another important thing in a network. This is not a device address or anything else. This is actually the last IP address in your network. For example,

**Network ID:** 198.168.1.0 

**Host ID:** 198.168.1.23

The address at the end of a network is a broadcast address. 

**Broadcast address:** 198.168.1.256

That's why the first and the last addresses in a network are not available for host devices. 

#### Now, why is this important?
Suppose you want to send the same type of data to all the host devices in a network at the same time. We don't need to send this data one by one to all devices; we just send this data to the broadcast address, and it automatically sends to all present devices on a network.


<p align="center">
  <img src="Broad%20cast%20address.jpg" alt="The broadcast address">
</p>

The other thing is when a device is lost on a network; suppose a device is trying to find a printer on a network. Now, this is not going to each IP to find out the printer's **IP**. This device normally sends a request to the broadcast address, and the broadcast address shouts out for the printer on the whole network. After this, the printer gives a sign of its presence and shares the IP address with the broadcast address. Lastly, the broadcast address replies to our request by sending us the location or address of the printer on the network.

# MAC addressing: 
MAC stands for Media Access Control. The MAC address and the IP address are two different things. We already discussed the IP addressing in detail above.

We just talk about the MAC address now.

This is a unique **12-digit** hexadecimal address (separated by colons or hyphens) assigned by an organisation at the time of manufacturing. This is the non-changeable physical address of a device in a network. This is very important when we want to communicate with devices in a LAN network. The MAC address works at the **2nd layer** of the **OSI model** to send and receive data between devices. The first **6** digits give us information about the manufacturer, and the last 6 digits identify the network device. 
Examples: 

00:1A:2B – Apple Inc.

3C:5A: B4 – Cisco Systems

AC:67: B2 – Intel Corporation

The full MAC address looks like:

00:1A:2B:3C: 4D:5E (colon-separated)

00-1A-2B-3C-4D-5E (hyphen-separated)

### Type of MAC addresses:
There are 3 main types of MAC addresses:
1. **Unicast MAC address:** When we want a connection between just a server and a device, we use the unicast MAC address. This build connection is actually between two devices in a network.
2. **Multicast MAC address:** When we want to pass a message between a small group of devices at a single time, we use this address. This starts with 01:00:5 and is used normally for streaming, video calling, and gaming. 
3. **Broadcast MAC Address (similar to Broadcast Address):** The MAC address FF: FF:FF:FF:FF:FF is used for sending requests or data segments to each device present in a network at the same time. This is similar to broadcast IP addresses in a network, but this is used only for a local network.
#### Can it be changed?
**Yes,** the MAC address can be changed, but only at the software level. We cannot change the real MAC address assigned by a manufacturer. Some particular software puts a layer of a random MAC address on the original one. Like in Kali Linux, we use the built-in feature (MAC changer) to change our MAC address temporarily at the software level.


# ARP: 
Think of this as a translator between your **IP** address and **MAC** address. **ARP** stands for Address Resolution Protocol, which is a **Layer 2** protocol of the **OSI model**. Suppose you are in a network and want to communicate with another host in the same network. Now you have the IP address of the host, but as you know, within the network, we need the MAC address of the destination host for communication. Now, ARP comes and helps us to find the MAC address of the desired host within a network. We use the ARP request and get the MAC address as a response. ARP sends a broadcast **(FF:FF:FF:FF:FF:FF)**  packet and gets the MAC address of the desired host. 
The packet or request contains the following things: 
1. Your IP 
2. Your MAC
3. Receiver IP
4. Receiver MAC

   **Suppose:**
   
   **Your IP:** 198.168.1.22
   
   **Your MAC:** 00-14-22-01-23-45
   
   **Receiver IP:** 198.168.1.34
   
   **Receiver MAC:**?
   
And here, when the broadcast was received by each host,  the host replied (by sending its MAC) whose IP matched the IP in our request, and finally, we got the MAC address.

Now, suppose you want to know the MAC address of a host outside of your network, and then, in this case, the scenario will be different. This means the source and the destination will connect through routers. 

### Types of ARP:
1. **Proxy ARP:** Suppose there are two networks A and B. A host in network A wants to send a data packet to a host that is in network B. But network B doesn't want to share the MAC addresses of its host devices. Here, network B uses the proxy server to hide the MAC addresses of all host devices. When the host from network A sends an ARP request to the proxy ARP router, instead of sending the destination MAC address, the proxy server sends its own MAC address and handles the further communications on behalf of the destination in network B. This is mostly used for security purposes.
2. **Reverse ARP:** This is actually a normal ARP method but in reverse order, meaning if you have the MAC address of a host device but want to know its IP address, then we use RARP. The source adds its MAC and IP address and the destination MAC address in a request. In response, the receiver sends back its IP address. This is used to update the cache table to handle duplicate IP addresses.
3. **Dynamic and Static ARP:** In dynamic **ARP,** the entries are added by the software automatically, while in static ARP, the administrator writes each IP address with its corresponding MAC address.
4. **Gratuitous ARP:** In gratuitous (without reason) **ARP,** the host asks for the MAC address of its machine. This means it sends a request to the whole network with its own IP address and demands the MAC address. In response, he gets the **MAC address** of his machine. This method is used to announce his own MAC address to the other host or update the cache table.

# Subnet Mask and CIDR notation.
These are two techniques for doing the same job.
1.	**Subnet mask:**  
The subnet mask decides the range and size of a network. It divides an IP address into two parts.
The first three octets (e.g., 198.2.21) decide the network address, and the last part tells us the host number. A private IP address also has a subnet mask, which ranges from **0.0.0.0** to **255.255.255.255.**
This is the hidden part of an **IP address**. Need for a subnet mask because our systems only understand the data in 0s and 1s form.  For example, the IP address is **198.168.1.50**, and the subnet mask is **255.255.255.0**. When the request goes on the network, this mask is translated into 0s and 1s form, like for a subnet mask **255.255.255.0**, the binary form is **11111111.11111111.11111111. 00000000.** To know about the range of a network, we count the 1s in binary data, which tells us, actually, the size of our network. Like in previous binary numbers, we have **24** 1s, which tells us this is a small network, like for a home or for a small corporate office. If we look at the previous IP address, part 198.168.1 is the network ID, and the next number, like 50, is the host ID in the network
2.	**CIDR notation:** 
The CIDR stands for Classless Inter-Domain Routing. We need this **CIDR notation** because writing a subnet mask after an IP address is not good practice. This method converts a whole subnet mask in binary to a single- or double-digit form. Like in previous examples for a subnet mask **255.255.255.0**, when we convert it into binary form, this becomes **11111111.11111111.11111111. 00000000.** So we see this is too long for practical writing. So, the CIDR notation gives us a method to count only 1s in a binary string. As if we count the 1s in the previous binary form subnet mask, which is **24**, we write this number with an IP address that tells us the IP of a host as well as its range or size. Like the IP address 198.168.1.50/24, the last digits 24 are the size of a network.

<p align="center">
  <img src="common subnet mask table.png" alt="Common subnet mask examples">
</p>

# Sub-netting:
The process of slicing a huge network into small pieces is called Sub-netting, and each network is called a subnet. Think of this as a network of a huge company that offers 200 connections, but connecting **200** devices with a network at a time becomes messy. We use the sub-netting technique and divide this whole network into small pieces, like two networks for each 100 host devices. This technique helps us establish better communication between devices and maintain security. 

But here again, we use the subnet mask that describes an IP address with two parts and also tells us the range and number of **IP addresses** that would be offered by a network. It tells us where the host ID starts and where the network **ID** ends. When we divide a network, a subnet mask borrows a bit from the previous network and creates a new one. 
#### Like:
**IP address is:** 198.168.1.50
        
**The subnet mask is:** 255.255.255.0
                                                        
After dividing it into two networks, it becomes two subnets.

**First subnet network ID:** 198.168.1.0
                                                        
**Second Subnet network ID:** 198.168.1.128

After this, the subnet mask will be:

**First network mask:** 255.255.255.128
                                                        
**Second network mask:** 255.255.255.128

### There are two methods of dividing a network into subnets:
1.	**FLSM:** 
The Fixed Length Subnet Mask divides a network into equal parts. Think a network offers **50 connections**, and when we convert it using the FLSM technique, it will divide this network in equal two parts, which means 25 connections for dividing this network into two parts. This is actually not a good practice because when the other network needs only **2 or 3** connections, then the remaining connections or IP addresses become useless, and still, this is not a good network.
2.	**VLSM:**
 In Variable Length Subnet Mask, we divide a network according to the exact needs of the network. This means that if we want to create two networks, the first needs **40 connections**, and the second one needs **60 connections**, and our total network capacity is **100** connections, then we divide this network using the **VLSM** technique. 
Before this technique and CIDR, we divided a network using the rigid classes technique, in which we divided a network according to A, B, C, D, and E classes. Here

A = A huge network that offers more than 16 million IPs for its devices.

B = A medium network that offers almost 65000 host IPs.

C offers almost 256 connections or IPs, and the other D and E are used for smaller networks. Before sub-netting, this technique fails because suppose a network working with 256 host devices, and now the company has grown and wants to buy an upgraded class network, which is class B, which offers **65000 host IPs**. Now, here, these may be too large for the present devices. Sub-netting solves this for today's modern networks.

**Host range:** 
The number of IPs that are usable for host devices like your router, mobile, printer, etc., is called the host range. In a network, the first IP is the network ID, and the last IP is the broadcast address. All the middle IPs are for the host devices, and this is also the host range.

||
| :---: |
**Network ID:** 198.168.1.0 
**Subnet mask:** 255.255.255.0
**Host range:** 198.168.1.1 to 198.168.1.255.
**Broadcast address:** 198.168.1.256 

# Ports, services, and protocols:

This is another important concept in networking and cybersecurity/ethical hacking. During scanning a system, this plays an important part in knowing which types of vulnerabilities and services exist. Ports and protocols allow us to collect some important information like version, open ports, etc., about the system.
1.	**Ports:**
 Think of ports like a room inside a building. This is the part of an IP address. You can also consider an IP address as a building and the ports as rooms inside the same building. There are almost **65535** total ports that exist in a system. Actually, every single service is like watching a video on YouTube, chatting with friends, getting mail from the office, etc.; it uses a different port or room in the building. Multitasking on a device is actually possible through different ports in a system. Some common ports in a system are 443 for HTTPS traffic, **8080** for **HTTP** traffic, and **25** for **SMTP**. Each port uses a specific protocol.  
There are almost 0 to 1000 well-known and mostly used ports in a system. From **1025** to **49151**, registered ports are used by applications; for example, port 8080 is an alternative to HTTP, and **3306** is for MySQL Server. The ports from **49152** to **65535** are used by the client side. Like you getting a response from a server. 


|Some common ports are:|
| :---: |
20     FTP Data
21     FTP Control
22     SSH
23     Telnet
25     SMTP
53     DNS
80     HTTP
110    POP3
143    IMAP
443    HTTPS

2.	**Protocols:**
These are sets of rules and regulations used by a port that can send and receive requests. Think of this as a specific language used by a port when communicating with other devices. The number **443** is the port number, and **HTTPS** is the protocol used to load a website securely. Similarly, **TCP** and **UDP** are the transmission protocols used to communicate between devices. For sending mail, we use the **SMTP** protocol, and for converting the domain name to
the IP address, we use the DNS (phone book), and so on.

<p align="center">
  <img src="protocols2.png" alt="Common Protocols" width="500">
</p>

These protocols are responsible for reliable and secure data movement by checking for errors, lost packets, retransmission, and ordering the data.

The TCP protocol is connection-oriented and uses a three-way handshake technique to talk with a device. 
Send a **SYN** request and get an **ACKNOWLEDGEMENT** with **SYN** and then send another **SYN** for ready to connect. We use it when we need perfect data. This is much slower than the UDP use for when data is important, like sending an email or chatting with a friend.
On the other hand, when we all focus on speed, we use the **UDP** (Connectionless) protocol. Here, the protocol doesn't care about the order of packets, retransmission, or error checking; it just sends data speedily. This is used for video calling, live streaming, live games, etc.

3.	**Services:**
 When we send a request through a specific port using a specific protocol, the other side, which is waiting for the connection, is known as a service. This is actually a running task on the server side. Like in the **HTTPS protocol**, the web server is waiting for the connection, and the process running during this is called a service. 
For example, we want to send an email to someone, and the process will be:

**Port:** 25

**Protocol:** SMTP

**Service:** The mail server is ready for further processing
|Some common services and protocols are:|
| :---: |
Web Server                     ( HTTP)              
Secure Web Server               (HTTPS)
SSH Server                      (SSH)
Mail Server                     (SMTP)
DNS Server                      (DNS)

# DNS:
Now, we will discuss about the DNS, which is essentially a book that maps IP addresses to their corresponding names. DNS stands for Domain Name System. Before DNS, the only way to browse a website or information on the Internet was to use the corresponding IP address to visit the specific site. After the repeated increasing of the website in the whole world, it becomes difficult to remember the IP address of each one. The human mind interacts with pictures and letters easily, but remembering numbers, especially when there are too many, becomes difficult. After that, the system of domain names was introduced, where we gave a unique name to every IP address. To find a domain by its name, we use the Domain Name System(DNS), which is responsible for giving us the IP address of the corresponding domain. 
Let's suppose we try to access the Google.com website. There are two ways to access this site: one by its name, the second by its IP address (8.8.8.8). 

When we try to access it by its name, the DNS system works for us to convert our name into the corresponding IP address and gives us back the IP to access the information inside this IP(website). 

This process only happens when we try to access a website for the first time because a memory in our ISP has the IP address of the recently visited website, which is called cache memory. 

Let's suppose we want to access the example.com website for the first time; then this process happens in two ways: the recursive method and the iterative method. 

1.	**Recursive Method:**
 Suppose you want to access example.com. When you type the name of the site, the DNS resolver takes your query and forwards it to the Root Server. The root server further starts to read the query from right to left, which means the .com gives the direction or address to the Root Server to the next destination, which is the **Top-Level Domain**. Here, the tasks are divided according to the top-level domains. Like .com, .edu, and .pk are top-level domains, for each, a query takes place in a different box where the .com is present; similarly for .edu and so on.  After this, the top-level domain reads the query and sends it to the Authoritative Server, which holds the real IP address. This gives the real IP address back to the top-level domain; the top-level domain gives this IP address back to the root server; the root server gives the IP back to the DNS resolver; and finally, the DNS resolver gives this IP back to us.





