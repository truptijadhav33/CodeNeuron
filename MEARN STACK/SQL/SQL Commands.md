### # SQL Commands | DDL, DQL, DML, DCL and TCL Commands

SQL commands are the fundamental building blocks for communicating with a database management system (DBMS).

SQL Commands are mainly categorized into five categories: 

- DDL – Data Definition Language
- DQL – Data Query Language
- DML – Data Manipulation Language
- DCL – Data Control Language
- TCL - Transaction Control Language


![[SQL-Commands.png]]

## 1. DDL - Data Definition Language

used for defining, altering and deleting database structures such as tables, indexes and schemas.


| Command  | Description                                                                                   | Syntax                                                               |
| -------- | --------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| CREATE   | Create database or its objects (table, index, function, views, store procedure, and triggers) | CREATE TABLE table_name (column1 data_type, column2 data_type, ...); |
| DROP     | Delete objects from the database                                                              | DROP TABLE table_name;                                               |
| ALTER    | Alter the structure of the database                                                           | ALTER TABLE table_name ADD COLUMN column_name data_type;             |
| TRUNCATE | Remove all records from a table, including all spaces allocated for the records are removed   | TRUNCATE TABLE table_name;                                           |
| COMMENT  | Add comments to the data dictionary                                                           | COMMENT 'comment_text' ON TABLE table_name;                          |
| RENAME   | Rename an object existing in the database                                                     | RENAME TABLE old_table_name TO new_table_name;                       |

## 2. DQL - Data Query Language

to get some schema relation based on the query passed to it. This command allows getting the data out of the database to perform operations with it.

|Command|Description|Syntax|
|---|---|---|
|SELECT|It is used to retrieve data from the database|SELECT column1, column2, ...FROM table_name WHERE condition;|
|FROM|Indicates the ****table(s)**** from which to retrieve data.|SELECT column1  <br>FROM table_name;|
|WHERE|Filters rows ****before**** any grouping or aggregation|SELECT column1  <br>FROM table_name  <br>WHERE condition;|
|GROUP BY|Groups rows that have the same values in specified columns.|SELECT column1, AGG_FUNCTION(column2)  <br>FROM table_name  <br>GROUP BY column1;|
|HAVING|Filters the results of `GROUP BY`|SELECT column1, AGG_FUNCTION(column2)  <br>FROM table_name  <br>GROUP BY column1  <br>HAVING condition;|
|DISTINCT|Removes ****duplicate rows**** from the result set|SELECT DISTINCT column1, column2, ...  <br>FROM table_name;|
|ORDER BY|Sorts the result set by one or more columns|SELECT column1  <br>FROM table_name  <br>ORDER BY column1 [ASC \| DESC];|
|LIMIT|By default, it sorts in ****ascending order**** unless specified as `DESC`|SELECT * FROM table_name LIMIT number;|

## 3. DML - Data Manipulation Language

deal with the manipulation of data present in the database.
DCL statements are grouped with DML statements.

|Command|Description|Syntax|
|---|---|---|
|INSERT|Insert data into a table|INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);|
|UPDATE|Update existing data within a table|UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;|
|DELETE|Delete records from a database table|DELETE FROM table_name WHERE condition;|
|LOCK|Table control concurrency|LOCK TABLE table_name IN lock_mode;|
|CALL|Call a PL/SQL or JAVA subprogram|CALL procedure_name(arguments);|
|EXPLAIN PLAN|Describe the access path to data|EXPLAIN PLAN FOR SELECT * FROM table_name;|

## 4. DCL - Data Control Language

Includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions and other controls of the database system.

|Command|Description|Syntax|
|---|---|---|
|GRANT|Assigns new privileges to a user account, allowing access to specific database objects, actions, or functions.|GRANT privilege_type [(column_list)] ON [object_type] object_name TO user [WITH GRANT OPTION];|
|REVOKE|Removes previously granted privileges from a user account, taking away their access to certain database objects or actions.|REVOKE [GRANT OPTION FOR] privilege_type [(column_list)] ON [object_type] object_name FROM user [CASCADE];|

## 5. TCL - Transaction Control Language

|Command|Description|Syntax|
|---|---|---|
|BEGIN TRANSACTION|Starts a new transaction|BEGIN TRANSACTION [transaction_name];|
|COMMIT|Saves all changes made during the transaction|COMMIT;|
|ROLLBACK|Undoes all changes made during the transaction|ROLLBACK;|
|SAVEPOINT|Creates a savepoint within the current transaction|SAVEPOINT savepoint_name;|
#### Reference:

[geeksforgeeks.org](https://www.geeksforgeeks.org/sql/sql-tutorial/)

#### Check out more:
[[Data Constraints]] || [[SQL Tables]]