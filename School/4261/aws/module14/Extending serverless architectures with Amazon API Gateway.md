Benefits of APIs
- Standardize app communication 
	- Connect software apps written in different languages in standardized way 
	- Hide implementation complexity 
- Protect microservices 
	- Choose whether to require authorization 
	- Check request formats 
	- Throttle the number of requests
	- Restrict resource access
- Monetize APi and track statistics
	- Track client usage for biling purposes 
	- Supply usage statistics per client 

Amazon API Gateway
- Provides ability to create, publish, and maintain REST, HTTP, and WebSocket APIs
- Configurable traffic management, authorization, and resource access control 
- Provides access to AWS services and publicly accessible endpoints 
- Hosts multiple versions and stages of an application's API 
- Establishes client usage plans to monetize and control APIs
- Can cache common responses 

Choosing an API type
- REST API 
	- Collection of routes and methods 
	- For apps that require API managemtn features, such as usage plans, payload validation, private API endpoints, and resource policies 
	- Supports cross-origin resource sharing (CORS)
	- Stateless
- HTTP APIs
	- Collection of routes and methods 
	- For microservices 
	- Lower latency and lower cost than REST APIs 
	- Supports CORS 
	- Stateless
- WebSocket APIs
	- Collection of WebSocket routes 
	- For real-time applications 
	- Establishes a session between client and backend services 
	- API management features are validate payload schema and data transformations
	- Stateful 

Solution: Shopping cart microservice 
- Amazon API Gateway shopping website HTTP API <--> Lambda shopping cart function <--> Amazon DynamoDB shopping cart table 

Key takeaways:
- Amazon API Gateway provides the ability to create, publish and maintain application APIs
- It provides access to AWS services and publicly accessible endpoints 
- Use REST APIs when full API management and control are required 
- Use HTTP APIs when lower latency and lower cost than REST APIs are required 
- Use WebSocket APIs for real-time applications that require an active session 

