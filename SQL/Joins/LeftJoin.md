LEFT JOIN:

	
The LEFT JOIN returns all the values from the left table, plus matched values from the right table or NULL in case of no matching join predicate.

	SYNTAX:


    SELECT table1.col1, table2.col2,…, table1.coln
    FROM table1
    LEFT JOIN table2
    ON table1.commonfield = table2.commonfield;
    

![image](https://user-images.githubusercontent.com/114629519/199334672-967a09eb-6e9b-4e61-9be2-6228b5109974.png)
