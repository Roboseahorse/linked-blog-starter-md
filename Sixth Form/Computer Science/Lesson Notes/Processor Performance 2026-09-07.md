---
date: 2026-09-07
tags:
  - computer-science
  - cpu
  - processor-performance
  - a-level
aliases:
  - CPU Performance
  - Processor Performance
---

## Processor Performance

> [!NOTE]
> Processor performance is mainly affected by **clock speed**, **number of cores**, and **cache memory**.

### Learning Objectives
- Describe the factors affecting CPU performance.
- Understand how **pipelining** improves processor efficiency.

### Words and Memory
- Memory is divided into equal-sized units called **words**.
- Common word lengths: **8, 16, 32, or 64 bits**.
- Each word has its own memory address.

> [!IMPORTANT]
> The word length affects how much data can be processed in a single operation.

### Address Bus
- The width of the address bus determines the maximum number of memory addresses.
- Formula:

```text
Number of addresses = 2^(address bus width)
```

| Address Bus Width | Maximum Addresses |
|-------------------|------------------|
| 8-bit | 256 |
| 32-bit | 4,294,967,296 |

- A computer with 4 GiB (2^32 bytes) of memory requires a **32-bit address bus**.

### Data Bus
- The data bus is **bi-directional**.
- Data can travel to and from memory.
- Bus width is determined by the number of wires (lines).

> [!NOTE]
> If the data bus width matches the word size, a whole word can be transferred in one operation.

### Machine Code and Instructions
- [[Assembly Language]] is closely related to machine code.
- Usually there is a **one-to-one relationship** between machine code instructions and assembly instructions.
- Instruction format depends on:
  - Word size
  - Address bus width

> [!IMPORTANT]
> The maximum operand size depends on the width of the address bus.

## Factors Affecting CPU Performance

### 1. Clock Speed
- The fetch-decode-execute cycle is controlled by the **system clock**.
- A higher clock speed means more cycles every second.
- More cycles generally allow instructions to be processed faster.

Example:
- A **4 GHz** processor performs approximately **4 billion clock cycles per second**.

### The System Clock
- Produces regular ON/OFF pulses.
- Synchronises processor operations.
- Actions usually occur on the **rising edge** of the clock signal.
- Different operations take a fixed number of cycles.

### 2. Number of Cores
- Modern processors often contain multiple cores.
- Each core can run its own fetch-execute cycle.

| Processor Type | Number of Cores |
| -------------- | --------------- |
| Single-core    | 1               |
| Dual-core      | 2               |
| Quad-core      | 4               |

Benefits:
- Multiple instructions can be processed simultaneously.
- Performance can increase significantly when software supports parallel processing.

Limitations:
- Not all programs can make full use of multiple cores.

### Parallel Processing
- Also called **concurrent processing**.
- Multiple cores work on different parts of a task at the same time.
- Some tasks cannot be easily split because instructions often depend on previous results.

### 3. Cache Memory
- Cache stores recently used data and instructions.
- It is much faster than RAM but more expensive.
- Located directly on the processor chip.

| Cache Level | Characteristics |
|------------|----------------|
| L1 Cache | Fastest, smallest |
| L2 Cache | Larger, slightly slower |

#### L1 Cache Types
- **Instruction Cache** → stores instructions.
- **Data Cache** → stores data.

> [!IMPORTANT]
> Splitting instruction and data caches allows both to be fetched at the same time.

Benefits of More Cache:
- Fewer accesses to RAM.
- Faster retrieval of frequently used data.
- Improved overall CPU performance.

## Pipelining
- A technique used to improve processor efficiency.
- Different stages of instructions are overlapped.
- While one instruction progresses through a stage, another instruction can enter the pipeline.

Example:
1. Instruction A enters Stage 1.
2. Instruction B enters Stage 1 while A moves to Stage 2.
3. Instruction C enters Stage 1 while A and B continue through later stages.

> [!NOTE]
> Modern pipelines may contain 10–12 or more stages.

## Exam Summary

> [!IMPORTANT] Key Facts to Remember
> - Clock speed affects how many cycles occur each second.
> - More cores enable parallel processing.
> - Larger and faster cache memory improves performance.
> - Address bus width determines maximum memory capacity.
> - Data bus width affects how much data can be transferred at once.
> - Pipelining improves efficiency by overlapping instruction stages.

## Self-Check Questions

> [!QUESTION]- Test Yourself
> 1. What are the three main factors affecting CPU performance?
> 2. Why does increasing clock speed improve performance?
> 3. What is the difference between L1 and L2 cache?
> 4. How does the address bus affect memory capacity?
> 5. What is parallel processing?
> 6. How does pipelining improve efficiency?

## Related Notes
- [[CPU]]
- [[Fetch Execute Cycle]]
- [[Memory]]
- [[Assembly Language]]
- [[Computer Architecture]]
