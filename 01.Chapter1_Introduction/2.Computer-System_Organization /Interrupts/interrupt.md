# Interrupts

## Overview
Interrupts allow the CPU to be informed of events by hardware components, ensuring timely responses without constant checking (polling).  
They occur when a device signals the CPU, often via the system bus, causing the CPU to stop its current activity and address the interrupt.

---

## Key Process

### 1. Device Driver and Controller Interaction:
- A **device driver** communicates with a **device controller** to start an I/O operation (e.g., reading a character from the keyboard).
- The **controller** transfers data to its local buffer and informs the driver once the task is complete.

### 2. Interrupt Trigger:
- The **device controller** signals the CPU using an **interrupt** to notify the completion of its task.
- The CPU stops its current process and jumps to a pre-defined location where the **Interrupt Service Routine (ISR)** resides.

### 3. Interrupt Handling:
- **Interrupt vector**: A table of pointers that holds addresses of specific ISRs for different devices. This allows the CPU to quickly transfer control to the appropriate routine without a generic intermediary.
- **Interrupt Service Routine (ISR)**: A function that processes the interrupt.
- **Saving and restoring state**: The CPU must save the state of the current computation (registers, program counter) before servicing the interrupt, and restore it afterward to resume operations seamlessly.

---

## Interrupt Architecture

- The **interrupt vector** is stored in low memory, containing addresses of ISRs.
- **State-saving**: ISRs must save the current processor state (such as register contents) before modifying anything and restore it before returning control to the main process.

---

## Important Concepts and Terms

- **Device Driver**: Software that communicates with hardware devices.
- **Device Controller**: A hardware component managing communication between the device and the CPU.
- **System Bus**: Main pathway through which the CPU communicates with other system components.
- **Interrupt Vector**: A table holding memory addresses for ISRs.
- **Interrupt Service Routine (ISR)**: A special routine that handles specific interrupts.

# Interrupt Implementation

## Basic Mechanism
- **Interrupt-Request Line**: A wire that the CPU checks after each instruction to detect whether a device has raised an interrupt.  
When an interrupt occurs, the CPU:
  1. Reads the interrupt number.
  2. Jumps to the corresponding handler in the interrupt vector (using the interrupt number as an index).
  3. Executes the interrupt handler, which saves the current state, processes the interrupt, restores the state, and returns to the pre-interrupt execution.

---

## Steps in Handling an Interrupt
1. Device controller raises an interrupt by asserting a signal.
2. CPU catches the interrupt, determines the cause, and dispatches to the correct handler.
3. Interrupt handler clears the interrupt by servicing the device.


### Interrupt-driven I/O Cycle Steps

1. Device driver initiates I/O.
2. I/O controller starts the I/O operation.
3. Interrupt is generated when the I/O is ready or an error occurs.
4. CPU receives the interrupt and transfers control to the interrupt handler.
5. Interrupt handler processes data and returns from the interrupt.
6. CPU resumes its previous task.
7. The process repeats as interrupts occur.

---

## Advanced Features in Modern Systems
- **Deferring interrupts**: Some operations are critical and cannot be interrupted; handling can be deferred during such operations.
- **Efficient dispatching**: The system must efficiently direct the interrupt to the correct handler.
- **Multilevel interrupts**: Systems prioritize interrupts (high-priority vs. low-priority) for more urgent response to critical events.

---

## Types of Interrupt Lines
- **Nonmaskable Interrupt**: Cannot be disabled, used for critical events like memory errors.
- **Maskable Interrupt**: Can be turned off during critical processing by the CPU.

---

## Interrupt Chaining
- If multiple devices share the same interrupt vector entry, **interrupt chaining** is used.
- Each vector entry points to a list of handlers. The handlers are checked one by one to find the one that can service the interrupt.

---

## Interrupt Priority System
- **Interrupt Priority Levels**: Allows the CPU to handle high-priority interrupts first while deferring lower-priority ones without disabling all interrupts. High-priority interrupts can preempt lower-priority ones.

