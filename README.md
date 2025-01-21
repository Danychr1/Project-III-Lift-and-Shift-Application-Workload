# Project-III-Lift-and-Shift-Application-Workload
# About the Project
This project demonstrates how to host and run a multi-tier web application stack on AWS Cloud using a Lift-and-Shift Strategy. It explores the process of migrating application workloads from on-premises environments to AWS Cloud while maintaining operational continuity.

# Scenario
  * Current Setup: Application services are hosted on physical or virtual machines in a datacenter.
  * Teams Involved: 
       *1 Virtualization Team, 
       *2 Data Center Operations, 
       *3 Monitoring Team, 
       *4 System Administrators.
Challenges:
Complex infrastructure management.
Difficulty scaling resources up or down.
High upfront capital expenditures (CapEx) and ongoing operational costs (OpEx).
Manual processes prone to human error and inefficiency.
Time-consuming maintenance and operations.
Solution: Cloud Computing
By migrating to AWS, the following benefits are achieved:

Pay-as-you-go model: Reduced costs with no upfront investment.
Infrastructure as a Service (IaaS): Flexible, scalable infrastructure.
Automation: Eliminate manual processes to save time and reduce errors.
Simplified Management: Easy infrastructure management with AWS tools and services.
AWS Services Used
Compute:
EC2 Instances for application servers (e.g., Tomcat, RabbitMQ, Memcached, MySQL).
Auto Scaling for cost-effective resource scaling.
Networking:
Elastic Load Balancer (ELB) – Replacing NGINX for load balancing.
Route 53 – Private DNS service.
Storage:
Amazon S3 / Elastic File System (EFS) for shared storage.
Elastic Block Store (EBS) for persistent VM storage.
Security and Management:
AWS Identity and Access Management (IAM).
Amazon Certificate Manager (ACM) for SSL/TLS.
Project Objectives
Build a flexible, scalable infrastructure.
Minimize costs with a pay-as-you-go model.
Modernize application deployment using AWS services.
Implement Infrastructure as Code (IaC) for efficient management and automation.
AWS Architecture Overview
EC2 Instances (application and backend services).
Elastic Load Balancer (ELB) for traffic distribution.
Auto Scaling Group for dynamic instance scaling.
S3/EFS for shared storage.
Route 53 for DNS management.
ACM for SSL/TLS certificates.
Execution Flow
Setup AWS Environment:

Login to AWS account.
Create key pairs and security groups.
Provision Resources:

Deploy Tomcat (Apache) servers.
Configure Elastic Load Balancer (ELB).
Set up backend services.
Launch EC2 instances with user data (Bash scripts).
Networking and DNS Configuration:

Update IP-to-name mapping in Route 53.
Map the ELB endpoint to the website name in GoDaddy DNS (or preferred DNS provider).
Application Deployment:

Build the application from source code.
Upload artifacts to an S3 bucket.
Download artifacts to Tomcat EC2 instances.
Testing and Verification:

Verify deployment functionality and connectivity.
Scaling and Automation:

Configure auto-scaling for Tomcat instances to optimize costs and performance.
This project demonstrates the practical application of AWS services to modernize and streamline web application hosting and management, showcasing scalability, cost optimization, and automation through cloud infrastructure.
