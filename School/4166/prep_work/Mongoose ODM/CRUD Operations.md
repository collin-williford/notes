CRUD Operations Using Model
 - When a model is created with mongoose.model(), the model has an associated connection with the MongoDB server
 - A model can perform CRUD operations on documents in the corresponding collection

Insert Documents
 - There are two ways to insert new documents
	 - first construct a new document, then call save() method on the document
	 - call create() method on the model by passing in the JavaScript object(s)
		 - can insert multiple documents with one call

Query Documents
 - Mongoose model provides three static methods for querying documents
	 - find()
	 - findOne()
	 - findById()
		- Note that findById(id) is the same as findOne({\_id: id})

Update Documents
 - Mongoose model provides four static methods for updating documents
	 - findByIdAndUpdate()
		 - return documnet
	 - findOneAndUpdate()
		 - return document
	 - updateOne()
		 - no return
	 - updateMany()
		 - no return 

Delete Documents
 - Mongoose model provides four static methods for deleting documents
	 - findByIdAndDelete()
		 - return document
	 - findOneAndDelete()
		 - return doc
	 - deleteOne()
		 - no return
	 - deleteMany()
		 - no return 

 

