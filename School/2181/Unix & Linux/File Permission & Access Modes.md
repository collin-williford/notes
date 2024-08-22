  - Owner Permissions
	 - The owner's permissions determine what actions the owner of the file can perform on the file 
- Group Permissions 
	- Determine what actions a user, who is a member of the group that a file belongs to can perform on the file
- Other (world) permissions 
	- permissions for others indicate what action all other users can perform on the file 

U = "user/owner"
G = "group"
O = "other"

Permission Indicators
 - when using ls -l it displays various info related to file permissions
 - Example 
	 - -rwxr-xr--
		 - first charcter - indicates its a regular file 
		 - rwx means owner can read, write and execute
		 - r-x means group can read and execute only 
		 - r-- means other can only read 


Changing Permissions
 - use **chmod** to change the file or directory permissions 
 - two ways to use chmod, in symbolic or absolute mode
 - Using chmod in symbolic mode
	 - +
		 - adds the designated permissions to a file or directory 
	- -
		- removes the designated permissions from a file or directory 
	- =
		- Sets the designated permissions 
	- Example of symbolic mode 
		- $chmod o+wx testfile
			- This will add write and execute to others for testfile
		- $chmod u-x testfile
			- This will remove execute for owner for testfile
		- can combine like this 
			- $chmod o+wx, u-x, g=rx testfile
- Using chmod with absolue mode
	- Each permission is assigned a value 
	- 0
		- No permissions
	- 1
		- Execute permissions
	- 2
		- Write permissions
	- 3 
		- Execute and write permissions 
	- 4
		- Read permissions
	- 5
		- Read and Execute permissions
		- 4 (read) + 1(execute) 
	- 6
		- Read and write permission 
		- 4 (read) + 2 (write) 
	- 7
		- All permissions 
		- 4 (read) + 2 (write) + 1 (execute) 
	- Examples
		- $chmod 755 testfile
			- This gives all permissions to owner, read and execute for group, read and execute for others
		- $chmod 743 testfile
			- This gives all permissions to owner, read to group, execute and write to execute to others


Changing Owners and Groups
 - chown 
	 - "change owner", is used to change owner of file 
	 - Syntax
		 - $ chown user filelist
- chgrp
	- "change group" used to change group of a file 
	- Syntax
		- chgrp group filelist




