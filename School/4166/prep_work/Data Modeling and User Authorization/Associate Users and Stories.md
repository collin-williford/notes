Relationships between Users and Stories
 - A user may create multiple stories
 - A story has one author 
 - Embed user inside story is not a good choice as there will be data duplication
 - Embed story inside user is not a good choice as stories are not always viewed together with users
 - Reference stories inside user will result in a mutable array 
 - We will model this relationship by reference the user inside story documents 

Story Schema
 - If a field of a document stores the \_id of a document in another collection, then the field is defined with two properties
	 - type
		 - schema.Types.ObjectId
	- ref
		- model name
- Example
	- The story schema's author field stores the \_id of its author 
		- author: {type: Schema.Types.ObjectId, ref: 'User'},

Join Collections
 - MongoDB supports join operation to combine the fields of two documents from different collections
 - In Mongoose, call populate() method on a documnet automatically replaces a field in the documnet with document from other collection
 - Example
	 - story.findById(id).populate('author')
	 - story.findById(id).populate('author', 'firstName')