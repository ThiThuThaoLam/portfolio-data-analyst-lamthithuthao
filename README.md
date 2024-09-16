# Projects as a data analyst

Hi and welcome to my portfolio.

Question? Email me at:
[lamthithuthao998@gmail.com](mailto:lamthithuthao998@gmail.com)

## Project 1: University Canada West - Academic Accommodations Data Analytic Platform

### Project Overview:
This project implements an AWS-based Data Analytic Platform to manage and analyze the Academic Accommodation data. It leverages various AWS services like S3, Glue, Athena, and EC2 to clean, process, and analyze data related to academic accommodations and services. The platform provides end-to-end data processing, from ingestion to visualization, ensuring seamless data management.

### Objective:
The objective of this project is to design and implement a scalable, automated data pipeline for managing student accommodation data. This platform is used to clean, process, and analyze data related to accessibility services, student demographics, and accommodation records.

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
1. **AWS S3**: Used for data storage, including raw and processed data.
2. **AWS Glue**: Utilized for data cleaning, structuring, and transformation.
3. **Amazon Athena**: Used for querying and analyzing the data.
4. **AWS EC2**: Hosts web and general servers to process the data and make it accessible.
5. **AWS VPC**: Provides a secure virtual network for communication between AWS resources.
6. **AWS S3 Replication**: Ensures data replication across different AWS regions for data availability.

### Project Phases:
1. **Data Ingestion with AWS S3**:
The raw data related to student accommodation services is ingested into AWS S3. Different folders such as Accessibility Services, Student Demographics, and Student Records and Complaints are created within the S3 bucket to store the respective data.

**Bucket Name**: academic-accommodations-accessibility-lamthithuthao
**Folders**:
- Accessibility Services
- Student Demographics
- Registrar Records
- Policy Impact Analysis
- Registrar
- Student Affairs and Services
- Student Records and Complain

2. **Data Cleaning using AWS Glue**:
The data ingested into S3 is cleaned and structured using AWS Glue. This includes renaming columns for clarity and performing data transformations. Glue’s data cleaning capabilities help ensure that the data is formatted and prepared for analysis.

**AWS Glue Job**: Academic-Accommodation-StudentDemographic-ETL-LamThiThuThao
**Steps Performed**:
- Rename fields (e.g., FirstName to AccommodationFirstName).
- Remove duplicates and handle missing values.
- Aggregate data where necessary.

3. **Data Analysis with Amazon Athena**:
Amazon Athena is used to query the cleaned data and perform analysis on student demographics and academic accommodations. The results from these queries are used to provide insights into student support services.

**Database**: academic_accommodation_database
**Tables**: academic_accommodation_table_lamthithuthao
**Sample Query**:
- sql
- Copy code
- SELECT year, apr FROM academic_accommodation_table_lamthithuthao LIMIT 10;

4. **Infrastructure with AWS VPC and EC2**:
The platform leverages AWS VPC for secure networking and AWS EC2 instances to host web servers and general-purpose servers. This ensures the processed data can be published and shared securely across the network.

- **VPC Name**: Aca_Acommo_VPC_TT_Thao-vpc.

- **Subnets**: Configured for public and private access.

- **Web Server**: Hosts the application for data access.

- **General Server**: Provides processing capabilities for large datasets.

5. **Data Replication with AWS S3**:
Data replication is enabled to ensure high availability and fault tolerance. The replication configuration copies objects between S3 buckets in the same or different AWS regions.

**Source Bucket**: academic-accommodations-accessibility-lamthithuthao

**Destination Bucket**: academic-accommodations-backup-thithuthao

### Deliverables:
- **Ingested Data**: Stored in AWS S3 in well-structured folders.
- **Cleaned Data**: Processed and transformed using AWS Glue.
- **Query Results**: Data analyzed with Amazon Athena.
- **Infrastructure**: Hosted on AWS VPC and EC2 for secure access and processing.
- **Replication Setup**: Ensures data availability across regions.

### Future Improvements:
- **Predictive Analysis**: Build machine learning models to predict future accommodation requirements based on historical trends.
- **Real-time Data Processing**: Incorporate AWS Lambda and Kinesis for real-time data processing.



## Project 2: AWS Data Analytic Platform for the City of Vancouver

### Project Title: AWS Data Analytic Platform for Lost and Found Animal Data

### Objective:
The primary goal of this project is to implement a Data Analytic Platform (DAP) for the City of Vancouver using AWS services. The platform will manage and analyze Lost and Found Animal data for the years 2023 and 2024. By using AWS tools, we aim to optimize data storage, cleansing, analysis, and visualization, ensuring accurate and actionable insights for stakeholders.

<img width="873" alt="Screen Shot 2024-09-16 at 11 08 37" src="https://github.com/user-attachments/assets/d01e5b41-7bc4-4f9a-8b96-7f6b26ad1ee3">

### Dataset:
The dataset used in this project includes:
- **Lost Animal Information 2023-2024**: Data regarding animals reported lost in Vancouver. Includes attributes like animal ID, report date, description, status, and location.

Additional datasets:
- **Animal Services Staff Data**: Internal staff metrics and performance data.
- **Register Reports**: Historical records of lost animal cases.

### Methodology:
1. **Data Discovery**: Identified and gathered relevant datasets for the Lost and Found Animal information for 2023 and 2024.
2. **Data Storage Design**: Structured a scalable storage solution using AWS S3 to store the collected datasets.
3. **Data Preparation**: Prepared and formatted the data to ensure consistency and compatibility for analysis.
4. **Data Ingestion**: Uploaded the prepared data to designated S3 buckets (Landing/2023 and Landing/2024 folders).
5. **Data Cleaning**: Used AWS Glue DataBrew to remove errors, duplicates, and inconsistencies in the dataset.
6. **Data Structuring**: Transformed and standardized the schema of the cleaned data.
7. **Data Analysis**: Analyzed the cleaned data using Amazon Athena to extract insights on lost animals and generate relevant statistics.
8. **Data Visualization**: Visualized the analysis results using Google Sheets to produce a clear and comprehensive report.
9. **Data Publishing**: Published the final analysis and insights using AWS EC2 for stakeholder access.

### Tools and Technologies:
- **AWS S3**: For data storage.
- **AWS Glue**: For data cleansing and structuring.
- **Amazon Athena**: For data querying and analysis.
- **Google Sheets**: For data visualization.
- **AWS EC2**: For data publishing and sharing results.
- **Python**: For any required data manipulation and scripting.

### Deliverables:
- **Data Analytic Platform (DAP)**: A fully functional platform built on AWS to manage Lost and Found Animal data for the City of Vancouver.
- **Data Visualizations**: Bar charts and graphs showing the results of data analysis, such as Lost Animal Reporting Rate and year-wise trends.
- **Comprehensive Report**: A detailed report summarizing the data analysis process, findings, and actionable insights for stakeholders.

### Project Phases:
1. **Data Discovery**: Sourcing and understanding the dataset from the City of Vancouver’s open data portal.
2. **Data Storage**: Setting up AWS S3 buckets for structured data storage.
3. **Data Ingestion**: Uploading formatted data to the appropriate S3 folders.
4. **Data Cleaning**: Using AWS Glue to remove inconsistencies and standardize data.
5. **Data Structuring**: Applying schema transformations and standardizing columns.
6. **Data Analysis**: Querying the cleaned data using Amazon Athena to extract insights.
7. **Data Visualization**: Using Google Sheets to create visual representations of the analysis.
8. **Data Publishing**: Publishing the results on AWS EC2 for access by stakeholders.

### Insights and Findings:
The analysis provided key insights into the Lost and Found Animal data:
- **Trends**: A clear trend in the number of lost animals year over year.
- **Survival Rate**: Analysis of the lost-to-found ratio of animals across different categories.

### Conclusion:
This project successfully demonstrates the development of a scalable data analytic platform using AWS to manage and analyze Lost and Found Animal data. The platform provides insights into operational data that can be used by the City of Vancouver to improve animal control services and resource allocation.

### Future Work:
- **Predictive Modeling**: Building models to predict future trends based on the historical data.
- **Improved Data Integration**: Including additional datasets from other departments for more comprehensive analysis.



