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

## What is Network/Networking?
While studying networking, let's first discuss the term' network' or networking. 
A network means at least two or more devices connected with each other to share information and process data. Here, devices connected with each other are called a network.
The process of communication between two or more devices is called networking.
In technical terms, every single device that is present in a network is called a node.
##	Types of Networks:
1.	LAN: LAN stands for Local Area Network, which works between nodes that are present in a particular network and connected with wires. No outsiders are allowed to access communication or data from this type of network. e.g., a network of your university lab.
2.	WAN: WAN stands for Wide Area Network, which means the Internet we use nowadays to access information or data worldwide. It can also be used to connect two or more LANs
3.	MAN: MAN stands for Metropolitan Area Network, which means a network that covers a city, a town, or a particular area that can be from 5 kilometres to 50 kilometres. This is larger than LAN and smaller than WAN
4.	PAN: Stands for Personal Area Network, which is used to establish a connection between a single person. e.g., a Bluetooth or NFC connection between a single device or person.
5.	WLAN: Stands for Wireless LAN, which is similar to LAN, but connects each node without a wired connection.
Sometimes, a VPN (virtual private network) is also considered a type of network because it allows us to connect to our destination by creating a virtual and private network connection by masks our IP (Internet Protocol) to keep everything private.

#	Network Devices:
In this session, I will discuss the types of physical devices we use to establish our network, enabling nodes to communicate with each other effectively.
For a cybersecurity or ethical hacker, Lerner, it is very important to know how data travels between different devices or networks
1. Router: A physical device that routes our traffic to access data from outside (from other LA parts or the Internet) of the network. It decides the best way for data to travel efficiently. e.g., We use a router in a LAN to access the WAN.
2. NIC: (Network Interface Card) This is a device or card that gives a system a particular address (assigned during manufacturing), which is used to get data from other devices and send data to other devices or nodes using this address. Modern devices have built-in NICs.
3. HUB: This particular device is used to send and receive data between different nodes within a network. The drawback of this device is that when we send a data segment to a particular node, it sends this same data to each node in the network; we get a, huge amount of traffic between devices, causing a slowdown in the network. To control this traffic, we use switches nowadays.
4. Switch: This is actually a HUB, but it sends and receives data between nodes or hosts intelligently. A switch has the address of each node in the network. When we send data to a particular node, it will match the address and only allow the corresponding device to receive data. This feature will help us to keep the traffic controlled within a network.

## There are further types of switches.
*	Circuit Switching: In Circuit Switching, we turn a full circuit into a path for sending data between just the sender and receiver. During this process, a dedicated path has been established between the sender and the destination address. No one else uses this path until they cut their connection.
*	Message Switching: In this type, a network uses a store-and-forward technique in which the whole data set is first stored in the switch and then sent to the destination address entirely at a time.
*	Packet Switching: In this technique, data travels between the sender and receiver by creating small segments of data. Each data packet receives the destination address and begins moving without considering the other data packets. 

    ## There are two types of packet switching: 
*	Connectionless or datagram approach: In this method, data packets start to move just by receiving the destination address. Every packet of data uses a different path in the network to reach the destination address. 
*	Connection-oriented or virtual circuit: During this, a connection has been established between sender and receiver. A virtual path has been created, and each data packet should follow this exact path to reach the destination address.

   



















