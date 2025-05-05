**Software design concepts** 
- Abstraction 
	- Considers the components, neglects implication details. Procedural and Data abstraction 
- Architecture 
	- overall structure or organization of software components, ways components interact, and structure of data used by components 
- Design Patterns 
	- Describe a design structure that solves a well-defined problem within a specific context 
- Separation of Concerns 
	- Any complex problem can be more easily handled if its subdivided into pieces 
- Modularity 
	- separates the "Separation of concerns" into modules 
- Information Hiding 
	- Designing of modules so that the algorithms and local data contained within them are inaccessible to other modules 
- Functional Indedependence 
	- Single-minded (high cohesion) components with aversion to execessive interaction with other components (low coupling)
- Stepwise Refinement 
	- Incremental elaboration of detail for all abstractions 
- Refactoring
	- A reorganization technique that simplifies the design without changing functionality 
- Design Classes
	- Provide design detail that will enable analysis classes to be implemented 

Quality attributes in design 
- Functionality 
- Usability (UX)
- Reliability 
- Performance 
- Supportability 

Why design is not coding 
- design is high-level abstraction 
- code is low-level abstraction 

Design Modules 
- Data Design Elements 
	- creates a model of data and/or information that is represented at a high level of abstraction 
- Architecture Elements 
	- Gives an overall view of the software (like the floorplan of a house)
- Interface elements 
	- Describes the externally observable behavior of a class 
- Component level elements 
	- describes the internal detail of each software component 
- Deployment-level elements 
	- Indicates how software functionality and sub-systems will be allocated within the physical computing environment 

Single word to describe the importance of computing?
- Quality 

**Software Architecure** 

Architectural Genres 
- Artifical intelligence 
- Device 
- Financial 
- Government 
- Legal 
- Military 
- Medical 

Architectural Styles 
- Data-Centered 
	- A datastore (file or database) resides at the center of this architecture and is accessed frequently by other components that update, add, delete or modify data within the store 
- Data-flow 
	- When input data are to be transformed through a series of computational or manipulative components into output data 
- Call-and-Return 
	- Main program/subprogram architectures 
		- A control hierarchy where a "main" program invokes several program components 
	- Remote procedure call architecture s
		- Components of a main program/subprogram architectures are distributed across multiple computers on a network 
- Object-oriented
	- The components of a system encapsulates data and the operations that must be applied to manipulate data 
- Layered 
	- A number of different layers are defined, each accomplishing operations that progressively become closer to the machine instruction set 

Architecture Description language 
- UML 
- A language used to describe the architecture of a software system 

Architecture Review 
- Means of assessing the ability of a software architect to meet the system's quality requirements and to identify any potential risks 
- Can reduce project costs by finding design problems early 
- Often makes use of experience-based review, prototype evaluation, scenario reviews and ckecklists

Method of conducting architecture review during a sprint?
- Reviewing the code emerging from the sprint 

**UI & UX**
Golden Rules 
- Place the user in control 
	- define interaction modes in a way that does not force a user into uncessary or undesired actions 
	- Allow user to be interruptible and undoable 
- Reduce users memory load 
	- reduce demand on short-term memory 
	- Establish meaningful defaults 
- Make the interface consistent 
	- Allow the user to put the current task into a meaningful context 
	- Maintain consistency across a complete product line 

Interface Consistency 
- all visual information is organized according to design rules that are maintained throughout all screen displays 
- input mechanisms are constrained to a limited set that is used consistently throughout the application 
- Mechanisms for navigation from task to task are consistently defined and implemented 

Usability Measures/Metrics
- Watch users interact with the system and answer the following questions
	- Is the system usable without continual help or instruction?
	- Do the rules of interaction help a knowledgeable user to work efficiently?
	- Do interaction mechanisms become more flexible as users become more knowledgeable?
	- Has the system been tuned to the physical and social environment in which it will be used 
	- Is the user aware of the state of the system? Does the user know where they are at all times?
	- Is the interface structured in a logical and consistent manner?
	- Are interaction mechanisms, lcons, and procedures consistent across the interface?
	- Does the interaction anticipate errors and help the user correct them?
	- Is the interface tolerant of errors that are made?
	- Is the interaction simple?

Common Issues present in the development of most user interfaces 
- System Response time 
- user help facilities 
- Error information handling 
- Command labeling 

UI & UX explained and idfferences
- User interface
	- UI design is design that is focused on the visual appearance of the software. That is how the software looks 
- User Experience 
	- UX design is design that is focused on how the user interacts with the software. This takes the usability, ease of use, and how the user actually interacts with the software into account. 

**Quality Concepts and Design Review Techniques** 
- "Costs of quality"
	- Prevention costs 
		- quality planning, fromal technical reviews 
	- Appraisal costs
		- conducting technical reviews, data collection and metrics evaluation, testing and debugging 
	- Internal failure costs
		- rework, repair, failure mode analysis 
	- External failure costs 
		- compliant resolution, produce return and replacement, help line support, warranty work 

How can reviews take place in agile 
- Informal review 
	- causal meeting for the purpose of reviewing a work product 
- Formal technical review 
	- prepare in advance 
	- meeting betwen 3-5 people 
	- focus is on a work product 

**Mobility & Pattern Based Design**
- Best practices in mobility design 
	- Identify your audience 
	- Design for context of use 
	- There is a fine line between simplicity and laziness
	- Use the platform as an advantage 
	- Make scrollbars and selection highlighting more salient 
	- Increase discoverability of advanced functionality 
	- Use clear and consistent labels 
	- Clever icons should never be developed at the expense of user understanding 
	- Support user expectations for personalization 
	- Long scrolling forms trump multiple screens on mobile devices 

Model-View-Controller
- decouples the user interface from the WebApp functionality and information content 
	- Model 
		- contains all application-specific content and processing logic, including all content objects, access to external design/information sources, and all processing functionality that is application speicific 
	- View
		- contains all interface-specific functions and enables the presentation of content and processing logic, including all content objects, access to external data and information sources, and all processing functionality required by the user 
	- Controller 
		- manages access to the model and the view and coordinates the flow of data between them 
	- "The view is updated by the controller when data from the model based on user input"

Design Pattern Common Mistakes 
- not enough time has been spent to understand the underlying problem and its content and forces you to select a pattern tha tlooks right but is inappropriate for the solution required 
- The problem has forces that are not considerd by the pattern you've chosen, resulting in poor or erroneous fit 
- A pattern is applied too literally and the required adaptinos for your problem space are not implemented 

**Security and Privacy**
- threat modeling 
	- an approach for creating an abstraction of a software system, aimed at identifying attackers' abilities and goals, and using that abstraction to generate and catalog possible threats that the system must mitigate 

OWASP top 10 
- Broken-access control 
- cryptographic failures 
- injection 
- insecure design 
- security misconfiguration 
- vulnerable and outdated components 
- indentification and authentication failures 
- Software and data integrity failures 
- security logging and monitoring failures 
- server-side request forgery 

Security coding practices 
- validate input 
	- validate input from all untrusted data sources 
- Heed compiler warnings 
	- Compile code using the highest warning level available for your compiler and eliminate warnings by modifying the code 
- Architect and design for security policies 
	- create a software architecture and desing your software to implement and enforce security policies 
- Keep it simple 
	- keep the design as simple and as small as possible 
- Default deny 
	- base access decisions on permission rather than execution 
- Least privilege 
	- Adhere to the principles of least privilege. Every process should execute within the least set of principles necessary to compute the job 
- Sanitize Data
	- Sanitize data sent to other systems. Sanitize all data passed to complex subsystems such as command shells, relational databases, and commerical off-the-shelf components 
- Practice Defense in Depth 
	- Manage risk with multiple defensive strategies 
- Use QA 
	- Use effective quality assurance techniques 
- Adopt 
	- Adopt a secure coding standard 

An Application's attack surface 
- The attack surface describes all the different points where an attacker could get into a system, and where they could get data out 
	- the sum of all paths for data/commands into and out of the application 
	- the code that protects these paths 
	- all valuable data used in the application, including secrets and keys, and intellectual property, critical business data, personal data and Personally identifable information 
	- The code that protects this data 

Privacy by Design 
- Proactive not Reactive; Preventative not Remedial 
- Privacy as the default
	- Purpose specification 
	- collection limitation 
	- Data minimization 
	- use, retention, and disclosure limitation 
- Privacy embedded into design 
- fully functionality 
- End-to-End security - lifecycle protection 
- Respect for user privacy 

Traceability 
- The ability to link and track relationships between various artifacts through the software development lifecycle, from requirements to design, code, tests, and ultimately deployment 

DevOps
- unify software development and It operations 
- goal is to shorten software development lifecycle

UML 
- Use case diagrams 
	- illustrates the interations betwen users (actors) and a system 
- Activity diagram 
	- display the order in which activities happened and whether they occur one after the other or at the same time 
