FULL OUTER JOIN:

	
The FULL OUTER JOIN combines the results of both left and right outer joins. 
The joined table will contain all records from both the tables and fill in NULLS for missing matches on either side

	SYNTAX:


    SELECT table1.col1, table2.col2,…, table1.coln
    FROM table1
    Left JOIN table2
    ON table1.commonfield = table2.commonfield;
    Union
    SELECT table1.col1, table2.col2,…, table1.coln
    FROM table1
    Right JOIN table2
    ON table1.commonfield = table2.commonfield;
    

![image](https://user-images.githubusercontent.com/114629519/199353853-c64d8f99-800a-4b9d-ba0c-d057ffea49fd.png)

