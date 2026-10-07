---
date: 2026-10-01
tags:
  - computer-science
  - a-level
spec code: H446
Continued from: "[[Operating system functions]]"
---

## Interrupts
- It is vital that the CPU can be interrupted when necessary
- Interrupts can be sent to the CPU by software, hardware devices if the CPUS internal clock
#### Interrupt examples
- AN I/O device sends an interrupt signal
- A printer runs out of paper
- A scheduled interrupt
- an error occurs in a program

#### Interrupts - using the stack
- The [[Sixth Form/Computer Science/Computer Science Shared/Lesson Notes/Topic 2/Processor Components 2026-09-03|CPU]] uses an **interrupt service routine** to process the interrupt
	- *When processing has finished the values can be popped from the stack ad reloaded into then CPU*

#### Interrupt priority
- If a higher priority interrupt occurs whilst an interrupt is being processes, the original interrupts registers will be pushed to the stack as well
- A stack is a **LIFO**(last in first out) data structure, so the last data to be pushed on will be the first to be retrieved 

## Processor scheduling
- A single CPU can only process instructions for one application at a time
- The operating system must schedule when each application can use the CPU
- This gives the illusion of [[Multitasking]]
#### Aims of scheduling
- To provide an acceptable response time to all users
- To maximise the time the CPU is usefully engaged
- To ensure fairness on a multi-user system

#### Scheduling algorithms
| Algorithm                          | How it works                                                               | Key point                                                                   |
| ---------------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| **Round Robin**                    | Processes receive a fixed **time slice** in turn                           | Pre-emptive and designed to share CPU time                                  |
| **First Come First Served (FCFS)** | Processes run in arrival order                                             | An early long job can delay everything behind it                            |
| **Shortest Job First (SJF)**       | The waiting job with the shortest estimated total execution time runs next | Non-pre-emptive                                                             |
| **Shortest Remaining Time (SRT)**  | The process with the shortest estimated remaining time runs                | Pre-emptive, so a shorter arriving process can take over                    |
| **Multi-level Feedback Queues**    | Processes move between queues with different priorities                    | CPU-heavy processes can move down, while long-waiting processes can move up |
#### Round Robin
Each process is allocated a **time slice**. When its time slice ends, an unfinished process gives up the CPU and waits for another turn.
#### First Come First Served
The first process to arrive runs until it finishes. This is simple, but a long process at the front of the queue can make shorter processes wait. **Like a supermarket queue**
#### Shortest Remaining Time
The OS estimates how much processing time each job has left. The job with the shortest remaining time is executed. A newly arrived shorter job can therefore pre-empt the currently running job.

> [!NOTE] Starvation
> **Starvation** happens when a process waits for a very long time because other processes keep being chosen ahead of it.
#### Shortest Job First
The waiting process with the shortest estimated total execution time is selected when the current process finishes. Unlike Shortest Remaining Time, SJF is **non-pre-emptive**, so the running process isn't replaced halfway through simply because a shorter job arrives. 

#### Multi-level Feedback Queues
Processes are placed into queues with different priority levels. A process that uses a lot of CPU time can be moved to a lower-priority queue. A process that has waited for a long time can be moved to a higher-priority queue.
