Software processes vs. Methodology
 - **Process** is a step by step structure, with milestones and stages while **Methodology** is a way of interacting with the stakeholders to move them from stage to stage
 - **Software Process:** is a model that describes and approach to the production and evolution of software
 - **Software Methodology:** Identifies how to perform activities for each period, how to represent the activities and products, and how to generate products
 - ![[Pasted image 20230906193042.png]]

Software Development Life Cycle 
Email Sender application
 - Requirements
	 - Collect email address and message
	 - Send and store in database
	 - Prevent user from bad input
- Design
	- Use HTML and CSS for building UI form
	- Python and MySQL for backend and database
	- Use JavaScript for input verification
- Implementation
	- Code and document the software 
- Verification
	- Does the form collect information?
	- Does it send and store the information?
	- Does the form prevent bad user input?
- Maintenance
	- Create lifecycle plan 
	- Fix bugs
	- New features


What is Requirements?
 - A process for finding out the goal of the system
 - Specify **WHAT** the customer want and, define **WHAT** the software system is required to do, **NOT HOW**.
  - Spending time strategically upfront, reduce cost and time later on 


Requirements vs Specification
 - Requirement - A non-technical definition of features that users expect from the system
 - Specification - A technical definition of what is required for building system. We aren't trying to design it, so KEEP IT SIMPLE


Functional vs Non-functional Requirements
 - Functional - A developer must implement these requirements so that users can achieve their goals with the product
	 - What should the program do?
		 - Send email when a new customer signs up
		 - Open a new account
- Non-Functional - Place constraints on what goals should be met in the product
	- Cover areas that don't directly effect the function of the program. They are typically constraints. These constraints might be implemented by the government (safety regulations), the company (quality regulations), or the client
		- Modifying data in the database should be updated within 2 seconds