---
date: 2026-09-07
tags:
  - computer-science
  - processor-performance
  - cpu
aliases:
  - Processor Performance
  - CPU Performance
---

## Processor Performance

### Learning Objectives
- Describe the factors affecting CPU performance:
  - Clock speed
  - Number of cores
  - Cache memory
- Understand how pipelining improves processor efficiency.

[!NOTE]
The three key factors that affect processor performance are **clock speed**, **number of cores**, and **cache memory**.

### Fetch-Execute Cycle
The processor repeatedly carries out the fetch-execute cycle:
1. Fetch an instruction.
2. Decode the instruction.
3. Execute the instruction.

### Words and Memory
- Memory is divided into equal-sized units called **words**.
- Common word lengths are 8, 16, 32, and 64 bits.
- Each word has its own memory address.

| Term | Meaning |
|--------|--------|
| Word | A fixed-size unit of data stored in memory |
| Word Length | Number of bits in each word |
| Memory Address | Unique location identifier |

### Address Bus
- The width of the address bus determines the maximum number of memory addresses.
- An 8-bit address bus can address 2^8 = 256 memory locations.
- 4 GiB of memory requires 2^32 addresses, so a 32-bit address bus is needed.

[!IMPORTANT]
The size of the address bus determines the maximum amount of RAM that can be addressed.

### Data Bus
- The data bus is bi-directional.
- Its width is determined by the number of wires it contains.
- If the data bus matches the word size, a whole word can be transferred in one operation.

### Machine Code and Instructions
- Assembly language closely corresponds to machine code.
- Processor architecture determines instruction format.
- Factors include:
  - Word size
  - Address bus width

### Factors Affecting Processor Performance
#### Clock Speed
- The fetch-execute cycle is driven by the system clock.
- Higher clock speeds allow more instructions to be processed per second.
- A 4 GHz processor generates approximately 4 billion clock cycles per second.

#### System Clock
- Synchronises processor operations using regular ON/OFF signals.
- Actions usually occur on the rising edge of the clock.
- Operations require a fixed number of clock cycles.

#### Number of Cores
- A dual-core processor contains two cores.
- A quad-core processor contains four cores.
- Multiple cores can process different instructions simultaneously.
- Performance gains depend on whether software can use all available cores.

### Parallel Processing
[[Parallel Processing]] involves multiple processor cores working at the same time.

Benefits:
- Different parts of a task can be processed concurrently.

Limitation:
- Some instructions must be completed sequentially.

### Cache Memory
Cache is very fast memory located on or near the processor.

| Cache Type | Characteristics |
|------------|----------------|
| L1 Cache | Fastest, smaller size |
| L2 Cache | Larger, slightly slower |

- Stores recently used data and instructions.
- Reduces the need to access slower RAM.
- L1 cache is commonly split into instruction cache and data cache.

[!NOTE]
More cache increases the likelihood that required data is already available, reducing access times.

### Pipelining
[[Pipelining]] improves performance by overlapping stages of instruction processing.

Example:
- Instruction 1 enters the pipeline.
- Before it finishes, Instruction 2 enters.
- Then Instruction 3 enters.

This allows multiple instructions to be processed simultaneously at different stages.

### Key Takeaways
- Clock speed affects how many cycles occur each second.
- Additional cores enable parallel processing.
- Cache memory reduces slow RAM access.
- Address bus width determines addressable memory.
- Data bus width affects data transfer size.
- Pipelining improves processor efficiency.

## Self-Check Questions
1. What are the three main factors affecting CPU performance?
2. How does clock speed influence performance?
3. What is the difference between L1 and L2 cache?
4. Why do additional cores not always increase performance proportionally?
5. How does pipelining improve efficiency?

## Related Notes
- [[CPU Architecture]]
- [[Fetch-Execute Cycle]]
- [[Cache Memory]]
- [[Parallel Processing]]
- [[Pipelining]]
