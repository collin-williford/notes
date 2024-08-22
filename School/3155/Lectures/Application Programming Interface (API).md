 - What is an API?
	 - it is not the database or evern the srever, it tsi the coe that governs teh access points for the server
	 - How does it work
		 - Your website sends JSON data to the api
		 - The api then sends JSON data back to your browser

Types of APIs
 - Public
 - Private
 - Partner API

Purposes of API
 - make life easier for developers
 - Control access to resources
 - used for communication between services

Uses Cases for APIs 
 - Database APIs
 - Operating System APIs 
 - Remote APIs
 - Web APIs

API Protocols
 - Remote Procedure Calls (RPC)
	 - It has a straight forward interaction between a client and a server. The client remotely calls a method in the server and the server executes the method
- Service Object Access Protocol (SOAP)
	- It enables XML messaging between system through HTTP
- Representation State Transfer Protocol (REST) 
	- Is seen as a more user-friendly alternative to SOAP, which many developers find challenging to use 
- GraphQL
	- Is initially created by Facebook for its internal use and it has a more efficient data loading due to increase mobile adoption


REST and RESTful API
 - REST is a set of architectural constrains,  not a protocol or a standard 
 - When a client request is made via a RESTful API, it transfers a representation of the state of the resource to the requester or endpoint 
 - In order for an API to be considered RESTful,  it has to conform to these criteria
	 - A client-server architecture managed through HTTP
	 - Stateless client-server communication, meaning no client information is stored between get requests and each request is serperate and unconnected
	 - Cacheable data that streamlines client-server interactions