Bigquery using Pyt CREATE TABLE `your_dataset.customer_info` (
  customer name STRING REQUIRED,
  zip_code STRING,
  email STRING,
  state  STRING 
hon: 
Data Cleaning and Transformation:
1.	Create Table

);  
2.	Inserting Rows Directly
INSERT INTO `your_dataset.customer_info` (customer_name, zip_code, email, state)
VALUES ('John Doe', '12345', 'john.doe@example.com', 'CA'),
('Jane Smith', '0000', 'jane.smith@example.com', 'NY'),       ('Alice Jones', '0000', 'alice.jones@example.com', 'TX');

Scenario: 
•	A BigQuery table contains customer data with inconsistent formatting (e.g., mixed case in names, missing zip codes). 
•	Handle exception for table not found and print the message ‘table not found’ if query fails.
•	Clean the data by standardizing name  prefix with Mr. and convert in upper case .Replace zip code value ‘0000’ with ‘12345’. 
•	Store all cleaned data into dataframe and add new column in dataframe as today_date and populate it with today’s date. Lastly print the dataframe. 
Output should be as follows.

Customer_name	Zip_code	Email_string	State	Todays_date
Mr. JOHN DOE	12345	john.doe@example.com	CA	23-03-2024
Mr. JANE SMITH	12345	jane.smith@example.com	NY	23-03-2024
Mr. ALICE JONES	12345	alice.jones@example.com	TX	23-03-2024
 

Data aggregation:
1.	Create Table

CREATE TABLE `your_dataset.your_table` (
  customer_id STRING,  -- Assuming customer_id is unique
  order_value FLOAT64,
  product_category STRING,  -- This might be redundant depending on your logic
  product_category STRING
);
2.	Inserting Rows Directly

INSERT INTO `your_dataset.your_table` (customer_id, order_value, product_category)
VALUES
  ('customer1', 100.60, 'Electronics'),
  ('customer2', 25.00, 'Clothing'),
  ('customer3', 150.00, 'Appliances')
  ('customer4', 35.00, 'Clothing'),
  ('customer5', 211.00, 'Electronics'),
  ('customer3', 320.70, 'Appliances');

Scenario: 
•	A BigQuery table contains customer order data. Write a python code to read data from table and load into dataframe . Group the data by product category and provide the total revenue(order_value)  for each category . 
Create a table and store the product_category and total revenue(order_value) for each product derived in above step. 
Print Table TABLE_ID created in dataset DATASET_ID for project project_id
Handle exception for table already exist and print (“table already exist”) 
New table should have 2 columns, product_category and total_revenue. Revenue amount should be half adjusted while storing into table. 
After inserting the records in new table. Print the number of records inserted. 
Print the table data. Output should be as follows. 

product_category	total_revenue
Clothing	60.00
Electronics	312.00
Appliances	471.00

Python Programming : 

Question 1:
Write a function in Python to check duplicate letters. It must accept a string, i.e., a sentence. The function should return True if the sentence has any word with duplicate letters, else return False.
E.g. Today is Sunday, Sunday is holiday
Output – True
I am giving exam
Output- False
Question 2:
Write a function in Python to parse a string such that it accepts a parameter- an encoded string. This encoded string will contain a first name, last name, and an id. You can separate the values in the string by any number of zeros. The id will not contain any zeros. The function should return a Python dictionary with the first name, last name, and id values. 
For example, if the input would be "John000Doe000123". Then the function should return: { "first_name": "John", "last_name": "Doe", "id": "123" }
Question 3:
Find the largest and the smallest number in a given array.
Array[11,17,19,76,99]



