# AWS Document Processing Project

## Overview

This project is an **AWS cloud application** built with **Terraform / OpenTofu**.

The idea is simple: a user uploads a document, and the system stores it, processes it, saves the results, and shows reports.

This project shows skills in:

- AWS
- Terraform / OpenTofu
- cloud architecture
- APIs
- security
- automation
- reporting

---

## What the project does

A user uploads a file such as:

- invoice
- receipt
- claim form
- policy document

The system then:

1. uploads the file to **Amazon S3**
2. triggers processing with **AWS Lambda**
3. extracts text/data from the document
4. stores the processed results
5. provides a secure API for viewing data
6. shows analytics in a dashboard

---

## AWS Services Used

- **Amazon S3** – stores uploaded files
- **AWS Lambda** – runs processing code
- **Amazon API Gateway** – creates secure API endpoints
- **AWS Step Functions** – controls workflow steps
- **Amazon DynamoDB** or **RDS** – stores processed data
- **Amazon Cognito** – handles login/authentication
- **Amazon CloudWatch** – logging and monitoring
- **Amazon EventBridge** – scheduled jobs and automation
- **Amazon QuickSight** – dashboards and reporting

---

## Why Terraform / OpenTofu is used

Terraform / OpenTofu is used to create and manage the AWS infrastructure as code.

This includes:

- S3 buckets
- Lambda functions
- IAM roles and permissions
- API Gateway
- Cognito
- Step Functions
- database resources
- CloudWatch logs
- scheduled jobs

Using Terraform / OpenTofu makes the project easier to manage, reuse, and deploy.

---

## Example Workflow

1. User uploads a document
2. File is stored in S3
3. Lambda starts processing
4. Step Functions manages the steps
5. Extracted data is saved to the database
6. User can view results through the API
7. Dashboard shows reports and trends

---

## Project Structure

```bash
docment-platform/
├── app/                    # frontend app
├── services/
│   ├── upload-api/         # API code
│   ├── processor/          # document processing logic
│   └── reporting/          # scheduled reporting jobs
├── terraform/
│   ├── modules/            # reusable IaC modules
│   ├── environments/       # dev and prod environments
│   └── versions.tf
├── docs/                   # diagrams and notes
└── README.md
