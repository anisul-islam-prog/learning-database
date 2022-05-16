# ztmDatabaseNotes

### What is database?

#### Answer:

A database is an organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). Together, the data and the DBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just database.

[reflink](https://www.oracle.com/database/what-is-database/)

### What is a query?

#### Answer:

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
|Action|Add, change, or delete data. Each task has a specific type of action query. Action queries are not available in Access web apps.|