SELF JOIN:

	
The The SELF JOIN joins a table to itself; temporarily renaming at least one table in the SQL statement.

    SYNTAX:

    SELECT a.col1, b.col2,..., a.coln
    FROM table1 a, table1 b
    WHERE a.commonfield = b.commonfield;
    
    

