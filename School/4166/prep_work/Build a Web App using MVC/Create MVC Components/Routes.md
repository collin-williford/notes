Modularize Routes
 - As the applicaiton grows bigger, more routes are needed
 - In the story sharing web app, routes are needed for handling request for users, stories, etc
 - Instead of including all of the routes in the app.js file, a much better apporach is to modularize routes into modules
 - Each route module handles requests for a particula type of resource

Create a Route Module 
 - Use the Express router object to create route modules
	 - //require the Express module
	 - const express = require('express');
	 - .
	 - //create a router object
	 - const router = express.Router();
	 - .
	 - //create routes in the module
	 - router.get('/', (req, res) => {...});
	 - .
	 - //export the router object
	 - module.exports = router;

Use a Route Module
 - In app.js, require and mount the route module as a middleware on the app object
	 - //require the route module
	 - const router = require('router');
	 - .
	 - //mount the route module, which handels al requrest with the url prefix '/stories' 
	 - app.use('/stories', router);
- All requests with '/stories' prefix will be handled by routes defined in this router

RESTful Routes
 - REST stands for REpresentational State Transfer
 - It is a standard that are widels used for building web services
 - The RESTful route standards defines 7 routes to support basic CRUB operations performed on a resource: create, read, update and delete
 - Each RESTful route includes the HTTP method, the name of the resource and sometimes the id of a particular resource

RESTful Routes for Stories
 - RESTful routes defined in the route module of stories 
 - ![](Pasted%20image%2020231001172301.png)



