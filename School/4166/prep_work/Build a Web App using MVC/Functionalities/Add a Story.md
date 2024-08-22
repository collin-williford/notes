Route: GET /stories/new
 - View
	 - Add a new template including a form to create a new story 
 - Controller
		 - render teh view template

Route: POST /stories
 - Model
	 - Implement an interface to allow controller to add a new story in the array
- Controller
	- get the new story from the POST request, adds the new story in the array, and redirects to '/stories'