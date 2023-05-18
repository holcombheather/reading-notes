# Data Modeling


## [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

1. What type of database is the best fit for the complex query intensive environment?
    - SQL (Relational DB) is designed to handle structured data and support complex querying through the standardized language SQL which allows you to retreive and manipulate data. 

2. What type of database is the best fit for hierarchical data storage?
    - NoSQL (non-relational or distributed DB) is designed to handle unstructured or semi-structured data.  Document-oriented databases can store nested or nested-like structures without predefined schemas which makes them great for storing JSON-like documents are data with varying attributes. 

3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.
    - SQL databases are designed to scale vertically where you increase the hardware resources of a single server to handle increasing loads. 
    - NoSQL (non-relational or distributed) databases are designed to scale horizonally by distributing data across multiple servers forming a cluster. You can add more servers to the cluster and effectively increase the database's capacity. This horizontal scaling provides greater flexilibilty and allows you to handle larger amounts of data. 


## [sql modeling techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)

1. Among data tables, what is a one-to-many relationship and how do we “relate” them?
    In a one-to-many relationship, one table can be related to more than one entry in another. For example one customer can be related to many orders. To relate the tables in this relationship you use a foreign key in table that represents the *many* side of the relationship (ex: orders). So the orders table would have a foreign key column that references the primary key of the customers table. The foreign key establishes the relationship between two tables by linking each of the order to its corresponding customer. 

2. Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.
    Propr to designing your relational database, it might be useful to **create a diagram** of the database tables and their relationships. 
    

3. Explain the difference between a primary and foreign key.
    - **Primary Keys**:  Remember the primary keys uniquely identify each row in a table.  A table typically has one primary key, but can have more.  When the key has more than one column, it is called a compound key.
    - **Foreign Key**: This is a column or set of columns which match a primary key in another table. 


## [sql vs nosql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

1. How do we treat keywords and parameters differently in SQL syntax?
    - Keywords in SQL have predefined meanings in SQL and are used to maniuplate the structure and data within a database. Ex: SELECT, INSERT, UPDATE, DELETE, JOIN
    - Parameters are placeholders or variables that are used to pass values dynamically into SQL statements until the actual values are provided when the SQL statement is executed. 
2. Define normalization within the context of schemas and data.
    - Process of organizing and structuring data in a relational database to minimize redundancy, improve data integrity, and enhance query performance. 
3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
    - One-to-one: A one-to-one is a relationship where one record in a table is associated with exactly one record in another table. For example: exmployee & employee ID. 
    - One-to-Many: One record in the first table can be related to many records in the second table. For example: department & employees. 
    - Many-to-many: A many-to-many relationship occurs when multiple records in one table can be associated with multiple records in another table. For example: students & courses. 


## Bookmark and Review

- [sequelize api](https://sequelize.org/master/)

## Reflection

What are your learning goals after reading and reviewing the [class README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-04/)?

- Describe and Define: 
    - The role of data models.
    - CRUD Operations.
    - The “Collection” design pattern.
    - Interfaces and Services.
    - The differences between SQL and NoSQL Databases.
    - SQL databases, tables, and queries.
    - Modeling relational data.
- Execute
    - Model real world data.
    - Create models with constraints, relations, type checking, and validity using Sequelize.
    - Create an extensible CRUD interface and an implementation for a data model.
    - Proficiency with the psql shell and basic SQL commands.