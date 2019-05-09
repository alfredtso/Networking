
# Terminology 
 Packet-switched networkds
	- like DHL, have distribution centre
- Packet 
- TCP (Tranmission Control Protocal)
- IP (Internet Protocol)
	- specifies the format of the packets sent and received among routers and end systems. 
- The Internets's principal protocol are collectively know as TCP/IP
- When involve multiple end systems that exchange data with each other, the app is distributed applications
	- Question is how does one programming running on one host instruct the internet to deliver data to another program on another host?
	- End systems attached to the internet provide a socket interface help this
		- A set of rules that the sending prog must follow
			- like the way we use postal service, stamp on the right, envelope..
			- and postal service provides more that one service, express, reception confirmation ... etc
- DSL (Digital subscriber line)
- Cable
- FTTH (fiber to the home)
	- each home has an optical network terminator (ONT)

- Subnet Mask
	- An IP address is divided into two logical parts
		- the network prefix
		- the host identifier
	- Format: 32 bits and use dotted-decimal notation
		- 255.255.255.0 is the subnet mask for the prefix 192.51.100.0/24
	- neither works like an IP address nor does it exist independently
	- applying the subnet mask to an IP address split the address into
		- extended network address
		- a host address

## Protocol
- Analogy
	-  People ask for time
	-  make use of answer and question
		-  depending on the answer, one would be able to generate the next question
		
## Physical Media
1. Guided media
	- the waves are along a solid medium, fibre-optic cable, twisted-pair copper
	1. Twisted-pair copper wire
		- consist of two insulated copper wires, about 1mm, twisted tgt to reduce electrical interference from similar pairs.
		- Unshielded Twisted Pair is one example and range 10Mbps to 10Gbps
		- category 6a cable can achieve 10Gbps and becoming the dominant solutin for high-speed LAN
	2. Coaxial cable
		- The copper conductors are concentric, quite common in cable tele
		- shared
	3. Fiber Optics
		- A pulse representing a bit
		- immune to electromagnetic inference, long range, hard to tap 
2. Unguided media
	- the waves propagate in the atmosphere such as in wireless LAN
	1. Terrestrial Radio Channels
	2. Satellite Radio Channel
		- a communication satallite links two or more Earth-based microwave transmitter/receivers
		1. Geostationary satellites
			- remain same spot
			- above 36k km, has 280 ms delay
			- can operate at speeds of hundred of Mbps
		2. low-earth orbiting satellite

## Packet Switching
- To send a message from a source end system to a destination, the source breaks long messages into smaller chunks of data knows as packets.  
- each packet travels through communication links and packet switches (router and link-layer switches) 

## Protocol Layering
- Application layer protocol like HTTP almost always implemented in software
	- So are transport-layer protocols
- Network layer is often a mixed implementation of soft and hardware
- Layer n protocol can be distributed among the end systems, packet switches and other componenet in the network, ie often there is a piece of layer n somewhere in the network
- Protocol layering provides a structured way to discuss system components and modularity makes it easier to update system componenets.
- Potential drawback of layering
	- Duplication of lower-level functionality
		- error recovery
	- Functionality at one layer might need info that is present only in a particular layer
		- violates the goal of separation of layers
- Protocols of various layers are called protocol stack
	- Physical
		- to move the individual buts within the frame from one node to the next, protocols depend on the actual medium of the link such as twisted-pair copper wire or fiber optics
		- eg Ethernet has many physical-layer protocol, one for coaxial cabler, another for fiber and so on
	- Link
		- Services provided by the link layer depend on the specific link layer protocol, such as Ethernet and Wifi provide diff service 
		- packet referred as frames
	- Network
		- packet refered to as datagrams
		- including IP protocol, defines the fields in the datagram and how the end systems and router act on these fields
		- only one IP protocols and many routing protocols
	- Transport
		- Used to transports application-layer messages with either TCP UDP
		- packet refered to as segment
	- Application
		- such as HTTP, SMTP, FTP, DNS(domain name system)
		- packet of info at this layer refered to as **message**

## Encapsulation
- An application-layer message is passed to the transport layer, the transport layer takes the message and appends addition info taht will be used by the receiver-side transport layer.
- a packet has two types of fields: header and a payload field

## Network under Attack
- Malware is usually self-replicating nowadsays
	- Viruses are malware that require some form of user intereaction to infect
		- eg e-mail containing malicious executable
	- Worm are malware that can enter a device without any user intervention
- Denial-of-service (DoS)
	- Vulnerability attack
	- Bandwidth flooding
	- Connection flooding
- Packet sniffing
- Masqureade as another user
	- IP spoofing
		
# Review Question
- What is the difference between a host and an end system? List several different types of end systems. Is a Web server an end system?
  - End systems are also referred to as hosts because they host (that is, run) application programs, these two terms can be used interchangeably. Host sometimes further divided into clients and services
- Circuit switch Vs Packet switching
	- in Circuit switched network, the resouces needed along a path are reserved for the duration of the comm between the end systems, packets' are not
	- circuit can transfer the data to receiver at the guaranteed constant rate
	- dedicated circuit are idle during slient periods -> underutilized
	- packet better sharing of tranmission capacity, simplier
 
