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

##	OSI model:
OSI means Open Systems Interconnection. The word "open" means any device or node in a network that is capable of accessing information or data from anywhere. The word "interconnect" means that the devices or nodes are connected.
In this model, we will study the 7 layers of data processing.
We studied it from bottom to top, which means we talked about the 7th layer first and then the 6th, 5th, and so on. The reason is that, when we send data or a request to a device or something, it starts to proceed in the sender device from layer **7 to 1**, and when the receiver receives the data, the data proceeds from layer **1 to 7**.
The seven layers are:

7. **Application layer:** This is where the user directly interacts with the application interface to send data or a request. For example, we send an **HTTP** or **HTTPS** request to a web server; here, the interface of the web and our action to send a request and to work on related protocols- all this is handled in this layer. Similarly, for the SMTP request for the email server, the DNS request for domain resolution, etc.
6. **Presentation Layer:** This layer is responsible for receiving data from the application layer and translating it for understanding between the network. It translates the data according to the application standard. It also handles the formatting of data, compression if data is large, and encryption/decryption of data for security purposes. The common protocols used by these layers are: **SSL** for website security, **JPEG** for conversions, etc.
5. **Session Layer:** After the data is ready to send, we need to establish a session between the sending point and the destination. The session layer is responsible for establishing the session, maintaining it, and terminating it. This layer uses the NetBIOS, **PPTP**, RPC, etc. protocols. 
4. **Transport Layer:** When everything is ready, we need to transport the data or request. The transport layer decides the reliable delivery path and breaks data into packets for safe and faster delivery. This layer also controls the flow of data, error checking and retransmission, and packet assembling. There are two important protocols used by this layer: **TCP** (Transmission Control Protocol) and UDP (User Datagram Protocol). **TCP** is more reliable than **UDP** because it ensures the data is safe and sent without errors or loss of packets, but it is slower than **UDP**. **UDP** just provides us with fast speed and doesn't care about errors in data, loss of packets, etc. **UDP** is mostly used in live streaming and video calling.


   



















