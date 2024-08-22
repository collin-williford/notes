Introduction
 - Non-volatile, long-term storage (e.g., disk)
	 - Must store very large amount of information 
	 - Must persist beyond process lifetime
	 - Must be accessible by multiple processes at once

Data organization on disks 
 - All data organized into equal-sized blocks on disk
 - Disk supports two main operations
	 - Read block x
	 - Write block x 
- Addressing disk blocks directly  -> too complex for users
- OS provides simpler abstraction for persistent data
- This abstraction is called file system 
	- Files 
		- Named collections of related data in file system 
- File split into blocks as well
- Logical blocks mapped to physical blocks 