This project simulates a network between offshore ship network and onshore network using Cisco Pocket Tracer. 
<img width="653" height="435" alt="image" src="https://github.com/user-attachments/assets/0194441c-da0b-4886-a7ac-39e1987fb7a2" />

The network consists of two routers, two switches, two offshore computers, one office computer onshore and one server onshore. 
Offshore network represent the ship’s operational environment and consists of router (ship-R1), switch and two crew computers (PC1 and PC2). Both computer belongs to VLAN 10 (ship operations).
Onshore network represents the shore-based business and server. It consists of router (shore-R2), switch, one business computer (PC3) and server. It is divided into VLAN 20-business and VLAN 30 -server. 
Offshore and onshore routers are connected using 10.0.0.0/30 subnet

The following IP addresses were implemented:\
Ship PC1	(192.168.10.11	  255.255.255.0	  192.168.10.1)\
Ship PC2	(192.168.10.12	  255.255.255.0	  192.168.10.1)\
Shore PC3	(192.168.20.11	  255.255.255.0	  192.168.20.1)\
Shore Server	(192.168.30.10	  255.255.255.0	  192.168.30.1)


ACLs are implemented to improve network security and restrict unauthorized communication between the different networks.
The network connectivity and ACL functionality was tested using Cisco Pocket Tracer to verify the effectiveness of security policies.  

Test	Expected Result
Ship PC1 to Shore Server   	Successful\
Ship PC2 to Shore Server	Successful\
Shore-PC3 to Shore Server	Successful\
Ship PC1 to Shore-PC3	Blocked\
Shore-PC3 to Ship PC1	Blocked\
Shore-PC3 to Ship PC2	Blocked


