# Distributed Systems

A **distributed system** is a collection of physically separate, possibly heterogeneous computer systems that are networked together to provide users with access to shared resources. These systems work together to increase computational speed, functionality, data availability, and reliability.

###  Overview and Purpose

Distributed systems connect multiple computers to create a unified system, providing:
- **Increased Computation Speed**: By distributing tasks across multiple machines.
- **Enhanced Functionality**: Different machines contribute unique capabilities.
- **Improved Data Availability**: Data is stored and accessible across various nodes.
- **Higher Reliability**: The failure of one system does not bring down the entire network, as resources are distributed.

Operating systems often integrate network access into file access, making networking seamless for users. This approach allows resource sharing without requiring users to explicitly manage network details, though some systems require users to invoke specific network functions (e.g., **FTP**, **NFS**).

###  Networks in Distributed Systems

Distributed systems rely on **networks** for communication and resource sharing. A **network** is a communication path between two or more systems, and distributed systems depend heavily on this connectivity.

Networks vary in several aspects:
- **Protocols**: The communication rules between systems. The most common is **TCP/IP**, which forms the backbone of the Internet. Some systems may use proprietary protocols for specific needs.
- **Distance Between Nodes**: Networks are categorized based on how far apart the connected systems are:
  - **Local-Area Network (LAN)**: Covers a small area, such as a room, building, or campus.
  - **Wide-Area Network (WAN)**: Spans larger areas, such as cities or countries.
  - **Metropolitan-Area Network (MAN)**: Links systems within a city.
  - **Personal-Area Network (PAN)**: Connects devices over short distances (e.g., Bluetooth or 802.11 devices).
  
The communication medium for networks can include copper wires, fiber optic cables, or wireless transmissions (e.g., satellite, microwave, or radio signals).

### Performance and Reliability

Networks vary in performance and reliability, influenced by factors such as:
- **Media Type**: Copper wires, fiber optics, or wireless signals have different bandwidths and latency.
- **Network Protocols**: TCP/IP offers reliable communication, but performance may vary based on the network configuration and usage.
- **System Redundancy**: Distributed systems often improve reliability by distributing resources and workload across multiple systems, mitigating the impact of any single system failure.

###  Types of Distributed Systems

####   1. Network Operating Systems

A **network operating system (NOS)** allows individual systems to share resources and communicate over a network, while still functioning independently. A computer running a network operating system is aware of other networked computers and can exchange messages with them, but it operates autonomously.

Key features of NOS include:
- **File Sharing**: Enables users to access files over the network.
- **Messaging**: Allows communication between processes on different machines.

Examples include systems that provide **FTP** for file transfer or **NFS** for network file access.

####   2. Distributed Operating Systems

A **distributed operating system** provides a more unified environment by tightly integrating multiple computers to create the illusion of a single operating system controlling the network. In this system, the distinction between individual machines is blurred, and resources are shared seamlessly across the network.

###  Applications of Distributed Systems

Distributed systems are used in various domains:
- **Cloud Computing**: A prime example of distributed systems, where services and resources are provided to users over the Internet.
- **Distributed Databases**: Data is stored and replicated across multiple nodes, ensuring availability and reliability.
- **Cluster Computing**: Multiple computers work together as a single system to perform complex computations efficiently.
- **Grid Computing**: Distributed computing resources from different locations work together to achieve a common goal, often used in scientific research and large-scale problem solving.

### Summary

Distributed systems offer numerous advantages, including increased performance, enhanced resource sharing, and improved fault tolerance. They rely heavily on network connectivity and can operate either as independent network operating systems or as a unified distributed operating system. 

