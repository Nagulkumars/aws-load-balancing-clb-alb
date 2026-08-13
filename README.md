# AWS Load Balancing with Classic and Application Load Balancer

## Project Overview

This project demonstrates hands-on AWS load balancing using **Classic Load Balancer (CLB)** and **Application Load Balancer (ALB)** with Amazon EC2 instances deployed across multiple Availability Zones in the AWS Ireland region.

- **Region:** Ireland (`eu-west-1`)
- **Load Balancers:** Classic Load Balancer and Application Load Balancer
- **Compute:** Amazon EC2
- **Availability:** Three Availability Zones
- **Deployment:** Launch Template and AMI
- **ALB Routing:** Target Group
- **Verification:** Multiple backend server responses

The project covers load balancer creation, multi-AZ EC2 deployment, Launch Templates, AMIs, Target Groups, and verifying traffic distribution across backend servers.

---

## Architecture

```text
                         AWS Ireland (eu-west-1)
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
          Classic Load Balancer       Application Load Balancer
                    │                           │
          ┌─────────┼─────────┐                │
          ↓         ↓         ↓                ↓
        AZ-1      AZ-2      AZ-3         Target Group
          │         │         │                │
         EC2       EC2       EC2              │
          │         │         │                │
          └─────────┴─────────┴────────────────┘
                         ↑
                  Launch Template
                         ↑
                        AMI
```

---

## AWS Services and Technologies Used

- Amazon EC2
- Classic Load Balancer
- Application Load Balancer
- Target Groups
- Launch Templates
- Amazon Machine Images (AMI)
- Availability Zones
- AWS Ireland Region
- Linux / Apache Web Server

---

# Project Implementation

### 1. EC2 Instance Deployment

Created and configured EC2 instances to act as backend web servers for load balancing.

### 2. Multi-AZ Deployment

Deployed the EC2 infrastructure across **three Availability Zones** in the AWS Ireland region to understand highly available application deployment.

### 3. Launch Template and AMI

Used an **AMI as the base image** and a **Launch Template** to maintain consistent EC2 instance configuration across the deployment.

### 4. Classic Load Balancer

Created and configured a **Classic Load Balancer** to distribute incoming application traffic across the EC2 backend instances.

### 5. Application Load Balancer

Created an **Application Load Balancer** for HTTP-based application traffic distribution.

### 6. ALB Target Group

Created a **Target Group** and configured the EC2 instances as targets for the Application Load Balancer.

### 7. Server Response Verification

Accessed the load-balanced application and verified responses from different backend EC2 servers.

### 8. Load Balancing Verification

Verified that requests could reach different backend servers through the configured load balancers.

---

# Screenshots

All screenshots are included in the order of the project workflow.

## Classic Load Balancer

### CLB Creation

`CLB Creation.jpeg`

Shows the creation of the Classic Load Balancer.

---

## Application Load Balancer

### ALB Creation

`ALB Creation.jpeg`

Shows the creation of the Application Load Balancer.

### ALB Target Group

`ALB - Target Group.jpeg`

Shows the Target Group configured for the Application Load Balancer.

---

## Server Response Verification

The load-balanced application was tested by accessing the application and verifying successful responses from the backend servers.

### 1st Server Response

`1st Server Response.jpeg`

Shows the response from the first backend server.

### 2nd Server Response

`2nd Server Response.jpeg`

Shows the response from the second backend server.

### 3rd Server Response

`3rd Server Response.jpeg`

Shows the response from the third backend server.

---

# Key Learning Outcomes

Through this project, I gained practical experience with:

- AWS load balancing
- Classic Load Balancer
- Application Load Balancer
- Target Groups
- EC2 deployment across multiple Availability Zones
- Launch Templates
- Amazon Machine Images (AMI)
- Backend server configuration
- HTTP traffic distribution
- Load balancer testing and verification
- High availability concepts
- Basic troubleshooting of load-balanced applications

---

# Skills Demonstrated

**AWS:** EC2, Classic Load Balancer, Application Load Balancer, Target Groups, Launch Templates, AMI

**Networking:** Load balancing, traffic distribution, Availability Zones, backend connectivity

**Systems:** Linux, Apache/web server configuration, EC2 administration

---

# Interview Summary

> I deployed EC2 web servers across three Availability Zones in the AWS Ireland region and used an AMI and Launch Template to maintain consistent server configurations. I implemented both Classic Load Balancer and Application Load Balancer configurations. For the ALB, I created a Target Group and registered the backend EC2 instances. I then tested the load-balanced application and verified responses from multiple backend servers.

---

# Project Outcome

This project strengthened my practical understanding of **AWS load balancing and high-availability architecture** by combining EC2, multiple Availability Zones, Launch Templates, AMIs, Classic Load Balancer, Application Load Balancer, Target Groups, and backend server verification.
