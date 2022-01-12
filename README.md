# Amazon Vine Analysis

## The purpose of this analysis was to look at Amazon reviews that were written by members of the Amazon Vine program to inform stakeholders if purchasing the Vine program will lead to greater reviews. 

## Project Overview:
1. Perform the ETL process using PySpark, AWS, and pgAdmin
2. Use Google Colab to analyze and export results

## Resources
- Source of data: [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
- Software: Google Colab, pgAdmin 4.6.1, AWS S3, AWS RDS, PostgreSQL 13.4, Python 3.7.10, Conda 4.10.3, Jupyter Notebook 6.3.0, Visual Studio Code 1.60.2
- Please see the refactored code here: [Amazon Reviews ETL](https://github.com/mthalken/Amazon_Vine_Analysis/blob/main/Amazon_Reviews_ETL.ipynb) and [Vine Review Analysis](https://github.com/mthalken/Amazon_Vine_Analysis/blob/main/vine_reiview_analysis.ipynb).

## Results 
In this analysis we chose the gift card dataset to see if the return on being a Vine member would lead to buying an increased amount of gift cards with 5 star ratings. 
 - When cleaning the data by dropping NA values, finding where helpful votes/total votes equal 50%, filtering 5 star ratings, and counting the total Vine users we arrived at 355 users and 90 total 5 star reviews for non Vine users. We found 0 vine users within those filters.  
 - We then looked to see if there were any vine users that had bought gift cards or left reviews. There were none. 

![png](https://github.com/mthalken/Amazon_Vine_Analysis/blob/main/images/summary.png)

![png](https://github.com/mthalken/Amazon_Vine_Analysis/blob/main/images/not_vine_users.png)

![png](https://github.com/mthalken/Amazon_Vine_Analysis/blob/main/images/vine_users.png)


## Summary
According to the gift card data there is no evidence to support positive bias for reviews in the Vine program. With that being said there needs to be further analysis done. 
 - Analysis could look at if Vine users are marketed or promoted to purchase gift cards and the benefits or lack of benefits of doing so. 
 - The analysis that should be done is a loop function to go through each of the datasets and then report the summary of each category and department type based on the Vine program. This would give an overall marketing strategy as well as a very comprehensive analysis to provide to the stakeholders for their decision. 

