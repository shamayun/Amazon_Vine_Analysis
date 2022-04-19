# Amazon Vine Analysis
### Overview of the analysis of the Vine program:
Amazon offers Vine members free products that have been submitted to the program by participating selling partners. Vine reviews are the independent opinions of the Vine Voices and the selling partners cannot influence, modify, or edit the reviews. Amazon does not modify or edit Amazon Vine reviews, as long as they comply with our posting guidelines.Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.
The objective of the analysis is to determine if there is any bias in reviews which were written as part of the Amazon Vine program.
### Resources:
* PySpark 3.2.1,
* PostgreSQL, 
* pgAdmin hosted on AWS , Pandas Library, Psycopg2 Library
### Steps Followed to Obtain Resut:
1. In order to properly process and analyze the review data, I have created a database schema within AWS to load the data.
2. Selected targetted reviews from [Amazon Review Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), Automobile Sector.
3. Transformed the DataFrame into four separate DataFrames using Google Colb/PySpark and Loaded the tables into pgAdmin. Prior to loading the data in pgAdmin, created table schema in pgAdmin to match data to be loaded. Also, check the load with small amount of rows to confirm the data will load correctly from AWS.
4. Confirmed number of rows were equal and accurate in pgAmin once upload the transformed data into the appropriate tables has been uploaded.
5. Analysed using SQL to determine if there was any bias of Vine Reviews

![ETL_tables_in_pgAdmin](https://user-images.githubusercontent.com/96354508/164105171-2d033e29-f89b-4acc-ac13-6734ded282ab.png)

### Summary:
* Vine Vs non-Vine Reviews:

![Total_no_vine_nonvine](https://user-images.githubusercontent.com/96354508/164105552-ae3b6d43-78e4-4279-a538-fc9e42dacb60.png)

* Vine Vs non-Vine Reviews by Stars:
* % of Vine Vs non_Vine Reviews by Stars:

![reviews_by_stars](https://user-images.githubusercontent.com/96354508/164105616-563d5d8b-f44a-4142-a7f8-c71a0923526c.png)

The summary states whether or not there is bias, and the results support this statement (2 pt)
An additional analysis is recommended to support the statement (2 pt)
