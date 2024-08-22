Understanding Computer Architecture 
 - Computer Architecture is like the blueprint of a computer's hardware. It describes how all the physical components of a computer are arranged and how they interact with each other. 


The CPU - The Brain of the computer 
 - The CPU is like the brain of the computer. The CPU executes program instructions to carry out tasks. 
 - These instructions and data are stored in Random Access Memory (RAM); think of RAM as the computer's short term memory
 - The CPU reads and writes data in RAM to perform its functions. The CPU is connected to the RAM using sets of wires, which we refer to as busses (data bus or address bus)


Instruction Set Architecture - The language of the CPU
 - Instruction Set Architecture (ISA) defines the instructions a CPU can understand
	 - Just like humans understand words and sentences,  The CPU understands specific commands known as instructions. ISA is the collection of these instructions that a particular CPU can understand. It's like the vocabulary and grammar for the CPU. 
- Different CPUs have different ISAs like languages in human culture
	- Examples include SPARC, IA32, MIPS, ARM, and x86
- ISAs tell the CPU how to understand and execute instructions


Microarchitecture - The Building Blocks of ISA 
 - Microarchitecture is the circuitry for a specific ISA
	 - The microarchitecture describes how a specific ISA is implemented in hardware. It's like a blueprint that guides how the physical components are arranged to execute the set of instructions. 
- Different Microarchitectures can implement the same ISA
	- Just as different builders can construct houses that all comply with the same building codes, different microarchitectures can execute the same instruction set but with distinct design approaches
- Understanding microarchitecture allows us to 
	- Bridge the gap between the high-level programming languages and the actual hardware operations
	- Create more efficient and effective software


Types of ISAs: RISC vs CISC 
 - ISAs can be classified into RISC (Reduced Instruction Set Computer) or CISC (Complex Instruction Set Computer) 
 - RISC uses simple instructions that executes quickly, like basic building blocks
	 - Popular RISC architectures include ARM and MIPS
- CISC provides more complex instructions that perform multiple functions. 
	- Popular CISC architectures include x86, used in many personal computers
- Imagine RISC as a simple Lego set, each block doing one thing; CISC is like a multi-tool Swiss knife, with each tool serving several purposes


Historical Perspective and Development 
 - RISC was developed in 1980's at Berkeley and Stanford
 - David Paterson and John Hennessy won eth e2017 Turing Award for RISC development


Comparing RISC and CISC Today
 - RISC is more common in high-end servers and mobile devices
 - CISC dominates desktop and many server-class computers
 - It's important to keep in mind that the comparison between RISC and CISC is not always clear-cut, as the line between the two has blurred with modern technological advances


The origin of modern computing architectures
 - Modern computer architecture emerged from various 1930s and 1940s ideas
 - Claude Shannon made the connection between Boolean algebra and electrical circuit design in 1937
	 - This laid the foundation for all digital circuit design and helped lead to modern computer architecture 
- Shannon's ideas were instrumental in moving from analog to digital computing
	- The binary system became the core of how computers process information, representing data in a series of ones and zeros


Intro to von Neumann Architecture 
 - The von Neumann architecture is the blueprint for most modern computers
	 - Almost all personal computers, laptops, and even smartphones follow this architecture
- It consists of five main parts that work together
	- These parts are the processing unit, control unit, memory unit, input, and output units
- Buses connect these units to enable communication 
	- Buses are like the computer's highway system, allowing data to flow between different parts of the computer


The CPU - The Brain of the Computer
 - The CPU is made of two main parts: the processing unit and the control unit 
 - The processing unit executes instructions (e.g., addition or subtraction)
 - The control unit guides the execution of these instructions
	 - The control unit acts like a traffic cop, directing the flow of data and instructions in the CPU
	 - It works with the processing unit by fetching instructions from memory, decoding them, and then executing them. 
- Together, these two units make up the CPU, handling all calculations


Processing Unit - ALU and Registers
- The Arithmetic/Logic Unit (ALU) does the math 
	- This includes both arithmetic operations (such as addition, sub, multi, division) and logical operations (such as comparisons)
- Registers are small storage areas that hold data and instructions
	- Registers are like variables in programming but within the hardware itself; they temporarily hold dat or instructions, allowing quick access for the CPU during execution. 
- In the von Neumann architecture, instructions are treated as data
	- This means that the processing unit works with both numbers and code


Control Unit - Managing Execution
 - The Control unit manages how instruction are performed. 
 - It loads instructions from memory and sends them to the processing unit
 - The program counter (PC) and instruction register (IR) help to track progress. 
 - PC keeps the address of the next instruction; IR stores the current one.
 - It's like a conductor leading an orchestra, ensuring each part plays in sync


Memory Unit - Storing Data and Instructions
 - The term memory sometimes refers to an entire hierarchy of storage in the system. It can include registers in the processing unit as well as secondary storage devices like hard disk drives (HDD) or solid-state drive (SSD)
 - For now we use the term "memory" interchangeably with internal random access memory (RAM) - memory that can be accessed by the CPU
- Memory stores program data and instructions close to the CPU
- Think of memory as the desk where you keep all your tools and documents


Input and Output Units - Connecting with the World
 - Input units like Keyboards and mice let you communicate with the computer
 - Output units like monitors and speakers show the computer's responses.
 - Some devices, like touchscreens, serve both input and output functions
 - These units make the computer and interactive tool, not just a number-cruncher
 - The I/O units are integral to the functionality and usability of the computer; without them, the computer would be a closed system, unable to interact with users or other devices


The von Neumann Architecture 
![[Pasted image 20230825170728.png]]


Buses and Word Sizes - Communication and Standards 
 - Buses are channels/wires that allow different parts to talk with each other
 - They carry data, memory addresses, and control signals between units
	 - The width of a data bus (e.g., 32 bits) determines how much data can be transferred at once
- Word size is the standard data size handled by the processor
	- It's like the standard portion size for the computer's meals
- Word sizes have changed over time, from 16 bits to today's 64 bits
- This communication system and standardization make the architecture universally applicable


Fetching Instructions: The First Step
 - The control unit starts by locating the next instruction 
 - The program counter (PC) register holds the address of this instruction 
 - A read command sends the address to the memory unit 
 - The memory unit reads the bytes and send them back to the control unit 
 - The instruction register (IR) stores these bytes;  the PC is updated for the next fetch


 Decoding: Understanding the Instruction
  - The control unit reads the instruction from the IR.
  - It breaks down the bits to understand the operation and operands
  - The definition of encoding is based on the ISA (instruction set architecture) 
  - Operand values are fetched from location like CPU registers or memory 
  - Now, the instruction is ready for execution by the processing unit 

![[Pasted image 20230825170225.png]]



Execution & Storing: Performing & Saving the Operation 
 - The processing unit (ALU) carries out the instruction on the data operands 
 - The result of this execution is ready to be stored 
 - The control unit places the results on the data bus 
 - The address for storage is placed on the address bus; a write command is issued. 
 - The memory unit writes the value to memory at the specific address

![[Pasted image 20230825170749.png]]


Execution and & Storing: Performing & Saving the Operation 
 - The processing unit (ALU) carries out the instruction on the data operands 
 - The result of the 