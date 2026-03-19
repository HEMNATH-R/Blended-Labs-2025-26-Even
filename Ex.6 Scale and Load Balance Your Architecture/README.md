# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture
## Author

* **Name**: HEMNATH R
* **Register Number**: 212224240057

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

1. Launched a new EC2 instance named Web Server in the N. Virginia region using Amazon Linux 2023 AMI and t2.micro instance type.
2. Enabled termination protection and stop protection, configured a security group, and added a user data script to install and start an Apache web server.
3. Monitored the instance using status checks, CloudWatch metrics, and system logs to ensure it was running properly.
4. Modified the security group to allow HTTP (port 80) traffic and accessed the web server using the public IP address.
5. Resized the instance to t2.small, increased the EBS volume size, explored EC2 service quotas, tested stop protection, and finally stopped the instance.


## Output Screenshots 

<img width="1915" height="832" alt="image" src="https://github.com/user-attachments/assets/b75c887a-99be-480f-b4b0-4afb015d7ebc" />

<img width="1911" height="829" alt="image" src="https://github.com/user-attachments/assets/bf62a7ff-c492-4157-b7cd-5b72846deac8" />

<img width="1913" height="806" alt="image" src="https://github.com/user-attachments/assets/df931208-1458-455d-8ee8-59cb349edd99" />

<img width="1911" height="802" alt="image" src="https://github.com/user-attachments/assets/42637cd0-3353-411a-a704-ca1f23a6917c" />

---


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
