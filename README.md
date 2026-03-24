# AWS MULTI-TEAM IAM SECURITY DESIGN PROJECT

## Overview

This project demonstrates the implementation of **AWS IAM policies and
groups** following the **principle of least privilege**.\
It simulates a real-world consulting scenario where multiple teams
require controlled and secure access to AWS services.

------------------------------------------------------------------------

## Objectives

-   Enforce **least privilege access**
-   Implement **group-based permission management**
-   Restrict access to sensitive services (e.g., IAM)
-   Provide **secure, role-based access** for different teams

------------------------------------------------------------------------

## Architecture

-   IAM Users assigned to **Groups**
-   Permissions managed via **Custom JSON Policies**
-   Use of **implicit deny** and **explicit deny (IAM)**
-   Resource-level restrictions (e.g., specific S3 buckets)

------------------------------------------------------------------------

## Teams & Permissions

### Junior Developers

-   EC2: Start and Stop instances only\
-   S3: Read/Write access to `company-dev-bucket`\
-   No access to other AWS services

------------------------------------------------------------------------

### Senior Engineers

-   Full access to EC2 and S3\
-   No IAM access

------------------------------------------------------------------------

### Support Team

-   EC2: Read-only\
-   CloudWatch: Read-only\
-   No S3 access\
-   No IAM access

------------------------------------------------------------------------

### QA Team

-   S3: Read/Write access to `company-qa-bucket`\
-   EC2: Read-only\
-   No CloudWatch access\
-   No IAM access\
-   Cannot delete the S3 bucket

------------------------------------------------------------------------

## Security Best Practices

-   Least privilege principle enforced\
-   Permissions assigned via **groups, not individual users**\
-   Explicit deny for IAM access\
-   Secure credential handling (no plain-text sharing)\
-   Password reset required on first login

------------------------------------------------------------------------

## Technologies Used

-   AWS IAM\
-   Amazon EC2\
-   Amazon S3\
-   Amazon CloudWatch

------------------------------------------------------------------------

## Key Learnings

-   Designing scalable IAM structures\
-   Writing custom IAM policies (JSON)\
-   Applying least privilege in real scenarios\
-   Structuring access for multiple teams
