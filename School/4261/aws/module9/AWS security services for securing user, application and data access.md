AWS Services for Security, Identity and Compliance 
- Identity and Access management 
	- Securely manage identities, resources, and permissions at sale 
	- Ex
		- AWS Identity and Access Management (IAM)
		- AWS IAM Identity Center 
		- Amazon Cognito 
		- AWS Organizations 
- Detection and response 
	- Enhance security posture and streamline security operations across an entire AWS environment
	- Ex
		- AWS CloudTrail 
		- Amazon Detective 
		- Amazon Inspector 
		- AWS Security Hub
- Network and application protection 
	- Enforce fine-grained security policies at network control points across an organization 
	- Ex
		- AWS Network Firewall
		- AWS Shield 
		- AWS WAF
- Data protection 
	- Protect data, accounts, and workloads from unauthorized access 
	- Ex
		- AWS Key Management System (AWS KMS)
		- AWS Secrets Manager 
		- Amazon Macie 
- Compliance 
	- Get a comprehensive view of compliance status and continously monitor using automated checks based on AWS best practices and industry standards 
	- Ex
		- AWS Artifact 
		- AWS Audit Manager 

Examples: AWS security services for defense in depth 
- Defend your borders
	- AWS WAF and AWS Shield 
- Protect your data 
	- Amazon Macie 
- Detect and respond to threats 
	- Amazon Inspector 
	- Amazon Detective 
	- AWS Security Hub 

AWS WAF
- Description 
	- A web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to your protected web application resources 
- Features 
	- Use managed or custom rules 
	- Allow or block requests based on things like IP address, country of origin, or header values 
	- Use AWS Shield (included at no additional cost) to help minimize the impact of distributed denial of service attacks 
- Example use cases 
	- Block requests that are missing the HTTP User-Agent header
	- Detect and manage malicious account creation attempts on the application's sign-up page 

Amazon Macie 
- Description 
	- A data security service that discovers sensitive data stored in Amazon Simple Storage Service (Amazon S3) by using machine learning and pattern matching, provides visibility into data security risks, and enables automated protection against those risks 
- Features 
	- Perform automated sensitive data discovery 
	- Create and run sensitive data discovery jobs 
	- Use built-in or custom data identifiers 
	- Review, analyze and manage findings
- Example use case
	- Use Macie to identify sensitive data being migrated into Amazon S3. Notify an administrator to review the data and decie wheather to allow process to continue putting the objects into Amazon S3

Amazon Inspector 
- Description 
	- A vulnerability management service that continously scans your AWS workloads for software vulnerabilities and unintended network exposure
	- Discovers and scans running EC2 instances, container images in Amazon Elastic Container Registry (ECR), and AWS Lambda functions 
- Features 
	- Centrally manage your environment through a single account by using AWS Organizations
	- Access vulnerabilities accurately with the Amazon Inspector Risk score 
	- Identify high-impact findings with the Amazon Inspector dashboard
	- Publish findings to Amazon EventBridge to support integration with other services 
- Example use case
	- Scan EC2 Amazon Machine Images (AMIs) and generate Amazon Inspector finding reports to help ensure that your AMIs are scanned for known vulnerabilities and updated prior to deployment 

Amazon Detective 
- Description 
	- Helps analyze, investigate, and quickly identify the root cause of security findings or suspicious activities 
	- Automatically collects log data from AWS resources and uses machine learning, statisticaly analysis and graph theory to generate visualizations that support faster and more efficient security investigations
- Features 
	- View data organized into a pre-built graph model with security-related relationships. The model summarizes contextual and behavioral insights 
	- Quickly validate, compare, and correlate the data to reach conclusions 
	- Automatically ingest and process relevant data from all enabled accounts
- Example use case
	- Triage a potential issue by finding all activity related to a specific IAM entity 

AWS Security Hub 
- Description 
	- Collects security data across AWS accounts, AWS services, and supported third-party products 
	- Helps you analyze your security trends and identify the highest priority security issues 
- Features 
	- Supports multiple security standards including the AWS Foundational Security Best Practices (FSBP) and external compliance frameworks 
	- Receives findings from other AWS services including Amazon Macie and Amazon Inspector 
	- Uses automation rules to automatically update critical findings when a security check fails 
- Example use case
	- Better prioritize the response and remediation efforts of security teams by searching, correlating and aggregating diverse security findings by accounts and resources 

Using AWS Security Hub with AWS Trusted Advisor 
- It provides recommendations based on five categories of AWS best practices 
	- cost optimization 
	- security 
	- fault tolerance
	- service limits 
	- performance improvement 
- It evaluates your account to suggest improvement and optimizations for your resources 
- Access Trusted Advisor through the AWS Management Console, 
- After enabling Security Hub for your AWS account, view your security controls and findings in the Trusted Advicor console 

Key takeaways 
- AWS security services help you implement a defense in depth strategy to your AWS workloads 
- Security services examples include the following 
	- AWS WAF to monitor web requests
	- Amazon Macie to identify sensitive data in Amazon S3
	- Amazon Inspector to identify vulnerabilities on EC2 instances, containers, and AWS Lambda functions 
	- Amazon Detective to analyze, investigate and quickly identify the root cause of security findings or suspicious activities 
	- AWS Security Hub to automatically consiolidate findings and help you monitor your cloud security posture against best practic es
- AWS Trusted Advisor inspects your AWS environment and then makes recommendations when oppourtunities exist to help close security gaps. AWS Security Hub recommendations are included in Trusted Advisor 


