# Projects as a data analyst

Hi and welcome to my portfolio.

Question? Email me at:
[lamthithuthao998@gmail.com](mailto:lamthithuthao998@gmail.com)

## Project 1: University Canada West - Academic Accommodations Data Analytic Platform

### Project Overview:
This project implements an AWS-based Data Analytic Platform to manage and analyze the Academic Accommodation data. It leverages various AWS services like S3, Glue, Athena, and EC2 to clean, process, and analyze data related to academic accommodations and services. The platform provides end-to-end data processing, from ingestion to visualization, ensuring seamless data management.

### Objective:
The primary objectives of this platform are:
- **Data Migration**: Move large datasets related to academic accommodations to a secure and scalable storage solution in AWS.
- **Data Cleaning and Structuring**: Use AWS Glue to automate the process of data cleaning and structuring.
- **Data Analysis**: Perform SQL-based data analysis using Amazon Athena to gain insights into the university's accommodation services.
- **Data Replication**: Implement cross-region data replication using AWS S3 to ensure high availability.
- **Data Security**: Use AWS KMS to encrypt sensitive data and manage access securely.
- **Data Visualization**: Create meaningful visualizations using Google Sheets or other tools for stakeholders to interpret data insights.
  
<img width="866" alt="Screen Shot 2024-09-16 at 11 18 47" src="https://github.com/user-attachments/assets/e9c7e810-5041-476d-a475-a208b20590b9">


### Dataset:
The data used in this project includes various records related to:
- **Accessibility Services**: Data related to academic support provided to students.
- **Student Demographics**: Data on students, including age, gender, and other demographic details.
- **Student Records and Complaints**: Focus on the specifics of requests and issues encountered by students during the accommodation process.
- **Policy Impact Analysis**: Evaluate the impact of institutional policies on the effectiveness of accommodations.
- **Registrar**: Include records of students' academic and accommodation-related data, tracked through the registrar.
- **Student Affairs and Services**: Address the broader support provided to students in both academic and non-academic contexts.
  
### Tools and Technologies:
The platform is built on various AWS services to achieve its objectives. Below are the key AWS tools and technologies used in the project:
1. **AWS S3**: For scalable storage of raw and processed data related to academic accommodations.
2. **AWS Glue DataBrew**: For cleaning and transforming raw data into a structured format.
3. **Amazon Athena**: For querying the data stored in S3 using SQL queries.
4. **AWS EC2**: To host web servers and processing servers for making the processed data accessible.
5. **AWS VPC**: For setting up a secure virtual private cloud (VPC) to ensure data is processed in a secure environment.
6. **AWS S3 Replication**: For cross-region replication of data to ensure disaster recovery and high availability.
7. **AWS CloudWatch**: For monitoring AWS resources and keeping track of costs.
8. **AWS CloudTrail**: For logging and auditing all API calls and changes made to the platform.
9. **AWS KMS**: For encrypting sensitive data to ensure security and compliance.

### Project Structure and Workflow:
1. **Data Ingestion with AWS S3**:
The raw data related to student accommodation services is ingested into AWS S3. Different folders such as Accessibility Services, Student Demographics, and Student Records and Complaints are created within the S3 bucket to store the respective data.

**Bucket Name**: academic-accommodations-accessibility-lamthithuthao
**Landing Folders**:
- Accessibility Services 
- Student Demographics
- Registrar Records
- Policy Impact Analysis
- Registrar
- Student Affairs and Services
- Student Records and Complain

<img width="1440" alt="AWS S3" src="https://github.com/user-attachments/assets/3f4031ae-ec8b-41d5-b1e8-c644c07f2333">


2. **Data Cleaning using AWS Glue**:
The data ingested into S3 is cleaned and structured using AWS Glue. This includes renaming columns for clarity and performing data transformations. Glue’s data cleaning capabilities help ensure that the data is formatted and prepared for analysis.

**AWS Glue Job**: academic-accommodation-cleaning-lamthithuthao
**Steps Performed**:
- Rename fields (e.g., FirstName to AccommodationFirstName).
- Remove duplicates and handle missing values.
- Aggregate data where necessary.

<img width="1440" alt="ETL" src="https://github.com/user-attachments/assets/be090af9-bbf3-4a30-87da-1d7a9b2fd789">


3. **Data Analysis with Amazon Athena**:
Amazon Athena is used to query the cleaned data and perform analysis on student demographics and academic accommodations. The results from these queries are used to provide insights into student support services.

**Database**: academic_accommodation_database
**Tables**: academic_accommodation_table_lamthithuthao

**Sample Query**:
- sql
- Copy code
- SELECT year, apr FROM academic_accommodation_table_lamthithuthao LIMIT 10;

<img width="1440" alt="Athena " src="https://github.com/user-attachments/assets/b4f402c7-e53a-4023-8ee5-71408fa16084">


4. **Infrastructure with AWS VPC and EC2**:
The platform leverages AWS VPC for secure networking and AWS EC2 instances to host web servers and general-purpose servers. This ensures the processed data can be published and shared securely across the network.

- **VPC Name**: Aca_Acommo_VPC_TT_Thao-vpc.

- **Subnets**: Configured for public and private access.

<img width="1440" alt="VPC" src="https://github.com/user-attachments/assets/89b4f4bd-e372-40da-bcda-ba02a1d6603e">


- **Web Server**: Hosts the web application that allows stakeholders to access the data results.

<img width="1440" alt="EC2_Web Server" src="https://github.com/user-attachments/assets/7127f83e-3731-47ce-af02-add85d377f9c">


- **General Server**: Performs further data analysis and generates visualizations as needed.

<img width="1440" alt="EC2_General Server" src="https://github.com/user-attachments/assets/7ca8486e-ea98-499d-9df6-2c7fee3c38ff">


5. **Data Replication with AWS S3**:
Data replication is enabled to ensure high availability and fault tolerance. The replication configuration copies objects between S3 buckets in the same or different AWS regions.

**Source Bucket**: academic-accommodations-accessibility-lamthithuthao

**Destination Bucket**: academic-accommodations-backup-thithuthao

<img width="1440" alt="Replication Rule" src="https://github.com/user-attachments/assets/0433c8c8-cb0b-4e7b-aa66-4200a524d932">


### Deliverables:
- **Ingested Data**: Stored in AWS S3 in well-structured folders.
- **Cleaned Data**: Processed and transformed using AWS Glue.
- **Query Results**: Data analyzed with Amazon Athena.
- **Infrastructure**: Hosted on AWS VPC and EC2 for secure access and processing.
- **Replication Setup**: Ensures data availability across regions.

### Future Improvements:
- **Predictive Analysis**: Build machine learning models to predict future accommodation requirements based on historical trends.
- **Real-time Data Processing**: Incorporate AWS Lambda and Kinesis for real-time data processing.
- **Advanced Visualization**: Use Amazon QuickSight to create interactive dashboards for deeper insights into accommodation data.

### Conclusion:
The Academic Accommodation Data Analytic Platform successfully leverages AWS services to streamline the management and analysis of academic accommodation data. By using AWS S3 for scalable storage, AWS Glue for data cleaning, Amazon Athena for querying, and AWS EC2 for publishing results, the platform provides a secure, scalable, and efficient solution for handling large datasets. The implementation of S3 Replication ensures data availability and disaster recovery, while AWS VPC safeguards the platform's infrastructure. This platform offers valuable insights into student demographics and accommodation trends, improving decision-making and resource allocation at the university. Future enhancements, such as real-time processing and predictive analytics, will further expand its capabilities.



## Project 2: AWS Data Analytic Platform for the City of Vancouver

### Project Title: AWS Data Analytic Platform for Lost and Found Animal Data

### Project Overview: 
 The primary goal of this project is to implement a Data Analytic Platform (DAP) for the City of Vancouver using AWS services. The platform is designed to manage and analyze public service data, specifically focusing on the Animal Control department’s datasets - Lost and Found Animal data for the years 2023 and 2024. By using AWS tools, we aim to optimize data storage, cleansing, analysis, and visualization, ensuring accurate and actionable insights for stakeholders.

### Objective:
The main objective of the project was to migrate and build a cloud-based data analytics platform on AWS. This platform was designed to handle large datasets from the City of Vancouver's Animal Control services, providing secure storage, automated processing, data analysis, and visual reporting. 
The key goals were:
- To formulate critical analytical questions to guide data collection and processing.
- To organize and structure the raw data from various sources into a unified format.
- To implement a fully automated data pipeline that performs ETL (Extract, Transform, Load) operations.
- To ensure the security and privacy of all datasets by applying AWS best practices for data governance.

<img width="873" alt="Screen Shot 2024-09-16 at 11 08 37" src="https://github.com/user-attachments/assets/d01e5b41-7bc4-4f9a-8b96-7f6b26ad1ee3">

### Dataset:
The dataset used in this project includes:
- **Lost Animal Information 2023-2024**: This dataset includes information about animals reported as lost in the City of Vancouver in the years 2023 and 2024. It is essential for understanding trends in lost animal reports and for answering questions related to the number of lost animals, reporting rates, and other factors. Data include attributes like animal ID, report date, description, status, and location.
- **Animal Control Office Staff Data**: This dataset contains information about the activities of the Animal Control Office staff, including their performance in handling lost animal cases. It can be used to assess staff productivity and efficiency in resolving lost animal cases.
- **Vancouver Animal Control Office Analysis Reports**: These are internal reports and metrics created for analyzing the overall performance of the Animal Control Office. The analysis may include the number of resolved cases, the average time taken to resolve a case, and the lost animal reporting trends for 2023 and 2024.
- **Register Reports (Historical Data)**: This dataset contains time sheets and historical logs related to lost and found animal cases in the City of Vancouver. It can be used to track how long cases remain unresolved and to study past trends in lost animal reports.
- **Lost Animal Reporting Rate (APR) Dataset**: This dataset calculates the Annual Percentage Rate (APR) of lost animals reported in the City of Vancouver. The APR dataset is used to analyze trends and provide insights on how the rate of lost animals changes over time.

### Methodology and Project Phases:
1. **Data Analytical Question Formulation**: The first step in the methodology was to formulate four key types of analytical questions:
- **Descriptive Analysis**: How many lost animal reports were submitted in 2023 and 2024?
- **Diagnostic Analysis**: What factors caused a spike in the number of lost animal reports?
- **Predictive Analysis**: How is the number of lost animal reports expected to change by the end of 2024?
- **Prescriptive Analysis**: What actions should the City of Vancouver take to reduce the number of lost animal reports?
  
2. **Data Discovery**: Identified and gathered relevant datasets for the Lost and Found Animal information for 2023 and 2024. In this step, we located the necessary datasets related to lost animals, staff activities, and internal reports of Vancouver Animal Control.

3. **Data Storage Design**: We design an effective and scalable storage solution using AWS S3. The structure consists of clearly organized folders for raw and processed data. Bucket Structure:
- **Landing Zone**: Raw data for 2023 and 2024.
- **Curated Zone**: Cleaned and processed data ready for analysis.

<img width="1440" alt="Lost Found Animal  - Landing Folders - 2024" src="https://github.com/user-attachments/assets/42d2d592-881e-4c7e-ab0c-ec03c20bc685">

<img width="1440" alt="Created Job - Data Cleaning" src="https://github.com/user-attachments/assets/54b5ae38-cdb1-4ff7-9a1f-f2e2e8b22241">


4. **Data Preparation**: Once data is collected, it is prepared by ensuring consistency and compatibility. This step involves formatting, cleaning, and structuring datasets to match the required standards. Tasks:
- Converting raw datasets into CSV format.
- Ensuring all fields are uniform and correct (e.g., AnimalID, ReportDate, AnimalName, etc.).
  
5. **Data Ingestion**: Uploaded the prepared data to designated S3 buckets (Landing/2023 and Landing/2024 folders).

6. **Data Cleaning**: We use AWS Glue DataBrew to identify and remove duplicates, handle missing values, correct data types, and standardize formats. This ensures the data is free from errors and inconsistencies.

<img width="1440" alt="Data Cleaning" src="https://github.com/user-attachments/assets/db52f69f-80ee-4af1-8bd5-d2d3bc801f42">

7. **Data Structuring**: After cleaning, the Data Structuring phase organizes the data into a clear schema, renaming columns for clarity, reordering them logically, and ensuring consistency across datasets (e.g., Lost Animal Reports for 2023 and 2024). The structured data is stored in AWS S3’s Curated Zone and validated with AWS Glue, ready for analysis using tools like Amazon Athena. This preparation ensures the data is accurate, reliable, and efficiently organized for downstream processing.

<img width="1440" alt="Data Structuring" src="https://github.com/user-attachments/assets/68bd7b88-f4a6-473c-9e4a-59817e82e906">

8. **Data Analysis**: Data analysis is done using Amazon Athena, where SQL queries are executed to extract insights.

**Example Query**:
- sql
- Copy code
- SELECT AnimalID, ReportDate, Status
- FROM animalcontrol_lostandfound_table
- WHERE Year = 2024 ORDER BY ReportDate;
=> The results of these analyses are used to calculate the lost animal Annual Percentage Rate (APR) and other performance metrics.

<img width="1440" alt="Amazon Athena" src="https://github.com/user-attachments/assets/083e6fbc-733b-4e5a-9cd5-ff82047f4ef3">

9. **Data Visualization**: The final analysis results are visualized using Google Sheets for clarity and ease of communication. Bar charts and other visual representations are created based on the analysis. The data visualizations are exported as PDF reports and shared with stakeholders.
  
10. **Data Publishing**: The processed datasets and visualization reports are published using AWS EC2, allowing external stakeholders to access the reports securely. The EC2 instances were created to host the files and reports, making them accessible via public IPs.

<img width="1440" alt="Screen Shot 2024-08-25 at 08 27 19" src="https://github.com/user-attachments/assets/952753a1-937f-4f50-9897-721d3b4bd8e3">

13. **Data Governance and Security**: Ensuring the security and governance of data is critical. AWS KMS (Key Management Service) is used to encrypt datasets, and S3 bucket permissions are tightly controlled to prevent unauthorized access.
- SSE-KMS encryption is applied to sensitive data.

<img width="1440" alt="KMS - Key" src="https://github.com/user-attachments/assets/7d6423c2-e6af-45cf-8f41-cde320503cf2">

- Replication rules and bucket versioning are used for backup and disaster recovery.

<img width="1440" alt="Replication rules " src="https://github.com/user-attachments/assets/aef1af14-1638-4f68-b3a7-a541a5c42330">


### Tools and Technologies:
- **AWS S3**: Organizing data into buckets and folders for efficient data retrieval during the analysis process -> The key storage service that handles datasets like Lost Animal Reports and staff performance logs.
- **AWS Glue**: Automating the data pipeline and ensuring that raw data is properly structured before analysis -> Glue ETL jobs ensure that the datasets are cleaned and transformed into a format ready for analysis.
- **AWS Glue DataBrew**: Identifying and removing duplicates, fixing inconsistencies, and formatting the data -> Cleans the raw data before it enters the structured storage (Curated Zone).
- **Amazon Athena**: Querying the Lost Animal Reports dataset to generate insights such as reporting trends and performance metrics -> Acts as the analysis engine, using SQL to query and analyze data directly from S3.
- **Google Sheets**: Creating bar charts, graphs, and other visual aids to represent the data analysis results -> Allows for easy creation of data visualizations to be shared with stakeholders.
- **AWS EC2**: Providing an environment to share final reports with stakeholders by hosting files and dashboards -> Acts as the server infrastructure for publishing data outputs.
- **AWS KMS (Key Management Service)**: Applying encryption to sensitive datasets in S3 buckets -> Protects data from unauthorized access and ensures compliance with security protocols.
- **AWS CloudWatch**: Tracking metrics like Estimated Charges and Number of Objects in S3 -> Helps monitor project costs and ensures efficient use of AWS resources.
- **AWS CloudTrail**: Monitoring all actions within the AWS environment -> Helps audit and log all actions taken on datasets to ensure security and governance.

### Deliverables:
- **Data Analytic Platform (DAP)**: A fully functional platform built on AWS to manage Lost and Found Animal data for the City of Vancouver. Also, Supports data ingestion, cleaning, transformation, and storage, ensuring scalability and security for future data needs.
- **Data Visualizations**: Visual representations of the data, including bar charts and graphs showing key metrics such as the Lost Animal Reporting Rate (APR) and year-wise trends for 2023 and 2024. These visualizations are created using Google Sheets and exported as PDFs for stakeholder review.
- **Comprehensive Report**: A detailed report summarizing the data analysis process, findings, and actionable insights drawn from the lost animal data. This report includes the methodology, analysis results, and recommendations, providing valuable information for stakeholders to improve Animal Control services.

### Insights and Findings:
The analysis provided key insights into the Lost and Found Animal data:
- **Trends**: A clear trend in the number of lost animals year over year.
- **Survival Rate**: Analysis of the lost-to-found ratio of animals across different categories.

### Conclusion:
The implementation of the AWS Data Analytic Platform for the City of Vancouver provides a scalable, secure, and efficient solution for managing and analyzing lost and found animal data. Utilizing AWS services such as S3, Glue, Athena, and EC2, the platform enables efficient handling of large datasets and delivers valuable insights. The 13-step process, from data discovery to visualization and publishing, ensures seamless migration and automation, improving the operational efficiency of the Animal Control department. The platform supports data-driven decision-making and is designed to scale as the city’s data needs grow, laying the foundation for future enhancements like real-time processing and predictive analytics.

### Future Work:
- **Predictive Analytics**: Develop machine learning models using Amazon SageMaker to predict trends such as the likelihood of lost animals being found based on historical data, providing more proactive approaches to animal control management.
- **Enhanced Data Governance**: Strengthen data governance policies with the addition of AWS CloudTrail logs and custom compliance reporting, ensuring that the platform remains secure, compliant, and auditable as it scales.
- **Advanced Data Visualizations**: Integrate more sophisticated visualization tools, such as Amazon QuickSight, to create interactive dashboards that provide deeper insights and improve user engagement.

### Author
**Lam Thi Thu Thao**
University Canada West
Course: BUSI 653 – Cloud Computing Technologies
Instructor: Prof. Mahmood Mortazavi Dehkordi
Date: August 16, 2024
