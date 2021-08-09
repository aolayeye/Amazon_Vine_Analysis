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
#### Review Classification
- There are 94 vine reviews and 40471 non-vine reviews in the filtered dataset
- There are 15711 5-star reviews in the filtered dataset
- There are 48 5-star paid(vine) reviews and 15663 5-star unpaid(non-vine) reviews
- 51.06% of the paid reviews were 5-star reviews, while 38.70% of the unpaid reviews were 5-star reviews

### Summary
Of video games with 20 or more votes and where the ratio of helpful_votes to total_votes was 50% or greater, 51.06% of reviews in the vine program were 5 stars. While 38.70% of unpaid reviews in the same filetered dataset were 5 stars. On a high-level we may conclude that there is some bias toward favorable reviews from Vine members in the video game dataset.

A better way to determine bias is to compare a random sample of paid reviews to a random sample of unpaid reviews in a t-test. In this test we would compare the average number of 5-star reviews in the paid reviews to the average number of 5-star reviews in the unpaid reviews.

Our Study design for this scenario would be as follows:
