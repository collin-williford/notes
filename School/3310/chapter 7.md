Understanding Requirements

Requirements Engineering 
- Inception 
	- Establish a basic understandin of the problem, the people who want a solution and the nature of hte solution that is desired, important to establish effective customer and developer communication 
- Elicitation 
	- Elicit requirements and busines goals from all stakeholders
- Elaboration 
	- focuses on developing a refined requirements model that identifies aspects of software function, behavior, and informaiton 
- Negotiation 
	- agree on the scope of a deliverable system that is realistic for developers and customers
- Specification 
	- can be any or all of the following: written documents, graphical models, mathematical models, usage scenarios, prototypes 
- Validation 
	- Requirements engineering work products produced during requirements engineering are assessed for quality and consistency 
- Requirements management
	- set of traceability activities to help the project team identify, control, and track requirements and their changes to requirements as the project proceeds

Non-functional Requirements 
- quality attribute, performance attribute, security attribute, or general system constraint 
- A two-phase process is used to determine which NFR's are compatible:
	- the first phase is to create a matrix using each NFR as a column heading and the system SE guidelines a row labels 
	- The second phase is for the team to prioritize each NFR using a set of decision rules to decide which to implement by classifying each NFR and guideline pair as complementary, overlapping, conflicting, or independent
- Cheatsheet on Non-functional requirements
	- Functional vs. Non-functional requirements
		- Functional 
			- Allow a user to process a credit card payment 
		- non-functional 
			- Each payment transaction is processed within a 2 second response time 
			- Handle a load of 1000 concurrent users 
			- Credit card data must be encrypted 
			- Payment flow should be intuitive and adhere to accessiblity standards
	- Trade-off examples 
		- Encryption improves data security but since its a CPU-intensive process, there can be an impact on performance 
		- Achieving ultra-low latency costs often cost more in terms of resource utilization 
		- Developers can improve performance with low-level tweaks and specialized code but it can reduce maintability 

Establishing the Groundwork
- Identify stakeholders
- Recognize multiple points of view 
- Work towards collaboration 
- The first questions 
	- who is behind the request for this work?
	- who will use this solution 
	- what will be the economic benefit of a sucessful solution 
	- is there another source for the solution that you need?

Collaborative Requirements Gathering 
- Meetings are conducted and attended by both software engineering and other stakeholders
- Rules for preparaition and participation are established 
- Agenda is suggested that is formal enough to cover all important but informal enough to encourage the free flow of ideas 
- A "facilitator" (customer, developer or outsider) controls the meeting 
- A "definition mechanism" (worksheets, flip charts, wall stickers or virtual forum) is used
- Goal is to identify the problem, propose solution elements, and negotiate different approaches 

Elicitation Work Products
- Statement of need and feasibility 
- Bounded statement of scope for the system or product
- List of cusomters, users, and other stakeholders who participated in requirements elicitation 
- Description of the system's technical environment
- List of requirements and the domain constraints that apply to each 
- Set of usage scenarios (written in stakeholder's own words) that provide insight into the use of the system or product under different operating conditions 

Use Case Definition 
- A collection of user scenarios that describe the thread of usage of a system 
- Each scenario is described from the point-of-view of an "actor" - a person or devide that interacts with the software in some way 

Analysis Model Elements 
- Analysis model provides a description of the required informational, functional, and behavioral domains for a computer-based system 
- Scenario-based elements 
	- functional descriptions are expressed in the customers own words and user stories and as interactions of actors with the system expressed using UML use case diagrams 
		- Class-based elements 
			- collections of attributes and behaviors implied by the user stories and expressed using UML class diagrams (infomation domain)
		- Behavioral elements
			- may be expressed using UML state diagrams as inputs causing state changes 

Negotiating Requirements
- Negotiations strive for a "win-win" result, stakeholders win by getting a product satisfying most their needs and developers win by getting achievable deadlines
- Handshaking is one-way to achieve "win-win"
	- Developers propose solutions to requirements, describe their impact, and communicate their intentions to the customers 
	- Customer review the proposed solutions, focusing on missing features and seeking clarification of novel requirements
	- Requirements are determined to be good enough if the customers accept the proposed solutions 
- Handshaking tends to improve identification, analysis and selection of variants 

Requirements Monitoring 
- Useful for incremental development includes:
	- Distributed debugging - uncovers errors and determines their cause 
	- Run-time verification - determines wheather software matches its specification 
	- Run-time validation - assesses wheather the evolving software meets user goals 
	- Business activity monitoring - evaluates whether a system satisfies business goals 
	- Evolution and codesign - provides information to stakeholders as the system evolves 

Validating Requirements 
- Is each requirement consistent with the overall objective for the system/product?
- Have all requirements been specified at the proper level of abstraction? That is, do some requirements provide a level of technical detail that is inappropriate at this stage?
- Is this requirement really necessary or does it represent an add-on feature that may not be essential to the objective of the system?
- Is each requirement bounded and unambiguous?
- Does each requirement have attribution? That is, is a source (generally a specific individual) noted for each requirement?
- Do any requirements conflict with other requirements?
- Is each requirement achievable in the technical environment that will house the system or product?
- Is each requirement testable, once implemeted?
- Does the requirements model properly reflect the information, function and behavior of system to be built?
- Has the requirements model been "partitioned" in a way that exposes progressively more detailed information about the system?
- Have requirements patterns been used to simplify the requirements model. Have all patterns been properly validated? Are all patterns consistent with customer requirements?