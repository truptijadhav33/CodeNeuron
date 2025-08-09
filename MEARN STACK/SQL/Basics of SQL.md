### Introduction

**Structured Query Language (SQL)**  is the standard language used to interact with relational databases.

- Mainly used to manage data. Whether you want to create, delete, update or read data, SQL provides the structure and commands to perform these operations.
- Widely supported across various database systems like MySQL, Oracle, PostgreSQL, SQL Server and many others.
- Mainly works with Relational Databases (data is stored in the form of tables)
### SQL Data Types :

![[SQL-DataTypes.jpg]]


| **Category**    | **Data Type**               | **Description**                                                    |
| --------------- | --------------------------- | ------------------------------------------------------------------ |
| **Numeric**     | `INT` / `INTEGER`           | Whole numbers (positive, negative, zero).                          |
|                 | `SMALLINT`                  | Smaller range of whole numbers.                                    |
|                 | `BIGINT`                    | Larger range of whole numbers.                                     |
|                 | `DECIMAL(p, s)` / `NUMERIC` | Fixed-point numbers with precision `p` and scale `s`.              |
|                 | `FLOAT` / `REAL`            | Approximate floating-point numbers.                                |
|                 | `DOUBLE PRECISION`          | Larger precision floating-point numbers.                           |
| **String/Text** | `CHAR(n)`                   | Fixed-length string of `n` characters.                             |
|                 | `VARCHAR(n)`                | Variable-length string up to `n` characters.                       |
|                 | `TEXT`                      | Large variable-length text data.                                   |
| **Date/Time**   | `DATE`                      | Date only (YYYY-MM-DD).                                            |
|                 | `TIME`                      | Time only (HH:MM:SS).                                              |
|                 | `DATETIME` / `TIMESTAMP`    | Date and time together.                                            |
|                 | `YEAR`                      | Year in four digits.                                               |
| **Boolean**     | `BOOLEAN` / `BOOL`          | True/false values (stored as 1/0 internally in some systems).      |
| **Binary**      | `BLOB`                      | Binary large object (images, files, etc.).                         |
|                 | `BINARY(n)`                 | Fixed-length binary data.                                          |
|                 | `VARBINARY(n)`              | Variable-length binary data.                                       |
| **Other**       | `JSON`                      | Stores JSON-formatted data (supported in MySQL, PostgreSQL, etc.). |
|                 | `ENUM`                      | String with predefined possible values (MySQL).                    |
|                 | `XML`                       | Stores XML-formatted data (in some SQL systems).                   |

### SQL Operators

SQL operators are symbols or keywords used to perform operations on data in SQL queries.


| **Category**             | **Operator**              | **Description**                                         |
| ------------------------ | ------------------------- | ------------------------------------------------------- |
| **Arithmetic Operators** | `+`                       | Addition.                                               |
|                          | `-`                       | Subtraction.                                            |
|                          | `*`                       | Multiplication.                                         |
|                          | `/`                       | Division.                                               |
|                          | `%`                       | Modulus (remainder after division).                     |
| **Comparison Operators** | `=`                       | Equal to.                                               |
|                          | `<>` or `!=`              | Not equal to.                                           |
|                          | `>`                       | Greater than.                                           |
|                          | `<`                       | Less than.                                              |
|                          | `>=`                      | Greater than or equal to.                               |
|                          | `<=`                      | Less than or equal to.                                  |
|                          | `BETWEEN ... AND ...`     | Checks if value is within a range.                      |
|                          | `LIKE`                    | Pattern matching using wildcards (`%`, `_`).            |
|                          | `IN`                      | Checks if value exists in a list of values.             |
|                          | `IS NULL` / `IS NOT NULL` | Checks if a value is (or isn’t) `NULL`.                 |
| **Logical Operators**    | `AND`                     | Returns true if both conditions are true.               |
|                          | `OR`                      | Returns true if at least one condition is true.         |
|                          | `NOT`                     | Negates a condition.                                    |
|                          | `ALL`                     | Returns true if all subquery values meet condition.     |
|                          | `ANY` / `SOME`            | Returns true if any subquery value meets condition.     |
| **Bitwise Operators**    | `&`                       | Bitwise AND.                                            |
|                          | `                         | `                                                       |
|                          | `^`                       | Bitwise XOR (exclusive OR).                             |
|                          | `~`                       | Bitwise NOT (inverts bits).                             |
|                          | `<<`                      | Bitwise left shift.                                     |
|                          | `>>`                      | Bitwise right shift.                                    |
| **Compound Operators**   | `+=`                      | Add and assign.                                         |
|                          | `-=`                      | Subtract and assign.                                    |
|                          | `*=`                      | Multiply and assign.                                    |
|                          | `/=`                      | Divide and assign.                                      |
|                          | `%=`                      | Modulus and assign.                                     |
| **Special Operators**    | `EXISTS`                  | Returns true if a subquery returns one or more rows.    |
|                          | `ANY`                     | Returns true if any subquery value meets the condition. |
|                          | `ALL`                     | Returns true if all subquery values meet the condition. |
|                          | `SOME`                    | Synonym for `ANY` in some SQL dialects.                 |

#### Check out more:
[[SQL Database]] || [[SQL Tables]]