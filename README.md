# ztmDatabaseNotes

### What is database?

A database is a structured collection of information or data that is often kept electronically in a computer system. A database management system is generally in charge of a database (DBMS). The data and the DBMS, as well as the applications that are linked with them, are together referred to as a database system, which is frequently abbreviated to just database.

### What is a query?

A query can be a request for data results from your database, or it might be a request for action on the data, or it can be both. A query can answer a basic question, conduct computations, aggregate data from many tables, and add, edit, or delete information from a database. It is also known as ***SQL Statement***. Following is an example of a query:
```
SELECT name
FROM users
WHERE role='manager';
```
In the above example, the `SELECT name`, `FROM users` and `WHERE role='manager'` are clauses. `name` is identifier i.e. the column name. Instead of `name`, you can use `*`(*wildcard*) which means the query should return all columns of the queried tables. `users` is the name of the table from where data is being selected.`WHERE role='manager'` is a condition. Here, `WHERE` is a keyword, `role` is a column in the table and it should match the expression `'manager'` for each rows.

Try running the example and changing the condition to `employee` in this [db fiddle](https://www.db-fiddle.com/f/ogAiTgZPjwvDxwVHiVK3Ek/0)


There are various types of queries because queries are so versatile, and you would build one dependent on the task.
| Major query types | Use |
|-------------------|-----|
|Select|To retrieve data from a table or make calculations.|
|Action|Add, change, or delete data. Each task has a specific type of action query.|

### What is a declarative programming language?

A declarative programming language is one example. Expressions do not explicitly describe computations, but rather convey the form of the outcome of some operation. It is the database system's query interpreter's responsibility to develop and execute a computing procedure to produce such a result.