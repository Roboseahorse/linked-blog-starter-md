---
date: 2026-09-28
tags:
  - computer-science
  - a-level
spec code: H446
---
## What is an operating system
- You need software to manage communication with your computer hardware
- The boot loader in ROM loads the operating system 9OS) into RAM when the computer is switched on
- 
### What functions does the OS provide
- User interface
- Memory management
	- Programs and their data need to be loaded into RAM
	- The operating System must manage the allocation of RAM to the different programs
- Interrupt handling
- Processor scheduling 

## [[Operating System Functions 2026-09-28#Paging|Paging]]
- Available memory is divided into fixed size chunks called **pages**
- Each page has an address
- A process loaded into RAM is allocated sufficient pages, but this pages may not be **continuous** (next to each other) in physical terms

## Segmentation
- Segmentation is a method of **chunking** memory into **blocks that correspond to diffrent types of data** needed by an application
- The arrangement of data becomes fragmented overtime as there is no guarantee that a new block will occupy the same space as the older one
