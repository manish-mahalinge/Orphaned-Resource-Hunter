# Orphaned-Resource-Hunter

This project provides an automated solution to identify and delete unused ("orphaned") resources across various AWS services. It's designed to help you reduce cloud costs and keep your AWS environment clean and efficient.

---

## The Challenge: Cloud Waste

- Unused or forgotten resources in cloud environments.
- They continue to incur costs even when not in use.
- Examples:
  - Old EC2 instances
  - Unattached EBS volumes
  - Unused S3 buckets
- Leads to cloud waste and budget overruns.

---

## Solution: Introducing the "Orphaned Resource Hunter"

An automated solution that scans your AWS account for orphaned resources and allows you to delete them through a simple web interface.

---

## How It Works: The Architecture

- **Lambda Functions**
  - Two main functions:
    - Scanner – identifies orphaned resources.
    - Delete – removes selected resources.

- **DynamoDB**
  - A NoSQL database used to store the list of orphaned resources.

- **API Gateway**
  - Provides a secure and scalable endpoint for the frontend.

- **Frontend UI**
  - A simple HTML file that interacts with the API.

---

## End-to-End Workflow

1. Scanner Lambda Runs.
2. User Access UI.
3. UI Displays Resources.
4. User Selects Resources.
5. Delete Lambda Removes the Resources.

---

## Benefits of the Project

### Cost Reduction

Direct Cost Saved By Deleting Orphaned Resources in Single Click.

### Resource LifeCycle Management

Establish a Process of Managing Resources.

### Scalability

Serverless Solution Deployable in Any AWS Account.

### Automation

Reduces the Manual Effort and Human Error.

### Infrastructure as Code

Deployed using CloudFormation.
