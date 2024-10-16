# Clustered Systems

## Overview
Clustered systems are a type of multiprocessor system that consists of multiple individual systems, or nodes, typically connected via a local area network (LAN) or a faster interconnect like InfiniBand. Unlike traditional multiprocessor systems, which have multiple CPUs within a single system, clustered systems are made up of two or more separate systems, each usually equipped with multiple cores. The primary goal of clustering is to provide high availability and enhanced computational power.

## Key Features
1. **High Availability**: 
   Clustered systems are designed to continue functioning even if one or more nodes fail. This is achieved through redundancy and the ability of the system to reallocate resources as needed. A layer of cluster software monitors nodes and can take over tasks from a failed node, minimizing service interruption.

2. **Graceful Degradation**: 
   This is the capability of a clustered system to provide service proportional to the number of functioning nodes. For example, if one node fails, the remaining nodes can continue to provide service without significant performance drops.

3. **Fault Tolerance**: 
   Some clustered systems are designed to tolerate failures of individual components without losing functionality. This requires mechanisms to detect, diagnose, and potentially correct failures.

4. **Asymmetric and Symmetric Clustering**:
   - **Asymmetric Clustering**: In this setup, one node operates actively while another remains in a hot-standby mode, ready to take over if the active node fails.
   - **Symmetric Clustering**: Multiple nodes run applications and monitor each other, allowing for more efficient use of resources.

5. **Parallelization**: 
   Clustered systems can achieve high-performance computing by running applications concurrently across multiple nodes. This requires applications to be designed for parallel execution, dividing tasks into smaller components that can run simultaneously.

## Types of Clusters
1. **Parallel Clusters**: 
   Allow multiple hosts to access shared storage, enhancing computational power. Special software and application versions are often required to support simultaneous data access.

2. **WAN Clusters**: 
   These clusters can connect nodes separated by long distances, allowing for greater flexibility and resource allocation.

3. **Database Clusters**: 
   Systems like Oracle Real Application Cluster enable multiple hosts to access a shared database, increasing performance and reliability. Access control and locking mechanisms ensure that data integrity is maintained.

## Technology Advancements
Cluster technology is evolving rapidly, supporting thousands of systems and enhancing capabilities through innovations like Storage Area Networks (SANs). These networks enable multiple systems to connect to a shared pool of storage, facilitating resource allocation and improving overall performance.

## Conclusion
Clustered systems represent a powerful solution for organizations needing reliable, high-performance computing environments. With their ability to provide continuous service and leverage the combined power of multiple nodes, clustered systems are well-suited for a variety of applications, from database management to high-performance computing tasks.
