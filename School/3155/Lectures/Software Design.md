 - User requirements are derived from discussions with stakeholders, which are then refined into system requirements to define the system's functional and non-functional requirements
 - System software designs is a blueprint of the system that will be developed 

 - High Level Design 
	 - Includes the description of system architecture, database design, brief description on systems, services, platforms and relationship among modules
- Low Level Design 
	- Describes detailed description of each and every module means it includes actual logic for every system component and it goes deep into each modules specifications.

SOLID Principles 
 - S
	 - Single responsibility: A class should only have one job 
- O 
	- Open/Closed: Objects or entities should be open for extension but closed for modification.  The last thing you want to do it go back to it and change it again and again whenever you implement a new functionality 
- L
	- Liskov Substitution: Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program. That requires the objects of your child's class to behave in the same way as the objects of your parent's class
- I
	- Interface Segregation: Many client-specific interfaces are better than one general-purpose interface
	- Reduce the side effects and frequency of required changes by splitting the code into multiple/independent parts. 
- D
	- Dependency Inversion: Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions. 