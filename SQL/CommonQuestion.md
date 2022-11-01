Solution in link 

1. What is SQL?

2. What is Database?

3. What is DBMS?

4. What is RDBMS? How is it different from DBMS?

5. How to create a table in SQL?
  Solution: 
CREATE TABLE table_name (
	column1 datatype,
	column2 datatype,
	column3 datatype,
   ....
);

6. How to delete a table in SQL?
Solution : DROP TABLE table_name;

7. How to change a table name in SQL?
  Solution : ALTER TABLE table_name
  RENAME TO new_table_name;
  
8. How to delete a row in SQL?
  Solution: DELETE FROM table_name
  WHERE [condition];
  
9. How to create a database in SQL?
	Solution: CREATE DATABASE database_name.

10. What is Normalization in SQL?
	Normalization is used to decompose a larger, complex table into simple and smaller ones. This helps us in removing all the redundant data.
	1st Normal Form : All attributes in the relation are atomic(indivisible value) And there are no repeating elements or groups of elements.
	2nd Normal Form : It is in 1st Normal Form.No partial dependency exists between non-key attributes and key attributes.
	3rd Normal Form : It is in 2NF.No transitive dependency exists between non-key attributes and key attributes through another non-key attribute
	
11. What is join in SQL?
	Joins are used to combine rows from two or more tables, based on a related column between them

12. How to insert a date in SQL?	
	"INSERT INTO tablename (col_name, col_date) VALUES ('DATE: Manual Date', '2020-9-10')";
	
13. What is Primary Key in SQL?

14. How do I view tables in SQL?
	Show tables;

15. What is ETL in SQL? 
	ETL stands for Extract, Transform and Load. It is a three-step process, where we would have to start off by extracting the data from sources. 
	Once we collate the data from different sources, what we have is raw data. This raw data has to be transformed into the tidy format, 
	which will come in the second phase. Finally, we would have to load this tidy data into tools which would help us to find insights.

16. What is the update command in SQL? 
	UPDATE employees
	SET last_name=‘Cohen’
	WHERE employee_id=101;
	The update command comes under the DML(Data Manipulation Langauge) part of sql and is used to update the existing data in the table.

17. What are the types of SQL Queries?
	DDL (Data Definition Language): the creation of objects
	DML (Data Manipulation Language): manipulation of data
	DCL (Data Control Language): assignment and removal of permissions
	TCL (Transaction Control Language): saving and restoring changes to a database
	
18. What are Nested Triggers?
	Triggers may implement DML by using INSERT, UPDATE, and DELETE statements. These triggers that contain DML and find other triggers for data modification are 		called Nested Triggers.
	
19. What is Data Integrity?
	Data Integrity is the assurance of accuracy and consistency of data over its entire life-cycle, and is a critical aspect to the design, implementation and 		usage of any system which stores, processes, or retrieves data. It also defines integrity constraints to enforce business rules on the data 
		when it is entered into an application or a database.
		
		
20. What is OLAP?
	OLAP stands for Online Analytical Processing. And a class of software programs which are characterized by relatively low frequency of online transactions. 	Queries are often too complex and involve a bunch of aggregations. 
	
21. What is the Cartesian product of the table? (Matrix Multiplication)
	The output of Cross Join is called a Cartesian product. It returns rows combining each row from the first table with each row of the second table. 
	For Example, if we join two tables having 15 and 20 columns the Cartesian product of two tables will be 15×20=300 rows.
	
22.What is the difference between SQL having vs where?
	![image](https://user-images.githubusercontent.com/114629519/199356597-7bdfdce9-17bb-46bb-99ea-62aae3a7a8ea.png)
	
23. How to find the nth highest salary in SQL?
	This is how we can find the nth highest salary in SQL SERVER using TOP keyword:

		SELECT TOP 1 salary FROM ( SELECT DISTINCT TOP N salary FROM #Employee ORDER BY salary DESC ) AS temp ORDER BY salary
	This is how we can find the nth highest salary in MYSQL using LIMIT keyword:

		SELECT salary FROM Employee ORDER BY salary DESC LIMIT N-1, 1
		
24.How to copy table in SQL?
	We can use the SELECT INTO statement to copy data from one table to another. Either we can copy all the data or only some specific columns.
      	 This is how we can copy all the columns into a new table:
		SELECT *
	 	INTO newtable
		FROM oldtable
		WHERE condition;
		
25. How to fetch alternate records from a table?
	Records can be fetched for both Odd and Even row numbers – To display even numbers –
	Select employeeId from (Select rowno, employeeId from employee) where mod(rowno,2)=0
	
	To display odd numbers –
	Select employeeId from (Select rowno, employeeId from employee) where mod(rowno,2)=1
	
26. How to find duplicate records in SQL?
	There are multiple ways to find duplicate records in SQL. Let’s see how can we find duplicate records using group by:
	SELECT 
   	 x, 
    	y, 
    	COUNT(*) occurrences
	FROM z1
	GROUP BY
    	x, 
    	y
	HAVING 
    	COUNT(*) > 1;
	
27. How to create an index in SQL?
	We can create an index using this command:
	CREATE INDEX index_name
	ON table_name (column1, column2, column3 ...);
	
 We start off by giving the keywords CREATE INDEX and then we will follow it up with the name of the index, after that we will give the ON keyword. Then, we will give the name of the table on which we would want to create this index. Finally, in parenthesis, we will list out all the columns which will have the index. Let’s look at an example:
 		CREATE INDEX salary
		ON Employees (Salary);
		
28. Difference between COALESCE() & ISNULL() ?
	COALESCE() accepts two or more parameters, one can apply 2 or as many parameters but it returns only the first non NULL parameter. 

	ISNULL() accepts only 2 parameters. 

	The first parameter is checked for a NULL value, if it is NULL then the 2nd parameter is returned, otherwise, it returns the first parameter.
	
29. What is the usage of NVL() function?
	This function is used to convert the NULL value to the other value.
	
30.How to store Videos inside SQL Server table?
	By using FILESTREAM datatype, which was introduced in SQL Server 2008

31.What is a function in SQL Server?
Functions are pre-written codes that return a value and which help the user achieve a particular task concerning viewing, manipulating, and processing data.
Examples of a few functions are:

AGGREGATE FUNCTIONS:
		MIN()- Returns the minimum value
		MAX()- Returns the maximum value
		AVG()- Returns the average value
		COUNT()

STRING FUNCTIONS:
		COALESCE()
		CAST()
		CONCAT()
		SUBSTRING()

DATE FUNCTIONS:
	GETDATE()
	DATEADD()
	DATEDIFF()
	
There are many types of functions such as Aggregate Functions, Date Functions, String Functions, Mathematical functions, etc.

