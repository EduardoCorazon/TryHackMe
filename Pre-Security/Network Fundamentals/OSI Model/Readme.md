# OSI Model

Open Systems Interconnection Model, used to illustrate how information is sent through the internet (from top to bottom 7 → 1)

![Untitled](OSI%20Model%20a6da548c92974b2d89cce21fd3ac4904/Untitled.png)

# Layer 7 - Application

Deals with everyday applications like email clients, browsers, or file servers. Mostly used in Graphical User Interfaces (GUI) for users to interact with data sent or received.

# Layer 6 - Presentation

Acts as a translator for data to and from the application layer (layer 7). The receiving computer will understand data sent to a computer in one format destined for in another format. For ex. when you send and email, the other user may have different email client, but the content of the email will still need to display the same information. Security Features like data encryption (HTTPS) occur at this layer.

# Layer 5 - Session

Once data has been translated from layer 6, the session layer begins to create a connection to the other computer that the data is destined for. Once a connection is established a session is created, It Synchronizes two computers to ensure that they are on the same page before data is sent and received. The layer divides up the data into smaller chunks (packets) and sends each piece one at a time. So if there is an error, it only needs to resend specific packets and not the entire data itself. Sessions are unique, meaning data can only travel across it’s session and can’t travel over different sessions.

# Layer 4 - Transport

Two different protocols:

**TCP** (Transmission Control Protocol) : Designed with reliability and guarantee. Used for File sharing and download, internet browsing, or sending an email.  Incorporates error checking

![Untitled](OSI%20Model%20a6da548c92974b2d89cce21fd3ac4904/Untitled%201.png)

**UDP** (User Datagram Protocol) : No synchronization, useful when small pieces of data are being sent like ARP, DHCP, or video streaming.  

![Untitled](OSI%20Model%20a6da548c92974b2d89cce21fd3ac4904/Untitled%202.png)

# Layer 3 - Network

Work with IP address, devices like routers are known as “layer 3 devices”. Routing determines the optimal path packets should be sent. It does this via the OSPF (Open Shortest Path First) and RIP (Routing Information Protocol). Re-assembles data from small packets chunks to a large piece of data.

# Layer 2 - Data Link

Works with MAC addresses, It receives packets from the network layer and sends them to the correct endpoint in the network by MAC address identification.

# Layer 1 - Physical

Layer refers to the physical components of hardware used in networking ie Ethernet Cables. Devices use electrical signals to transfer data via binary 0 and 1 electric pulses. 

![Untitled](OSI%20Model%20a6da548c92974b2d89cce21fd3ac4904/Untitled%203.png)