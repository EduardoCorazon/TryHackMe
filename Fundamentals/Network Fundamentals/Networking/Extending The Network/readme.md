# Extending The Network

# Port Forwarding:

Allows you to access a service/port on an internal network over the internet. For example 192.168.1.10 is hosting a service on port 80, I enable port forwarding so I can access that service via the routers IP. So to access I would type in 82.62.51.70:80 

![Untitled](Extending%20The%20Network%20a3ce3a26f10940b48331880450950122/Untitled.png)

# Firewall

Used to permit or deny traffic entering or exiting a network. Can be a dedicated device, embedded in a router, or a software like [Snort](https://www.snort.org/). There are 5 categories of firewalls but in general there are 2 key ideas that distinguish them. 

Stateful - determines the behavior of a device based upon the entire connection, consumes more resources since it’s dynamic, if a connection from a host is bad, it will block the entire device.

Stateless - Inspects individual packets, use fewer resources but are only effective based on the rules, good for defending against DDoS attacks, a device sending a bad packet will not mean that the entire device is blocked. 

![Untitled](Extending%20The%20Network%20a3ce3a26f10940b48331880450950122/Untitled%201.png)

![Untitled](Extending%20The%20Network%20a3ce3a26f10940b48331880450950122/Untitled%202.png)

# VPN

A Virtual Private Network allows two computers in different networks to communicate with each other securely. For example, only devices on the same network can directly communicate. The devices connected to network #3 are still part of their isolated networks but also create a VPN so only devices that are connected via this VPN can communicate with each other.

![Untitled](Extending%20The%20Network%20a3ce3a26f10940b48331880450950122/Untitled%203.png)

![Untitled](Extending%20The%20Network%20a3ce3a26f10940b48331880450950122/Untitled%204.png)

# VLAN

A Virtual Local Area Network allows specific devices within a network to be virtually split up. This means they both benefit from an internet connection but are treated separately, thus each vlan can have different rules thus adding security. 

![Untitled](Extending%20The%20Network%20a3ce3a26f10940b48331880450950122/Untitled%205.png)

^In the example above, the Sales Department and Accounting Department both have access to the internet but are not able to communicate with each other