## Do Now: Scheduling Algorithms

> [!QUESTION] 1) Gap Fill
> **Word bank:** fair | starvation | burst time | preemptive | queue | Round Robin | FCFS | Shortest Job First | CPU | Multi-Level Feedback Queue
>
> 1. A scheduling algorithm decides which process gets access to the **CPU** next.
> 2. **Round Robin** gives each process an equal share of processor time.
> 3. **FCFS** schedules processes in the order they arrive.
> 4. A benefit of Round Robin is that it is **fair** because every process receives CPU time.
> 5. **Shortest Job First** selects the process with the shortest execution time.
> 6. One drawback of Shortest Job First is that long processes can suffer from **starvation**.
> 7. A process waiting to be executed is typically placed in a **queue**.
> 8. Shortest Job First requires the **burst time** of each process to be known in advance.
> 9. **Multi-Level Feedback Queue** is a more complex scheduling algorithm that groups processes into queues and adjusts priorities.
> 10. Shortest Time Remaining is a **preemptive** scheduling algorithm because a running process can be interrupted.

> [!QUESTION] 2) State what is meant by a scheduling algorithm. [2]
> **Answer:** An algorithm that decides **which process runs on the CPU and when**, allocating processor time between processes.

> [!QUESTION] 3) State two benefits of Round Robin scheduling. [2]
> **Answer:**
> - It is **fair**, as every process receives processor time.
> - It helps prevent **starvation**, because processes are repeatedly given a time slice.

> [!QUESTION] 4) Shortest Job First vs First Come, First Served [4]
> | Process | Execution time |
> |---|---:|
> | A | 10 ms |
> | B | 2 ms |
> | C | 1 ms |
> | D | 3 ms |
>
> **Answer:** Shortest Job First would run **C, B, D, then A**. This completes several short processes before the 10 ms process, reducing the average waiting and completion time. With [[First Come First Served|FCFS]], if A arrived first, the shorter jobs could all be left waiting behind it.

## Lesson Objectives

By the end of this topic, you should be able to:

- Describe **distributed, embedded, multi-tasking, multi-user and real-time operating systems**.
- Describe the purpose of the **BIOS, device drivers and virtual machines**.

## Distributed Operating Systems

A [[Distributed Operating System]] coordinates work across **multiple computers**. A single job can be divided between different machines, while the OS manages communication with their hardware.

Resources available across the computers can include:

- **Processor time**
- **Memory**
- **Input/output facilities**

The OS coordinates the distribution of tasks by passing instructions between computers.

> [!IMPORTANT] Key Point
> To the user, the system can appear to behave like a single powerful computer even though processing is being distributed across several machines.

### Advantages and limitation

| Advantage                                                                         | Limitation                                                             |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Access to greater computational power                                             | The programmer has little or no control over how tasks are distributed |
| The user can work as though using one system                                      | Task distribution is handled by the OS, and can be a bottle neck       |
| Programs do not need to be written differently just to use the distributed system | The underlying distribution is hidden from the user, so less control   |

## Multi-tasking Operating Systems

A [[Multi-tasking]] operating system makes a single processor appear to perform multiple tasks at the same time by **scheduling processor time** between processes.

For example, a computer might let you:

- Read a document
- Browse the web
- Listen to music
- Run background processes

All at the same time. To do this, the CPU rapidly switches between processes, giving each access to processor time.

> [!NOTE]
> Multi-tasking links directly to [[CPU Scheduling]]. Scheduling algorithms decide which process gets CPU time and when.

## Multi-user, Multi-tasking Systems

A [[Multi-user Operating System]] allows many users to share the resources of a powerful computer, such as a **mainframe**.

- Users connect through their own terminals.
- Each user receives a **time slice** of CPU time.
- Each terminal may also be running several processes.

> [!IMPORTANT] Exam Distinction
> **Multi-tasking** means one system handles multiple processes. **Multi-user** means multiple users share the computer's processing resources.

## Mobile Operating Systems

A smartphone uses a **multi-tasking operating system**, so several applications and background processes can operate during the same period.

Mobile operating systems must also interact closely with device-specific hardware. A lower-level system can handle hardware and specialised features such as cellular and Wi-Fi connectivity, while the main OS handles the **user interface** and applications.

### Open-source mobile operating systems

Android is an example of an open-source, Linux-based mobile operating system. Its openness allows device manufacturers to customise the system for their hardware, add features and change the user interface.

> [!NOTE]
> Customisation can help manufacturers differentiate their devices through features, interfaces and available applications.

## Embedded Operating Systems

An [[Embedded System]] is designed to perform a specific or limited set of functions. Many household devices contain an embedded OS and run relatively simple programs.

Typical characteristics include:

- **Minimal OS features**
- Application programs stored in **ROM**
- A **limited amount of RAM**
- A simple, minimal **user interface**

Examples can include washing machines and other household appliances.

> [!QUESTION]- Think About It
> For a washing machine, possible inputs include buttons, a door sensor and temperature sensors. Outputs could include the motor, heater, display and status lights.

## Real-time Operating Systems

A [[Real-Time Operating System|real-time operating system (RTOS)]] must respond to inputs within strict timing requirements. These systems may need to handle many inputs at once and are often used where predictable responses are important.

In safety-critical environments, systems may include:

- A **failsafe** that detects a hardware failure and responds appropriately.
- **Hardware redundancy**, where crucial components are duplicated in case one fails.

### Therac-25 case study

The Therac-25 was a radiation therapy machine whose software had serious safety failures. It is a useful reminder that software controlling safety-critical equipment needs careful design, testing and safeguards.

> [!IMPORTANT] Exam Point
> For a real-time OS, the key idea is meeting required **response deadlines**, rather than simply being "fast" in general.

## BIOS

[[BIOS]] stands for **Basic Input/Output System**. In the model used for this course, it is stored in ROM and is involved when the computer starts up.

Its roles include:

1. Starting the boot process.
2. Initialising and testing hardware.
3. Loading the operating system into RAM.

> [!NOTE]
> A simple exam description is: **BIOS initialises/tests hardware and begins loading the operating system when the computer boots.**

## Device Drivers

A [[Device Driver]] is software that provides an interface between the **operating system** and a hardware device.

Drivers are:

- **Hardware dependent**
- **Operating-system specific**
- Used so the OS can control devices such as speakers and graphics hardware

The driver hides hardware-specific details from the operating system.

**Typical communication path:**

`Program -> Operating System -> Device Driver -> Hardware`

> [!IMPORTANT] Key Point
> Because the driver handles device-specific instructions, the OS does not need to know every low-level detail of each hardware device.

## Virtual Machines

A [[Virtual Machine]] uses software to **emulate a computer or execution environment**.

Uses include:

- Running one operating system inside another environment.
- Emulating different hardware.
- Executing intermediate code, such as a Java Virtual Machine executing Java bytecode.
- Emulating older computer or arcade hardware on modern systems.

> [!NOTE]
> A virtual machine provides a software-created environment that behaves like a machine or platform to the software running inside it.

## Exam-Style Summary

| Topic | What to remember |
|---|---|
| **Distributed OS** | Coordinates processing and resources across multiple computers |
| **Multi-tasking OS** | Schedules CPU time so multiple processes appear to run at once |
| **Multi-user OS** | Allows multiple users to share processing resources |
| **Embedded OS** | Minimal system designed for a dedicated device or purpose |
| **Real-time OS** | Must respond within required timing constraints |
| **BIOS** | Initialises/tests hardware and begins the boot process |
| **Device driver** | Interface allowing the OS to communicate with specific hardware |
| **Virtual machine** | Software emulation of a machine or execution environment |

## Self-Check

> [!QUESTION]- 1. What does a distributed OS do?
> It coordinates processing and resources across multiple computers, while presenting them to the user as one system.

> [!QUESTION]- 2. How can one CPU appear to run several processes at once?
> The operating system schedules processor time and switches rapidly between processes.

> [!QUESTION]- 3. Give two characteristics of an embedded OS.
> It has minimal features, limited RAM, programs commonly stored in ROM, and a simple user interface. Any two.

> [!QUESTION]- 4. Why is hardware redundancy useful in a safety-critical system?
> Crucial components are duplicated so another component can continue or support safe operation if one fails.

> [!QUESTION]- 5. What is the purpose of a device driver?
> It provides an interface that lets the operating system communicate with and control a particular hardware device.

> [!QUESTION]- 6. What is a virtual machine?
> A software-created environment that emulates a machine or execution platform.

## Related Notes

- [[Operating Systems]]
- [[CPU Scheduling]]
- [[Embedded Systems]]
- [[Real-Time Operating System]]
- [[BIOS]]
- [[Device Drivers]]
- [[Virtual Machines]]
