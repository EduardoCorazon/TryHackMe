# Packets & Frames

# TCP/IP Model

TCP is connection-based meaning that a realizable connection between client and server must be established before data is sent.

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled.png)

### TCP Packets

Contain sections of information known as headers that are added from encapsulation

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%201.png)

### Three-Way Handshake

Used to establish a reliable connection between two computers. It uses a few special messages listed below:

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%202.png)

Data sent is given a random sequence number and when reconstructed on the other computer the sequence number increases by +1. The order is based on these steps:

1. SYN - client provides initial sequence number (ISN) of 0 to **SYN**chronise with
2. SYN/ACK - Server provides ISN of 5000 to **SYN**chronise with and **ACK**nowledge the client ISN of 0
3. ACK - client **ACK**nowledge server ISN of 5000 and provides the final sequence number: ISN+1 (5000+1)

The table below Best explains this relationship:

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%203.png)

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%204.png)

### TCP closing a connection:

TCP closes a connection once a device has determined that the other device has received the data. It’s best practice to close TCP connections as soon as possible since it takes up system resources.

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%205.png)

##########################################################################

# UDP/IP Model

UDP is a stateless protocol meaning it doesn’t require a constant connection between two devices, aka a three-way handshake does not occur.

### UDP Packets

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%206.png)

### UDP Connection

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%207.png)

##########################################################################

# Ports 101

Ports range from 0 to 65,535

Well known ports (aka common ports) are from 0 to 1024

The format for ports is: {IP}:{port} 

for example 10.0.0.4:80 ←HTTP is running on port 80 on PC 10.0.0.4

![Untitled](Packets%20&%20Frames%20ed169171f0f947ab9b7f3cd8871b6537/Untitled%208.png)

For a full list of common ports:

[http://www.vmaxx.net/techinfo/ports.htm](http://www.vmaxx.net/techinfo/ports.htm)