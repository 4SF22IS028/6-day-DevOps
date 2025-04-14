# DevOps Training Overview

# Cloud Computing & AWS EC2

We kicked off by diving into **Cloud Computing**, focusing on **AWS EC2**, and learning how to manage cloud infrastructure. 

# Key Highlights:
- **Cloud Service Models**: Explored **IaaS**, **PaaS**, and **SaaS**, with hands-on experience with **AWS** as an **IaaS** provider.
- **EC2 Instances**: Configured, launched, and managed **EC2 instances** on AWS.
- **Linux Families**: Worked with **Red Hat** and **Debian-based Linux** systems, installing and configuring **Apache HTTP** server.
- **AWS Credentials**: Learned to configure and securely manage **AWS credentials** for automation tasks.

# Key Commands:
<pre><code>
# Install Apache HTTP Server on EC2
yum install httpd -y

# Start the Apache server
service httpd start
</code></pre>

---

# Infrastructure as Code with Terraform

We delved deep into **Terraform** to automate cloud infrastructure provisioning, reducing manual intervention and ensuring consistency.

# Key Highlights:
- **Infrastructure as Code (IaC)**: Understood the concept of IaC and applied it with **Terraform** to manage AWS resources.
- **Terraform Commands**: Worked with **Terraform scripts** to create and manage resources like EC2 instances, VPCs, and more.
- **State Management**: Explored how Terraform tracks resources and maintains the state of infrastructure.

# Key Terraform Commands:
<pre><code>
# Initialize Terraform and set up cloud provider configuration
terraform init

# Validate configuration files
terraform validate

# View execution plan to check proposed changes
terraform plan

# Apply the configuration to create resources
terraform apply

# Destroy the resources created by Terraform
terraform destroy
</code></pre>

---

# Docker & Containerization

**Docker** was introduced to provide a platform for creating **portable applications**. We explored how containerization improves efficiency and resource usage.

### Key Highlights:
- **Docker Basics**: Learned how Docker allows applications to run in isolated containers, promoting **microservices architecture**.
- **Container Management**: Created, started, and managed Docker containers and images.
- **Microservices**: Moved from monolithic applications to a microservices approach, deploying each service independently.

# Key Docker Commands:
<pre><code>
# Install Docker on an EC2 instance
yum install docker -y

# Start Docker service
service docker start

# Create a container from the Ubuntu image
docker create ubuntu /bin/bash

# Run the container
docker run -it ubuntu /bin/bash

# List all containers
docker ps -a

# Start a specific container by ID
docker start <container_id>
</code></pre>

---

# Kubernetes for Container Orchestration

We explored **Kubernetes**, the powerful container orchestration platform that automates container management, scaling, and deployment in production.

# Key Highlights:
- **Kubernetes Basics**: Introduced to Kubernetes concepts like **pods**, **deployments**, and **services**.
- **Scaling and Managing Applications**: Used **kubectl** commands to deploy, scale, and manage containerized applications.
- **Cluster Management**: Managed Kubernetes clusters for high availability and reliability.

# Key Kubernetes Commands:
<pre><code>
# Deploy an application to Kubernetes
kubectl apply -f <deployment_yaml>

# Scale the number of replicas
kubectl scale deployment <deployment_name> --replicas=3

# Check the status of the pods
kubectl get pods

# Expose the application as a service
kubectl expose deployment <deployment_name> --type=LoadBalancer --port=8080
</code></pre>

---

# Web Application Deployment & Git Integration

Throughout the training, we also focused on **Git** for version control, automating deployment with **Terraform**, and using **Docker** to manage application containers.

# Key Highlights:
- **Git Integration**: Pushed code to remote repositories and automated workflows using Git and Terraform.
- **CI/CD Workflow**: Integrated deployment processes with **Terraform** and **Docker**, ensuring smooth and scalable applications.

# Key Git Commands:
<pre><code>
# Clone the repository from GitHub
git clone -b master https://github.com/prathikshhaa/Dimple-CapsuleProject.git

# Add remote origin to the repository
git remote add origin https://github.com/prathikshhaa/DevOps-terraform-script.git

# Push code to GitHub
git push --set-upstream origin master
</code></pre>

---

# Key Takeaways

By the end of the training, here are the core concepts I mastered:

1. **Cloud Infrastructure Management**: Leveraged AWS EC2 instances for cloud computing and resource management.
2. **Automation with Terraform**: Automated the creation and management of cloud resources using Terraform scripts.
3. **Containerization with Docker**: Gained hands-on experience in containerizing applications, enabling platform-independent deployments.
4. **Kubernetes Orchestration**: Learned how Kubernetes simplifies the deployment, scaling, and management of containerized applications.
5. **Version Control & CI/CD**: Integrated Git for version control and automated deployment pipelines with Terraform and Docker.

---

# Conclusion

This **DevOps training** equipped me with essential tools and practices for managing modern cloud-based infrastructure and deploying scalable applications. From **cloud computing** to **container orchestration**, I now have a solid foundation in the **DevOps lifecycle**, enabling me to streamline workflows, improve scalability, and enhance the efficiency of software deployment.