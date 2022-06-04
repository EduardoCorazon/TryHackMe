# Local Area Network (LAN)

### Star Topology:

Most commonly used, devices are connected to a central switch. The switch then relays frames between devices and keeps track of each device’s MAC address in its CAM table

Pros: More Scalable and efficient

Cons: More expensive than other topologies and requires more maintenance with scale thus increasing troubleshooting

![Untitled](Local%20Area%20Network%20(LAN)%20bfc24f49171442e6b9b411ae447e65b6/Untitled.png)

### Bus Topology:

All devices are connected to a single cable called the backbone. Prone to bottlenecking and slowness if devices are simultaneously requesting data. Thus making it difficult to troubleshoot since all data travels the same route.

![Untitled](Local%20Area%20Network%20(LAN)%20bfc24f49171442e6b9b411ae447e65b6/Untitled%201.png)

Pros: Easiest and most cost-efficient to set up 

Cons: Can’t handle large amounts of data ; A single point of failure along the backbone cable can break the entire network

### Ring/Token Topology:

Devices are directly connected to each other meaning there is little cabling compared to a Star Topology. It sends data across the loop until it reaches the destined device. A device will only send received data from another device if the device does not have any data to send itself. If it does happen to have data, it will send its own data first before sending the data from another device.

![Untitled](Local%20Area%20Network%20(LAN)%20bfc24f49171442e6b9b411ae447e65b6/Untitled%202.png)

Pros: Because data only travels in one direction it’s easy to troubleshoot ; less prone to bottlenecks because large amounts of traffic are not traveling across the network at any one time.

Cons: It’s not an efficient way to send data ;  a cut-cable or broken device will result in the entire network breaking.