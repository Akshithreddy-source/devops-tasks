# DevOps Task Submission

Name: Akshith Reddy

Task 1: Implement IAM Best Practices

Objective:
To implement AWS IAM best practices including group creation, least privilege access, MFA for root user, and restricted S3 access using a custom policy.


Steps Performed:

1. Created IAM Groups
* Admin
* Dev
* ReadOnly

2. Applied Least Privilege
* Assigned appropriate permissions to each group

3. Enabled MFA for Root User
* Configured MFA using authenticator app

4. Created Custom S3 Policy
* Restricted access to a specific folder in S3 bucket

5. Attached Policy
* Attached custom policy to Dev group

---

Screenshots
1.
<img width="1910" height="816" alt="image" src="https://github.com/user-attachments/assets/3fbad21f-9ff8-4d56-9dc9-32f78a4ac3d2" />
2.
<img width="1914" height="819" alt="image" src="https://github.com/user-attachments/assets/744bfc09-2f89-4052-bdc8-dc33f4547dcd" />
3.
<img width="1885" height="818" alt="image" src="https://github.com/user-attachments/assets/cf5b3cb3-4a6c-4776-8a9d-a91ca71d964b" />




---

Result:
Successfully implemented IAM best practices.

***********************************************************


Task 2: Enable CloudWatch Monitoring

Objective
To monitor AWS resources using CloudWatch by creating alarms, enabling notifications, monitoring load balancer metrics, and enabling detailed monitoring for EC2.

Steps Performed
1. Created CPU Utilization Alarm
* Selected EC2 CPUUtilization metric
* Set threshold greater than 70%

2. Configured SNS Notification
* Created SNS topic
* Subscribed email and confirmed notification

3. Monitored ALB Metrics
* Created target group and load balancer
* Generated traffic using DNS
* Viewed metrics in monitoring tab

4. Enabled Detailed Monitoring for EC2
* Enabled 1-minute detailed monitoring for instance


Screenshots
<img width="1887" height="802" alt="image" src="https://github.com/user-attachments/assets/9f2f51c8-8dbb-4bdb-9848-22bf48fe011e" />

***************************************************************************
Taak 3

# AWS S3 Bucket Setup

## Overview

This project demonstrates how to create and configure an Amazon S3 bucket, upload files, and make them publicly accessible using a bucket policy.

---

## Steps Performed

### 1. Created S3 Bucket

* Bucket Name: `akshith-devops-s3-bucket-01`
* Region: (your region)
* Block Public Access: Disabled

---

### 2. Uploaded Files

* Created folder: `images/`
* Uploaded files into the folder
* Verified files inside the bucket

---

### 3. Configured Bucket Policy

Added the following policy to allow public access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadAccess",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::akshith-devops-s3-bucket-01/*"
    }
  ]
}
```

---

### 4. Tested Public Access

Opened file using browser URL:

```
https://akshith-devops-s3-bucket-01.s3.amazonaws.com/images/<file-name>
```

---

## Screenshots

1.
<img width="1847" height="705" alt="image" src="https://github.com/user-attachments/assets/e9bf705c-276f-48d8-885d-5f337148f266" />
2.<img width="1875" height="804" alt="image" src="https://github.com/user-attachments/assets/36a86b25-b0db-43f8-9786-1be3cd2cb178" />


---

## Outcome

* Created S3 bucket
* Uploaded files
* Configured public access using bucket policy
* Verified file access using URL

---

## Learning

* S3 bucket creation and configuration
* Bucket policies
* Public access setup
* Object URL usage

*****************************************************************
# Task 3: RDS MySQL Deployment using AWS

## Objective
To deploy a MySQL database on AWS RDS in a private subnet and connect it securely from an EC2 instance.

---

## Steps Performed

1. Created a VPC with public and private subnets.
2. Launched an EC2 instance in the public subnet.
3. Created a DB Subnet Group using private subnets.
4. Deployed MySQL RDS instance in private subnet.
5. Configured Security Groups:
   - Allowed MySQL (3306) access only from EC2.
6. Enabled automated backups.
7. Connected EC2 to RDS using MySQL client.

---

## Architecture

- EC2 (Public Subnet) → Application Server
- RDS MySQL (Private Subnet) → Database
- Secure connection via Security Groups

---

## Outcome

Successfully connected EC2 instance to RDS MySQL database and executed SQL queries.

---
<img width="1919" height="697" alt="image" src="https://github.com/user-attachments/assets/e9f712b2-7d91-4dce-b577-5119a68b11a9" />

## Screenshots

rds :
<img width="1903" height="759" alt="image" src="https://github.com/user-attachments/assets/be10d75f-d62a-4ca5-8227-c24e1490fa88" />

2. Security group (rd-sg):
<img width="1897" height="771" alt="image" src="https://github.com/user-attachments/assets/c4f0a1d0-19f6-4e1a-a111-b4c975d4578c" />

3. Database connection
   <img width="1919" height="697" alt="image" src="https://github.com/user-attachments/assets/5f6247f2-d670-416a-a348-9e25574e4bce" />
