## Do Now

### I Do

A processor uses a word length of **8 bits** and has an address bus of **10 lines**.

#### (a) What is the maximum number of addressable words in memory?

The address bus has **10 lines**.

Each address line can carry two possible values: **0** or **1**.

- 1 line → 2¹ = 2 addresses
- 2 lines → 2² = 4 addresses

2^10 = 1024

**Answer: 1024 words**

#### (b) What is the overall memory capacity in KiB?

8 bits = 1 byte

1024 words × 1 byte = 1024 bytes

1024 bytes ÷ 1024 = 1 KiB

**Answer: 1 KiB**

### You Do

#### Question 1

A processor uses a word length of **16 bits** and has an address bus of **12 lines**.

(a) Maximum number of addressable words:

2^12 = 4096

**Answer: 4,096 words**

(b) Overall memory capacity:

16 bits = 2 bytes

4096 × 2 = 8192 bytes

8192 ÷ 1024 = 8 KiB

**Answer: 8 KiB**

#### Question 2

A processor uses a word length of **32 bits** and has an address bus of **14 lines**.

(a) Maximum number of addressable words:

2^14 = 16384

**Answer: 16,384 words**

(b) Overall memory capacity:

32 bits = 4 bytes

16384 × 4 = 65,536 bytes

65536 ÷ 1024 = 64 KiB

**Answer: 64 KiB**

#### Question 3

A processor uses a word length of **64 bits** and has an address bus of **16 lines**.

(a) Maximum number of addressable words:

2^16 = 65536

**Answer: 65,536 words**

(b) Overall memory capacity:

64 bits = 8 bytes

65536 × 8 = 524,288 bytes

524288 ÷ 1024 = 512 KiB

**Answer: 512 KiB**

---

## Lesson Notes

### Stored Program Concept

The instructions are loaded and executed in order. The order can only be changed with an Interrupt signal or a Jump command where it **Interrupts** the queue or **Jumps** the queue.

> [!NOTE]
> Programs must be loaded into main memory before execution. Instructions are fetched, decoded and executed sequentially.

### CPU Architectures
- Modern CPU chips often incorporate aspects of both von Neumann and Harvard architecture.
- In desktop computers, there is one main memory for holding both data and instructions, but **cache memory** is divided into an **instruction cache and a data cache** so data and instructions are retrieved using Harvard architecture

> [!NOTE]
> Some digital signal processors have **multiple parallel data buses** (e.g. two write, three read) and one instruction bus

### Von Neumann Architecture

Instructions and data are stored in a **common main memory** and transferred using a single **shared bus**. Here affordability takes priority instead of speed.

| Feature       | Description                                 |
| ------------- | ------------------------------------------- |
| Memory        | Data and instructions share the same memory |
| Bus           | One shared bus                              |
| Advantages    | Simpler design, cheaper                     |
| Disadvantages | Bottleneck caused by shared bus, slower     |

### Harvard Architecture

Alternative model that separated the data and instructions into **different memories** using different busses, the program and instructions are no longer competing for the same bus. Here, speed takes priority instead of affordability. It is used mostly in **embedded systems**.

| Feature       | Description                                       |
| ------------- | ------------------------------------------------- |
| Memory        | Separate memories for data and instructions       |
| Bus           | Separate buses                                    |
| Advantages    | Parallel access to data and instructions, quicker |
| Disadvantages | More complex control unit, expensive              |

### CISC vs RISC


| CISC                        | RISC                       |
| --------------------------- | -------------------------- |
| Complex instructions        | Simple instructions        |
| Shorter programs            | More instructions required |
| Easier compiler translation | Better pipelining          |
| Little RAM required         | Simple hardware            |
#### CISC
- In **Complex Instruction Set Computers** (CISC), a large instruction set is used to accomplish tasks in as few lines of assembly language as possible.
- A single assembly language instruction such as:

> 	MULT A, B

could be used to multiply A by B and store the result back in A.

> [!NOTE]
> A CISC instruction combines a “load/store” instruction with the instruction that carries out the actual calculation

#### RISC
- **Reduced Instruction Set Computers** (RISC) take an opposite approach

- A minimum number of very simple instructions, each taking one clock cycle, are used to accomplish all the required operations in multiple general purpose registers

### GPU and Parallel Processing

> [!IMPORTANT]
> GPUs contain thousands of cores and are designed for highly parallel processing tasks.

### Self-Check

> [!QUESTION]
> 1. What causes the Von Neumann bottleneck?
> 2. Why is Harvard architecture faster?
> 3. What is the difference between CISC and RISC?
> 4. Why are GPUs effective for graphics processing?
