Project Overview: The project implements a dimensional data mart using sakila, a dataset that involves the transactions of movie rentals. This primarily focuses on the payment transactions, and give insight on total revenue/payments per country. It also give information regarding the impact of the length of a film on a customer's impact on total revenue and payments. The project also showed how transaction information changed over time. 

Data Sources: I sampled my data from https://dataedo.com/kb/databases/mysql/sample-databases. 
The Sakila data was imported into MySQL by executing the SQL file in MySQL workbench. I used dataset given and converted the customer table into a csv. I obtained data for dim_films by using MongoDB atlas and creating a MongoDB cluster. 

Strategy: 
The strategy was to implement an ETL pipeline using python in VScode. I planned to take data from the sakila db and converting some columns into different formats to show understanding. Then, I wanted to create a datamart using the central fact table and supporting dimension tables. Finally, queries would be written to show functionality of the new data mart.  
Process: 
The first step in the project was to extract different data types and implement them into the data warehouse. This was done by using data orginiating from MongoDB, MySQL, and local files. 
  - The date dimension was implemented directly into MySQL workbench. This was the format that was given by our professors. 

The second step involved transforming the data. This involved cutting out unimportant columns and also converting the dates into readable format. In addition, the keys from the data were replaced with surrogate keys and columns were renamed to match schema. 

The third step was to upload these transformed dataframes into the new sakila_dw data warehouse. 

The resulting data was queireid to test the functionality of the new data warehouse and the validity of the data in it. 

SQL query information: 
The first query shows that the warehouse allows for payment transactions to be analyzed given the infomation of films, stores, and customers. It joins the fact table with dim tables in order to calculate total revenue and payment counts.
The second query shows the total revenue and total payments a customer resulted in given the length of the film. 
The third query shows the number of unique customers and transactions in each country. These are also shown in related to the year showing how these variables change over time. 
