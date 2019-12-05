# SQL Review Sheet
By Xavier Collantes (xcollantes)

[Basics](#Basics)
  - [Data Definition Language](#Data-Definition-Language)
  - [Data Manipulation Language]('#Data-Manipulation-Language')
  - [Data Query Language](#Data-Query-Language)
  - [Case](#Case)

## Basics
### Data Definition Language
Build, change, remove database schema objects: database, index, views.


`CREATE DATABASE <database_name>;`

```
CREATE TABLE <table_name> (
  <field_name> <data_type>(size),
  <field_name> <data_type>(size),
);
```

Completely destroy database table.

```
DROP TABLE <table_name>;
```

Nuke entire database.

```
DROP DATABASE <database_name>;
```

Add new column to table.
```
ALTER TABLE <table_name>
ADD (<column_name> <data_type>,
     <column_name> <data_type>);
```

Change a column.
```
ALTER TABLE <table_name>
MODIFY <column_name> <data_type>;
```

Remove column in table.
```
ALTER TABLE <table_name>
DROP <column_name>;
```


### Data Manipulation Language
Insert, change, remove data within the schema.


Put data into the table.
```
// Implicit position, place matters
INSERT INTO <table_name>
VALUES (field_value1, field_value2, field_value3);

// Explicit position, column name matched with field value
INSERT INTO <table_name> (column1, column2, column3)
VALUES (field_value1, field_value2, field_value3);
```

Change data in column when column already exists.
```
UPDATE <table_name>
SET <column_name> = <new_data>;
```

Remove data from table.
```
DELETE FROM <table_name>
WHERE <condition>;

// *WARNING: This will delete all records in table if no condition is
specified.*
DELETE FROM <table_name>;
```


### Data Query Language
Getting data from database.

Return data from table.
```
SELECT <field1>, <field2>
FROM <table_name>
WHERE <condition>;
```

Return top results.
```
// MySQL
SELECT <field1>
FROM <table_name>
WHERE <condition>
LIMIT <number>;

// MS SQL
SELECT TOP <number|percent> <column_name>
...

// Oracle SQL
SELECT <field1>
FROM <table_name>
WHERE <condition>
AND ROWNUM <= <number>;
```

Return if a value is in set.
```
SELECT <field1>, <field2>
FROM <table_name1>
WHERE <data> IN (SELECT field5, field6
                 FROM <table_name2>);
```




### Data Control Language
Permissions management.
```
GRANT
```

```
REVOKE
```

### Data Transaction Language


### Case
If then else of SQL. Returns a value.
```
UPDATE <table_name>
SET <column_name> = CASE
                      WHEN <condition> THEN <RETURN>
                      WHEN <condition> THEN <RETURN>
                      ELSE <RETURN>
                    END;
```



## JOINS


(https://www.diffen.com/difference/Inner_Join_vs_Outer_Join)
(https://teamsql.io/blog/?p=923)


