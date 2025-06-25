# data-analyst-ang
# Descriptive Analysis of Annual Retention Records
# Project Title:
Understanding the demographics associated with the annual retention records of students in UCW
# Objectives:
To analyze and evaluate by:
- Obtaining information from raw academic and performance sources
- Using relevant data transformation methods (like profiling, cleaning and enriching in the AWS platform)
- Feeding the clean data to AWS to obtain analytical insight
- The detection of quality problems in data, data gaps, and recommendations for the improvement of quality
# Dataset:
1. RetentionID - A unique identifier assigned to each retention record.
2. StudentID - A unique code representing each student in the dataset.
3. RetentionStatus -  Indicates the current retention outcome or classification (e.g., retained, dropped out).
4. RetentionDate - The date on which the retention status was recorded or updated.

   The table below is a screenshot of the dataset:

![image](https://github.com/user-attachments/assets/35fadced-b881-4de7-9ed0-ac389d52b5ee)

# Methodology
 1-	Data Collection and Preparation:

 Tools used: Used the AWS server S3 bucket to store the dataset.

 ![image](https://github.com/user-attachments/assets/34fa2520-7be4-455f-ab02-fe343bbc2f61)

Clearing: Used AWS GlueBrew for cleaning the dataset to find a single source of truth.

 ![image](https://github.com/user-attachments/assets/3358e465-359e-4ece-8345-9d99a4c6bc22)

2- Data Statistics:

Used an Excel file to calculate the total number of students who dropped out and were retained per year.

![image](https://github.com/user-attachments/assets/aab98a2a-342b-4222-9c9c-2829fdb43a08)

Applied the calculation in the server using AWS Athena

![image](https://github.com/user-attachments/assets/33dd9b3d-f8bb-486f-aa6d-b6772843e935)

3- Data Visualization

The image below shows the data visualization using AWS GlueBrew. In which we joined Student Demographics with Retention Records.

![image](https://github.com/user-attachments/assets/519ab618-4659-4845-a6fb-504b0ca226c9)

4- Student Segmentation

Segmented students based on the retained and the dropped out.

5- Insights and Findings:

A. Business Focus:
- The project investigates student retention patterns by analyzing demographic and academic data.
- The central business question is:
"Which student demographics are associated with higher or lower retention rates?"

B. Key Data Metrics:
- Annual Retention Rate is the main performance metric used to assess student persistence.
- Other important metrics include:
   Retention rate by enrollment type (e.g., full-time vs part-time)
   Predicted probability of dropout

C. Data Integration:
- The project combines data from two key datasets:
- Student Demographics (Age, Gender, Ethnicity, Enrollment Status)
- Retention Records (Status and Dates)
- Inner Join was used to enrich the data for analysis.

6- Recommendations
- Add a Centralized Data Dictionary Sheet:
Include a dedicated sheet that clearly defines each column (e.g., StudentID, RetentionStatus, etc.), data types, and example values. This improves clarity and supports future data scaling or automation.

# Tools and Techniques

a. Amazon S3 (Simple Storage Service)
- Used to store raw, cleaned, and curated academic datasets.
- Buckets shown: academic-raw-angela, academic-cln-angela, academic-etl-angela, academic-cur-angela.

b. AWS Glue
- Managed ETL service for data transformation and integration.
- Includes both Glue Jobs and Glue Data Catalogue for managing and tracking datasets.

c. AWS Glue DataBrew: No-code data preparation tool used to visually clean and transform raw academic data.

d. Amazon Athena: Serverless query service used to analyze data directly in S3 using SQL.

![image](https://github.com/user-attachments/assets/35c06133-900c-4904-8498-5c5820209291)

# Deliverables

![image](https://github.com/user-attachments/assets/8f185421-0546-4d2b-aa8f-a81b47d7973a)

# AWS Deployment and Service Models
![image](https://github.com/user-attachments/assets/947adcca-4d30-4500-a81f-a5b4aed9c880)
![Screenshot (501)](https://github.com/user-attachments/assets/c399a875-9251-46b7-87c9-389e24131b3a)
![Screenshot (502)](https://github.com/user-attachments/assets/a04fdf11-e25f-4dbe-bbfa-1b23a01e885a)
![Screenshot (503)](https://github.com/user-attachments/assets/8fb29a8b-1078-4ca0-869e-f09942f8f13c)

I used Draw.io to design a clear, structured diagram comparing cloud deployment models—Private, Public, Hybrid, and Multi-Cloud—focusing on their key differences in infrastructure location, access management, and security responsibilities. I organized the diagram to highlight how cloud solutions (like AWS) offer more flexibility and scalability than traditional on-premises setups, using real-world examples like virtual servers in Virginia or AWS's global infrastructure. This visual helped reinforce the concepts from my case study, making complex cloud architectures easier to understand at a glance.
# AWS Cost Analysis 
![image](https://github.com/user-attachments/assets/a8268f04-e830-431e-8df7-94e51adab065)
![image](https://github.com/user-attachments/assets/a662d716-a5f9-4f28-a81d-bbb56aaaf4a8)
![image](https://github.com/user-attachments/assets/b1b90d5e-e6b1-43f4-9932-3cefd5da8d8a)
![image](https://github.com/user-attachments/assets/ff8bd495-217d-4337-877f-b52c03dfcac3)
I analyzed Case Study #4 on Delaware North's cloud migration to AWS, which highlights their shift from on-premises data centers to AWS, resulting in a 30% server reduction, cost savings via EC2 Reserved Instances, and improved operational efficiency. Additionally, I reviewed Case Study #5 and completed the AWS Academy Module 2 Knowledge Check.
# AWS Global infrastructure
![image](https://github.com/user-attachments/assets/c08e235a-8ced-4e7f-92ce-409e9a226959)
![image](https://github.com/user-attachments/assets/585b6f6b-3274-42d3-b549-b779b346f997)
Case Study #7 deepened my understanding of AWS's global architecture—particularly Regions, Edge Locations, and the shared security model between AWS and clients like UCIV for low-latency data delivery. 
# AWS IAM 
![image](https://github.com/user-attachments/assets/ab5d9469-092b-4c48-af5d-7765f2d9f110)
This diagram illustrates the shared responsibility model between AWS and UCW, showing UCW's role in managing EC2 instances, software security, and data protection while AWS handles the underlying infrastructure. It also maps these responsibilities across Availability Zones (1-8) and categorizes the dataset environment into software, platform, and network components.
# AWS VPC
![image](https://github.com/user-attachments/assets/7a1532f3-3a05-438b-8ceb-a3dff5919a75)
# AWS Lambda 
![image](https://github.com/user-attachments/assets/cebdbd78-f659-49f3-9b32-7d5f5403e6bb)
I created Lambda; however, the instance didn't stop.
# AWS EBS
![image](https://github.com/user-attachments/assets/ca538ac6-bbea-4c67-a4bf-593465feb6b4)
![image](https://github.com/user-attachments/assets/e643b49d-4937-42ae-9ada-f352aac6ebc4)
While creating EC2, an error message occured saying the code was not found.
