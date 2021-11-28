# Amazon Vine Analysis

This week module is all about Big data and the use of **Amazon Web Services (aws)** such as online storage and databases. In specific, we will analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

## ETL on Amazon Product Reviews

In this week project an analysis of the Toys customer reviews dataset from the [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) is carried out.  The information from the dataset is used to create an **AWS RDS database** containing 4 tables in `pgAdmin`.  

The process is performed by using `PySpark`, that allows us to use `Python` to write Spark applications.  The reviews dataset is extracted into a DataFrame, transform it into four separate DataFrames that match the [table schema](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Resources/challenge_schema.sql) in `pgAdmin` and load them as tables into the database.  The code could be find in [here](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Amazon_Reviews_ETL.ipynb), and images of the four tables in `pgAdmin` are shown below.

### The Customers Table:

![customer](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Customer_table.png)
- This table shows how many reviews were written by each customer.  

### The Products Table:

![products](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Products_table.png)
- Name and Identification Number of the products that have been reviewed.

### The Review Id Table:

![review](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Review_id_table.png)
- Information about the reviews including identification numbers, who write each review, date, among other ones.

### The Vine Table:

![vine](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Images/Vine_table.png)
- Information about the Vine Program. 

## Determine Bias of Vine Review

In this part of the analysis, the focus is on the Vine Program, we will determine if there is any bias towards reviews written as part of the Vine program. `Python` is used as the mean to determine additional findings that allows us to perform the analysis.  The code is shown [here](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Vine_Review_Analysis.ipynb) and the Vine Table as a `csv` file in [here](https://raw.githubusercontent.com/LeidyDoradoM/Amazon_Vine_Analysis/main/Resources/vine_table.csv).

1. The total number of (Vine and non-Vine) reviews is: 63294 

2. The total number of (Vine and non-Vine) 5-stars reviews is: 30414

3. The percentage of 5-star Vine reviews is: 1,4%

4. The percentage of 5-star non-Vine reviews is: 98,6%

## Summary 

Positivity bias is a tendency for people to judge reality more favorable than it really is. In this analysis, the positivity bias could be reflected in the tendency of reviewers to evaluate the toys with 5-stars.  If we look at the percentages, 5-star reviews approximately make the 50% of the total of reviews, while only 1,4% of the 5-star reviews belong to customers in the Vine program. This unbalanced shows how the Vine-program reviewers tend to be more critical in their evaluation of toys and consequently, there is not a strong bias towards 5-star reviews for the reviewers in the Vine Program.

These insights could be further analyzed by calculating the percentages of the other star-levels reviews, especially the ones in the bottom (1-star or 2-star reviews). In addition, we could extend this analysis to another product reviews to see if there is a general conclusion of positivity bias in the Vine program.
