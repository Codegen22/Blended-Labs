# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name:** Akshaay Vardhan S
* **Register Number**: 212224220007
* **Date of Submission**: 14-02-2026
---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

#### 1. Created a VPC I went to the VPC dashboard in AWS and created a new VPC with the CIDR block 10.0.0.0/16. I gave it a meaningful name so I could easily identify it later.
#### 2. Created a Public Subnet Inside the VPC, I created a new subnet with the CIDR block 10.0.1.0/24. I enabled the option to auto-assign public IPv4 addresses so that any instance launched       in this subnet would automatically receive a public IP.
#### 3. Created and Attached an Internet Gateway I created a new Internet Gateway and attached it to my VPC. This allows resources inside the VPC to communicate with the internet.
#### 4. Configured Route Table I created a new route table and added a default route 0.0.0.0/0 pointing to the Internet Gateway. Then I associated this route table with the public subnet to         allow internet access.
#### 5. Created a Security Group I created a security group and added inbound rules to allow:
    SSH (Port 22) for remote access
    HTTP (Port 80) to allow web traffic
#### 6. Launched an EC2 Instance I launched a new EC2 instance using the Amazon Linux 2 AMI and selected the t2.micro instance type. I selected the public subnet, attached the security group I      created, and selected my key pair for SSH access.
#### 7. Configured the Web Server


## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1920" height="1080" alt="Screenshot (181)" src="https://github.com/user-attachments/assets/c58a0824-c56c-4d47-9be2-3c3e7f12b8ca" />


### Screenshot 2: EC2 Instance Running


<img width="1920" height="1080" alt="Screenshot (193)" src="https://github.com/user-attachments/assets/08e35bb5-0b2e-4864-be17-abeb2c6c55d0" />

### Screenshot 3: Web Server Output in Browser

<img width="1920" height="1080" alt="Screenshot (196)" src="https://github.com/user-attachments/assets/f7f7336c-ad96-48cc-aba5-63e8bac31623" />


## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
