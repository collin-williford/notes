Controller Functions
 - A controller funciton is a callback function in the route
	 - app.get('/stories', (req, res) => {});
	 - This controller function 
		 - gets all stories from  the model 
		 - passes all stories to the template engine to generate a html page shows all stories
		 - returns the generated html page to the client 

Controller Module
 - A controller module includes all of the callback functions from the same route module
 - Controller function naming convention
	 - index: GET /stories
	 - new: GET /stories/new
	 - create: POST /stories
	 - show: GET /stories/:id
	 - edit: GET /stories/:id/edit
	 - update: PUT /stories/:id
	 - delete: DELETE /stories/:id
- The controller module exports all of the controller functions so that they can be used in the route module 
