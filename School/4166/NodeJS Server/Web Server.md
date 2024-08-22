 - Interpret HTTP Requests
 - Retrieve requested resource from the backend
 - Create HTTP response and send it to the client, the response may include
![[Pasted image 20230917194711.png]]

NodeJS Server
 - To create a web server, we use the HTTP core module
	 - //require the module
	 - const http = require('http');
	 - .
	 - //create a server
	 - const server = http.createServer();
	 - .
	 - //register an event listener for incoming requests
	 - server.on('request', (req, res) => {
	 - // handel incoming requests
	 - });
	 - .
	 - //blind the server to a particular port number
	 - server.listen(port, host, ()=> {
	   //opertaion after successful binding
	   });

Parse HTTP Request
 - The parameter "req" of the callback function stores the HTTP request
	 - req.method
	 - req.url
	 - req.headers

Create HTTP Response
 - The parameter "res" of the callback function stores the HTTP response
	 - res.setHeader(name, value)
	 - res.writeHead(statusCode\[", statusMessage]\[,headers])
	 - res.statusCode
	 - res.write()
	 - res.end()