START
Basic
Front: 
Describe how the TCP/IP protocol stack layers are related to the OSI layers.
Back: 
- Application layer of TCP/IP corresponds to the Application, Presentation, and Session layers of OSI. It comprises the communications protocols used in process-to-process communications across the IP network (e.g., HTTP) and relies on the Transport layer protocols to establish host-to-host data transfer.
- Transport layer of TCP/IP corresponds to the Transport layer of OSI. The primary protocols for this layer are TCP and UDP. The layer is responsible for host-to-host communications, connection, reliability, flow control and multiplexing. The port value identifies the host process responsible for processing of the information.
- Internet layer from TCP/IP corresponds to the Network layer from OSI. It's responsible for transmitting data between networks, provides fragmentation/defragmentation of data according to the MTU. It defines the IP address for addressing the hosts.
- The Link layer from TCP/IP corresponds to the Data Link layer from OSI. It comprises the protocols that only operate on the local network that the host connects to. Uses MAC address to identify the hosts on the network and ARP to resolve this address from the known IP address.
- The Physical layer corresponds to the Physical OSI layer and defines the hardware components used for the network.
<!--ID: 1745138784651-->
END
