Ordinary Files
 - An ordinary file is a file on the system that contains data, text or program instructions

Directories
 - Directories store both special and ordinary files

Special Files
 - Some special files provide access to hardware such as hard drives, CD-ROM drives, modems, and Ethernet adapters. Other special files are similar to aliases or shortcuts and enable you to access a single file using different names

Listing Files:

Example below :
-rw-rw-r--     2     amrood    amrood    4096    Dec   25    09:59   uml
 - First column - file type and permission given on the file 
 - Second column - Number of memory blocks taken by the file or directory 
 - Third column - owner of the file 
 - Fourth column - The group of the owner. Every Unix user will have an associated group
 - Fifth column - file size in bytes
 - Sixth column - date and time file was created or modified last
 - Seventh column - File or directory name

When using ls -l every file begins with a d, -, or l. These characters indicate the type of the file that's listed
 - - 
	 - regular file such as ASCII text file, binary executable or hard link 
 - b 
	 - Block special file. Block input/output device file such as a physical hard drive 
- c 
	- Character special file. Raw input/output device such as a physical hard drive 
- d
	- Directory file that contains a listing of other files and directories 
- l 
	- Symbolic link file. Links on any regular file 
- p 
	- Named pipe. A mechanism for inter-process communications
- s
	- Socket used for inter-process communications

Listing Files
 - $ls
	 - $ls -l
		 - get more info about each file
	Metacharacters
	 - * and ? are meta characters
		* Ex: $ls ch* .doc
				Displays all the files names which start with ch and end with .doc
	Hidden Files
		$ls -a 
			Will display hidden files 

Creating Files
	$ vi filename
		vi will create ordinary files on any Unix system
		This will open a file with the given name. Press i key to enter edit mode 

Display Content of a File 
	$ cat filename 
		cat command lets you see the contents of a file 

Counting words in a file 
	wc command to count the total number of lines, words and characters in a file 
		$ wc filename 

Copying Files
	cp command to copy file 
		$ cp source_file destination_file 

Renaming Files 
	mv command to change name of file 
		$ vm old_file new_file 

Deleting Files 
	rm to delete existing file 
		$ rm filename 


