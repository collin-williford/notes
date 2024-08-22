MongoDB captures reslationship between data in two ways
 - Embed model
	 - Stores related data in a single document
		 - Pros
			 - retrieve all realted data with a single query 
			 - avoid expensive join operations
		- Cons
			- large documents. May exceed 16BM document size limit
			- may not fit for all query criteria
- Normalized model
	- reference the \_id of related data from a different collection
		- Pros
			- smaller documents
			- flexible queries
		- Cons
			- Multiple queries or join operations are needed to query all related data 

In MongoDB
 - An entity is modeled as a document
 - An attribute of an entity is modeled as a field of the document
- A relationship may exist between entities
	- one-to-one relationship
	- one-to-many relationship
	- many-to-many relationship

Model Relationships
 - MongoDB captures relationships between data with 
 - Embeded Model
	 - Stores related data in a single document
	 - Best performance
- Normalized Model
	- Store related data in a seperate documents, and reference the \_id field of one document in the other
	- provides flexibility for query 

One-to-One Relationship
 - Using embedded model for one-to-one relationship unless the document exceedes the maximum document size of 16 MB
 - Example
	 - Each theature has an address. The theater docment embeds its address as a subdocument

One-to-Many Relationship
 - Example
	 - each book as a publisher, and a publisher may publish many books
- Embed "one" inside "many" as a subdocument
- Embed "many" as an array of subdocuments in "one"
- Store \_id of "many" as an array inside "one"
- Store \_id of "one" inside "many"

Embed One Inside Many
 - Embedding the publisher as a subdocument in each book document 
 - Their will be duplicated data
 - Any change to a pubiisher requries updating all of their books

Embed Many Inside One
 - Embedding the books as an array of subdocuments in the publisher document 
 - Easy to find all documents published by a publisher
 - Not easy to find all books written by a particular author 
 - The document may exeed the maximum document size of 16 MB

Reference Many in One
 - Store books and publishers in seperate collections
 - Store the \_id of books as an array in the publisher document 

Reference One in Many
 - Store books and publisher in seperate collections
 - Store the \_id of publisher in the book document 

Summary 
 - Use embedded model for 
	 - one-to-one relationship
	 - One-to-many relationships when 
		 - The "many" documents always appear with or are viewed in the context of "one" document
		 - And embedding "many" as an array of subdocuments in "one" does not exceed the maximum document size 
- Use the reference model
	- flexible query is needed
	- The embeded documents are unbounded in a one-to-many relationship
	- many-to-many relationship
