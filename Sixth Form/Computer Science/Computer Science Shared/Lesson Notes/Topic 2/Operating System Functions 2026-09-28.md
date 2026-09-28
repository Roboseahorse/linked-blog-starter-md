## Functions of an Operating System

An **operating system (OS)** is system software that manages computer hardware and provides an interface between the user, application software and hardware.

> [!IMPORTANT] Core OS Functions
> - User interface
> - Memory management
> - Interrupt handling
> - Processor scheduling

### User Interface

The OS hides much of the complexity of the computer's hardware by providing a **user interface**. This lets users interact with the computer without directly controlling the hardware.

Common interfaces include graphical user interfaces and command-line interfaces.

### Memory Management

Programs and their data must be loaded into [[RAM]] before the CPU can work with them. The OS manages how RAM is allocated between processes. If there isn't enough physical RAM for everything at once, the OS may use [[Virtual Memory]].

#### Paging

**Paging** divides memory into fixed-size blocks called **pages**. A process can be allocated several pages, and the pages do not need to be next to one another physically in RAM.

> [!NOTE] Page Table
> A **page table** maps a process's logical memory locations to their physical locations in memory.

This lets a process use free areas of memory even when those areas are non-contiguous.

#### Segmentation

**Segmentation** divides memory into variable-size sections called **segments**. Segments can correspond to logical parts of a program, such as a function or subroutine.

| Feature | Paging | Segmentation |
|---|---|---|
| Block size | Fixed | Variable |
| Division based on | Memory pages | Logical program sections |
| Placement | Pages can be non-contiguous | Segments are allocated separately |

#### Virtual Memory

A computer has a limited amount of physical RAM. **Virtual memory** uses an area of secondary storage to hold pages that aren't currently needed in RAM.

When a required page isn't in RAM, it can be moved into RAM and another page may be moved out.

> [!WARNING] Disk Thrashing
> If the system repeatedly moves pages between RAM and virtual memory, it spends too much time swapping data instead of running programs. This is called **disk thrashing**, and it can make the computer noticeably slower.

### Interrupts

An **interrupt** is a signal that requires the CPU's attention. Interrupts can come from hardware devices, software or timing mechanisms.

Examples include:
- An I/O device requesting attention
- A printer running out of paper
- A program error
- A scheduled timer interrupt
- A power failure

#### Interrupt Service Routine

When an interrupt is accepted:

1. The processor pauses its current work.
2. The current register contents are **pushed onto the stack** so the process state is preserved.
3. The CPU runs an **Interrupt Service Routine (ISR)** to deal with the interrupt.
4. When the ISR finishes, the saved values are **popped from the stack** and restored.
5. The processor can continue its previous work.

> [!NOTE] Stack
> A stack uses **LIFO**, Last In, First Out. The most recently pushed item is the first one retrieved.

#### Interrupt Priority

Interrupts can have different priorities and are handled according to their priority level. If a higher-priority interrupt occurs while another interrupt is being processed, the current state can also be pushed onto the stack before the higher-priority interrupt is serviced.

### Processor Scheduling

A single CPU core executes instructions for one process at a time. The OS scheduler decides when each process gets CPU time, quickly switching between processes to support apparent [[Multitasking]].

The **scheduler** aims to:
- Provide acceptable response times
- Keep the CPU usefully occupied
- Treat processes or users fairly

### Scheduling Algorithms

| Algorithm | How it works | Key point |
|---|---|---|
| **Round Robin** | Processes receive a fixed **time slice** in turn | Pre-emptive and designed to share CPU time |
| **First Come First Served (FCFS)** | Processes run in arrival order | An early long job can delay everything behind it |
| **Shortest Job First (SJF)** | The waiting job with the shortest estimated total execution time runs next | Non-pre-emptive |
| **Shortest Remaining Time (SRT)** | The process with the shortest estimated remaining time runs | Pre-emptive, so a shorter arriving process can take over |
| **Multi-level Feedback Queues** | Processes move between queues with different priorities | CPU-heavy processes can move down, while long-waiting processes can move up |

## Round Robin

Each process is allocated a **time slice**. When its time slice ends, an unfinished process gives up the CPU and waits for another turn.

#### First Come First Served

The first process to arrive runs until it finishes. This is simple, but a long process at the front of the queue can make shorter processes wait.

#### Shortest Remaining Time

The OS estimates how much processing time each job has left. The job with the shortest remaining time is executed. A newly arrived shorter job can therefore pre-empt the currently running job.

> [!NOTE] Starvation
> **Starvation** happens when a process waits for a very long time because other processes keep being chosen ahead of it.

#### Shortest Job First

The waiting process with the shortest estimated total execution time is selected when the current process finishes. Unlike Shortest Remaining Time, SJF is **non-pre-emptive**, so the running process isn't replaced halfway through simply because a shorter job arrives.

#### Multi-level Feedback Queues

Processes are placed into queues with different priority levels. A process that uses a lot of CPU time can be moved to a lower-priority queue. A process that has waited for a long time can be moved to a higher-priority queue.

---
### Exam-Style Summary

> [!IMPORTANT] Remember This
> - The OS manages hardware and gives users and applications an interface to the computer.
> - [[Paging]] uses fixed-size pages, while [[Segmentation]] uses variable-size logical sections.
> - A page table maps logical addresses to physical memory locations.
> - [[Virtual Memory]] extends available memory using secondary storage, but excessive swapping can cause disk thrashing.
> - An interrupt pauses normal processing so an ISR can deal with an event.
> - Register contents can be stored on a LIFO stack while an interrupt is serviced.
> - The scheduler allocates processor time using algorithms such as Round Robin, FCFS, SJF, SRT and Multi-level Feedback Queues.

### Self-Check

> [!QUESTION]- 1. What are four main functions of an operating system?
> User interface, memory management, interrupt handling and processor scheduling.

> [!QUESTION]- 2. What's the main difference between paging and segmentation?
> Paging uses fixed-size blocks, while segmentation uses variable-size sections that can correspond to logical parts of a program.

> [!QUESTION]- 3. What does a page table do?
> It maps logical memory locations to physical memory locations.

> [!QUESTION]- 4. Why is virtual memory useful, and what is its main drawback?
> It lets the computer run processes whose memory requirements exceed available RAM. Heavy swapping is much slower and can cause disk thrashing.

> [!QUESTION]- 5. What happens when the CPU services an interrupt?
> The current process state is saved, the ISR runs, then the saved state is restored so the previous process can continue.

> [!QUESTION]- 6. What's the difference between SJF and SRT?
> SJF is non-pre-emptive and chooses the shortest waiting job after the current one finishes. SRT is pre-emptive and can switch to a newly arrived process with a shorter remaining time.
