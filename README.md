# 💼 DAP-Vancouver-SreeCharan: AWS Data Analytics Portfolio

---

## 📊 Project 1: AWS Data Analytics Platform – City of Vancouver

### 🔍 Overview

A cloud-native platform developed for analyzing **Employee Remuneration and Expenses** from the City of Vancouver. Built using AWS services to ensure scalability, governance, and security.

---
### Dataset:
The dataset was sourced from the City of Vancouver Open Data Portal and includes:

Employee Name and Role (e.g., Civil Engineer I)

Department and Position Title

Base Salary and Total Remuneration

Work-Related Expenses

Reporting Year


### 🧰 Technologies Used

| Service       | Purpose                               |
| ------------- | ------------------------------------- |
| Amazon S3     | Data storage (raw, clean, curated)    |
| AWS Glue      | ETL pipelines, DataBrew for profiling |
| Amazon Athena | SQL queries on S3 datasets            |
| AWS KMS       | Encryption for secure data storage    |
| IAM           | Role-based access control             |
| CloudWatch    | Monitoring ETL jobs and alarms        |
| CloudTrail    | Auditing and activity logging         |

---

### 🔄 Workflow Summary

<img width="452" alt="image" src="https://github.com/user-attachments/assets/803224e5-256d-4cfd-9d5f-90d5cbac317a" />

#### 🗂️ Step 1: Data Ingestion
<br>

* Dataset from [Vancouver Open Data Portal]( https://opendata.vancouver.ca/explore/dataset/employee-remuneration-and-expenses-earning-over-75000/analyze/?disjunctive.department&disjunctive.title&refine.title=Civil+Engineer+I&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJsaW5lIiwiZnVuYyI6IkFWRyIsInlBeGlzIjoicmVtdW5lcmF0aW9uIiwic2NpZW50aWZpY0Rpc3BsYXkiOnRydWUsImNvbG9yIjoiI2ZmNTAwMCJ9LHsiYWxpZ25Nb250aCI6dHJ1ZSwidHlwZSI6ImxpbmUiLCJmdW5jIjoiQVZHIiwieUF4aXMiOiJleHBlbnNlcyIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiNmNmIzMzIifV0sInhBeGlzIjoieWVhciIsIm1heHBvaW50cyI6bnVsbCwidGltZXNjYWxlIjoieWVhciIsInNvcnQiOiIiLCJjb25maWciOnsiZGF0YXNldCI6ImVtcGxveWVlLXJlbXVuZXJhdGlvbi1hbmQtZXhwZW5zZXMtZWFybmluZy1vdmVyLTc1MDAwIiwib3B0aW9ucyI6eyJkaXNqdW5jdGl2ZS5kZXBhcnRtZW50Ijp0cnVlLCJkaXNqdW5jdGl2ZS50aXRsZSI6dHJ1ZSwicmVmaW5lLnRpdGxlIjoiQ2l2aWwgRW5naW5lZXIgSSJ9fX1dLCJkaXNwbGF5TGVnZW5kIjp0cnVlLCJhbGlnbk1vbnRoIjp0cnVlLCJ0aW1lc2NhbGUiOiIifQ%3D%3D)
<br>
<img width="452" alt="image" src="https://github.com/user-attachments/assets/09089591-2285-49bf-9207-29940d0e40c8"/>

* Stored in S3 bucket: `employeeremuneration-raw-sca`



#### 🔍 Step 2: Data Profiling & Cleaning
<br>

* AWS Glue jobs cleaned data and handled nulls, renamed columns

<br>
<img width="452" alt="image" src="https://github.com/user-attachments/assets/e4fd48d6-ea06-4aee-9344-9a336448f94b"/>

<br>

* Output saved to `clean` and `curated` S3 layers

<img width="452" alt="image" src="https://github.com/user-attachments/assets/c5b051cc-80d3-4e3c-b3f0-69f39966ebea" />


#### 📚 Step 3: Data Cataloging
<br>

* Glue Data Catalog generated tables for Athena querying

<img width="452" alt="image" src="https://github.com/user-attachments/assets/f60a5fc0-a1af-495c-baff-7c42249ba44a" />


#### 📈 Step 4: Data Summarization
<br>

* Visual ETL jobs aggregated pay metrics by role and year
* Results stored in Parquet for faster querying

<img width="452" alt="image" src="https://github.com/user-attachments/assets/a7b9deea-aad6-4acb-81bb-20576f841ecd" />


## 📊 Project 2: AWS Data Analytics Platform – City of Vancouver
  
### 🔍 Overview

A cloud-native platform developed for analyzing **Employee Remuneration and Expenses** from the City of Vancouver. Built using AWS services to ensure security, encruption and decryprion, Quality Check.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/0952d8c2-4e75-4a2f-b63e-d8d3e2c6a86d" />


#### 🔐 Step 5: Security & Encryption

* KMS custom key used for SSE-KMS encryption<br>
<img width="468" alt="image" src="https://github.com/user-attachments/assets/c0bc5ba2-9cd3-4ec2-8e8a-905cc3c94542" />

* IAM roles restrict unauthorized access
<br>
<img width="468" alt="image" src="https://github.com/user-attachments/assets/e816d68e-1698-414d-a346-116ad9cc36a0" />

* S3 versioning and cross-region replication applied
<br>
<img width="468" alt="image" src="https://github.com/user-attachments/assets/cc8b65e2-2375-4630-b13d-74dffc7d6d6d" />


#### 🧪 Step 6: Governance & Quality Control

* ETL outputs routed to `/passed` and `/failed` S3 folders

<img width="468" alt="image" src="https://github.com/user-attachments/assets/2da174f6-5994-410e-92b4-5f745f7952ee" />
<br>

* Enforced completeness and freshness rules

<img width="468" alt="image" src="https://github.com/user-attachments/assets/82001647-16d4-4d70-9cca-46818a4b4670" />


#### 📊 Step 7: Monitoring & Logging

* Dashboards created in CloudWatch
* Alarms notify on job failures or cost spikes

<img width="468" alt="image" src="https://github.com/user-attachments/assets/26f8f10c-ec3f-4a70-8837-fd412b2064da" /> 
<br>
* CloudTrail logs actions and stores them securely<br>

<img width="468" alt="image" src="https://github.com/user-attachments/assets/d8c6a577-2a5a-40a9-9ad8-83f3c7a53eab" />

<br>
<img width="468" alt="image" src="https://github.com/user-attachments/assets/ad360a8e-b046-4ea0-a29a-2fe6fc660f23" />

<br>

#### Step 8: Cost Estimation
<br>

<img width="452" alt="image" src="https://github.com/user-attachments/assets/4a34079a-4987-4506-93d0-3b151affb672" />

### Deliverables:

Fully cleaned and transformed datasets stored in S3 (raw, clean, curated)

ETL pipelines with data validation (pass/fail paths)

CloudWatch dashboards for monitoring job executions and storage utilization

Audit trail of data access and operations via AWS CloudTrail

Cost estimation and performance efficiency metrics

Final analysis report and stakeholder presentation materials

## Conclusion:

This project successfully demonstrates the application of AWS cloud services in transforming municipal data into actionable insights. By analyzing compensation patterns and implementing monitoring and governance mechanisms, the City of Vancouver can strengthen its commitment to financial accountability, operational efficiency, and data-driven decision-making.


---

## 🧪 Project 3: AWS Cloud Portfolio Demonstration (Simulated Case Study)

### 🗺️ Concepts Demonstrated

### Module 1: AWS Deployment and Service Models

Case Studies Covered:

Traditional vs. Cloud Computing Models

Cloud Deployment Models (Public, Private, Hybrid, Community)

Cloud Service Models (IaaS, PaaS, SaaS)

Traditional vs Cloud Model   
-----------------------------------------
<img width="746" alt="Screenshot 2025-06-24 at 5 36 51 PM" src="https://github.com/user-attachments/assets/fd4693cd-bc88-42e6-90be-cf6cc403a0e2" />


Deployment Models         
-----------------------------------------
<img width="808" alt="Screenshot 2025-06-24 at 5 36 13 PM" src="https://github.com/user-attachments/assets/44f1a11d-3db3-4ed3-a35a-18e95877e7ba" />

IaaS / PaaS / SaaS Breakdown
-----------------------------------------
<img width="1126" alt="Screenshot 2025-06-24 at 7 26 39 PM" src="https://github.com/user-attachments/assets/0e6def55-9367-488d-a2cd-9399c8995966" />

* Explanation: This module laid the foundation for understanding cloud computing by comparing traditional and cloud models. It emphasized the benefits of elasticity, scalability, and cost-effectiveness. The deployment models helped distinguish the environments in which AWS services operate, while the service models clarified the levels of control and responsibility. Scoring 100% in the module demonstrates a strong grasp of AWS’s layered architecture and deployment strategies.

### Module 2: AWS Cost Analysis

Case Studies Covered:

Total Cost of Ownership (TCO) – Delaware North

AWS Pricing Calculator

AWS Support Plans

<img width="1182" alt="Screenshot 2025-06-24 at 6 04 08 PM" src="https://github.com/user-attachments/assets/cc100697-ef8d-4f0c-a401-9795482e5d60" />

* Explanation: This module introduced financial planning in AWS. The TCO case study illustrated how cloud adoption leads to long-term savings. The AWS Pricing Calculator provided hands-on experience in estimating service costs, while the Support Plans comparison highlighted the differences between Basic, Developer, and Business support tiers. A perfect score reflects comprehensive understanding of AWS pricing and financial management tools.

### Module 3: AWS Global Infrastructure

Case Study Covered:

AWS Regions, Availability Zones, and Edge Locations

<img width="1064" alt="Screenshot 2025-06-24 at 5 40 09 PM" src="https://github.com/user-attachments/assets/edb37fcc-15c0-4472-ae11-5b8eae5b09c8" />

* Explanation: This module examined AWS’s global footprint. The case study demonstrated how data center distribution enhances performance, security, and disaster recovery. It helped understand how Regional Edge Caches, Edge Locations, and Regions work together to provide low latency and high availability. The perfect score indicates a full understanding of AWS’s global infrastructure.

### Module 4: AWS IAM

Case Studies Covered:

Shared Responsibility Model

IAM Practice Lab (Roles and Permissions)

<img width="602" alt="Screenshot 2025-06-24 at 5 40 33 PM" src="https://github.com/user-attachments/assets/260fa3de-44f0-4031-932a-4b22826898aa" />

* Explanation: This module focused on securing access to AWS resources. The shared responsibility model clarified which aspects are managed by AWS and which are user responsibilities. The IAM lab offered practical experience in creating users, groups, and policies. A 90% score demonstrates effective understanding of AWS security best practices.

### Module 5: AWS VPC

Case Study Covered:

Build Your VPC: Lab

<img width="1187" alt="Screenshot 2025-06-24 at 6 17 58 PM" src="https://github.com/user-attachments/assets/34907569-0747-4507-b653-44b4625e459e" />
* Explaination: This lab walked through the creation of a Virtual Private Cloud, including subnets, route tables, and gateways. It emphasized secure networking, isolation, and traffic control within AWS. A perfect score reflects proficiency in designing and configuring secure virtual networks.

### Module 6: AWS Lambda

Case Study Covered:

Create and Verify AWS Lambda Function

<img width="941" alt="Screenshot 2025-06-24 at 6 20 03 PM" src="https://github.com/user-attachments/assets/880ec0bb-aab0-4c27-b778-035043dc68f9" />
* Explanation: The module explored serverless computing using AWS Lambda. The case study guided through deploying functions that respond to triggers without provisioning servers. Scoring 90% reflects strong understanding of event-driven architecture and function execution in the cloud.

### Module 7: AWS EBS

Case Study Covered:

Working with Amazon EBS: Lab

<img width="655" alt="Screenshot 2025-06-24 at 6 32 41 PM" src="https://github.com/user-attachments/assets/015ce3a4-131b-4968-91dc-36d00fd3af0f" />
* Explanation: The lab involved creating, mounting, and restoring EBS volumes. It highlighted the importance of durable and persistent block storage for EC2 instances. The perfect score confirms mastery of EBS volume lifecycle operations and storage configuration.
