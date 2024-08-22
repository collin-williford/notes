Route: GET /stories/:id/edit
 - View 
	 - Add a new template including a form for editing a story 
- Controller
	- Gets the story from the model and render the view template

Route: PUT /stories/:id
 - Model
	 - implement an interface to allow controller to edit the story with id 
- Controller
	- gets the updated information from the put request, updates the story in the array, and redirects to '/stories/:id'