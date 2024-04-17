Examples to CREATE and DROP tables
===========================================

CREATE TABLE statement
----------------------

In the previous video, we saw the general syntax to create a table:

```sql
1.  CREATE TABLE TableName  (
2.   COLUMN1 datatype,
3.   COLUMN2 datatype,
4.   COLUMN3 datatype,
5.   ...
6.  );
```

Consider the following examples:

1.  Create a TEST table with two columns - ID of type integer and NAME of type varchar. For this, we use the following SQL statement.

```sql
1.  CREATE TABLE TEST (
2.   ID int,
3.   NAME varchar(30)
4.  );
```


2.  Create a COUNTRY table with an integer ID column, a two-letter country code column, and a variable length country name column. For this, we may use the following SQL statement.

```sql
1.  CREATE TABLE COUNTRY (
2.   ID int,
3.   CCODE char(2),
4.   Name varchar(60)
5.  );
```

3.  In the example above, make ID a primary key. Then, the statement will be modified as shown below.

```sql
1.  CREATE TABLE COUNTRY (
2.   ID int NOT NULL,
3.   CCODE char(2),
4.   Name varchar(60)
5.   PRIMARY KEY (ID)
6.  );
```

In the above example, the ID column has the **NOT NULL** constraint added after the datatype, meaning that it cannot contain a NULL or an empty value. This is added since the database does not allow Primary Keys to have NULL values.

DROP TABLE
----------

If the table you are trying to create already exists in the database, you will get an error indicating **table XXX.YYY already exists**. To circumvent this error, create a table with a different name or first DROP the existing table. It is common to issue a DROP before doing a CREATE in test and development scenarios.

The syntax to drop a table is:

```sql
1.  DROP TABLE TableName;
```

For example, consider that you wish to drop the contents of the table COUNTRY if a table exists in the dataset with the same name. In such a case, the code for the last example becomes

```sql
1.  DROP TABLE COUNTRY;
2.  CREATE TABLE COUNTRY (
3.   ID int NOT NULL,
4.   CCODE char(2),
5.   Name varchar(60)
6.   PRIMARY KEY (ID)
7.  );
```

WARNING: Before dropping a table, ensure it doesn't contain important data that can't be recovered easily.

Note that if the table does not exist and you try to drop it, you will see an error like **XXX.YYY is an undefined name**. You can ignore this error if the subsequent CREATE statement is executed successfully.

In a hands-on lab later in this module, you will practice creating tables and other SQL statements.

