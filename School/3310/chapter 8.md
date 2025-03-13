Requirements Modeling 

Requirements Analysis 
- specifies software's operational characteristics
- Indicates software's interface with other system elements 
- establishes constrains that software must meet

Requirements analysis allows the software engineer to:
- elaborate on basic requirements established during earlier requirement engineering tasks 
- build models that depict the user's needs from several different perspectives 

Requirements Models (aka Analysis Model)
- Scenario-based models 
	- depict requirements from the point of view of various system "actors" 
- Class-oriented models 
	- represent object-oriented classes (attributes and operations) and how classes collaborate to achieve system requirements 
- Behavioral models 
	- depict how the software reacts to internal or external "events"
- Data models 
	- depict the information domain for the problem 
- Flow-oriented models 
	- represent functional elements of the system and how they transform data in the system 

Rules of Thumb
- The level of abstraction should be relatively high - focus on requirements visible in problem or business domains 
- Analysis model should provide insight into information domain, function, and behavior of the software 
- Delay consideration or infrastruction and other non-functional models until later in the modeling activity 
- The analysis model provides value to all stakeholders to keep the model as simple as it can be 

Requirements Modeling Principles 
1. The information domain of a problem must be represented and understood 
2. The functions that the software performs must be defined 
3. The behavior of the software (as a consequence of external events) must be represented 
4. The models that depict information, function, and bahavior must be partitioned in a manner that uncovers detail in a layered fashion
5. The analysis task should move from essential information toward implementation detail 

Information Domain 
- Inputs 
- Outputs 
- Storage 

Scenario-Based Modeling: Actors and Profiles 
- A UML actor models an entity that interacts with a system object
	- Actors may represent roles played by human stakeholders or external hardware as they interact with system objects by exchanging information 
- A UML profile provides a way of extending an existing model to other domains or platforms 
- This might allow you to revise the model of a Web-based system and model the system for various mobile platforms 
- Profiles might also be used to model the system from the viewpoints of different users 

Use Cases
- Use case is a "contract for behavior" and more formal that a user story 
- Use-cases are simply an aid to defining what exists outside the system (actors) and what should be performed by the system (use-cases) 
	- What should we write about?
	- How much should we write about it?
	- How detailed should we make our description?
	- How should we organize the description?

What to write about?
- The first two requirements engineering tasks - inception and elicitation - provide you with the information you'll need to begin writing use cases
- To begin developing a set of use cases, list the functions or activities performed by a specific actor
- You can obtain these from a list of required system functions, through conversations with stakeholders, or by an evaluation of activity diagrams developed as part of requiremets modeling 
- Use cases of this type are sometimes referred to as primary scenarios 

Alternative Interactions 
- Description of alternative interactions is essential to completely understand function described a use case
	- Can the actor take some other action at this point?
	- Is it possible that the actor will encounter some error condition at this point?
	- Is it possible that he actor will encounter some other behavior at this point (behavior that is invoked by some event outside the actor's control)?
- Answers to these questions result in the creation of a set of secondary scenarios represent alternative use cased behavior 

Defining Exceptions
- An exception describes a situation (either a failure condition or an alternative chosen by the actor) that causes the system to exhibit somewhat different behavior
- Questions to ask
	- Are these cases in which some "validation function" occurs during this use case?
	- Are there cases in which a supporint function (or actor) will fail to respond approprately?
	- Can poor system performance result in unexpected or impropor user actions?

Documenting Use Cases
- What are the main functions or tasks that are performed by the actor?
- What system information will the actor acquire, produce or change?
- Will the actor have to inform the system about changes in the external environment?
- What information does the actor desire from the system?
- Does the actor wish to be informed about unexpected changes?
- What are the preconditions, triggers, exceptions, and open issues?

Class-based modeling
- represents
	- **objects** that the system will manipulate
	- **operations** (also called methods or services) that will be applied to the objects to effect the manipulation
	- **relationships** (some hierarchical) between the objects
	- **collaborations** that occur between the classes that are defined 
- The elements of a class-based model include classes and objects, attributes, operations, CRC models, UML class diagrams 

Identifying Analysis Classes
- Examining the usage scenarios developed as part of the requirements model and perform a "grammatical parse"
	- classes are determined by underlining each noun or noun phrase and entering it into a simple table
	- Synonyms should be noted 
	- If the class (noun) is requried to implement a solution, then it is part of the solution space; otherwise, if a class is necessary only to describe a solution, it is part of the problem space 
- But what should we look for once all of the nouns have been isolated?

Potential Analysis Classes
- **External entities** (e.g., othe systems, devices, people) that produce or consume information 
- **Things** (e.g., reports, displays, letters, signals) that are part of the information domain for the problem 
- **Occurrences or events** that occur within the context of system operation
- **Roles** played by people who interact with the system 
- **Organizational units** that are relevant to an application 
- **Places** that establish the context of the problem and overall function 
- **Structures** (e.g., sensors, four-wheeled vehices, or computers) that define a class of objects or related classes of objects 

Analysis Class Selection 
- Retained Infomation 
	- Potential class will be useful during analysis only if information about it must be remembered
- Needed Services
	- Potential class must have a set of identifiable operations that can change the value of its attributes in some way 
- Multiple attributes 
	- Focus should be on "major" information; a class with a single attribute may be better represented as an attribute of another class
- Common attributes 
	- A set of attributes can be defined for the potential class and the attributes apply to all instanes of the class 
- Common operations 
	- A set of operations can be defined for the potential class and the operations apply to all instances of a class
- Essential requirements 
	- External entities that appear in the problem space and produce or consume information essential to the solution will usually be defined as analysis classes in the model 

Defining Attributes 
- **Attributes** describe a class that has been selected for inclusion in the analysis model.
	- It is the attributes that define the class - that clarify what is meant by the class in the context of hte problem space
	- To develop a meaningful set of attributes for an analysis class, you should study each use case and select those "things" that reasonably "belong" to the class
- What data items (composite and/or elementary) fully define this class in the context of the problem at hand?

Defining Operations
- Operations define the behavior of an object
	- Operations they can generally be divided into four broad categories:
		- Operations that manipulate data in some way
		- Operations that perform a computation 
		- Operations that inquire about the state 
		- Operations that monitor an object for the occurance of a controlling event 
- These functions are accomplished by operating on attributes and/or associations 
- Therefore, an operation must have "knowledge" of the class attributes and associations 

CRC Modeling 
- Class-reponsibility-collaborator (CRC) modeling provides a simple means for identifying and organizing the classes that are relevant to system or product requirements 
	- A CRC model is really a collection of standard index cards that represent classes
	- The cards are divided into three sections 
		- Along the top of the card you write the name of the class 
		- list the class responsibilities on the left
		- list the collaborators on the right 

CRC Model Review Process
- All stakeholders in the review (of the CRC model) are given a subset of the CRC model index cards. No reviewer should have two cards that collaborate 
- The review leader reads the use case deliberately. As the review leader comes to a named object, she passes a token to the person holding the corresponding class index card.
- When the token is passed, the holder of the class card is asked to describe the responbilities noted on the card. The group determines whether one of the responsibilities satisfies the use case requirement 
- If an error is found, modifications are made to the cards. This may include the definition of new classes (CRC index cards) or revising list of responsibilities or collaborations on existing cards 

Functional Modeling 
- The functional model addresses two application processing elements: 
	- user-observable functionality that is delivered by the app to end users 
	- operations contained within analysis classes that implement behaviors associated with the class 
- UML activity diagrams can be used to represent processing details 
- UML activity diagram supplements a use case by providing a graphical representation of the flow of interaction within a specific scenario 

Sequence Diagram 
- The UML sequence diagram can be used for behavioral modeling 
- Sequence diagrams can also be used to show how events cause transitions from object to object 
- Once events have been identified by examing a use case, the modeler creates a sequence diagram - a representation of how events cause flow from one object to another as a function of time 
- Sequence diagram is a shorthand version of a use case

Behavioral Modeling 
- A **behavioral model** indicates how software will respond to internal or external events or stimuli 
- This information is useful in the creation of an effective design for the system to be built 
- UML activity diagrams can be used to model how system elements respond to internal events 
- UML state diagrams can be used to model how system elements respond to external events 

Creating Behavioral Models 
- Evaluate 
	- Evaluate all use cases to fully understand the sequence of interaction within the system 
- Identify 
	- Identify elements that drive the interaction sequence and understand how these events relate to specific objects 
- Create 
	- Create a sequence diagram for each use case 
- Build 
	- Build a state diagram for the system 
- Review 
	- Review the behavioral model for accuracy and consistency 

Identifying Events 
- A use case represents a sequence of activities that involves actors and the system 
- An event occurs whenever the system and an actor exchange informaiton 
- An event is not the information that has been exchanged, but rather the fact that information has been exchanged 
- A use case needs to be examined for points of information exchange 
- Events are used to trigger state transitions 

Swimlane Diagrams 
- The UML swimlane diagram is a useful variation of the activity diagram that allows you to represent the activity diagram that allows you to represent the flow of activities described by the use case 
- Swimlane diagrams indicate which actor (if there are multiple actors involved in a specific use case) or analysis class has responsibility for the action described by an activity rectangle 
- Responsibilities are represented as parallel segments that devide the diagram vertically, like the lanes in a swimming pool 







