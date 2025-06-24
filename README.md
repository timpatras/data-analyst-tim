📘 Week 2 Portfolio: Design of Academic Data Lake
Task Title:
Designing a Scalable Academic Data Lake Architecture on AWS
Objective:
To organize and classify academic datasets into a structured AWS S3 bucket system using appropriate storage classes, regional deployment, and tagging strategies for efficient data retrieval and cost optimization.
________________________________________
Summary of Activities
✅ 1. Dataset Classification and Folder Structure
Five key datasets were defined:
•	Course Enrollments
•	Course Completion Records
•	Student Demographics
•	Retention Records
•	Faculty Workload
Each dataset was organized under the S3 bucket academic-raw-tim with clearly structured folder paths including Year=25 and Quarter=Q2 to support time-based partitioning and data lifecycle management.
✅ 2. Region Selection
All datasets were deployed in the Virginia region (US East 1) to take advantage of:
•	Lower latency for academic applications
•	Cost-efficient storage and compute
✅ 3. Metadata Tagging
Each dataset was tagged for governance using key metadata fields like:
•	Owner = Academic
•	Write Frequency = daily/weekly/monthly
•	Read Frequency = daily/weekly/monthly
This helps with data cataloging, cost allocation, and automated lifecycle policies.
✅ 4. Storage Class Assignment
Datasets were assigned a combination of:
•	Standard: For frequently accessed data (e.g., Course Enrollments)
•	Infrequent Access (IA): For less-accessed data (e.g., Retention Records)
This design balances performance and storage cost based on usage patterns.
________________________________________
Key Learnings & Reflections
•	Learned how to apply data governance best practices through folder structuring, tagging, and storage class assignment.
•	Developed a better understanding of AWS S3 optimization techniques for academic data environments.
•	Gained hands-on experience in partitioning datasets for scalable analytics and efficient querying.
Week 3 Portfolio: Dataset Profiling and Cleaning Design
Task Title:
Designing Data Profiling and Cleaning Strategy for Academic Datasets
Objective:
To identify potential data quality and structural issues across academic datasets and apply appropriate profiling and cleaning techniques to ensure consistency, accuracy, and readiness for analytical processing.
________________________________________
Summary of Activities
✅ 1. Dataset Profiling Conducted
Performed profiling on:
•	Student Demographics
o	Columns profiled: StudentID, Age, Gender, Ethnicity
o	Result: No structural or data quality issues found.
•	(Other datasets not specified in profiling sheet—assumed clean or pending profiling)
✅ 2. Identification of Common Issues
Based on second sheet analysis, the team studied potential issues such as:
•	Data Structure Issues:
o	Nested fields
o	Inconsistent schemas
o	Mixed data types
o	Multi-valued fields
•	Data Quality Issues:
o	Missing data
o	Duplicate entries
o	Inconsistent naming/formatting
o	Incorrect data entries
✅ 3. Cleaning Techniques Applied or Planned
•	For Structural Issues:
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
Tools & Technologies Used
•	Excel for manual profiling and issue documentation
•	Planned Tools: Python (Pandas), AWS Glue for automated cleaning in future stages
________________________________________
Reflection
•	Understood how profiling serves as the foundation for data cleaning.
•	Learned to categorize and apply different cleaning strategies based on type of issue.
•	Realized that even if data appears clean, validation checks are essential before ingestion or analysis.

Week 4 Portfolio: ETL Design and Implementation on AWS
Task Title:
Designing and Implementing an ETL Pipeline with Cost Monitoring and Data Catalog Integration
Objective:
To develop a visual and functional ETL process on AWS for profiling and enriching academic datasets. This includes defining business objectives, evaluating costs, integrating CloudWatch alarms, and utilizing AWS Glue and Athena for querying and analysis.
________________________________________
Summary of Activities
✅ 1. Cost Evaluation of Dataset Profiling and Cleaning
•	Assessed ingestion and cleaning costs of datasets using the AWS Pricing Calculator.
•	Projected low monthly costs for storing and processing academic data due to efficient use of S3 Standard-IA and optimized request patterns.
✅ 2. ETL Process Design
•	Created a Visual ETL diagram using draw.io to outline:
o	Data ingestion from raw S3 bucket
o	Profiling, cleaning, and enrichment stages
o	Storage in curated zones
o	Query layer setup using AWS Athena
•	Defined system-level roles for User, Curated, and Data Catalog in the ETL workflow.
✅ 3. Business Questions Defined
•	Focused on enabling queries to answer:
o	What are the demographic patterns of enrolled students?
o	How does retention vary by faculty workload?
o	Which courses have the highest completion rates?
✅ 4. Data Enrichment
•	Enriched raw data by:
o	Standardizing inconsistent formats
o	Mapping and correcting invalid values
o	Creating derived columns to support analysis (e.g., age group, completion status)
✅ 5. ETL Implementation
•	Implemented the designed ETL process using:
o	AWS Glue for cleaning and cataloging
o	S3 for staging and storing enriched datasets
o	AWS Athena for validation through SQL queries
✅ 6. Monitoring with CloudWatch
•	Set up CloudWatch alarms to:
o	Notify if costs exceed thresholds
o	Track number of ETL jobs and data transfer activity
________________________________________
Tools & Technologies Used
•	AWS Glue
•	AWS S3 (raw and curated layers)
•	AWS Athena
•	AWS CloudWatch
•	Draw.io for ETL diagramming
________________________________________
Reflection
This week marked the transition from design to implementation. I gained practical experience with AWS Glue and CloudWatch, and saw how critical monitoring is for cost and performance optimization. I also reinforced my understanding of aligning business questions with ETL outputs to support data-driven decision-making.
AWS Deployment and Service Models 
The activity of the week aimed at studying the AWS Deployment and Service models with more emphasis on the contrast between the traditional computing infrastructure and the emerging cloud-based solutions. The first case study focused on the difference between the dataset location, access, and privacy of the traditional models hosted by UCW premises or AWS Cloud models, which offers the global reach within the network, IAM-based control access, and control privacy features. The second case study discussed four cloud deployment models which are; Private cloud, Public cloud, Hybrid cloud, and Multi-Cloud. These models imply different trade-offs in the access control, distribution in datasets and privacy protection via policies. The third case study was about Cloud Service Models that included Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS). This was explained on the impact it has on the location of dataset, complexity of Accessibility, and the control of privacy by the user. Finally, I managed to take and pass the AWS Academy Cloud Foundations Module 1 Knowledge Check scoring 100 out of 100 and proving my knowledge of the deployment principles described.

