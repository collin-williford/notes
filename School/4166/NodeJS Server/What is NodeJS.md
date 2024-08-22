 - NodeJS is more than a wrapper for V8 JS engine 
 - Its core modules provide an API for working with OS, file system, network, etc
 - A number of external dependencies
	 - V8 JS engine
	 - Libuv
	 - llhttp

Modules
 - JavaScript supports modularization by using modules
 - In NodeJS, each file is treated as a module, which can be used by other files 
 - Each module is wrapped in a function 
 - Therefore, local variables of a module have function scope, and is not accessible outside of the file 
 - A module can export its variables to be used by another module
	 - module.exports
	 - exports

Require Modules
 - In NodeJS, to use a module, call the require function 
	 - Core module: call require function with module name 
		 - const fs = require('fs');
	- Local module: call require function with relative path to the file 
		- const fs = require('./...');
	- Third party module: first install the package using NPM, and then call require function with module name