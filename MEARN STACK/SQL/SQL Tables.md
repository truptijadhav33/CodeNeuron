organizing data into rows and columns.

### CREATE TABLE:

The `CREATE TABLE` command in SQL defines how your data will be stored, including the table name, column names, data types, and rules (constraints) such as `NOT NULL`, `PRIMARY KEY`, and `CHECK`.
*Syntax:*

```sql
CREATE table table_name
(
Column1 datatype (size),
column2 datatype (size),
.
.
columnN datatype(size)
);
```

*Example:*

```sql
CREATE database college;
USE college;
CREATE table student(
	roll_no INT,
    name VARCHAR(20),
    age int
    );
```

After creating a table, use the following command to view the **structure of your table:**

```sql
DESC table_name;
```


## Inserting Data into the Table

After creating the table, you can use INSERT INTO command to add data into it.

*Example:*
```sql
INSERT INTO student values(1,"adam",14),(2,"bob",12);
SELECT *FROM student;
```

## DROP TABLE:

The **`DROP TABLE`** command in ****SQL**** is a powerful and essential tool used to permanently delete a table from a database, along with all of its data, structure, and associated constraints such as indexes, triggers, and permissions.

*Syntax:*

```sql
DROP TABLE table_name;
```

*Example:*
```sql
DROP TABLE student;
```

To verify if a table is dropped, you can use the **SHOW TABLES** (MySQL)

```sql
SHOW TABLES;
```



