Challenges with microservice applications 
- Dependencies 
	- Handling microservice dependencies 
	- Chaining microservices sequentially or in parallel 
- Error Scenarios 
	- Handling retries after a timeout or error 
- Microservice coordination 
	- Scaling an application 
	- Maintaining state for stateless microservices 
	- Passing data between microservices 
	- Monitoring and troubleshooting



AWS Step Functions 
- Is a serverless orchestration service to manage workflows between multiple AWS services
- Has state machines (workflows) that contain a series of event-driven states (steps)
- Manages each workflow's state, checkpoints, and restarts 
- Provides error handling capability 
- Can transfer data between states 
- States can filter and manipulate data 

Step Functions use cases
- Microservice orchestrations 
- Data processing 
- Machine Learning 
- Security Automation 

State Machine state (step) types 
- Work states 
	- Task: Integrates with AWS services 
	- Activity: Performs a task hosted anywhere
	- Pass: Passes or filters input data to next state 
	- Wait: Delays workflow for a specified time 
	- State has wait for callback state option: Pauses workflow and waits for callback 
- Transition states
	- Choice: Adds conditions to control flow to next state
	- Parallel: Adds branches of nested state machines inside a state machine 
	- Map: Separates workflow for each data record in data set that runs in parallel 
- Stops States 
	- Success: Stops state machine and marks execution as successful 
	- Fail: Stops state machine and marks execution as failed 
	- State has the end parameter: Stops state machine 

Key takeaways:
- AWS Step Functions is a serverless orchestration service to manage workflows between mulitple AWS services 
- A state machine (workflow) is a series of event-driven states (steps)
- A Step Functions state machine is a collection of states defined in the Amazon States Language 
- States can be grouped into work, transition, and stop states 
- A task state can invoke an AWS service or request an activity hosted on any compute service with an HTTP connection 

