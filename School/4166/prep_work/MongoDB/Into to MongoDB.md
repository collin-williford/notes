 - Each data record is stored as a document 
 - A document is composed of field-and-value pairs
	 - {
	 - name: "sue", 
	 - age: 25, 
	 - status: "A"
	 - }
- Documents are stored in collections
	- Collections are analogous to tables in relational database
- A database contains a set of collections

BSON vs JSON 
 - Documents are viewed in JSON format
 - Documents are stored in BSON format
 - BSON is a binary representaiton of JSON 
	 - Faster to parse and lighter to store than JSON
	 - Supports more data types than JSON

\_id field
 - Every document has a unique \_id field, acting as the primary key 
 - The \_id field can be of any type other than array 
 - If the \_id field is not provided when a document is inserted, MongoDB automatically adds an \_id field with a unique ObjectId value
 - ObjectId values are 12 bytes in length
	 - 4-byte timestamp value
	 - 5-byte random value
	 - 3-byte increment counter

Mongo Shell
 - The mongo shell is an interactive JavaScript interface to MongoDB, which can be used to access MongoDB
 - The mongo shell is included as part of the MongoDB installation
 - To start mongo shell, type mongo in terminal window 