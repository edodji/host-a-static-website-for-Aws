# Static Website Hosting on AWS

## Project Overview
This project demonstrates how to host a static HTML web application on AWS, utilizing various AWS services to ensure high availability, security, and scalability. The reference architecture diagram and deployment scripts used in this project are available in the project's GitHub repository.

## Features Implemented

1. **Virtual Private Cloud (VPC) Configuration**  
   - Created a VPC with both public and private subnets across two different Availability Zones.

2. **Internet Gateway Deployment**  
   - Configured an Internet Gateway to facilitate connectivity between VPC instances and the wider Internet.

3. **Security Groups Setup**  
   - Established Security Groups to act as a network firewall mechanism.

4. **Multi-AZ Deployment**  
   - Leveraged two Availability Zones to enhance system reliability and fault tolerance.

5. **Public Subnets Utilization**  
   - Used Public Subnets for infrastructure components like the NAT Gateway and Application Load Balancer.

6. **EC2 Instance Connect Endpoint**  
   - Implemented secure connections to assets within both public and private subnets.

7. **Private Subnet Web Server Deployment**  
   - Positioned web servers (EC2 instances) within Private Subnets for enhanced security.

8. **Internet Access for Private Subnets**  
   - Enabled instances in both the private Application and Data subnets to access the Internet via the NAT Gateway.

9. **Website Hosting on EC2 Instances**  
   - Hosted the static website on EC2 instances.

10. **Application Load Balancer (ALB) Implementation**  
    - Deployed an ALB and target group to evenly distribute web traffic to an Auto Scaling Group of EC2 instances across multiple Availability Zones.

11. **Auto Scaling Group (ASG) Setup**  
    - Configured an Auto Scaling Group to automatically manage EC2 instances, ensuring website availability, scalability, fault tolerance, and elasticity.

12. **Version Control with GitHub**  
    - Stored web files on GitHub for version control and collaboration.

13. **Secure Communications**  
    - Secured application communications using AWS Certificate Manager (ACM).

14. **AWS Simple Notification Service (SNS)**  
    - Configured SNS to send alerts regarding activities within the Auto Scaling Group.

15. **Domain Name Registration and DNS Setup**  
    - Registered a domain name and configured a DNS record using Route 53.

## Repository Contents
- **Architecture Diagram**: A visual representation of the AWS infrastructure.
- **Deployment Scripts**: Scripts used to automate the deployment process.
- **Configuration Files**: Relevant configurations for security groups, VPC, and scaling policies.

## Deployment Steps
1. Clone the repository:
   ```sh
   git clone <repository_url>
   ```
2. Configure AWS credentials:
   ```sh
   aws configure
   ```
3. Deploy the infrastructure using Terraform/CloudFormation:
   ```sh
   terraform apply
   ```
4. Upload web files to EC2 instances.
5. Verify deployment by accessing the domain name via Route 53.

## Conclusion
This project successfully demonstrates hosting a static website on AWS while utilizing best practices for security, scalability, and availability. The infrastructure is fully automated and supports auto-scaling and load balancing, ensuring optimal performance and resilience.

