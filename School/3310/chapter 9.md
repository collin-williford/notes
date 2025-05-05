Design Concepts

Software Design 
- Encompasses the set of principles, concepts, and practices that lead to the devleopment 
- Design pinciples estabish and overriding philosophy that guides the designer as the work is performed 
- Design concepts must be understood before the mechanics of design practice are applied 
- Software design practices change continuously as new methods, better analysis, and broader understanding evolve 

Software Engineering Design 
- Data/Class design 
	- transforms analysis classes into implementaiton classes and design structures 
- Architectural Design 
	- Defines relationships among the major software structural elements 
- Interface design 
	- defines how software elements, hardware elements and end-users communicate 
- Component-level design 
	- Transforms structural elements into procedural descriptions of software components 

Design and Quality 
- The design must implement all of the explicit, requirements contained in the analysis model, and it must accommodate all of the implicit requirements desired by the customer 
- The design should be a readable, understandable guide for those who generate code and for those who test and subsequently support the software 
- The design should provide a complete picture of the software, addressing the data, functional, and behavioral domains from an implemenation perspective 

Quality Guidelines 
1. A design should exhibit an architecture 
	1. Created using recognizable architectural styles or patterns 
	2. Composed of well designed components
	3. implemented in an evolutionary fashion 
2. A design should be modular 
3. A design should contain distinct representations of data, architecture, interfaces, and componnents 
4. A design should lead to data structures that are drawn from recognizable data patterns 
5. A design should contain functionally independent components 
6. A design should lead to interfaces that reduce the complexity of connections between components and the external environment 
7. A design should be derived using a repeatable method that is driven by software requirements analysis 
8. A design should be represented using meaningful notation 

Quality Attributes 
- Functionality 
	- Capability (Size and Generality of Feature Set), Reusability (Compatibility, Interoperability, Portability), Security (Safety and Exploitability)
- Usability (UX) 
- Reliability 
- Performance 
- Supportability 

Common Design Characteristics 
- Each new software design methodology introduces unique heuristics and notions - yet they each contain:
	- A mechanism for the translating the requirements model into a design representation 
	- A notation for representing functional components and their interfaces
	- Heuristics for refinement and partitioning 
	- Guidelines for quality assessment

Design Componets 1
- Abstraction 
	- data (named collection of data describing data object), procedural (name sequence of instructions with specific and limited function)
- Architecture 
	- Overall structure or organization of software components, ways components interact, and structure of data used by components 
- Design Patterns 
	- Describe a design structure that solves a well-defined design problem within a specific context 
- Separation of concerns 
	- Any complex problem can be more easily handled if its subdivided into pieces 
- Modularity 
	- Compartmentalization of data and function 


Design Components 2
- Information Hiding 
	- Controlled interfaces which define and enforces access to component procedural detail and any local data structure used by the component 
- Functional independence 
	- single-minded (high cohesion) components with aversion ot excessive interaction with other components (low coupling)
- Stepwise Refinement 
	- Incremental elaboration of deail ofr all abstractions 
- Refactoring 
	- A reorganization technique that simplifies the design without changing functionality 
- Design Classes 
	- Provide design detail that will enable analysis classes to be implemented 

Desing Class Characteristics 
- Complete 
	- Includes all necessary attributes and methods and sufficient (contains only those methods needed to achieve class intent)
- Primitiveness 
	- each class method focuses on providing one service 
- High cohesion 
	- small, focused, single-minded classes 
- Low coupling 
	- class collaboration kept to minimum 

information Hiding 
- Reduces the likelihood of "side effects"
- Limits the global impact of local design decisions 
- Emphasizes communication through controlled interfaces 
- Discourages the use of global data 
- Leads to encapsulation, an attribute of high quality design 
- Results in higher quality software 

Architecture Properties 
- Structural properties 
	- This aspect of the architectural design representation defines the ocmponents of a system (modules, objects, filters) and the manner in components are packaged and interaact with one another 
- Extra-functional properties 
	- The architectural design description should address how the design architecture achieves requirements for performance, capacity reliability, security, adaptability, and other characteristics 
- Families of related systems 
	- The architectural design should draw upon repeatable patterns (building blocks) often encountered in the design of similar systems 

Design Patterns Template 
- Pattern name 
	- Describes the essence of the pattern in a short by expressive name 
- Intent 
	- describes the pattern and what it does 
- Also known as 
	- Lists any synonyms for the pattern 
- Motivation 
	- Provides an example of the problem
- Applicability 
	- notes specific design situations in which the patten is applicable 
- Structure 
	- describes the classes that are required to implement 
- Participants 
	- Describes the responsibilities of the classes that are required to to implement the pattern 
- Collaborations
	- Describes how the participants collaborate to carry out their responsibilities 
- Consequences 
	- Describes the "design forces" that affect the pattern and the potential trade-offs that must be considered when the pattern is implemented 
- Related Patterns 
	- Cross-references related design patterns 

Design Modeling Principles 1
1. Design should be traceable to the requirement model 
2. Always consider the architecture of the system to be built
3. Design of data is important as design of processing functions 
4. Interfaces (both internal and external) must be designed with care 
5. User interface design should be tuned to the needs of the end-user and stress ease of use 
6. Component-level design should be functionally independent 
7. Components should be lously coupled to each other than the environment
8. Design representations (models) should be easily understandable 
9. The design should be developed iteratively 
10. Creation of a design model does not preclude using an agile approach 

Data Design elements 
- Data Model - data objects and database architectures
	- Examines data objects independently of processing 
	- Focuses attention on the data domain 
	- Creates a model at the customer's level of abstraction 
	- Indicates how data objects relate to one another 
- Data object can be an external entity, a thing, an event, a place, a role, an organization unit or structure 
- Data objects contain a set of attributes that act as an quality, characteristic, or descriptor of the object 
- Data objects may be connected to one another in many different ways 

Architectural Design Elements 
- Architectural design for software - equivalent to the floor plan of a house 
- The architectural model is derived from three sources 
	- Information about the application domain for the software to be built 
	- Specific requirements model elements such as data flow analysis classes and their relationships (collaborations) for the problem at hand 
	- Availability of architectural patterns and styles 

Interface Design Elements 
- Interface is a set of operations that describes the externally observable behavior of a class and provides access to its public operations 
- Important elements 
	- User interface (UI)
	- External interfaces to other systems 
	- Internal interfaces between various design components 
- UI or User Experience (UX) is a major engineering action to ensure the creation on usable software products 
- Internal and external interfaces should incorporate both error checking and appropriate security features 

Component-Level Design Elements 
- Describes the internal detail of each software component 
- Defines 
	- Data structures for all local data objects 
	- Algorithm detail for all component processing functions 
	- Interface that allows access to all component operations 
- Modeled using UML component diagrams 

Deployent Design Elements 
- Indicates how software functionality and subsystem will be allocated within the physical computing environment 
- Modeled using UML deployment diagrams 
	- Descriptor form deployment diagrams - show the computing environment but does not indicate configuration details 
	- Instance form deployment diagrams - identify specific hardware configurations and are developed in the latter stages of design 

