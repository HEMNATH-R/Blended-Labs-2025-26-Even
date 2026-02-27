# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: HEMNATH R
* **Register Number**: 212224240057

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

1. Created a VPC I went to the VPC dashboard in AWS and created a new VPC with the CIDR block 10.0.0.0/16. I gave it a meaningful name so I could easily identify it later.

2. Created a Public Subnet Inside the VPC, I created a new subnet with the CIDR block 10.0.1.0/24. I enabled the option to auto-assign public IPv4 addresses so that any instance launched in this subnet would automatically receive a public IP.

3. Created and Attached an Internet Gateway I created a new Internet Gateway and attached it to my VPC. This allows resources inside the VPC to communicate with the internet.

4. Configured Route Table I created a new route table and added a default route 0.0.0.0/0 pointing to the Internet Gateway. Then I associated this route table with the public subnet to allow internet access.

5. Created a Security Group I created a security group and added inbound rules to allow: SSH (Port 22) for remote access HTTP (Port 80) to allow web traffic.

6. Launched an EC2 Instance I launched a new EC2 instance using the Amazon Linux 2 AMI and selected the t2.micro instance type. I selected the public subnet, attached the security group I created, and selected my key pair for SSH access.

7. Configured the Web Server.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/aba5ecb0-d9d2-4382-9b1e-ddc2862798c7" />


---

### Screenshot 2: SSH Connection to Instance

<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/ec3d4859-14ca-4b2e-a4cd-d7fa06717532" />


---

### Screenshot 3: Instance Monitoring / Status

<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/2032fb4a-7c1f-497b-b481-f357f31b4dc9" />


---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
