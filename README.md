# Amazon_Vine_Analysis

The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program, a service that allows manufacturers and publishers to receive reviews of their products and determine if there are any biases between Vine members and Non-Vine member's reviews.

Companies that will pay a fee to Amazon and may provide free products to Vine members who are then required to publish a review. In order to determine if there is any bias towards favorable reviews from Vine members vs. non-members, we need to identify the percentage of 5 star ratings to total rating. As part of this exercise, we were asked to choose from 50 datasets to extract, transform and load into a dataframe in order to complete our analysis. Throughout this analysis, we use:

    - PySpark to extract the dataset, transform the data, connect to AWS RDS instance and load the transformed data into pgAdmin.
    - Google Colaboratory to import PySpark libraries and connect to Postgres in order to create SQL tables and export the results.

Of the 50 datasets, I chose to analyze reviews that were made by users in the "Software" category.

## Results

![image](https://user-images.githubusercontent.com/103547108/183547707-588de773-77b1-42ce-9628-b45fa0ec9adc.png)

### 1. How many Vine reviews and non-Vine reviews were there?

![image](https://user-images.githubusercontent.com/103547108/183547323-857076cf-06c2-430f-a930-24ec155ec265.png)

### 2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

Vine members gave 102 out of 248 reviews a 5 star rating.
Non-Vine members gave 5,153 out of 17,513 reviews a 5 star rating.

### 3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

41.1% of the reviews for Vine members were rated 5 stars.
29.4% of the reviews for Non-Vine members were rated 5 stars.

![image](https://user-images.githubusercontent.com/103547108/183547453-7621426a-91b7-4cc5-b278-4582b96e9bf1.png)

## Summary

Based on the results, Vine members did not show bias when rating their products considering that the number of 5-star ratings was about 12% less than Non-Vine members (41% vs. 29%). With this, we can assume that Vine customers are more critical when submitting their review. However, in order to support this assumption further, we should include all of the data rather than filtering it to a percentage of helpful vs. total votes as we did for this analysis. Reviewing the data as is would give us more information and allow us to further support our assumption as shown below.

![image](https://user-images.githubusercontent.com/103547108/183547992-24487525-57a7-45a3-aa0c-b2faf5e1eba8.png)

Running the same analysis using datasets from different product categories can provide us with the whole picture of whether reviews made by Vine members are bias.
