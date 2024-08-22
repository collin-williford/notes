Middleware
 - A middleware is a function that is being executed in a request response cycle
 - A middleware function has the following structure
![](Pasted%20image%2020230926113150.png)

Middleware Stack
 - Middleware funcitons are executed equentially
	 - The order of the fuctions matters
- If the current middleware function doesn't send a response, it must call teh next one, otherwirse the request will be left hanging
- If a middleware function sends a response, it can omit next as the third argument

Mount a Middleware function
 - app.use(\[path], function, \[function...])
	 - mounts a middleware function or functions at a given path 
- For each incoming request if its URL or the prefix of the URL matches the path, it executes the middleware functions
	- Different routes, HTTP method does not matter
- If path is not specified, it defaults to '/' and the middleware function will not be executed for every request to the app

Example
 - app.use('/apple', ((req, res, next) => {...}));
	 - This middleware function will be executed if the request's URL is '/apple', '/apple/images', '/apple/images/news', etc
- app.use((req, res, next) => {});
	- This middleware function will be executed for any incoming requests

Built-in Middleware
 - Express has the following built-in middlware function 
	 - express.static
	 - express.json
	 - express.urlencoded

Serving Static Files
 - express.static() returns a middleware function that can be used to server static files, such as images, CSS files and JS files
 - Pass the name of the directory that contains the static files as an argument 
 - For example, if all of the app's static files are stored in ./pubilic folder
	 - app.use(express.static('public'));

Body-parser Middleware
 - express.urlencoded() returns a middleware function that parses incoming requests with URL-encoded payloads
	 - app.use(express.urlencoded({extended: true}));
- express.json() returns a middleware funciton that parses incoming requests with JSON payloads
	- app.use(express.json());
- Both are available with Express 4.16.0+

Third-party Middleware
 - morgan
 - method-override
 - session
 - express-validator
 - connect-flash
 - helmet
 - 