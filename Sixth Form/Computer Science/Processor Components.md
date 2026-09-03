---
date: 2026-09-03
tags:
  - computer-science
  - unit1
  - architecture
  - cpu
aliases:
  - CPU Components
  - Processor Components (OCR Unit 1)
---
# Processor Components

> OCR A Level Computer Science (H446 – Paper 1)
> Unit 1: Components of a computer and their uses

---

## Central Processing Unit (CPU)

> [!NOTE] Definition
> The **processor** (a.k.a. the [[Central Processing Unit (CPU)]]) is made up of several distinct components, each with its own role.

- [[Control Unit]]
- [[System Bus|Buses]]
- [[Arithmetic-Logic Unit (ALU)]]
- [[Dedicated Registers|Dedicated registers]]

---

## Control Unit

> [!IMPORTANT] Core takeaway
> The **[[Control Unit]]** coordinates the activity of *all* other CPU components — like a conductor directing an orchestra.

- Sends control signals along the **[[System Bus|control bus]]**
- Connects the control unit to other computer components

---

## What is a Bus?

> [!NOTE] Definition
> A **bus** is a series of connectors that transfer signals between internal components.

- Typically consists of **8, 16, 32, or 64 lines**
- Forms the backbone of communication inside the CPU

---

## System Bus

The **[[System Bus]]** is made up of three separate buses:

| Bus | Carries |
|---|---|
| **Control Bus** | Control signals |
| **Data Bus** | Data |
| **Address Bus** | Memory addresses |

- Connects the [[Central Processing Unit (CPU)|Processor]], **Input/Output**, and **Memory**

### Control Signals Include…

- **Memory read** — moves data from the addressed RAM location onto the data bus
- **Memory write** — writes data from the data bus into the addressed RAM location
- **Bus request** — a device signals it wants to use the data bus
- **Bus grant** — CPU grants a device access to the data bus
- **Clock** — synchronises operations across the system

---

## Arithmetic-Logic Unit (ALU)

> [!NOTE] Definition
> The **[[Arithmetic-Logic Unit (ALU)]]** is the "problem-solving" part of the processor — it performs arithmetic, logical, and shift operations.

- **Arithmetic operations:** Add, Subtract, Multiply, Divide
- **Logical operations:** AND, OR, NOT, XOR
- **Shift operations:** move bits left/right within a register

---
## The Accumulator

> [!IMPORTANT] Why it matters
> Writing every intermediate result back to "slow" memory would be inefficient. Instead, the CPU uses super-fast **[[Dedicated Registers|registers]]** to store working data temporarily.

- The **[[Accumulator]]** is a general-purpose register
- Holds intermediate/working results (e.g. building up `2 + 3 + 4`)
- Allows immediate re-use of results in later calculations

---

## Executing Instructions

To carry out a sequence of instructions, the processor must temporarily hold:

- The **current instruction** being executed
- The **address of the data** it needs
- **The data itself**
- The **address of the next instruction**

> [!NOTE] Analogy
> The [[Control Unit]] coordinates all of this — like a conductor controlling every section of an orchestra.

---

## Dedicated Registers

> [!IMPORTANT] Exam-critical definitions
> These five registers appear constantly in exam questions on the [[Fetch-Execute Cycle]].

| Register                                   | Role                                                                   |
| ------------------------------------------ | ---------------------------------------------------------------------- |
| **[[Program Counter (PC)]]**               | Holds the memory address of the *next* instruction to be executed      |
| **[[Current Instruction Register (CIR)]]** | Holds the *current* instruction, split into **opcode** and **operand** |
| **[[Memory Address Register (MAR)]]**      | Holds the address in memory to fetch/store data from or to             |
| **[[Memory Data Register (MDR)]]**         | Temporarily holds data moving between processor and main memory        |
| **[[Accumulator]]**                        | Holds intermediate results of an instruction                           |
|                                            |                                                                        |

---

## Fetch-Execute Cycle

> [!NOTE] Definition
> The **[[Fetch-Execute Cycle]]** describes the repeating stages a processor uses to carry out program instructions — repeated for *every* instruction in a program.

```
Fetch → Decode → Execute → (repeat)
```

### Fetch (Steps 1–4)

1. Address of next instruction copied from [[Program Counter (PC)|PC]] → [[Memory Address Register (MAR)|MAR]]
2. Instruction at that address copied to [[Memory Data Register (MDR)|MDR]]
3. **Simultaneously**, [[Program Counter (PC)|PC]] is incremented
4. Contents of [[Memory Data Register (MDR)|MDR]] copied to [[Current Instruction Register (CIR)|CIR]]
### Decode (Steps 5–7)

5. Instruction in [[Current Instruction Register (CIR)|CIR]] is decoded
6. Split into **opcode** and **operand** to determine instruction type; extra data fetched from memory if needed
7. Data passed to the [[Accumulator]]

> [!NOTE] Opcode vs Operand
> - **Opcode** — specifies the operation to carry out
> - **Operand** — holds either:
> 	- the *address* of data (copied to [[Memory Address Register (MAR)|MAR]]), **or**
> 	- the *actual data* (passed to [[Memory Data Register (MDR)|MDR]])

### Execute (Step 8)

8. Instruction is executed
	- Result held in the [[Accumulator]], **or**
	- Result sent/stored to main memory

---

## Plenary — Self-Check Questions

> [!QUESTION] Can you answer these?
> - What are the four main components of the processor? → [[Arithmetic-Logic Unit (ALU)|ALU]], [[Control Unit]], [[Dedicated Registers|registers]], [[System Bus]]
> - Name the **three buses** making up the system bus
> - Name the **five special registers** involved in the [[Fetch-Execute Cycle]]

---

## Related Notes
- [[Central Processing Unit (CPU)]]
- [[Control Unit]]
- [[Arithmetic-Logic Unit (ALU)]]
- [[System Bus]]
- [[Fetch-Execute Cycle]]
- [[Dedicated Registers]]
