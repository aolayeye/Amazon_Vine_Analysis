# Amazon_Vine_Analysis
## Overview
This project is about analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.
In this project, we will PySpark to perform the ETL process to extract a video games dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in the video games dataset.

#### Control Flow
1. Using PySpark extract the video games dataset from AWS S3 bucket
2. Transform the data
3. Connect to an AWS RDS instance, and load the transformed data into pgAdmin
4. Use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in the video games dataset.

## Results: Review Classification
Our review classification was based on the following:
- video games with 20 or more votes
- ratio of helpful_votes to total_votes greater than 50%
- percentage classification is based on 5-Star reviews
##### Review Classification
-There were 4291 vine reviews and 1781706 non-vine reviews
##### 5-Star Review Classification
-There are 48 5-star vine reviews and 20439 5-star non-vine reviews
##### 5-Star Review Percentage Classification
-0.23% of the 5-star useful reviews were paid reviews, while 99.77% were unpaid reviews

### Summary
