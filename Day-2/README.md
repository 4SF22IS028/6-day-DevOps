 Day 2 – AWS Load Balancer Setup and PuTTY Usage
 What I Learned:
How to launch and connect to EC2 instances using PuTTY.

Created a target group and added EC2 instances to it.

Set up a load balancer to distribute traffic across multiple instances.

Explored security groups, ports, and how to expose services.

Verified setup using public IPs and tested the load balancer behavior.

 Commands Used in PuTTY & AWS Setup:
# Connect to EC2 using PuTTY (with .ppk file) <pre><code>Host: ec2-user@your-public-ip Port: 22 Auth: Use your .ppk private key</code></pre>
# Update package list <pre><code>sudo apt update </code></pre>
# Install Apache2 web server<pre><code> sudo apt install apache2 -y </code></pre>
# Start Apache service <pre><code>sudo systemctl start apache2 </code></pre>
# Enable Apache to run on boot <pre><code> sudo systemctl enable apache2 </code></pre>
# Check status of Apache <pre><code>sudo systemctl status apache2</code></pre>
# Change index page to identify instance <pre><code>echo "Instance 1 - Running" </code></pre>
<pre><code>sudo tee /var/www/html/index.html </code></pre>
⚙️ Load Balancer Configuration Steps:
1. Go to EC2 Dashboard > Load Balancers > Create Load Balancer 
2. Choose "Application Load Balancer"
3. Name: my-load-balancer
4. Scheme: internet-facing
5. Listeners: HTTP (port 80)
6. VPC and Subnets: Select at least 2 public subnets
7. Security Group: Allow HTTP (port 80)
8. Target Group: - Name: my-target-group - Protocol: HTTP - Port: 80 - Target Type: Instance
9. Register EC2 instances with the target group
10. Create the load balancer </code></pre>

 # Testing:
<pre><code># Open in browser: http://<load-balancer-dns-name> # Refresh to verify load balancing between instances </code></pre>

# Key Learnings:

On Day 2, I explored key concepts of AWS and web server deployment. I connected to EC2 instances using PuTTY, installed and configured Apache web server, and modified the default index page to identify individual instances.

I also learned how to set up a Load Balancer in AWS, create a Target Group, and register EC2 instances to distribute incoming traffic. Using the load balancer's DNS name, I successfully tested round-robin traffic between the instances. This helped me understand real-world deployment strategies and high availability architecture.

 Skills Gained: EC2 configuration, PuTTY SSH connection, Apache server management, Load Balancer setup, Target Group configuration, Web server testing via public IP and DNS.


