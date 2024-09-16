Projects

Hi and welcome to my portfolio.

Question? Email me at:
[lamthithuthao998@gmail.com](mailto:lamthithuthao998@gmail.com)

Project 1: 



Project 2: AWS Data Analytic Platform for the City of Vancouver

## Project Title: AWS Data Analytic Platform for Lost and Found Animal Data

## Objective:
The primary goal of this project is to implement a Data Analytic Platform (DAP) for the City of Vancouver using AWS services. The platform will manage and analyze Lost and Found Animal data for the years 2023 and 2024. By using AWS tools, we aim to optimize data storage, cleansing, analysis, and visualization, ensuring accurate and actionable insights for stakeholders.

<img width="873" alt="Screen Shot 2024-09-16 at 11 08 37" src="https://github.com/user-attachments/assets/d01e5b41-7bc4-4f9a-8b96-7f6b26ad1ee3">

## Dataset:
The dataset used in this project includes:
- **Lost Animal Information 2023-2024**: Data regarding animals reported lost in Vancouver. Includes attributes like animal ID, report date, description, status, and location.

Additional datasets:
- **Animal Services Staff Data**: Internal staff metrics and performance data.
- **Register Reports**: Historical records of lost animal cases.

## Methodology:
1. **Data Discovery**: Identified and gathered relevant datasets for the Lost and Found Animal information for 2023 and 2024.
2. **Data Storage Design**: Structured a scalable storage solution using AWS S3 to store the collected datasets.
3. **Data Preparation**: Prepared and formatted the data to ensure consistency and compatibility for analysis.
4. **Data Ingestion**: Uploaded the prepared data to designated S3 buckets (Landing/2023 and Landing/2024 folders).
5. **Data Cleaning**: Used AWS Glue DataBrew to remove errors, duplicates, and inconsistencies in the dataset.
6. **Data Structuring**: Transformed and standardized the schema of the cleaned data.
7. **Data Analysis**: Analyzed the cleaned data using Amazon Athena to extract insights on lost animals and generate relevant statistics.
8. **Data Visualization**: Visualized the analysis results using Google Sheets to produce a clear and comprehensive report.
9. **Data Publishing**: Published the final analysis and insights using AWS EC2 for stakeholder access.

## Tools and Technologies:
- **AWS S3**: For data storage.
- **AWS Glue**: For data cleansing and structuring.
- **Amazon Athena**: For data querying and analysis.
- **Google Sheets**: For data visualization.
- **AWS EC2**: For data publishing and sharing results.
- **Python**: For any required data manipulation and scripting.

## Deliverables:
- **Data Analytic Platform (DAP)**: A fully functional platform built on AWS to manage Lost and Found Animal data for the City of Vancouver.
- **Data Visualizations**: Bar charts and graphs showing the results of data analysis, such as Lost Animal Reporting Rate and year-wise trends.
- **Comprehensive Report**: A detailed report summarizing the data analysis process, findings, and actionable insights for stakeholders.

## Project Phases:
1. **Data Discovery**: Sourcing and understanding the dataset from the City of Vancouver’s open data portal.
2. **Data Storage**: Setting up AWS S3 buckets for structured data storage.
3. **Data Ingestion**: Uploading formatted data to the appropriate S3 folders.
4. **Data Cleaning**: Using AWS Glue to remove inconsistencies and standardize data.
5. **Data Structuring**: Applying schema transformations and standardizing columns.
6. **Data Analysis**: Querying the cleaned data using Amazon Athena to extract insights.
7. **Data Visualization**: Using Google Sheets to create visual representations of the analysis.
8. **Data Publishing**: Publishing the results on AWS EC2 for access by stakeholders.

## Insights and Findings:
The analysis provided key insights into the Lost and Found Animal data:
- **Trends**: A clear trend in the number of lost animals year over year.
- **Survival Rate**: Analysis of the lost-to-found ratio of animals across different categories.

## Conclusion:
This project successfully demonstrates the development of a scalable data analytic platform using AWS to manage and analyze Lost and Found Animal data. The platform provides insights into operational data that can be used by the City of Vancouver to improve animal control services and resource allocation.

## Future Work:
- **Predictive Modeling**: Building models to predict future trends based on the historical data.
- **Improved Data Integration**: Including additional datasets from other departments for more comprehensive analysis.



