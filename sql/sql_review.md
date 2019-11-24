# SQL Review Sheet
By Xavier Collantes (xcollantes)

[Basics](#Basics)
  - [Data Definition Language](#Data-Definition-Language)
  - [Data Manipulation Language]('#Data Manipulation Language')
  - [Data Query Language](#Data Query Language)

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
INSERT INTO <table_name> VALUES (field_value1, field_value2, field_value3);

// Explicit position, column name matched with field value
INSERT INTO <table_name> (column1, column2, column3) VALUES (field_value1, field_value2, field_value3);
```

```
UPDATE
```

```
DELETE
```
### Data Query Language
Getting data from database.
```
SELECT
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

