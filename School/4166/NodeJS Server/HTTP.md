 - HTTP Overview
	 - Web client and server communicates over the HTTP protocol 
	 - Client initiates the communication by sending an HTTP request message 
	 - Server responds with an HTTP response message

HTTP Request 
 - Request Line
	 - Method 
		 - Tells server what operation needs to be preformed 
	 - URL
		 - Target resource
	- Version of protocol being used
- Header Fields 
	- Fields 
		- field name 
		- field value 
- Not all HTTP requests contain a body
![[Pasted image 20230917193720.png]]

HTTP Request Method
 - GET
	 - Request a representation of the specified resource
- POST
	- Submits an entity to the specified resource
- PUT
	- Replaces all current representation of the target resource with the request payload
- DELETE
	- Deletes the specified resource

HTTP Response 
 - Status Line
	 - Version 
		 - protocol 
	- Status code
		- written by machine 
	- Status phrase
		- written by human 
- Header Fields
	- can tell that is included 
- Blank Line
- Body 
	- Payload of response 
	- HTML page that is being sent to client 
![[Pasted image 20230917194043.png]]

HTTP Status Code
 - 200 OK
	 - successful operation
	 - GET
- 201 Created 
	- used to tell client the requested data has been created on server 
	- PUT/POST
- 301 Moved Permanently 
	- URL changing 
	- Redirection 
- 400 Errors
	- Client Errors
		- 400 Bad Request
		- 401 Unauthorized
		- 403 Forbidden
		- 404 Not found 
- 500 Internal Server Error
	- Server Errors