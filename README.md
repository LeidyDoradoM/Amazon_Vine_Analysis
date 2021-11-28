# Amazon Vine Analysis

This week module is all about Big data and the use of **Amazon Web Services (aws)** such as online storage and databases. In specific, we will analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

## ETL on Amazon Product Reviews

In this week project an analysis of the Toys customer reviews dataset from the [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) is carried out.  The information from the dataset is used to create an **AWS RDS database** containing 4 tables in `pgAdmin`.  

The process is performed by using `PySpark`, that allows us to use `Python` to write Spark applications.  The reviews dataset is extracted into a DataFrame, transform it into four separate DataFrames that match the [table schema](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Resources/challenge_schema.sql) in `pgAdmin` and Load them as tables into the database.  The code could be find in [here](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Amazon_Reviews_ETL.ipynb), and a glance of the four `pgAdmin` tables are shown below.

### The Customers Table:

![customer](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Customer_table.png)


### The Products Table:

![products](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Products_table.png)

### The Review Id Table:

![review](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Review_id_table.png)

### The Vine Table:

![vine](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Vine_table.png)

## Determine Bias of Vine Review

Using your knowledge of PySpark, Pandas, or SQL, you’ll determine if there is any bias towards reviews that were written as part of the Vine program. For this analysis, you'll determine if having a paid Vine review makes a difference in the percentage of 5-star reviews.

How many Vine reviews and non-Vine reviews were there?
How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

## Summary 

In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.