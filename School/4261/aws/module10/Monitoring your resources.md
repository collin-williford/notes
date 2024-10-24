Monitoring distrubuted application components
- Operational health 
- Resouce utilization 
- Application performance 

CloudWatch 
- Collects and tracks metrics for AWS services across Regions in a metric repository 
- Collects logs by using Amazon CloudWatch Logs
- Supports built-in AWS service metrics or custom metrics 
- Calculates statistics from metrics or custom metrics 
- Provides alarms for responsive event-driven architectures
- Provides notifications to make changes to monitoried resources 

EventBridge 
- Processes events with an event bus or a pipe 
	- Pipes are point-to-point integrations between one source and one target 
	- Event buses are routers that receive events and optionally delivers them to one or multiple targets 
- Makes routing decisions with configurable rules 
	- Rules run based on matching an event pattern or on a shcedule with Amazon EventBridge Scheduler 
	- Targets can be in another AWS account, in another Region or in both 

Monitoring your resource costs 
- AWS Cost Explorer
- AWS Budgets
- AWS cost and Usage report 

Key Takeaways:
- CloudWatch alarms can send notifications to Amazon EC2 Auto Scaling and SNS topics 
- CloudWatch collects logs and metrics from AWS services across Regions 
- You can use CloudWatch dashboards to visualize metrics and alarms 
- EventBridge processes and routes event with an event bus or a pipe 
- AWS Cost Explorer, AWS Budgets, and AWS Cost and Usage Report can help you understand and manage the cost of your AWS infrastructure 

