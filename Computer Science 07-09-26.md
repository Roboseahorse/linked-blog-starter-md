> [!question] Do Now
>DN: how do the machine do instructions relate to assembly language programs?
>
Assembly language is translated using a compiler into machine code that the computer can understand
*In most cases, one assembly language instruction corresponds to one machine code instruction*

Assembly language is very closely related to machine code
- **Generally there is a one to one correspondence between a machine code instruction and uts assembly language equivalent**

The processor can only send signals to the address buss it can not receive signals this is called **Omnidirectional** 
The input and output is **bidirectional** between all [[Processor Components 2026-09-03|Busses]] (control bus, data bus,  and address bus)
## Accumulator
- Stores results from the ALU
	- Rather than writing working data back to 'slow' memory, processors have several locations if super fast memory

System clock - continuous cycling signal used as a timing pulse
CIR - holds the current instructing being processed
Accumulator - a single memory location in which arithmetic and logic results are stored

### Fetch *(steps 1-4)*:
1. The address of the next instruction is copied from the pc to the MAR
2. The instruction held at that address is copied to the memory data register
3. Simultaneously the contents To the program counter are incremented
4. The content of the MDR are copied to the CIR

### Decode *(steps 5-7)*
5. The instruction held in the CIR is decoded
6. It is split into operand and opcode to determine the type of instruction it is. Additional data, if required, is fetched from memory
7. and is passed to the accumulator

--- 
## Words
- Memory is divided up into equal units called **words**
	- Word length is usually 8, 16, 32, or 64 bits
- Each word has a separate memory address

## Address bus
- The width of the address buss determines the maximum possible memory addresses of the system
- With an 8-but address bus, the maximum number of memory addresses is 2<sup>8</sup> =256
- An average PC has a memory of capacity of 4 Gib ( gbibibyte) which is 2<sup>32</sup> bytes 
	- Therefore it **MUST** have a *32* bit address buss