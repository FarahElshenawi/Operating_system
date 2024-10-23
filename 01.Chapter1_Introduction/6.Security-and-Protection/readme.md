# Security and Protection

In systems with multiple users and concurrent execution of multiple processes, access to data and resources must be strictly regulated. Mechanisms are put in place to ensure that only authorized processes can operate on resources like files, memory segments, and CPU. This is essential for maintaining the integrity and security of the system.

## Protection

**Protection** refers to the mechanisms that control access to resources in a computer system. It ensures that processes and users only interact with resources they are authorized to access.

### Key Points:
- **Memory protection**: Memory-addressing hardware ensures that a process can only access its own address space.
- **CPU protection**: The system's timer ensures that no process can monopolize the CPU indefinitely.
- **Device control**: Device-control registers are protected from user access, ensuring peripheral device integrity.

Protection mechanisms not only prevent unauthorized access but also improve system reliability by detecting errors early at the interface level, preventing a malfunctioning subsystem from contaminating a healthy one. An important aspect of protection is distinguishing between **authorized** and **unauthorized** usage, which is discussed in further detail in Chapter 17.

## Security

While protection focuses on controlling access, **security** defends the system from both external and internal attacks. These attacks can range from viruses and worms to more complex threats like identity theft, denial-of-service (DoS) attacks, and theft of service.

### Types of Attacks:
- **Viruses and worms**: Malicious software that can spread and cause harm.
- **Denial-of-service (DoS)**: An attack that exhausts system resources, preventing legitimate users from accessing services.
- **Identity theft**: Unauthorized access through stolen authentication credentials.
- **Theft of service**: Unauthorized use of system resources.

Operating systems implement various security features to protect against these threats. Security measures vary across systems, with some leaving it to policy or additional software, while others integrate it directly into the OS.

## User Identification and Authorization

Security and protection require the system to distinguish between users. Most operating systems maintain a list of **user names** and associated **user identifiers (user IDs)**. These unique IDs are used to authenticate users and associate them with their processes and threads. In some systems, such as Windows, the user ID is referred to as a **security ID (SID)**.

### Key Concepts:
- **User ID (UID)**: A unique identifier assigned to each user, used during authentication.
- **Group ID (GID)**: A set of users that are grouped together for resource access, allowing permissions to be managed for the entire group instead of individual users.
- **Privilege escalation**: Sometimes a user needs elevated privileges for a specific task, such as accessing restricted devices. For example, in UNIX systems, the **setuid** attribute allows a program to run with the file owner’s user ID, rather than the current user’s ID.

In most cases, user IDs and group IDs are sufficient for managing access. However, privilege escalation mechanisms are in place when users need temporary elevated access to system resources. Once the task is complete, these privileges are relinquished.

