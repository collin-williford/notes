 - Authorization is the process that checks if a user is permitted to access a resource or perform an action 
 - For example, Gmail only allows authenticated users to access their emails
 - Depending on the business logic, the authorization rules may vary from application to another 
 - Let's take the story telling app as an example to define a set of authorized rules 

Authorization Rules 1
 - Everyone can access
	 - Landing page
	 - Stories page
	 - Story Detail page
- No access control is needed for accessing these resources

Authorization Rules 2
 - Guests can access
	 - new account page
	 - login page
- Guests can 
	- Signup a new account
	- Login to the app
- If a users is a guest (not logged in), then the user can access these pages and perform these actions
- Otherwise, the user is redirected to the profile page

Authorization Rules 3
 - Authenticated users can access
	 - profile page
	 - new story page
- Authenticated users can 
	- create a new story 
	- logout
- If a user is logged in, then the user can access these pages and perform these actions
- Otherwise, the user is redirected to the login page

Authorization Rules 4
 - An authenticated user who creates a stoyr can access 
	 - The edit story page
- An authenticatd user who creates a story can 
	- edit the story 
	- delete the story 
- if a user is logged in and is the author of the story, then the user can access these pages and perform these actions
- Otherwise, the user is redirected to 
	- The login page if not logged in 
	- The erroe page if logged in but not the author of the story 