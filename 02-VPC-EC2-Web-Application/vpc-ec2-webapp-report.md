# Lab Report: VPC, EC2, and Web Application Deployment

## Overview
This lab provided hands-on experience with AWS networking and compute services by deploying a web application inside a pre-configured Amazon Virtual Private Cloud (VPC). The focus was on understanding how networking components work together to allow internet-facing applications to run securely on EC2 instances.

## Objectives
- Understand the structure and configuration of an Amazon VPC
- Validate public subnet, internet gateway, and routing configuration
- Review and understand security group rules
- Launch an EC2 instance in a public subnet
- Use a user data script to automatically configure and start a web application

## Environment Summary
The lab environment included a pre-created VPC with a defined IPv4 address range. A public subnet was available within the VPC, along with an attached internet gateway and a route table that allowed outbound internet access.

A security group was already associated with the environment to control inbound and outbound traffic for a web-facing EC2 instance.

## Work Performed

### 1. VPC and Network Review
I began by examining the VPC configuration to understand its address range, DNS settings, and overall structure. I reviewed the public subnet and confirmed that it was associated with a route table that allowed traffic to flow both locally within the VPC and externally through an internet gateway.

This step helped reinforce how public subnets rely on route tables and gateways to enable internet connectivity.

### 2. Security Group Analysis
Next, I reviewed the security group used for the web application. The inbound rules allowed HTTP and HTTPS traffic, enabling users to access the application through a browser. The outbound rules allowed necessary traffic such as DNS resolution and communication with AWS services.

This demonstrated how security groups act as stateful firewalls that control traffic at the instance level.

### 3. EC2 Instance Deployment
I launched an EC2 instance using a Linux-based Amazon Machine Image and selected an instance type suitable for lightweight workloads. The instance was placed in the public subnet and assigned a public IP address to allow browser access.

An existing IAM instance profile was attached to allow the instance to securely access required AWS resources without embedding credentials.

### 4. Application Bootstrapping with User Data
Instead of manually configuring the instance after launch, I provided a user data script that automatically installed required dependencies, retrieved application assets from storage, and started the web application.

This highlighted the importance of automation and how EC2 user data can be used to achieve consistent and repeatable deployments.

### 5. Validation
Once the instance reached a running state and passed health checks, I accessed the application using the public IP address over HTTP. Successful access confirmed that the network configuration, security rules, and application setup were functioning as intended.

## Key Learnings
- Public subnets require an internet gateway and proper routing to enable internet access
- Security groups define both inbound and outbound traffic rules and are critical for application security
- EC2 user data enables automated configuration without manual intervention
- IAM roles are the preferred way for EC2 instances to access AWS services securely
- Networking, security, and compute services must work together for successful deployments

## Conclusion
This lab strengthened my understanding of AWS networking fundamentals and demonstrated how real-world web applications are deployed using EC2 within a VPC. It reinforced the importance of proper network design, security controls, and automation when building cloud-based solutions.
