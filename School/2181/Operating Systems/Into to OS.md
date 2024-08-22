 - The operating system is a special system sofware between the computer hardware and application programs

 - The OS implements abstractions to make hardware easier to use

 - The OS shares hardware resouces among multiple programs that are running on the system

- The OS kernel implements core OS functionality needed to use the system

 -  A policty dictates the "what", "when", etc. whereas a mechanism corresponds to "how" a particular functionality is implemented

 - The OS provides a system call interface to users of the system and also a device interface for interactig with hardware devices

 - In an interrupt-driven system, a user-level program makes a system call in order to access functionality and a hardware device issues a interrupt to initiate OS actions

 - The type of interrupt that is triggered by a user program making a system call is referred to as a trap

 - In the user mode, it executes only user-level instructions and only specific regions of memory. In the kernel mode, it can execute any instruciton, and access any memeory location

 - The OS uses abstraction called process to manage concurrently running program instances. It is possible for the OS to run multiple instances of the same program

 - The linux terminal has commands to display running level processes, kill them or change their priority level

 - Linux commands can be combined to perform more than one function at a time