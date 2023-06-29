+++
title = "TCP Vs UDP "
weight = 15
chapter = false
pre = "<b> 1.5 </b>"
+++

Here's a table comparing the main differences between TCP (Transmission Control Protocol) and UDP (User Datagram Protocol):

| Feature            | TCP                                 | UDP                                       |
|--------------------|-------------------------------------|-------------------------------------------|
| Connection-oriented or Connectionless | Connection-oriented              | Connectionless                           |
| Reliability        | Reliable data delivery with acknowledgments and retransmissions | Unreliable data delivery without acknowledgments or retransmissions |
| Ordering           | Guarantees ordered delivery of data | Does not guarantee ordered delivery of data |
| Error Checking     | Performs error checking using checksums | No error checking mechanism               |
| Flow Control       | Implements flow control to prevent overwhelming the receiver | No flow control mechanism                 |
| Congestion Control | Implements congestion control to avoid network congestion | No congestion control mechanism           |
| Overhead           | Higher overhead due to additional control mechanisms | Lower overhead due to minimal control mechanisms |
| Example Applications | Web browsing, email, file transfer | Streaming media, online gaming, DNS requests |

The table highlights the key differences between TCP and UDP in terms of their connection-oriented/connectionless nature, reliability, ordering, error checking, flow control, congestion control, overhead, and example applications. Understanding these differences is essential for selecting the appropriate protocol based on the specific requirements of the network application.