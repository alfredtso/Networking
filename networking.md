
# Terminology 
- Packet-switched networkds
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

