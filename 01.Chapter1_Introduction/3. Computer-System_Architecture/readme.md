# Computer-System Architecture

Computer-System Architecture refers to how a computer system is structured in terms of its hardware components. Here's a summary of the major categories according to the number of general-purpose
processors used.:

### 1. Single-Processor Systems
- **Definition**: Systems with one CPU and a single processing core.
- **Components**: Special-purpose processors (e.g., disk controllers, keyboard processors) that handle specific tasks.
- **Characteristic**: Only one general-purpose CPU executes processes, while special-purpose processors do not run processes.
- **Example**: Historically common, but rare today.

### 2. Multiprocessor Systems
- **Definition**: Systems with multiple processors that may have multiple cores.
- **Symmetric Multiprocessing (SMP)**: Each CPU performs all tasks independently, sharing memory and resources.
- **Multicore Processors**: CPUs with multiple cores on one chip, enhancing efficiency through faster on-chip communication.
- **Non-Uniform Memory Access (NUMA)**: Each CPU has local memory for faster access, with slower interconnect access to other CPUs' memory.
- **Example**: Common in modern computers, laptops, and mobile devices.

### 3. Clustered Systems
- **Definition**: Systems composed of multiple individual computers or nodes connected via a network.
- **Purpose**: Often used for high-availability services and fault tolerance, allowing service continuation even in case of failure.
- **Types**:
  - **Asymmetric Clustering**: One node runs while others are in standby.
  - **Symmetric Clustering**: Multiple nodes run applications and monitor each other, offering better resource utilization.
- **Parallelization**: Programs are divided into tasks that run on separate nodes in the cluster.
