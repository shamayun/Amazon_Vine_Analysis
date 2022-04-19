# Amazon Vine Analysis
### Overview of the analysis of the Vine program:
Amazon offers Vine members free products that have been submitted to the program by participating selling partners. Vine reviews are the independent opinions of the Vine Voices and the selling partners cannot influence, modify, or edit the reviews. Amazon does not modify or edit Amazon Vine reviews, as long as they comply with our posting guidelines.Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.
The objective of the analysis is to determine if there is any bias in reviews which were written as part of the Amazon Vine program.
### Resources:
* PySpark 3.2.1,
* PostgreSQL, 
* pgAdmin hosted on AWS , Pandas Library, Psycopg2 Library
### Steps Followed to Obtain Result:
1. In order to properly process and analyze the review data, I have created a database schema within AWS to load the data.
2. Selected targetted reviews from [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), Automobile Sector.
3. Transformed the DataFrame into four separate DataFrames using Google Colb/PySpark and Loaded the tables into pgAdmin. Prior to loading the data in pgAdmin, created table schema in pgAdmin to match data to be loaded. Also, check the load with small amount of rows to confirm the data will load correctly from AWS.
4. Confirmed number of rows were equal and accurate in pgAmin once upload the transformed data into the appropriate tables has been uploaded.
5. Analysed using SQL to determine if there was any bias of Vine Reviews

![ETL_tables_in_pgAdmin](https://user-images.githubusercontent.com/96354508/164105171-2d033e29-f89b-4acc-ac13-6734ded282ab.png)

### Summary:
* Vine Vs non-Vine Reviews:
Total number of vine reviews in automobile were 82 out of 24,824 which is less than .5% of the toal reviews.

![Total_no_vine_nonvine](https://user-images.githubusercontent.com/96354508/164105552-ae3b6d43-78e4-4279-a538-fc9e42dacb60.png)

* Vine Vs non-Vine Reviews by Stars (Number & Percentage:
33 out of 82 vine reviews were 5 stars, 40% of total vine reviews. 12,807 out of 24,824 non-vine reviews were 5 stars, 52% of total reviews.

![reviews_by_stars](https://user-images.githubusercontent.com/96354508/164105616-563d5d8b-f44a-4142-a7f8-c71a0923526c.png)

Based on the numbers in the summary table, I can conclude that there is no evidence of positivity bias for 5 start reviews in the Vine program in automobile market. The non-vine customers tend to leave even more reviews with high rating. 

According to the results, non-vine customers more often rate a product with only 1 star (20% as apposed to 4%). So, I can conclude that non-vine customers tend to weigh mostly intwo categories, 1 star or 5 stars, while vine customers try to evaluate a product fairly. They often leave 3 or 4 stars reviews. Non-vine customers do not hesitate to rate one star when needed.

![Rating_comparison ](https://user-images.githubusercontent.com/96354508/164110716-08d1fa84-2ff6-439e-b647-2230636b1a9e.png)

