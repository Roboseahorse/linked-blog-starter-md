---
date:
tags:
  - computer-science
  - a-level
spec code: H446
Teacher: MR PAYNE
Continued from: "[[Types Of Operating System 2026-10-05]]"
---
## Embedded operating system
- Many devices in your home have an embedded OS and run simple programs
	- The OS has minimal feaures
	- application programs are held in ROM
	- There is a limited amount of RAM
	- The user interface is simple and minimaql

## Real time operating systems
- Some operating systems must operate in real time
	- Must respond extremely quickly to inputs
	- many need to cope with many inputs simutaneously
- Real time Operating systems are usually seen in **Saftey-critcial** enviroments
- IF a hardware component fails the OS must have a **failsafe**to detect this and respond appropratly
- There is hardware **redundancy** - Crucial components are duplicated in case one fails 

## [[BIOS]]
- BIOS (Basic input output system) is stored in **ROM**
- The BIOS boots the computer at start-up
	- Initialise and test hardware
	- Loads the operating system into RAM

## Device drivers
- A driver is a program that provides an interface for the OS to interact with a deice
	- Drivers are hardware dependent and OS specific
		- *Drivers are needed to allow the OS to control hardware devices rom speakers to graphics card*
- The OS does not need to know the specifics of the hardware to be able to interact with it
	- Any brand of hardware devices can be controlled as long as there is an OS compatble driver 

## Virtual Machine
- Software is used to emulate a machine
- Can be used for running one OS inside another to emulate different hardware
- A virtual machine can execute intermediate code e.g. java virtual machine executes java byte by byte
	- *The NAME virtual machine can emulate the hardware of old arcade machine so that their games can be played on a modern PC*
