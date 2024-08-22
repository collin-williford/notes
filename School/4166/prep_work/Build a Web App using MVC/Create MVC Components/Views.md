 - Views includes ejs templates and static html files
 - Created a view template for the landing page, still need view template for 
	 - showing a list of all stories
	 - showing details of a particular story 
	 - creating a new story 
	 - editing an existing story 
- All these view templates will have the same layout

Layout
 - Nav and footer are the same across these templates
 - The only difference is the content area
 - Instead of repeating the same code in each template, create shared components using partials 

Partials
 - A partial is a template file that can be included in other view templats
 - Partials are usually stored in the '/views/partials' folder
 - include partials in other views by calling 
	 - <%- include ('RELATIVE/PATH/TO/FILE')%>
- For Example:
	- <%- include ('./partials/header.ejs')%>

