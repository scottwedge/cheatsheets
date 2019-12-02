## Indexing
Used to speed up database querying.

Indexing creates a table in disk space consisting of two columns: key, pointer.  The key is the search term and the pointer is the address of the datablock or location of something.

There are two types of indexing:

### Primary Indexing
Table with fixed two columns. The key is the search term and the pointer is the address of the datablock or location of something.

There are two types of Primary Indexing:

#### Dense Index
![Dense](https://www.guru99.com/images/1/070119_0833_IndexinginD2.png)
Each key corresponds to another key in the target table.  The pointer is a one to one relationship.  

In this case, the index is large but has more tracking.

#### Sparse Index
![Sparse](https://www.guru99.com/images/1/070119_0833_IndexinginD3.png)
Each key corresponds to a block of records in target table.  A range of index keys store the same address.

### Secondary Indexing


**Syntax:**

`CREATE INDEX <index_name> ON <table_name> (field1, field2);`

MS Access

`DROP INDEX <index_name> ON <table_name>;`

SQL Server

`DROP INDEX <table_name>.<index_name>;`

Oracle

`DROP INDEX <index_name>;`

MySQL

```
ALTER TABLE <table_name> 
DROP INDEX <index_name>;
```

Convention is to begin index_name with 'idx_'.

(https://www.w3schools.com/sql/sql_create_index.asp)


## Horizontal Scaling
