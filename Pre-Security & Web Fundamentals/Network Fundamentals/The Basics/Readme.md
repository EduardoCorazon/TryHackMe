# The Basics

ipconfig ← Windows | ifconfig ← Linux

IP = Internet protocol, identifies devices on a network, **logical identifier**

MAC = Media Access Control, can be spoofed, **physical identifier**

^every device has a NIC (Network Interface Card) which has a unique MAC

ICMP = ping 

**Default Gateway = router’s IP** 

It’s the address of a device on the network that can send information to another network (it’s usually the first or last host address in a network) | NOTE*: In the case of a subnet network 

**Subnet Mask:** 

identifies how many host and networks can be made, for ex an ip 10.0.0.x/24 means there is only one network and x has to be between 1-254 ****

![Untitled](The%20Basics%20e0842de49ec64801b750170345beac88/Untitled.png)

Subnet Class:

![Untitled](The%20Basics%20e0842de49ec64801b750170345beac88/Untitled%201.png)

**CIDR (aka class notation)**: /24 = subnet of 255.255.255.0 → /32 subnet of 255.255.255.255

Address Resolution Protocol (ARP):

arp -a

**ARP Request**: asks devices on a network whether or not it has a specific IP address

**ARP Reply**: If the device does have the requested IP it will return an acknowledge message and the initial device will store the IP and MAC relationship in its cache.

AKA. associates an IP address with a MAC address

![Untitled](The%20Basics%20e0842de49ec64801b750170345beac88/Untitled%202.png)

Dynamic Host Configuration Protocol (DHCP):

Assigns a dynamic IP address to a device on a network. The IP address can be set to static or it can be set to lease meaning it will be renewed after a certain period of time

![Untitled](The%20Basics%20e0842de49ec64801b750170345beac88/Untitled%203.png)