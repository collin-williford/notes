Home Directory 
	you can go in your home directory anytime with 
		$cd ~
	if you have to go into another users home directory then 
		$ cd ~username 
	to go into you last directory use 
		$cd -

Absolute/Relative Pathnames 
 - A pathname is absolute if it is described in relation to the root thus pathnames begin with /
 - Relative pathnames never begin with  / and are based on your current directory 
 - To determine where you are use 
	 - $pwd 

Listing Directories 
	to list the files in a directory 
		$ls dirname 

Creating Directory 
 - $mkdir dirname 

Creating Parent Directories 
 - mkdir will case issues
	 - $mkdir /tmp/amrood/test
		 - This will fail
- so use -p option to the mkdir
	- $mkdir -p /tmp/amrood/test 

Removing Directories 
 - directories can be deleted using rmdir
	 - $rmdir dirname 

Changing Directories 
 - cd command to change directory 
	- $cd dirname 

Renaming Directories 
 - mv command can be used to rename directory 
	 - $mv olddir newdir

