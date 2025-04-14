# DevOps-Terraform Repository Link 

<pre><code>https://github.com/prathikshhaa/DevOps-Terraform.git</code></pre>

#  Day 3 – Terraform Learning Summary

#  Overview

Today was focused on learning Terraform, a powerful Infrastructure as Code (IaC) tool used to automate and manage cloud infrastructure efficiently.

#  What is Terraform?
Terraform is an open-source IaC tool created by HashiCorp. It allows you to define and provision infrastructure using a simple, declarative language called HCL (HashiCorp Configuration Language). Instead of manually configuring cloud resources, you describe them in .tf files and let Terraform handle the provisioning.

#  Key Concepts Learned

 🔹 Providers - Plugins that allow Terraform to interact with cloud platforms (e.g., AWS, Azure). 
 🔹 Resources - The actual infrastructure elements you want to create (like EC2, S3). 
 🔹 Variables - Used to parameterize values for flexibility and reusability. 
 🔹 Outputs - Print specific values after applying your code (e.g., public IP of a server). 
 🔹 State File - terraform.tfstate keeps track of infrastructure resources. 
 🔹 Modules - Reusable components that help you organize complex infrastructure setups. </code> </pre>
 
 Commands Practiced
#  Initialize the working directory (downloads provider plugins) 
<pre> <code> terraform init </code></pre>
#  Validates the syntax and configurations
<pre> <code> terraform validate</code></pre>
#  See what actions Terraform will take without making any changes
<pre> <code> terraform plan</code></pre>
#  Apply the configuration to create the actual infrastructure
<pre> <code> terraform apply</code></pre>
#  Destroy the infrastructure that was created
<pre> <code> terraform destroy </code> </pre>

#  Recommended Terraform Project Folder Structure

<pre> <code> terraform-project/ │ ├── main.tf # Main Terraform configuration file (resources go here) ├── variables.tf # All input variables are declared here ├── outputs.tf # Used to display outputs after terraform apply (e.g., public IP) ├── terraform.tfvars # Contains values for the variables (optional but useful) ├── provider.tf # Contains provider block (e.g., AWS, Azure) ├── versions.tf # Terraform & provider version constraints (optional but good practice) ├── backend.tf # (Optional) Remote backend config if using remote state like S3 │ ├── modules/ # Reusable Terraform modules (optional, for large projects) │ └── ec2/ # Example module for EC2 instance │ ├── main.tf │ ├── variables.tf │ └── outputs.tf │ ├── .terraform/ # Auto-generated directory for provider plugins (don't touch manually) ├── .terraform.lock.hcl # Locks provider versions used in this project └── terraform.tfstate # The state of your infrastructure (do not edit manually) </code> </pre>

#  Explanation of Important Files

# File/Folder	          Purpose
main.tf	              Where you define your resources (e.g., EC2, S3, VPC).
variables.tf	        Declares variables to keep your code flexible.
terraform.tfvars	    Assigns values to those variables (can be ignored from git).
outputs.tf	          Prints values like IP addresses or instance IDs after deployment.
provider.tf	          Specifies the cloud provider and region (e.g., AWS).
versions.tf	          Locks Terraform and provider versions to avoid breaking changes.
backend.tf	          If you use remote backends (like S3), configure it here.
modules/	            Reusable logic – good for teams and DRY (Don't Repeat Yourself).
.terraform/          	Auto-generated plugins and config – never edit manually.
terraform.tfstate   	Terraform tracks what’s been deployed using this file. Keep it safe!

# steps:
terraform init
terraform validate
terraform plan
terraform apply
terraform destroy will automatically delete all the resources created by terraform scripts

#  What I Understood
<pre> <code>  Terraform helps automate cloud provisioning.  It avoids manual clicks and human error.  Makes infrastructure reproducible and version-controlled.  Very powerful for DevOps practices and scalable projects.  The state file is crucial — don’t delete or ignore it.  Clean and modular code makes Terraform maintainable. </code> </pre>


