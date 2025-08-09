the process of creating and managing databases.
A database acts as a container where all your data tables, views, stored procedures etc are stored.

### CREATE DATABASE:

****CREATE DATABASE**** Command is used to create a new database within a SQL based ****Database Management System**** (DBMS) such as MySQL, PostgreSQL, or SQL Server.

*Syntax:*
```sql
CREATE DATABASE database_name;
```

*Example:*
```sql
CREATE DATABASE college;
```

## Switching to New Database:

*Syntax:*
```sql
USE database_name;
```

****Example:****

```
USE college;
```

## Deleting a Database

The DROP DATABASE command can be used to delete the database and all its contents.

*Syntax:*

```sql
DROP DATABASE database_name;
```

*For Example:*

```sql
DROP DATABASE college;
```

### Database Already Exists

- If you try to create a database with a name that already exists, you’ll see an error. To avoid this, either choose a new name or use the `IF NOT EXISTS` clause to only create the database if it doesn't already exist.

*Example:*

```sql
CREATE DATABASE IF NOT EXISTS instagram;
```

- To avoid any error while running the ****DROP DATABASE**** command use the IF EXISTS clause, which will delete the database only if it exists in the system.
*Example:*

```sql
DROP DATABASE IF EXISTS college;
```

