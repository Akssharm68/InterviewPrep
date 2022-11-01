INNER JOIN:

	
  The INNER JOIN creates a new result table by combining column values of two tables (table1 and table2) based upon the join-predicate. 
  The query compares each row of table1 with each row of table2 to find all pairs of rows which satisfy the join-predicate.

	SYNTAX:

	SELECT table1.col1, table2.col2,…, table1.coln
	FROM table1
	INNER JOIN table2
	ON table1.commonfield = table2.commonfield;

![image](https://user-images.githubusercontent.com/114629519/199333474-02d0cbef-02c6-45bb-b0ca-4fadda1b358f.png)
