# Introductory Networking

## Table of Contents

## The OSI Model
When discussing computer networking, there are two models which are generally used to describe the theory behind networks: OSI (Open Systems Inteconnection)
and the shorter TCP/IP (Transmission Control Protocol/Internet Protocol). The OSI model has 7 layers that describe how communication occurs between computers.
### Physical
This layer describes the physical hardware of the computer and the means of sending electrical pulses which communicate information. Devices that operate at
this layer inlcude repeaters, modems, transceivers, and hubs.
### Data Link
The second layer of the model is concerned with the physical address of the NIC or the MAC (Media Access Control) address. When delivering information on the
local network segment, ARP (Address Resolution Protocol) will be used to locate the device with the correct MAC address and send it the data. Devices that 
operate on the data link layer include switches, bridges, wireless access points, and the NIC (Network Interface Card).
### Network
While the data link layer works with physical addressing, the Network layer uses logical or IP addresses to send data. Having an IP address for the intended
recipient is required in order for data to be transmitted outside of the local network. This address comes in the form of IPv4 (most common addressing scheme)
or IPv6. Devices that work at this layer include routers, layer 3 switches, and packet filtering firewalls. 
### Transport
The transport layer is responsible for selecting the protocol with which the data will be transmitted. The TCP (Transmission Control Protocol) is connection
oriented which means that it ensures proper delivery of each packet and allows the receiving host to control the speed of the transfer. UDP (User Datagram Protocol)
is connectionless and makes no effort to ensure that all of the packets were received. The latter protocol is more often used in real time applications in which 
some missing data is not likely to have a major impact like video conferencing. Multilayer switches, advanced firewalls, and Itrusion Detection Systems operate at 
this layer.
### Session
Functions of the session layer include establishing and ending sessions and managing data transfer. Sessions are unique to the communicating devices and are important
for ensuring that data is kept orderly. Dialog can occur in 3 different formats: simplex where one system talks and the other only listens, half duplex in which only
one computer or the other can communicate at a time, and full duplex in which both hosts can communicate simultaneously.
### Presentation
The concern of the presentation layer is transforming data to ensure that it is in a format that is useable for the required application. It is at this layer that 
compression and decompression or encryption and decryption will occur. 
### Application
The application layer provides an interface for software programs on hosts which can then be used to transmit data. 

### Review Questions
* Which layer would choose to send data over TCP or UDP?
- 4
* Which layer checks received packets to make sure that they haven't been corrupted?
- 2
* In which layer would data be formatted in preparation for transmission?
- 2
* Which layer transmits and receives data?
- 1
* Which layer encrypts, compresses, or otherwise transforms the inital data to give it a standardised format?
- 6
* Which layer tracks communications between the host and receiving computers?
- 5
* Which layer handles logical addressing?
- 3
* When sending data over TCP, what would you call the "bite-sized" pieces of data?
- Segments
* Which layer would the FTP protocol communicate with?
- 7
* Which transport layer protocol would be best suited to transmit a live video?
- UDP

## Encapsulation
Encapsulation is the name of the process that occurs when data is passed down the OSI stack starting at the application layer. At each layer a header, or PDU
(Protocol Data Unit), is added to the data. This header contains information relevant to the specific layer like a destination and source IP address at the 
Network layer or an indication of which protocol is being used to transfer the data at the transport layer. The physical layer is the only one where a PDU is not added.
When the reciving host receives the data it performs the process of de-encapsulation and uses the information in the PDUs to ensure the data reaches its proper place. 
This process of communication is important because it standardizes the ways in which computers communicate. Without these processes, it may have been entirely impossible
to communicate with some other hosts on the Internet. 

### Review Questions
* How would you refer to data at layer 2 of the encapsulation process?
- Frames
* How would you refer to data at layer 4 of the encapsulation process?
- Datagrams
* What process would a computer perform on a received message?
- De-encapsulation
* Which is the only layer of the OSI model that adds a *trailer* during encapsulation?
- Data link
* Does encapsulation provide an extra layer of security (Aye/nay)?
- Aye

## TCP/IP Model
While the OSI model is used for learning about the basics of networking, the TCP/IP model more accurately reflects the basis of understanding computer networking in 
the real world. While the functions of each of the 7 OSI model layers are still present, they are now condensed down into 4 layers. 
### Network Interface
Encompasses the OSI physical and data link layers. 
### Internet
New name for the OSI network layer. 
### Transport
The same as the OSI transport layer. 
### Application
Encompasses the session, presentation, and application layers of the OSI model.
### TCP
Transmission Control Protocol is one important part of the suite of protocols that make up TCP/IP. Since this protocol is connection oriented, it has a very specific 
manner in which it sets up and tears down connections. The process of creating a connection with another host is called the three-way handshake since there are a series
of 3 messages which are sent. First, the host sends a SYN (synchronize) packet to the other host to let it know that it wants to connect. The receiving host then sends
a SYN/ACK (synchronize/acknowlegement) to inform the sending host that it has received its connection request. Finally, the sending host sends an ACK (acknowledgement) packet 
to the receiving host and the connection is now established. 

### Review Questions
* Which model was introduced first, OSI or TCP/IP?
- TCP/IP
* Which layer of the TCP/IP model covers the functionality of the Transport layer of the OSI model?
- Transport
* Which layer of the TCP/IP model covers the functionality of the Session layer of the OSI model?
- Application
* The Network Interface layer of the TCP/IP model covers the functionality of two layers in the OSI model. These layer are the Data-Link and?..
- Physical
* Which layer of the TCP/IP model handles the functionality of the OSI network layer?
- Internet
* What kind of protocol is TCP?
- Connection-based
* What is SYN short for?
- Synchronise
* What is the second step of the three-way handshake?
- SYN/ACK
* What is the short name for the "Acknowledgement" segment in the three-way handshake?
- ACK