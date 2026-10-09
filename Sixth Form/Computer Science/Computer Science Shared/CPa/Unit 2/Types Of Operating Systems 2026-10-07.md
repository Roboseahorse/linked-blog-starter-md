## Do Now

### Fill in the Blanks

**Word bank:** distributed | embedded | multi-tasking | multi-user | real-time | time slicing | scheduling algorithm | processor starvation | power | guaranteed

> [!QUESTION]- A ________ operating system runs across multiple devices, allowing the workload to be spread across multiple processors.
> **distributed**

> [!QUESTION]- An ________ operating system is designed to perform a small range of specific tasks on a particular device.
> **embedded**

> [!QUESTION]- Embedded operating systems generally consume significantly less ________ than other types of operating systems.
> **power**

> [!QUESTION]- A ________ operating system allows a user to carry out multiple tasks seemingly simultaneously.
> **multi-tasking**

> [!QUESTION]- Multi-tasking operating systems use ________ to rapidly switch between programs and applications in memory.
> **scheduling**

> [!QUESTION]- A ________ operating system allows multiple users to make use of one computer.
> **multi-user**

> [!QUESTION]- A ________ is used to ensure processor time is shared fairly between jobs.
> **time slicing**

> [!QUESTION]- Fair scheduling helps prevent ________, where a process is continually denied processor time.
> **processor starvation**

> [!QUESTION]- A ________ operating system is designed to perform a task within a ________ time frame.
> **real-time**; **guaranteed**

### Exam Style Questions

> [!QUESTION]- 1. State what is meant by a distributed operating system. [2]
> An operating system where the user's request is split over many machines.

> [!QUESTION]- 2. State two characteristics of an embedded operating system. [2]
> An operating system that is designed to work on a specific piece of kit and is resource efficient.

> [!QUESTION]- 3. Explain why a scheduling algorithm is needed in a multi-user operating system. [3]
> To efficiently share resources fairly between the multiple users.

## Learning Objectives

- Describe **distributed**, **embedded**, **multi-tasking**, **multi-user**, and **real-time** operating systems.
- Explain the purpose of **BIOS**, **device drivers**, and **virtual machines**.

## Types of Operating System

### Distributed Operating Systems

> [!NOTE] Definition
> A **distributed operating system** coordinates processing across multiple computers.

A program may use resources from another computer, including processor time, memory, and I/O facilities. The OS coordinates the distribution of tasks between machines.

> [!IMPORTANT] Key Point
> The user can access the combined computational resources while the OS handles task distribution behind the scenes.

### Multi-tasking Operating Systems

> [!NOTE] Definition
> A **multi-tasking operating system** lets several tasks appear to run simultaneously by scheduling processor time between them.

For example, you might read a document, browse the web and listen to music while background processes are also running.

### Multi-user, Multi-tasking Systems

A **multi-user** system lets several users share the resources of a powerful computer such as a [[Mainframe]]. Each user receives processor time, while each terminal may also run several processes.

> [!IMPORTANT] Don't Mix These Up
> **Multi-tasking** means several processes share processor time. **Multi-user** means several users share the computer's resources.

### Mobile Operating Systems

Smartphones have multi-tasking operating systems. Mobile operating systems also work with device-specific hardware and features such as cellular connectivity and Wi-Fi, while the main OS handles the interface and applications.

### Embedded Operating Systems

> [!NOTE] Definition
> An **embedded operating system** is designed for a device that performs a specific or limited set of tasks.

They commonly have minimal features, limited [[RAM]], programs stored in non-volatile memory such as [[ROM]], and a simple user interface.

### Real-time Operating Systems

> [!NOTE] Definition
> A **real-time operating system (RTOS)** responds to inputs within defined timing requirements.

Real-time systems may need to handle several inputs at once. In safety-critical environments, systems can include failsafes and hardware redundancy.

| Term | Meaning |
|---|---|
| **Failsafe** | A mechanism designed to move the system towards a safe state if something fails |
| **Hardware redundancy** | Critical components are duplicated in case one fails |

### Therac-25 Case Study

The **Therac-25** was a computer-controlled radiation therapy machine used in the 1980s. Software and system-design failures contributed to severe radiation overdoses, showing why safety-critical computer systems need careful engineering and testing.

## System Software Supporting the OS

### BIOS

**BIOS** stands for **Basic Input/Output System**. In traditional PC systems, BIOS firmware runs when the computer starts, initialises and tests hardware, and begins the boot process that leads to the operating system loading.

### Device Drivers

> [!NOTE] Definition
> A **device driver** is software that provides an interface between the operating system and a hardware device.

Drivers are normally **hardware dependent** and **operating-system specific**.

`Program → Operating System → Device Driver → Hardware`

### Virtual Machines

> [!NOTE] Definition
> A **virtual machine (VM)** uses software to provide a virtualised or emulated computing environment.

Uses include running one operating system inside another, executing intermediate code such as Java bytecode in the JVM, and emulating older hardware.

## Comparison Table

| Type | Main purpose | Typical characteristic |
|---|---|---|
| **Distributed OS** | Coordinate work across multiple computers | Processing/resources can be shared across machines |
| **Multi-tasking OS** | Run multiple processes apparently at once | CPU time is scheduled between processes |
| **Multi-user OS** | Support multiple users | Computing resources are shared between users |
| **Mobile OS** | Operate mobile devices | Supports apps and mobile-specific hardware |
| **Embedded OS** | Control a dedicated device | Limited resources and focused purpose |
| **Real-time OS** | Meet defined response deadlines | Predictable timing is important |

## Exam-style Summary

> [!IMPORTANT] What to Remember
> - **Distributed:** processing is coordinated across multiple computers.
> - **Multi-tasking:** processor time is scheduled between processes.
> - **Multi-user:** several users share computing resources.
> - **Embedded:** designed for a dedicated device with limited resources and functions.
> - **Real-time:** responds within specified timing constraints.
> - **BIOS:** firmware involved in hardware initialisation and booting.
> - **Device driver:** lets the OS communicate with hardware.
> - **Virtual machine:** provides a virtualised or emulated execution environment.

## Self-check Questions

> [!QUESTION]- What's the difference between multi-user and multi-tasking?
> Multi-user systems support multiple users sharing resources. Multi-tasking systems allow multiple processes to share processor time.

> [!QUESTION]- Why do embedded operating systems usually need fewer resources?
> They're designed for a limited, specific purpose, so they usually need fewer features and less memory.

> [!QUESTION]- What does a device driver do?
> It provides the interface that allows the operating system to communicate with and control hardware.

## Related Notes

- [[Functions of an Operating System]]
- [[Systems Software]]
- [[Processor Scheduling]]
- [[BIOS and Booting]]
- [[Device Drivers]]
- [[Virtual Machines]]
