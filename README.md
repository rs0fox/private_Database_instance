Established a Virtual Private Cloud (VPC) comprising two Public and two Private Subnets, each equipped with an Internet Gateway (IGW) and a VPC Gateway endpoint dedicated to S3 services.  
Initiated the creation of an S3 Bucket.  
Introduced three distinct environments: Development (Dev), Quality Assurance (QA), and Production (Prod). Dev and QA environments are situated in the Mumbai region, while Prod is deployed in North Virginia.  
Set up an RDS Instance Database within the private subnet, along with a tailored Subnet group, Option group, and Parameter group. 
Deployed an EC2 Instance within the Public subnet.  
Configured Security Group Inbound Rules to allow the EC2 Instance Database access via its dynamically assigned EC2 Private IP.
Configured Security Group Inbound Rules for the EC2 Instance to permit access only from specified IPs, managed through the main.tf file within each environment.
Created IAM Roles, IAM Instance Profile, and IAM Policy granting read and write permissions to the S3 bucket specific to each environment. 
Established separate backend.tf files for each environment, hosted within an S3 bucket.
