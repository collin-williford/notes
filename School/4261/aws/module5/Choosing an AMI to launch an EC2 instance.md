Amazon Machine Image (AMI)
- An AMI provides the information that is needed to launch an instance, including the following
	- A template for the root volume: 
		- Contains the guest operating system and perhaps other installed software 
	- Launch permissions
		- Controls who can access the AMI 
	- Block device mappings
		- Specifies any storage volumes to attach to the instance 

AMI benefits 
- Repeatability 
	- An AMI can be used repeatedly to launch instances with efficiency and percision 
- Reusability 
	- Instances launched from the same AMI are identically configured 
- Recoverability 
	- You can create an AMI from a configured instance as a restorable backup
	- You can replace a failed instance by launching a new instance from the same AMI 

Choosing an AMI 
- Choose an AMI based on the following
	- Region 
	- Operating system 
	- Storeage type of the root device 
	- Architecture
	- Virtualization type
		- For best performance use an AMI with a Hardware Virtual Machine virtualization type 
- AMI source
	- Quick Start
		- Linux and Microsoft Windows AMIs that are provided by AWS
	- My AMIs
		- Any AMIs that you create
	- AWS Marketplace
		- Pre-configured templates from third parties 
	- Community AMIs 
		- AMIs shared by others. Use at your own risk 

Instance store-backed versus Amazon EBS-backend AMI 
- Characteristic 
	- Boot time for the instance
		- Amazon EBS-Backed Instance 
			- Boots faster
		- Instance Store-Backed Instance 
			- Takes longer to boot
	- Maximum size of root device
		- Amazon EBS-Backed Instance 
			- 16 TiB
		- Instance Store-Backed Instance 
			- 10 GiB
	- Ability to stop the instance
		- Amazon EBS-Backed Instance 
			- Can stop the instance 
		- Instance Store-Backed Instance 
			- Cannto be in a stopped state; instances are running or terminated
	- Ability to change the instance type 
		- Amazon EBS-Backed Instance 
			- Can change the instance type by stopping instance
		- Instance Store-Backed Instance 
			- Can't change the instance type because the instance can't be stopped
	- Instance charges
		- Amazon EBS-Backed Instance 
			- You are charged for instance usage, EBS volume usage, and storing your AMI as an EBS snapshot
		- Instance Store-Backed Instance 
			- You are charged for instance usage and storing your AMI in Amazon S3
	- Use case
		- Amazon EBS-Backed Instance 
			- Persistent storage
		- Instance Store-Backed Instance 
			- Temporary storage 

Amazon EC2 instance lifecycle 
- An Amazon EBS-backed instance becomes pending and then running. Running instances can be rebooted, terminated, or stopped. A stopped instance can be started or terminated

Creating a new AMI
- (Optional) Import a virtual machine 
- Quick Start or other existing AMI OR MyAMI
- Launch an instance
	- Unmodified instance 
- Connect to the instance and manually modify it or run a script that modifies the instance (ex. update software)
	- Modified instance
- Capture as a new AMI: 
	- Create a new image
		- new AMI
	- Create a bundle
		- New AMI 
- Optional: Copy the AMI to any other Regions where you want to use it 
	- New AMI 

EC2 Image Builder 
- EC2 Image builder automates the creation, management and deployment of up-to-date and compliant golden VM images
	- Provides a graphical interface to create image-building pipelines 
	- Creates and maintaines Amazon EC2 AMIs and on-premises VM images 
	- Produces secure, validated, and up-to-date images
	- Enforces version control 

Key takeaways 
- An AMI provides the information that's needed to launch and EC2 instance 
- Benefits of AMIs include repeatability, reusability and recoverability 
- For best performance, use an AMI with the HVM virtualization type 
- There are multiple sources to get AMIs including Quick Start, Community AMIs, AWS Marketplace, and My AMIs (That store AMIs that you created)

