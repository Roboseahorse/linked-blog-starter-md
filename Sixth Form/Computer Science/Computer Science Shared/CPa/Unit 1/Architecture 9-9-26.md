
> [!NOTE] Harvard vs Von neumann
> the core difference is that **Von Neumann Architecture uses a single shared memory and bus for both data and instructions**, while **Harvard Architecture uses separate physical memories and pathways for each**

## John von Neuman
- The most common implantation of this concept is the von Neuman architecture

## Harvard architecture
- An alternate model separates the data and instructions into separate memories using different buses
- Program instructions and data are no longer competing for the same bus
### Use of Harvard architecture
- Different sized memories and word lengths can be used for data and instructions
- Harvard principles are used with specialist embedded systems and digital signals processing **(DSP)**, where speed takes priority over the complexities of the design



| Von neumann                                                | Harvard architecture                                                                                            |
| ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| USed in PCs laptops servers and high performance computers | Used in digital signal processing, microcontrollers and in embedded systems such as microwaves oven and watches |
## Contemporary processor architecture 
- Modern CPU chips often incorporate aspects of both von Neuman and Harvard architecture
- In desktop computers, there is one main memory for holding both dara and instructions, but **cache memory** is divided into an **instruction cache and a data cache** so data and instructions are retrieved using Harvard architecture
## CISC and RISC
### CISC
- In complex instruction set computers CICS, a large instruction set is used to accomplish tasks in as few lines of assembly language as possible
	- •A **CISC** instruction combines a “load/store” instruction with the instruction that carries out the actual calculation
### RISC
- reduced instruction set computers (**RICS** ) takes an opposite approach 
- •A minimum number of very simple instructions, each taking one clock cycle, are used to accomplish all the required operations in multiple general purpose registers


| CICS                                                                                                    | RISC                                                                                                   |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Quicker to code programs                                                                                | The hardware is simpler to build with fewer circuits needed for carrying out complex instructions      |
| The compiler has very little work to do to translate a high-level language statements into machine code | Because each instruction takes the same amount of time, i.e. One clock cycle #, pipelining is possible |
| Because the code is relatively short, very little RAM is required  to store the instructions            | RAM in now cheap, and RISC use of RAM and software allows better performance processors at less cost   |
