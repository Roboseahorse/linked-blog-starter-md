---
date: 2026-10-01
tags:
  - computer-science
  - a-level
spec code: H446
---
# Homework 3: Types of Processor

**Unit 1: Components of a Computer**

### Question 1

a) A low-cost von Neumann machine has an address bus of $16\text{ bits}$. In this computer, a unit of addressable memory is two bytes. How many $\text{KiB}$ of addressable memory can be used? `[1]`

- [ ] *128 KiB*

b) i) Explain the basic difference between [[Architecture 9-9-26#John von Neuman|von Neumann architecture]] and [[Architecture 9-9-26#Harvard architecture|Harvard architecture]]. `[2]`

- [ ] ![[Architecture 9-9-26#^HarvardvsVonnNeuman]]

ii) Why is Harvard architecture potentially able to achieve higher processing speeds than von Neumann architecture? `[1]`

- [ ] *Harvard uses diffrent data busses for each instruction meaning instructions can be processed quicker*
    

iii) Give a typical use of each type of architecture. `[2]`

- [ ] **von Neumann:** *Laptops*
    
- [ ] **Harvard:** *Micro controllers*
    

### [[Architecture 9-9-26#CISC and RISC|Question 2]]

Compare the features of a Reduced Instruction Set Computer (RISC) architecture with that of Complex Instruction Set Computer (CISC) architecture, stating **one** advantage of each. `[6]`

- [ ] *RISC uses a small, fixed-length instruction set optimized for single-clock execution and [[Processor Performance 2026-09-07#Pipelining|pipelining]], whereas CISC uses a large, variable-length instruction set capable of multi-step operations directly in memory*

### Question 3

Describe briefly the features of a [[Types of Processor 2026-09-09#GPU and Parallel Processing|Graphics Processing Unit (GPU)]], stating why it is particularly suitable for image processing. `[3]`

- [ ] *A graphics processing unit contains its own memory for storing instructions, additionally it contains lots of cores which can all work simultaneously to carry out many instructions at once, this makes the GPU suitable for image processing*

**Total: 15 marks**