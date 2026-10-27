# Date : 27.07.2026
# Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/95dbb825-7a57-4a1e-97c2-6272694bbe22" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output 
•	Router CLI configuration 
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/79691ba3-c9ea-464c-abe7-353c962b4f73" />
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/7cb820c4-0b27-46aa-9030-e41066f260d9" />


•	IP configurations on PCs 

<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/75f2e4bd-b214-440c-a576-98a5b41b7c51" />
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/b9a7e290-63a7-4847-aa78-c94de2f05e03" />



•	Successful ping between PC0 and PC1
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/4e214a2c-97e7-4123-9f92-584d891c260e" />
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/34cadc97-13a9-4295-835c-229199836b66" />


________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

