**📘 Week 2 Portfolio: Design of Academic Data Lake**

**Task Title:**

**Designing a Scalable Academic Data Lake Architecture on AWS**

**Objective:**
To organize and classify academic datasets into a structured AWS S3 bucket system using appropriate storage classes, regional deployment, and tagging strategies for efficient data retrieval and cost optimization.
________________________________________
**Summary of Activities**

**✅ 1. Dataset Classification and Folder Structure**

**Five key datasets were defined:**

•	Course Enrollments

•	Course Completion Records

•	Student Demographics

•	Retention Records

•	Faculty Workload

Each dataset was organized under the S3 bucket academic-raw-tim with clearly structured folder paths including Year=25 and Quarter=Q2 to support time-based partitioning and data lifecycle management.

**✅ 2. Region Selection**

**All datasets were deployed in the Virginia region (US East 1) to take advantage of:**

•	Lower latency for academic applications

•	Cost-efficient storage and compute

**✅ 3. Metadata Tagging**

**Each dataset was tagged for governance using key metadata fields like:**

•	Owner = Academic

•	Write Frequency = daily/weekly/monthly

•	Read Frequency = daily/weekly/monthly

This helps with data cataloging, cost allocation, and automated lifecycle policies.

**✅ 4. Storage Class Assignment**

**Datasets were assigned a combination of:**

•	Standard: For frequently accessed data (e.g., Course Enrollments)

•	Infrequent Access (IA): For less-accessed data (e.g., Retention Records)

This design balances performance and storage cost based on usage patterns.
________________________________________
**Key Learnings & Reflections**

•	Learned how to apply data governance best practices through folder structuring, tagging, and storage class assignment.

•	Developed a better understanding of AWS S3 optimization techniques for academic data environments.

•	Gained hands-on experience in partitioning datasets for scalable analytics and efficient querying.

**Week 3 Portfolio: Dataset Profiling and Cleaning Design**

**Task Title:**

**Designing Data Profiling and Cleaning Strategy for Academic Datasets
Objective:**

To identify potential data quality and structural issues across academic datasets and apply appropriate profiling and cleaning techniques to ensure consistency, accuracy, and readiness for analytical processing.
________________________________________
**Summary of Activities**

**✅ 1. Dataset Profiling Conducted
Performed profiling on:**

•	Student Demographics

o	Columns profiled: StudentID, Age, Gender, Ethnicity

o	Result: No structural or data quality issues found.

•	(Other datasets not specified in profiling sheet—assumed clean or pending profiling)

**✅ 2. Identification of Common Issues**

**Based on second sheet analysis, the team studied potential issues such as:**

**•	Data Structure Issues:**

o	Nested fields

o	Inconsistent schemas

o	Mixed data types

o	Multi-valued fields

•	Data Quality Issues:

o	Missing data

o	Duplicate entries

o	Inconsistent naming/formatting

o	Incorrect data entries

**✅ 3. Cleaning Techniques Applied or Planned**

**•	For Structural Issues:**

o	Flatten arrays / expand JSON objects

o	Standardize schema and column types

o	Convert mixed data types

o	Split multi-valued fields using delimiters

•	For Quality Issues:

o	Impute or drop missing values

o	Remove duplicates

o	Standardize inconsistent values

o	Map or correct incorrect entries manually
________________________________________
**Tools & Technologies Used**

•	Excel for manual profiling and issue documentation

•	Planned Tools: Python (Pandas), AWS Glue for automated cleaning in future stages
________________________________________
**Reflection**

•	Understood how profiling serves as the foundation for data cleaning.

•	Learned to categorize and apply different cleaning strategies based on type of issue.

•	Realized that even if data appears clean, validation checks are essential before ingestion or analysis.

**Week 4 Portfolio: ETL Design and Implementation on AWS
Task Title:**

Designing and Implementing an ETL Pipeline with Cost Monitoring and Data Catalog Integration
Objective:

To develop a visual and functional ETL process on AWS for profiling and enriching academic datasets. This includes defining business objectives, evaluating costs, integrating CloudWatch alarms, and utilizing AWS Glue and Athena for querying and analysis.
________________________________________
**Summary of Activities**

**✅ 1. Cost Evaluation of Dataset Profiling and Cleaning**

•	Assessed ingestion and cleaning costs of datasets using the AWS Pricing Calculator.

•	Projected low monthly costs for storing and processing academic data due to efficient use of S3 Standard-IA and optimized request patterns.

**✅ 2. ETL Process Design**

•	Created a Visual ETL diagram using draw.io to outline:

o	Data ingestion from raw S3 bucket

o	Profiling, cleaning, and enrichment stages

o	Storage in curated zones

o	Query layer setup using AWS Athena

•	Defined system-level roles for User, Curated, and Data Catalog in the ETL workflow.

**✅ 3. Business Questions Defined**

•	Focused on enabling queries to answer:

o	What are the demographic patterns of enrolled students?

o	How does retention vary by faculty workload?

o	Which courses have the highest completion rates?

**✅ 4. Data Enrichment
•	Enriched raw data by:**

o	Standardizing inconsistent formats

o	Mapping and correcting invalid values

o	Creating derived columns to support analysis (e.g., age group, completion status)

**✅ 5. ETL Implementation**

**•	Implemented the designed ETL process using:**

o	AWS Glue for cleaning and cataloging

o	S3 for staging and storing enriched datasets

o	AWS Athena for validation through SQL queries

**✅ 6. Monitoring with CloudWatch**

**•	Set up CloudWatch alarms to:**

o	Notify if costs exceed thresholds

o	Track number of ETL jobs and data transfer activity
________________________________________
**Tools & Technologies Used**

•	AWS Glue

•	AWS S3 (raw and curated layers)

•	AWS Athena

•	AWS CloudWatch

•	Draw.io for ETL diagramming
________________________________________
**Reflection**

This week marked the transition from design to implementation. 

I gained practical experience with AWS Glue and CloudWatch, and saw how critical monitoring is for cost and performance optimization. I also reinforced my understanding of aligning business questions with ETL outputs to support data-driven decision-making.

**AWS Deployment and Service Models**

The activity of the week aimed at studying the AWS Deployment and Service models with more emphasis on the contrast between the traditional computing infrastructure and the emerging cloud-based solutions. The first case study focused on the difference between the dataset location, access, and privacy of the traditional models hosted by UCW premises or AWS Cloud models, which offers the global reach within the network, IAM-based control access, and control privacy features. The second case study discussed four cloud deployment models which are; Private cloud, Public cloud, Hybrid cloud, and Multi-Cloud. These models imply different trade-offs in the access control, distribution in datasets and privacy protection via policies. The third case study was about Cloud Service Models that included Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS). This was explained on the impact it has on the location of dataset, complexity of Accessibility, and the control of privacy by the user. Finally, I managed to take and pass the AWS Academy Cloud Foundations Module 1 Knowledge Check scoring 100 out of 100 and proving my knowledge of the deployment principles described.

![image](https://github.com/user-attachments/assets/74b53978-3cad-4e49-aa5b-f50f65e584d7)

![image](https://github.com/user-attachments/assets/6d9ab690-9277-4587-9078-8f4159ab3c39)

![image](https://github.com/user-attachments/assets/433f5299-30bf-484b-b5f3-653b012b86a8)

![image](https://github.com/user-attachments/assets/64e569fe-a3ef-4d7b-8e71-6cdfbea919bb)

**AWS Cost Analysis**

we studied AWS service costs by calculating them with the help of the AWS Pricing Calculator, considered support plans and passed the Module 2 knowledge check. Case Study #5 was concerned with cost implication of data profiling and analysis. Under the first estimation, Academic- Profiling-Cost-Evaluation, the upfront cost was found to be 0 and the total cost of 12 months was 52.92 USD with more or less cost monthly. The second estimate which was named Academic-Data-Analysis-Cost-Evaluation had a monthly cost of USD 7.21 and a total cost of USD 86.52. These results indicate the operational scaling with such services as Athena usage and the number of scanned objects. In Case Study 6 the role of the Academic Department was placed on Developer Support Plan, which is perfect to the development/testing environments and non-production environments that need support using business-hours. Lastly, I took a Knowledge check of module 2 achieving 80%, which is above the passing mark, and proves to understand the pricing, billing, and support services offered by AWS.

![image](https://github.com/user-attachments/assets/a1ee88e0-8ddb-41bc-8795-dcd1ba5e2fbd)

![image](https://github.com/user-attachments/assets/ed73647f-3cdb-4194-a044-311be29cfb13)

![image](https://github.com/user-attachments/assets/004f816e-dd25-45f4-941f-f2dda5f476c0)

**AWS Global infrastructure**

As a follow-up to AWS Foundations, we studied in Module 3 the infrastructure of AWS worldwide. Case Study 7 high lighted the management data regarding the data as stored and handled and maintained in various layers of the AWS global architecture which include Regional Edge caches, Edge fundamental localities and AWS Domains. Each layer of the infrastructure performs a different use: caches edged on temporary content which is not sensitive (such as courses lists) to access them quickly, edges locations (such as dashboards and reports) should be visible to regional users, and the regional storage (such as S3 in the Canada Central region) contains sensitive data such as student records and they are encrypted and have IAM controls enabled. The buildings provide low latencies, data confidentiality, as well as, efficiency within the distributed systems. To support my learning, I took Module 3 Knowledge Check that showed me a perfect score of 100% and showed that I have a good knowledge of the global infrastructure of AWS, availability zones that AWS offers, and architectural advantages of the distributed systems provided by AWS.

![image](https://github.com/user-attachments/assets/6c0fa190-9de8-4341-b089-67697967acb2)

![image](https://github.com/user-attachments/assets/37a6e926-bdb2-4842-973a-970ea928ace4)

**AWS IAM**

It turned to the principles of AWS IAM (Identity and Access Management) including distribution of the responsibility and exploration of the practice through the lab activities. In the Case Study 8, it was discussed that the relationship was shared responsibility between UCW and AWS. UCW handles the configuration of operating system, software and user level authorisation to the EC2 instances whereas AWS takes care of the physical infrastructure, storage and network virtualization. This model is secure, controllable and scalable. This study (Case Study #9) allowed us to undertake IAM exercises in which we were able to create users and assign each to one or more of the support and admin groups and then test the permissions against EC2 action. All the assignments passed with a 40/40 score confirming proper configuration of IAM roles and permissions. At the end of the module, I passed the Module 4 Knowledge Check with full 100 marks, which in turn meant that I had the background about IAM roles, group policies, access control, and AWS security framework.

![image](https://github.com/user-attachments/assets/78e0a472-0aa5-4b93-90e5-752e4f887d48)

![image](https://github.com/user-attachments/assets/e95c9306-4b11-461b-9ec7-188849c68e9c)

![image](https://github.com/user-attachments/assets/0195f3f1-41e5-4fb0-8741-db46b90c5351)

**AWS VPC**

we discussed configuration and working of virtual private clouds (VPCs) in AWS. In Case Study 10, we had to finish the Lab 2 in which we used to get a feel about how to create a customised VPC and subnets, route table, security groups and ec2 instances. This lab was developed, and all the work performed was graded with 100 percent (30/30). The most important steps were the creation of new subnets, the connection of these new subnets with the route tables, the creation of the security group, launching the instances of the EC2, and confirming that the instances are up and reachable via the web. This practical exercise has made us realise key concepts of networking in clouds and reinforced our knowledge on our setting up public/private subnets and firewalls settings. I completed the Module 5 Knowledge Check with a score of 100 per cent, which means that I am confident to understand how VPC architecture works, what IP ranges are used, why NAT gateways exist and what security concepts I can apply in this case.

![image](https://github.com/user-attachments/assets/00e042c6-1b7a-44ab-b378-c2d20f0912ce)

![image](https://github.com/user-attachments/assets/9b62f0cc-8235-4637-a087-a7a5757af467)

**AWS Lambda**

we learned about AWS Lambda functions during Module 6 which was about serverless computing. Case Study 11 led us through the process of designing and setting an AWS Lambda function to cause the automated shutdown of EC2 instance. The activities included developing the Lambda function, creating a scheduled CloudWatch event, and connecting the defined automatic action in order to shut an EC2 instance down, and checking the success of the automatization. The lab was done correctly with the top score of 20/20. This practice proved the effectiveness of event-based computing as a key to automatize the management of cloud resources and cut the superfluous expenses. To ensure that the learning was solid, I did the Module 6 Knowledge Check that scored 100 which confirmed that I understand AWS Lambda architecture, triggers, and uses of automation.

![image](https://github.com/user-attachments/assets/3dc9ec21-cc83-432e-90ed-74e26f8d57be)

![image](https://github.com/user-attachments/assets/a85d2bdb-2a47-4a5f-ba40-eedca551536e)

**AWS EBS**

we paid extra attention to Amazon Elastic Block Store (EBS) during the modules 7 activities. The Case Study 12 entailed taking Lab 4 in which we learned how to create and manage EBS volumes. The laboratory assignments were to create an EBS volume and attach that volume to an EC2 instance and also mount the volume followed by snapshot creation and restoration. They achieved all the labs tasks and scored 25/25. This practical task explained the value of the persistent block storage in AWS and how EBS can be used to implement backup, recovery, and scalability. I answered the HTML9 Module 7 Knowledge Check to reinforce our studies and this tool confirmed that I was well informed when it comes to EBS use cases, types of volume, lifecycle and cost considerations with the final score standing at 100 percent.

![image](https://github.com/user-attachments/assets/0b00f803-7707-40cf-b169-b912c451fc21)

![image](https://github.com/user-attachments/assets/423394f4-a107-474b-87a2-cb8c4dfe0652)


