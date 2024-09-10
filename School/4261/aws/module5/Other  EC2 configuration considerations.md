EC2 instance user data
- When you launch an EC2 instance, you can specify user data to run an initialization script (shell script or cloud-init directive)

Retrieving instance metadata
- Instance metadata is information about your instance 
- It acessible from your instance at this url : \http://169.254.169.254/latest/meta-data/
- It can be retrieved from a user data script 

Working with user data on running instanches 
- First, you need to stop the instance 
- Next, you can navigate to the edit user data page to modify the user data 
- Then, you need to remove the config_scripts_user file
- Finally, you have two options to re-run user data script 
	- restart the instance. After the instance restarts, the user data will begin to run 
	- You can run the /var/lib/cloud/instance/scripts/part-001 command to re-run the user data scritp without 

Manually running commands best practice 
- Web server A
	- Originaly user data
- Manually run additional commands to configure instance 
	- user data is updated
- Web server A
	- New user data
- Copy user data 
- New Web server
	- Instance initialization is correct 

AMI deployment models
- Basic AMI 
	- Base AMIs 
	- AMIs configured with OS-only 
	- Fully configuratble and upgradeable 
	- Shorter build time 
	- Slower boot time  
- Silver AMI 
	- AWS Managed Services (AMS) provided mutable AMIs 
	- Configurations half baked into the AMI 
	- Some configurations need to be done manually or by user data scripts 
	- Provides a balance between boot speed and build time 
- Golden AMI 
	- Customized immutable AMIs 
	- Configurations fully baked into the AMIs
	- All instances using the same golden AMI behave the same 
	- SHorter boot times but increases build times 
	- Shorter lifespan of the AMI 

Placement groups 
- Placement groups give you control of where a group of interdependent instances run in an Availability Zone 
	- Placement Benefits 
		- Increase network performance between instances 
		- Reduce correlated or simultaneous failure
	- Placement limitations
		- An instance can be be launched in only one placement group at a time 
		- Instances with a tenancy of host can't be launched in a placement group 
	- Placement strategies 
		- Cluseter
		- Partition 
		- Spread 

Key takeaways
- user data lets you configure an EC2 instance when you launch it 
- Informaiton about a running instance can be accessed in the instance through an instance metadata URL 
- There are three main AMI deployment models
	- Basic AMIs 
	- Silver AMIs
	- Golden AMIs
- Placement groups give you control of where a group of interdependent instances run in an Availability Zone 