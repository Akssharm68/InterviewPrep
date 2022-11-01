RIGHT JOIN: 

The RIGHT JOIN returns all the values from the right table, plus matched values from the left table or NULL in case of no matching join predicate.

    SYNTAX
    SELECT table1.col1, table2.col2,…, table1.coln
    FROM table1
    RIGHT JOIN table2
    ON table1.commonfield = table2.commonfield;
    
![image](https://user-images.githubusercontent.com/114629519/199337107-5a1bfcd8-a7cd-496a-ba00-f1e8be6e3c19.png)
