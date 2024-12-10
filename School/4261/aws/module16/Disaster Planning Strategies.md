Failures can occur at any scale
- Small-scale events
	- A server stops responding
- Large-scale events
	- Mulitple resources across an Availability Zone are unavailable 
- Global events
	- Failure is widespread and impacts a large number of users and systems

Avoiding and planning for disaster 
- Fault tolerance
	- Minimize how often your applications and data become unavailable 
- Backup 
	- Make sure you have a backup plan for handling data in case of a disaster 
- Disaster recovery 
	- Recover your data and get your applications back online after a disaster 

Factors that influence disaster planning strategies 
- Time dependency 
	- How quickly does this need to be remedied to avoid business impact?
- Data loss
	- What is the amount of data you are OK with losing?
	- What is the type of data you are OK with losing?
- Geographic location 
	- Does this impact multiple AWS Regions
	- Do different Regions require different measurements of how quickly you must recover and how much data loss is OK?
- Cost 
	- Does the cost represent the correct level considering business impact and risk?

Determining RPO
- RPO is the maximum acceptable amount of data loss, measured in time 

Example: Determining RPO 
- Determine that a loss of a maximum of 800 records is acceptable for your appliation 
- Use existing patterns to determine that no more than 100 records are created an hour 
- Calculate that an RPO of 8 hours is acceptable 

Preparing a BCP
- A business continuity plan (BCP) is a system of prevention and recovery from potential threats to a company
- A BCP consists of the following:
	- Business impact analysis 
	- Risk assessment 
	- Disaster recovery plan 
	- Evaluated and determined RPO and RTO

Key takeaways:
- Failures can occur at any time and on a small, large or global scale 
- A disaster recovery plan will help limit businesses and customer impact when a disaster occurs 
- RPO is the maximum acceptable amount of data loss after an unplanned data-loss incident 
- RTO is the amount of time an application system, and process can be down without causing significant damage to the business 
- A BCP is a system of prevention and recovery from potential threats to a company that includes RPO and RTO 

