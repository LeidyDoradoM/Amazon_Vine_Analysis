# Amazon Vine Analysis

This week module is all about Big data and the use of **Amazon Web Services (aws)** for cloud services as online storage and managing online databases. In specific, we will analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

## ETL on Amazon Product Reviews

We will analyze the Toys customer reviews dataset from the [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt).  , and from there we will create an **AWS RDS database** with 4 tables in *pgAdmin*.

and extract the dataset into a DataFrame. You'll transform the DataFrame into four separate DataFrames that match the table schema in pgAdmin. Then, you'll upload the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded.

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