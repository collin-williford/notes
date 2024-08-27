AWS shared responsibility model 
- Customer
	- Responsible for security In the cloud 
		- Customer Data 
		- Platform, applications, identity and access management 
		- Operating system, network and firewall configurations 
		- Client-side data encryption and data integrity, authentication 
		- Server-side encryption (file system and/or data)
		- Networking traffic protection (encryption, integrity, identity)
- AWS
	- Responsible for security of the cloud 
	- AWS foundation services 
		- Compute 
		- Storage
		- Database 
		- Networking
	- AWS Global Infrastructure 
		- Regions
		- Availability Zones 
		- Edge locations 

Security is a Well-Architected Framework pillar 
- Operational Excellence
- Security 
- Reliability 
- Performance Efficiency
- Cost Optimization 
- Sustainability 

Design pinciples for the security pillar 
- Implement a strong identity foundation 
	- Implement the principle of least privilege and enforce separation of duties with appropriate authroization for each interation with your AWS resources. 
	- Centralize identity managment, and aim to eliminate reliance on long-term, static credentials 
- Protect data in transit and at rest
	- Classify yor data into sensitivity levels, and use mechanisms, such as encryption, tokenization, and access control, where appropriate 
- Apply security at all layers 
	- Apply a defense-in-depth approach with multiple security controls, and apply it to all layers 
		- Ex: edge of network, virtual private cloud, load balancing, every instance and compute service, operating system, applicaiton and code
- Keep people away from data
	- use mechanisms and tools to reduce or eliminate the need for direct access or manual processing of data 
	- This reduces the risk of mishandling or modification and human error when handling sensitive data 
- Maintain traceability 
	- Monitor, alert, and audit actions and changes to your enviroment in real time
	- Integrate log and metric collection with systems to automatically investigate and take action 
- Prepare for security events 
	- Prepart for an incident by having management and investigation policies and processes that align to your organization requirements. 
	- Run incident response simulations, and use tools with automation to increase your speed for detection, investigation and recovery 
- Automate security best practices
	- Automated software-based security mechanisms improve your ability to securely scale more rapidly and cost-effectively 
	- Create secure architectures, which includes implementing controls that are defined and managed as code in version-controled templates 

User permissions to access resources

Principel of least privilege 
- Best practices
	- Grant only the permissions that are required to perform a task 
	- Start with a minimum set of permissions 
	- Grant additional permissions as necessary 
	- Revoke unnecessary permissions 

Use encryption 
- client <-- Protect data in transit by using a crypotgraphic protocol (TLS) -> AWS Cloud storage bucket 

Protecting data at rest with client-side encryption 
- Client encrypts data before it is sent 
- Encrypted data comes and goes from AWS Cloud storage bucket 
- Client retrieves encrypted data and decrypts it for use 

Protecting data at rest with server-side encryption 
- Client <-- Uncncrypted data --> AWS Cloud storage bucket 
- Server encrypts data when it is stored 
- Server decrypts data when it is requested 

Key takeaways:
- Security and compliance are shared responsibilities between AWS and customers
- The security pillar of the Well-Architected Framework provides design principles to architect secure solutions 
- The principle of least privilege is a key part of implementing a strong identity foundation 
- Another key security design principle is protecting data at rest and in transit. Encryption is one important mechanism for protecting data 