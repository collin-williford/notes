What is Express
 - A web framework built on top of the Node http module 
	 - Minimalist
	 - Un-opioniated
- As compared to vanila Node API, Express
	- provides an easy way to handle routing, interpret requests and generate responses
	- uses template engine for rendering dynamic HTML views
	- uses middleware for sessions, authentication, authorization, input validation, etc

Create an Express App
 - Install the Express Package
	 - //require the Express module
	 - const express = require('express');
	 - .
	 - //create an Express Application
	 - const app = express();
	 - .
	 - //bind the app to a particular port number
	 - app.listen(port, host, () => { });

Route Handling
 - Express defines routes in the following structure:
	 - app.METHOD(path, handler);
	 - METHOD is an HTTP request method, thus it can be get, post, put, delete
	 - path is a path on the server
	 - route handler is a funciton, which will be executed when the method and path matches an incoming request
		 - Example
		 - //handle GET request at '/'
		 - app.get('/', (req, res) => {
			 - res.send('Hello World');
		 });

Request(req) Object
 - Extens the http.IncomingMessage of class Node
 - Provides additional methods and properties for parsing an incoming request message

Route Parameters
 - The request URL may contain parameters
	 - Request URL
		 - \http://localhost:3000/books/34
		 - identify which book is being requested
	- To extract the value of the parameters, the route path inlcudes a name at the same position as the result parameter in the request URL
		- Route path: /books/:bookid
	- The req.params returns an object containing a name and value pair for each route parameter
		- req.params: {booksid: "34"}
		- use req.params.bookid to retrievethe value

Query Strings
 - A query string is text represented as key/value pairs in the URL following a question mark (?) after the hostname
 - The req.query returns an object containing a property for each query string parameters in the request URL
	- Example:
		- URL: localhost: 8084/?name=alice&email=alice@abc\.com
		- req.query: {name: 'alice', email: 'alice@abc.\com'}

Request Body 
 - Client may send data to server through the request body in a POST request
 - Body-parser middleware are used to populate body data in req.body
 - req.body returns an object containing key-value pairs of data submitted in the request body 

Response (res) Object
 - Exctens the http.ServerResponse class
 - Provides additional methods to make it easy to generate various responses
 - res.send(\[body]): 
	 - Can send a response of various types 
	 - the parameter can be a Buffer object, a String, an object, Boolean, or an Array
- res.sendFile(path, \[options], \[file name])
	- send a file at a given path 
	- Unless root is set in the options object, path must be an absolute path to the file
		- res.sendFile('./views/index.html', {root: _\_dirname});
- res.json(\[body])
	- send a Json response
- res.render(view, \[locals], \[callback])
- res.redirect(\[status], path)
	- redirect a request to the URL derived from the specified path 
	- status defaults of 302, be can be changed
- res.status(code)


