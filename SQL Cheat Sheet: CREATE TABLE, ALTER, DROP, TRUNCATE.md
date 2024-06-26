SQL Cheat Sheet: CREATE TABLE, ALTER, DROP, TRUNCATE
----------------------------------------------------

| Command | Syntax | Description | Example |
| --- | --- | --- | --- |
| CREATE TABLE | `CREATE TABLE table_name (col1 datatype _optional keyword_, col2 datatype _optional keyword_,col3 datatype _optional keyword_,..., coln datatype _optional keyword_)` | `CREATE TABLE` statement is to create the table. Each column in the table is specified with its name, data type and an optional keyword which could be **PRIMARY KEY**, **NOT NULL**, etc., | `CREATE TABLE employee ( employee_id char(2) PRIMARY KEY, first_name varchar(30) NOT NULL, mobile int);` |
| ALTER TABLE - ADD COLUMN | `1. ALTER TABLE table_name ADD column_name_1 datatype....ADD COLUMN column_name_n datatype;`  <br>`2. ALTER TABLE table_name ADD COLUMN column_name_1 datatype....ADD COLUMN column_name_n datatype;` | `ALTER TABLE` statement is used to add the columns to a table. | `1. ALTER TABLE employee ADD income bigint;`  <br>`2. ALTER TABLE employee ADD COLUMN income bigint;` |
| ALTER TABLE - ALTER COLUMN | `ALTER TABLE table_name ALTER COLUMN column_name_1 SET DATA TYPE datatype;` | `ALTER TABLE ALTER COLUMN` statement is used to modify the data type of columns. | `ALTER TABLE employee ALTER COLUMN mobile SET DATA TYPE CHAR(20);` |
| ALTER TABLE - DROP COLUMN | `ALTER TABLE table_name DROP COLUMN column_name_1 ;` | `ALTER TABLE DROP COLUMN` statement is used to remove columns from a table. | `ALTER TABLE employee DROP COLUMN mobile ;` |
| ALTER TABLE - RENAME COLUMN | `ALTER TABLE table_name RENAME COLUMN current_column_name TO new_column_name;` | `ALTER TABLE RENAME COLUMN` statement is used to rename the columns in a table. | `ALTER TABLE employee RENAME COLUMN first_name TO name ;` |
| TRUNCATE TABLE | `TRUNCATE TABLE table_name IMMEDIATE;` | `TRUNCATE TABLE` statement is used to delete all of the rows in a table. The IMMEDIATE specifies to process the statement immediately and that it cannot be undone. | `TRUNCATE TABLE employee IMMEDIATE ;` |
| DROP TABLE | `DROP TABLE table_name ;` | Use the `DROP TABLE` statement to delete a table from a database. If you delete a table that contains data, by default the data will be deleted alongside the table. | `DROP TABLE employee ;` |

