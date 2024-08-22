Integrate Database with Express App
 - Use a native driver for the database
	 - use the database's native query language
	 - better performance
 - Use a data mapper (ORM or ODM)
	 - adds an abstract layer
	 - represents the application data as objects
	 - write queries in the same language for your back-end code
- To integrate a MongoDB database, we can ues
	- MongoDB Node Driver
	- Mongoose ODM

MongoDB Node Driver
 - Provides an API to allow node applications to access MongoDB
 - Uses asynchronous API for communication between the application and the database
	 - Supports both callback and promises
	 - If a callback function is not passed, a promise will be returned

MongoDB Node Driver Classes
 - MongoClient class
	 - allows for maknig connections to MongoDB
- Db class
	- represents a MongoDB Database
- Collection class
	- embodies a MongoDB collection allowing for CRUD operations on that MongoDB collection

Use MongoDB Node Driver
 - Install mongodb package
 - Connect to MongoDB server
	 - MongoClient.connect(url)
- Select the database
	- client.db(database_name)
- Get a reference of the colleciton
	- db.collection(collection_name)
- Perform CRUD operations on the collection

CRUD Operations
 - A collection object can perform CRUD operations by calling
	 - find()
		 - find all matching documents in the collection 
	- findOne()
		- find the first matchign documents in the collection 
	- insertOne()
		- insert a doucment into the colleciotn 
	- insertMany()
		- Inserts an array of documents into the collecion 
	- updateOne()
		- update a single document in the collection 
	- updateMany()
		- UPdate multiple documents in the collection
	- deleteOne()
		- Delete a document from the collection
	- deleteMany()
		- delete multiple documents from the collection 
	- 