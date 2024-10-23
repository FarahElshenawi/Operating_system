# Operating System System Calls

## Table of Contents
1. [Overview](#overview)
2. [System Calls](#system-calls)
3. [Examples of System Calls](#examples-of-system-calls)
4. [Application Programming Interface (API)](#application-programming-interface-api)
5. [Types of System Calls](#types-of-system-calls)
    - [Process Control](#process-control)
    - [File Management](#file-management)
    - [Device Management](#device-management)
    - [Information Maintenance](#information-maintenance)
    - [Communications](#communications)
    - [Protection](#protection)
6. [Conclusion](#conclusion)

## Overview
System calls provide the interface between a running program and the operating system. They allow programs to request services from the kernel, enabling them to perform functions like process management, file operations, and device management.

## System Calls
A system call is a programmatic way in which a computer program requests a service from the operating system's kernel. System calls provide the necessary mechanisms to perform operations that require access to hardware or that need higher privileges than what a standard application has. They serve as the fundamental interface between a running program and the operating system.

## Examples of System Calls
Different operating systems provide different sets of system calls. Below are some examples of common system calls for both Windows and Unix-based systems:

### Windows
| Function                     | Description                          |
|------------------------------|--------------------------------------|
| `CreateProcess()`            | Creates a new process.              |
| `ExitProcess()`              | Terminates a process.               |
| `WaitForSingleObject()`      | Waits for a process to finish.      |
| `CreateFile()`               | Creates or opens a file.            |
| `ReadFile()`                 | Reads data from a file.             |
| `WriteFile()`                | Writes data to a file.              |
| `CloseHandle()`              | Closes an open file or process.     |
| `SetConsoleMode()`           | Sets the console mode.              |
| `GetCurrentProcessID()`      | Retrieves the current process ID.    |

### Unix
| Function                     | Description                          |
|------------------------------|--------------------------------------|
| `fork()`                     | Creates a new process.              |
| `exit()`                     | Terminates a process.               |
| `wait()`                     | Waits for a process to finish.      |
| `open()`                     | Creates or opens a file.            |
| `read()`                     | Reads data from a file.             |
| `write()`                    | Writes data to a file.              |
| `close()`                    | Closes an open file or process.     |
| `ioctl()`                    | Manipulates device parameters.       |
| `getpid()`                   | Retrieves the current process ID.    |

## Application Programming Interface (API)
An Application Programming Interface (API) is a set of routines, protocols, and tools for building software and applications. It defines the methods and data structures that developers can use to interact with the operating system, libraries, or other services. APIs abstract the underlying system calls, providing a more user-friendly interface for programmers.

- **Types of APIs:**
  - **Library APIs:** Function calls provided by software libraries.
  - **Web APIs:** Interfaces for web services (e.g., REST APIs).
  - **Operating System APIs:** Interfaces for interacting with the operating system.

## Types of System Calls
System calls can be grouped into six major categories:

1. **Process Control**
    - **Key Functions:**
        - `create process()`: Creates a new process.
        - `terminate process()`: Halts execution of a process.
        - `wait event()`: Waits for a specific event to occur.
        - `signal event()`: Signals that an event has occurred.

2. **File Management**
    - **Key Functions:**
        - `create file()`: Creates a new file.
        - `delete file()`: Deletes an existing file.
        - `open()`: Opens a file for reading or writing.
        - `close()`: Closes an opened file.

3. **Device Management**
    - **Key Functions:**
        - `request device()`: Requests access to a device.
        - `release device()`: Releases access to a device.
        - `read()`: Reads data from a device.
        - `write()`: Writes data to a device.

4. **Information Maintenance**
    - **Key Functions:**
        - `get time or date()`: Retrieves the current system time or date.
        - `set time or date()`: Sets the system time or date.
        - `get system data()`: Retrieves system-wide data.

5. **Communications**
    - **Key Functions:**
        - `create connection()`: Establishes a communication connection.
        - `send message()`: Sends a message to another process.
        - `receive message()`: Receives a message from another process.

6. **Protection**
    - **Key Functions:**
        - `get file permissions()`: Retrieves file permissions.
        - `set file permissions()`: Modifies file permissions.

## Conclusion
Understanding system calls and their corresponding APIs is crucial for programming at a low level and effectively interacting with the operating system. This knowledge enables developers to utilize the full capabilities of an OS, manage resources efficiently, and write robust applications.
