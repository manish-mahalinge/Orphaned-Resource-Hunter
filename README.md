# 🚀 Cloud Cost Sentinel - Serverless AWS Cost Optimization Platform

Cloud Cost Sentinel is a serverless AWS solution designed to identify and remove orphaned AWS resources that generate unnecessary cloud costs.

The platform automatically scans AWS resources, stores findings, and allows users to safely remove unused resources through a web-based interface.

---

## Problem Statement

In AWS environments, resources are often left behind after applications, testing environments, or infrastructure components are removed.

Common examples include:

* Unattached EBS Volumes
* Unused Elastic IP Addresses
* Empty or abandoned S3 Buckets
* Unused EFS File Systems

These orphaned resources continue generating charges and contribute to cloud waste.

Cloud Cost Sentinel helps organizations identify and eliminate such resources automatically.

---

# Architecture

```text
User
 │
 ▼
GitHub Pages Frontend
 │
 ▼
Amazon API Gateway
 │
 ▼
Scanner Lambda (Python + boto3)
 │
 ├── EBS Volumes
 ├── Elastic IPs
 ├── S3 Buckets
 └── EFS File Systems
 │
 ▼
Amazon DynamoDB
 │
 ▼
Frontend Dashboard

Delete Request
 │
 ▼
Delete Lambda
 │
 ▼
SNS Notification
```

---

# Features

### Resource Discovery

Detects orphaned:

* EBS Volumes
* Elastic IP Addresses
* S3 Buckets
* EFS File Systems

### Automated Cleanup

* One-click resource deletion
* Secure API-driven workflow
* Reduced manual effort

### Cost Optimization

* Reduces unnecessary AWS spending
* Eliminates forgotten resources
* Encourages resource lifecycle management

### Serverless Architecture

* No servers to manage
* Automatic scaling
* Pay-per-use model

### Infrastructure as Code

* Entire infrastructure deployed using AWS CloudFormation
* Reproducible and version-controlled deployments

### CI/CD Automation

* Automated deployment using GitHub Actions
* Continuous integration for Lambda functions and infrastructure updates

---

# Technology Stack

## Cloud Services

* AWS Lambda
* Amazon API Gateway
* Amazon DynamoDB
* Amazon SNS
* AWS IAM
* Amazon EC2
* Amazon EBS
* Amazon EFS
* Amazon S3

## DevOps

* GitHub Actions
* CloudFormation
* Git

## Programming

* Python
* boto3
* HTML
* JavaScript

---

# Workflow

### Step 1: User Initiates Scan

The user accesses the web dashboard and starts a resource scan.

### Step 2: API Gateway Receives Request

The frontend sends a request to API Gateway.

### Step 3: Scanner Lambda Executes

Lambda uses boto3 APIs to inspect AWS resources and identify orphaned resources.

### Step 4: Results Stored

Detected resources are stored in DynamoDB.

### Step 5: Results Displayed

The frontend retrieves and displays the findings.

### Step 6: Resource Deletion

The user selects resources for removal.

### Step 7: Delete Lambda Executes

The deletion Lambda removes the selected resources.

### Step 8: Notification Sent

SNS sends confirmation notifications after successful cleanup.

---

# Security

* IAM Least Privilege Access
* API Gateway Controlled Access
* Resource Validation Before Deletion
* Serverless Security Model

---

# Business Impact

### Cloud Cost Reduction

Automates identification and removal of unused AWS resources.

### Improved Governance

Provides visibility into cloud resource utilization.

### Reduced Operational Overhead

Eliminates repetitive manual audits.

### Scalable Solution

Can be deployed in any AWS account with minimal configuration.

---

# Future Enhancements

* Multi-Account AWS Support
* AWS Organizations Integration
* CloudWatch Cost Analytics Dashboard
* Scheduled Automated Scans
* Resource Tag-Based Cleanup Policies
* Approval Workflow Before Deletion
* Cost Savings Reports

---

# Key Learnings

Through this project, I gained hands-on experience with:

* Serverless Architecture
* AWS Lambda Development
* REST API Design
* Infrastructure as Code
* Cloud Cost Optimization
* CI/CD Automation
* IAM Security Best Practices
* DynamoDB Data Modeling

---

# Author

**Manish Mahalinge**

Cloud & DevOps Engineer

AWS | Kubernetes | Terraform | Jenkins | GitOps | DevSecOps
