# Nat-OSPF-ACL
Ospf,Nat,ACL project
Introduction

You are completing the configuration of the Corporation One network.

You are not required to configure host addressing.

You will practice and be assessed on the following skills:

=    Configuration of OSPFv2 routing

=    Customization of OSPF.

=    Configuration of static NAT.

=    Configuration of dynamic NAT with PAT.

=    Configuration of various types of ACLs.

=    Configuration of a router with NTP as a system time source.

=    Backing up an IOS image to a TFTP server.

Instructions

Part 1:      Configure OSPF

Step 1:      Activate OSPF.

Use process ID 10 for OSPF activation on all routers.

a.     Activate OSPF by configuring the interfaces of the network devices in the Satellite network, where required.

b.     Activate OSPF using network statements and inverse masks on the routers in the Corporate network.

Note: For the purposes of this assessment, please enter the network statements in the following order:

1)     On RTR-D

=   the Serial0/1/1 network

=   the Serial0/2/0 network

=   the Serial0/1/0 network

2)     On RTR-E

=   the Serial0/1/1 network

=   the Serial0/1/0 network

=   the GigabitEthernet0/0/0 network

3)     On RTR-F

=   the Serial0/1/0 network

=   the Serial0/1/1 network

=   the GigabitEthernet0/0/0 network

=   the GigabitEthernet0/0/1 network

Step 2:      Configure router IDs.

Configure router IDs on the multiaccess network routers as follows:

RTR-A: 9.9.9.9

RTR-B: 8.8.8.8

RTR-C: 7.7.7.7

Step 3:      Customize OSPF operation.

a.     Configure router RTR-A with the highest OSPF interface priority so that it will always be the designated router of the multiaccess network.

b.     On router RTR-A, configure a default route to the ISP cloud using the exit interface command argument.

c.     Automatically distribute the default route to all routers in the network.

d.     Configure the hello and dead timer values on the interfaces that connect RTR-A and RTR-D to be twice the default values.

e.     Configure the OSPF routers so that the default cost value for all Gigabit Ethernet interfaces will be 10 and the cost value for Fast Ethernet will be 100.

f.       Configure the OSPF cost value of RTR-D interface Serial0/1/1 to 50.

g.     Configure OSPF so that routing updates are not sent into networks where OSPF updates are not required.

Part 2:      Configure NAT

In this part of the practice skills assessment, you will configure static and dynamic NAT at the network edge.

Step 1:      Configure static NAT

Configure static NAT to translate the address of the Net 1 Server on LAN 1 to the public address of 192.0.2.115. Verify that the translations are occurring.

Step 2:      Configure dynamic PAT.

a.     Create access list 1 to allow all addresses in the 192.168.0.0/16 network to be translated.

b.     Create a NAT pool named POOL-1. It should use address in the range 192.0.2.116 - 192.0.2.118.

c.     Configure NAT to dynamically use the addresses in the pool for all traffic entering and exiting the company network. Remember that it is likely that more than three hosts will be accessing traffic on the Internet.

Part 3:      Configure ACLs

Configure access control lists to meet the following requirements.

Note: Use host and any keywords whenever possible. Always explicitly configure the default deny condition when it is to be used as part of the ACL functionality so that it can be logged when the condition is met. You do not need to specify the default deny condition if it is counteracted with permit ip any any for this assessment. All ACLs should be placed in the most efficient location possible according to the guidelines specified in the curriculum.

a.     Create a named standard access list to explicitly prevent all external traffic accessing the telnet lines on RTR-A. Name the list VTY-BLOCK. All addresses on the 192.168.0.0/16 network only should be allowed to access the VTY lines. Verify that the list works as specified.

b.     Create a numbered standard ACL to prevent all hosts on Net 1 from accessing Net 2. Use 10 as the number for the list.

c.     Create an extended numbered ACL that will prevent traffic from the Net 4 network from accessing the HTTP service that is running on Corp Server. All other traffic from Net 4 hosts should be able to access the network. Number the list 101.

Part 4:      Manage Network Devices

Step 1:      Configure NTP

Configure router RTR-E to use Corp Server as its time source.

Step 2:      Backup IOS to Server

Backup the IOS image file on router RTR-E to Corp Server.
