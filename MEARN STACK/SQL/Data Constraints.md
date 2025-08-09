
In SQL, **data constraints** are rules you apply to a table's columns to control the type, range, and validity of data stored in them.  
They help enforce **data integrity**—meaning your database stays consistent, accurate, and reliable.

|Constraint Name|Description|Example Usage|
|---|---|---|
|**NOT NULL**|Ensures a column cannot store `NULL` values.|`name VARCHAR(50) NOT NULL`|
|**PRIMARY KEY**|Uniquely identifies each record in a table; automatically `NOT NULL` and `UNIQUE`.|`id INT PRIMARY KEY`|
|**FOREIGN KEY**|Enforces referential integrity between two tables by linking a column to another table’s primary key.|`FOREIGN KEY (dept_id) REFERENCES department(id)`|
|**COMPOSITE KEY**|A primary key made up of two or more columns to uniquely identify a row.|`PRIMARY KEY (order_id, product_id)`|
|**UNIQUE**|Ensures all values in a column (or combination of columns) are unique.|`email VARCHAR(100) UNIQUE`|
|**ALTERNATE KEY**|Any candidate key that is not chosen as the primary key; still unique.|If `email` is unique but `id` is the primary key, then `email` is an alternate key.|
|**CHECK**|Ensures column values meet a specified condition.|`salary INT CHECK (salary > 0)`|
|**DEFAULT**|Assigns a default value to a column if no value is provided during insertion.|`status VARCHAR(10) DEFAULT 'active'`|


