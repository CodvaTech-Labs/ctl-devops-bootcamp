+++
title = "Networking - OSI Model"
weight = 13
chapter = false
pre = "<b> 1.3</b>"
+++

## OSI Model
The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes and defines the functions of a communication system or network. It helps in understanding how different components of a network interact and communicate with each other. The OSI model consists of seven layers, each serving a specific purpose and providing a set of services to the layer above it. The seven layers of the OSI model are:
Certainly! Here's an explanation of the OSI (Open Systems Interconnection) model in table format with examples:

| Layer              | Function                                                                                                         | Protocols/Examples                                                                                           |
|--------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Application        | Provides network services directly to user applications.                                                        | HTTP, FTP, DNS, SMTP, Telnet                                                                                |
| Presentation       | Handles data translation, encryption, and compression to ensure compatibility between different systems.           | JPEG, MPEG, SSL/TLS                                                                                          |
| Session            | Establishes, manages, and terminates communication sessions between applications.                                | NetBIOS, SIP, NFS                                                                                           |
| Transport          | Ensures reliable and transparent transfer of data segments between network hosts.                                | TCP, UDP                                                                                                     |
| Network            | Routes and delivers data packets across different networks.                                                     | IP, ICMP, OSPF, BGP                                                                                          |
| Data Link          | Establishes and manages a reliable link between two directly connected nodes.                                   | Ethernet, Wi-Fi, PPP, HDLC, MAC                                                                              |
| Physical           | Transmits raw bitstream over the physical medium.                                                               | Ethernet cables, fiber optic cables, radio waves                                                              |

Now, let's provide examples for each layer:

- Application Layer: HTTP (Hypertext Transfer Protocol) is used for web browsing, FTP (File Transfer Protocol) is used for file transfer, DNS (Domain Name System) is used for domain name resolution, and Telnet is used for remote login.

- Presentation Layer: JPEG (Joint Photographic Experts Group) is a file format for image compression, MPEG (Moving Picture Experts Group) is used for video and audio compression, and SSL/TLS (Secure Sockets Layer/Transport Layer Security) provides secure communication over the internet.

- Session Layer: NetBIOS (Network Basic Input/Output System) allows applications on different devices to establish sessions, SIP (Session Initiation Protocol) is used for establishing multimedia sessions, and NFS (Network File System) enables file sharing over a network.

- Transport Layer: TCP (Transmission Control Protocol) provides reliable, connection-oriented data delivery, while UDP (User Datagram Protocol) provides connectionless, unreliable data delivery.

- Network Layer: IP (Internet Protocol) handles the addressing and routing of data packets across networks, ICMP (Internet Control Message Protocol) is used for network troubleshooting and error reporting, OSPF (Open Shortest Path First) is a routing protocol, and BGP (Border Gateway Protocol) is used for routing between autonomous systems.

- Data Link Layer: Ethernet is a widely used protocol for local area networks (LANs), Wi-Fi is used for wireless communication, PPP (Point-to-Point Protocol) is used for point-to-point connections, HDLC (High-Level Data Link Control) is a synchronous data link protocol, and MAC (Media Access Control) addresses are unique identifiers for network interfaces.

- Physical Layer: This layer deals with the physical transmission of data and includes technologies like Ethernet cables, fiber optic cables, and radio waves for wireless communication.

The OSI model provides a layered approach to network communication, where each layer performs specific functions and interacts with adjacent layers to facilitate data transmission across networks.                          |
