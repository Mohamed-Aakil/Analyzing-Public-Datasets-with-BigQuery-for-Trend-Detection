# Analyzing-Public-Datasets-with-BigQuery-for-Trend-Detection 

## Introduction ##
This report presents a comprehensive analysis of public datasets using Google Cloud's BigQuery to detect emerging trends. The project was carried out as part of the INFO 607 course during Spring 2024. The team members involved in this project were Abhishek Baj, Hassaan Alvi, Mohamed Shehaf Aakil, and Priyanka Choudhary. The primary goal was to leverage BigQuery to process large datasets efficiently and provide actionable insights through advanced data analytics and visualizations across various sectors such as healthcare, finance, and social media.

# BigQuery as a Premier Data Warehouse Solution ##
BigQuery offers robust data analysis capabilities, handling large datasets with ease. Its serverless architecture eliminates the need for infrastructure management, allowing seamless scaling. The pay-as-you-go pricing model ensures cost-effectiveness and optimized resource utilization. In a data-intensive world where exponential data generation occurs through social media, IoT, and transactions, BigQuery provides efficient query processing and quick insights from large datasets, facilitating data-driven decision-making and offering a competitive edge in fast-paced markets.

## Project Scope ##
In-Scope
•	Comprehensive data analysis using BigQuery public datasets.
•	Advanced SQL data manipulations and trend analysis.
•	Integration with Google Data Studio for visualizations.
Out-of-Scope
•	Integration with non-Google Cloud services.
•	Real-time data processing or streaming analytics.

## Project Plan ##
Problem Statement
The goal is to examine public datasets and generate actionable insights using BigQuery, organized into several sections: initial exploration, detailed exploration, tracking trends, and assessing impacts in various sectors.
Setup and Preliminary Learning
•	Access and set up Google Cloud Platform and BigQuery accounts.
•	Explore BigQuery documentation and Google Cloud training modules.
•	Engage with online courses on BigQuery SQL and Google Cloud services.
Introduction to Generative AI
•	Research Generative AI technologies for data analysis.
•	Explore Google Cloud APIs and tools for Generative AI, such as Vertex AI.
•	Select relevant datasets in BigQuery.
•	Design initial queries to establish data baselines.
•	Plan specific Generative AI tasks for the project.

## Software and Hardware ##
Google BigQuery and Google Cloud Platform
•	Scalable and serverless: Efficient data handling without infrastructure concerns.
•	Managed cloud service: No physical hardware needed.
•	Focus on data analysis: Reduced overhead, streamlined data operations.
Additional Tools
•	Google Data Studio: For data visualization.
•	Vertex AI: For machine learning tasks.
•	Google Cloud Storage: For data storage and management.

## Experimentation Plan ##
Data Preparation and Integration
•	Data access: Utilize public datasets in Google BigQuery.
•	Data cleansing: Remove duplicates, correct errors, fill missing values.
•	Data schema setup: Define schema to support analysis needs.

## Datasets & Tables##
Table names are represented as follows:
•	Current project <dataset> . <table>
•	Different Project <project> : <dataset> . <table> 
Example: publicdata:samples.wikipedia
 
## Loading Data Using Web Browser ##
•	Upload from local disk or from Cloud Storage
•	Start the Web browser
•	Select Dataset
•	Create table and follow the wizard steps 
 
## Loading Data Using bq Tool ##
“Bq load” command
Syntax
 
•	If not specified, the default file format is CSV (comma separated values)
•	The files can also use newline delimited JSON format
•	Schema
o	Either a filename or a comma-separated list of column_name:datatype pairs that described the file format
•	Data source may be on local machine or on Cloud Storage

## Loading Limitations ##
•	1000 imports jobs per table per day
•	10,000 import jobs per project per day
•	File size (for both CSV and JSON)
o	1GB for compressed file
o	1TB for uncompressed file
	4GB for uncompressed CSV with newlines in strings
•	10,000 files per import job
•	1TB per import job

## Query Development and Execution ## 
•	Query formulation: Develop SQL queries for trend exploration.
•	Performance optimization: Optimize queries for efficient processing.
•	Iterative testing: Test and refine queries for accuracy.

## Analysis and Visualization ##
•	Data analysis: Identify patterns, trends, and anomalies.
•	Data visualization: Create visual representations with Google Data Studio.
•	Advanced tools integration: Use AI Platform for predictive modeling.

## Security and Compliance ##
•	Data usage guidelines: Adhere to ethical considerations.
•	Compliance checks: Ensure data governance standards are met.

## Datasets & Analysis ##
# Dataset 1: Google Trends - International
The International Google Trends dataset provides critical insights for individual users and businesses by automating and exposing anonymized, aggregated, and indexed search data in BigQuery. This dataset includes two separate BigQuery tables: one for the Top 25 stories and another for the Top 25 rising queries. New top terms are appended daily, with each set expiring after 30 days. Additionally, a rolling five-year window of historical data is available for each country and region globally, providing valuable signals for analyzing trends and making informed decisions.

## Key Analytical Inquiries ##
•	Identifying top rising search terms in different countries and regions.
•	Highlighting the most frequent search terms across all regions.
•	Analyzing search term trends by DMA (Designated Market Area) region.
•	Tracking the trend of specific search terms over time.
•	Identifying terms with the highest score and percent gain in recent months.
•	Comparison of rising terms across various countries to identify regional differences.
•	Tracking the changes in popularity of terms in different regions over time.
•	Analyzing weekly and monthly performance of terms to identify trends and patterns.
•	Identifying emerging trends by comparing current and previous months.
•	Detailed analysis of performance metrics of top terms across different regions and countries.

# Dataset 2: E-commerce Retail Data - Brazil
This dataset analyzes the operations of a major e-commerce retailer, Target, in Brazil. It includes eight CSV files offering a detailed perspective on 100,000 orders placed from 2016 to 2018. The objective is to uncover valuable insights and provide actionable recommendations for the company.

## Key Analytical Inquiries ##
•	Identifying data types of all columns in the "customers" table.
•	Determining the time range during which orders were placed.
•	Counting the number of cities and states where customers placed orders.
•	Analyzing order trends over time to identify growing trends in the number of orders.
•	Identifying monthly seasonality in the number of orders.
•	Determining the time of day when Brazilian customers predominantly place their orders.
•	Tracking monthly order volume by state and analyzing customer distribution.
•	Calculating the percentage increase in order costs from 2017 to 2018.

## Analysis and Visualization ##
Regional Variation in Search Term Popularity
The results show significant variation in the average percent gain of search terms across different regions, indicating localized spikes in interest tied to specific events or cultural factors.
The results show a significant variation in the average percent gain of search terms across different regions. For instance, "עומר אדם" (Omer Adam) has a consistently high average percent gain of 34,900 across multiple districts in Israel, indicating a widespread and substantial increase in interest.
Diverse Interest Levels Across Regions: The chart and data reveal that while certain regions like Tottori Prefecture in Japan show high average scores (46.41) for the term "台湾 地震" (Taiwan earthquake), other regions display varying levels of interest and engagement. This suggests localized spikes in interest that could be tied to specific events or cultural factors.
 

## Consistency in Search Trends ##
Certain terms consistently exhibit high percent gains, showing significant and sustained interest within specific regions.
The query results indicate that the term "עומר אדם" (Omer Adam) in Israel consistently exhibits a high percent gain of 34900, showing significant and sustained interest in this term within the region.
Data Distribution and Analysis: The histogram highlights that the majority of data points for percent gain are clustered at a high value of 34900, suggesting a concentrated surge in interest for the term, which could be due to a specific event or ongoing popularity within the specified timeframe.
 
## High Frequency of Sports-Related Terms ##
Sports-related terms dominate search frequency, indicating strong global interest in sports events and teams.
The data reveals that sports-related terms like "Arsenal," "PSG," "Chelsea," "Real Madrid," and "F1" dominate the top positions in terms of search frequency. This indicates a strong global interest in sports events and teams.
Distribution of Popular Terms: The bar chart illustrates the frequency distribution of various search terms, with a steep drop-off after the top few terms. This suggests that while a few terms have very high search volumes, there is a long tail of less frequently searched terms, indicating diverse interests among users.

## Uniform High Scores Across Different DMAs ##
Certain topics garner significant interest and engagement uniformly across multiple regions, highlighting diverse interests across different DMAs.
The query results indicate that several terms achieve the maximum score of 100 across different Designated Market Areas (DMAs). This suggests that certain topics, such as "Houston weather," "Marjorie Taylor Greene," and "Kensington Metropark alligator," have garnered significant interest and engagement uniformly across multiple regions.
Diverse Interest in Various Topics: The pie chart illustrates a wide array of topics with high average scores, indicating a broad and diverse set of interests across different DMAs. The even distribution of scores across many terms highlights the variety in search behaviors and interests among users in different market areas.

## High Average Percent Gain in Portugal and Chile 

The query results highlight that the term "eleições nacionais de Portugal" in Portugal and "toriyama" in Chile have the highest average percent gains, with 148,350 and 93,900 respectively. This indicates significant spikes in interest for these terms in their respective countries.
The scatter plot shows that while a few terms have extremely high average percent gains, the majority of terms have more moderate gains. This suggests that a limited number of topics have captured intense interest, whereas most other topics have seen more modest increases in attention.
 








E-commerce Trends in Brazil
•	The highest number of orders is placed during the afternoon period (1 PM to 8 PM), while the fewest orders occur in the early morning hours (12 AM to 6 AM).
 
•	Majority of customers are concentrated in densely populated cities such as Sao Paulo and Rio de Janeiro.
 
•	Significant seasonal peaks in order volumes can be attributed to festival seasons.
 

Actionable Insights
Increase Customer Base in Untapped Cities
•	Provide discounts and offers during festival seasons to attract customers from less penetrated cities.
Expand Delivery Network
•	Partner with local businesses in cities lacking sellers.
•	Develop sellers in cities with a significant customer base to ensure faster delivery and improve customer satisfaction.
Encourage Written Reviews
•	Offer incentives to customers to encourage them to leave detailed written reviews, enhancing customer experience and boosting sales.
Capitalize on Seasonal Demand
•	Offer a wider range and larger quantity of products.
•	Provide attractive promotions and discounts to maximize sales during seasonal peaks.











References
•	"Google Cloud Platform," Google Trends Data on BigQuery, Google Inc., 2023. [Online]. Available: Google Trends
•	"Google Cloud Platform," BigQuery SQL Reference Guide, Google Inc., 2023. [Online]. Available: BigQuery SQL Reference
•	"Google Cloud Platform," BigQuery Performance and Cost Optimization, Google Inc., 2023. [Online]. Available: BigQuery Performance
•	J. Doe, "Analyzing Spatial and Temporal Data Using BigQuery," Towards Data Science, 2023. [Online]. Available: Towards Data Science
•	"Google Cloud Platform," Integrating BigQuery with Data Visualization Tools, Google Inc., 2023. [Online]. Available: BigQuery Data Studio

![image](https://github.com/Mohamed-Aakil/Analyzing-Public-Datasets-with-BigQuery-for-Trend-Detection/assets/96182727/b9041545-3835-4fc2-8cfb-74af631ac349)
