Validators
 - Validators are rules defined in schemas
 - Mongoose has several built-in validators
 - All SchemaTypes have the required validator
	 - The field must be provided if required is set to true
- Numbers have min and max validators
- Strings have the following validators
	- enum
		- specifies the set of allowed values for teh field
	- match
		- specifies a regular expression that the string must match
	- minLength
	- maxLength

Validation on Insert
 - By default, documents are validated before they are saved to the database
 - Before saving a document, the validate() method is called, which checks the validation rules
	 - if a validation rule is violated, save is aborted and the error is returned 
	 - otherwise, the document will be inserted in the database
- You can set a schema's validateBeforeSave to false to bypass validation

Validation on Update
 - Mongoose also supports validation for update operations
 - Update validators are off by default, and can be turned on by setting runValidators to true when calling update methods

