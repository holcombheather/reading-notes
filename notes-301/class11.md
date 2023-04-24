# MongoDB

## SQL vs NoSQL

SQL | NoSQL
--- | ---
Uses a schema | Does not use a schema
Structured data storage | Unstructured data storage
Vertically scalable | Horizontally scalable
ACID compliant | Not always ACID compliant
Not suitable for large-scale and rapid data growth | Suitable for large-scale and rapid data growth

## What kind of data is a good fit for an SQL database?
Structured and well-defined data, such as financial transactions, inventory management, and customer relationship management (CRM) systems.

Real world example: Bank transaction records, online store order management system, and airline reservation systems.

## What kind of data is a good fit for a NoSQL database?
Unstructured or semi-structured data, such as social media data, sensor data, and user-generated content, which can be difficult to organize in a structured way.

Real world example: Twitter feeds, clickstream data, and weather sensor data.

## Which type of database is best for hierarchical data storage?
NoSQL databases are best suited for hierarchical data storage because they can store unstructured and semi-structured data, which is ideal for hierarchical data.

## Which type of database is best for scalability?
NoSQL databases are more scalable than SQL databases. They are designed to handle large amounts of data that can be distributed across multiple servers and nodes, making them well-suited for scaling horizontally.

### Videos:
[SQL vs NoSQL (Video)](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

## What does SQL stand for?
SQL stands for Structured Query Language.

## What is a relational database?
A relational database is a type of database that stores data in tables with predefined relationships between them. The relationships are defined by primary and foreign keys that link data across tables.

## What type of structure does a relational database work with?
A relational database works with a structured data model, where data is organized in predefined tables with defined relationships between them.

## What is a ‘schema’?
A schema is a blueprint or plan for organizing data in a database. It defines the structure of the database and specifies the rules and constraints that must be followed when adding, updating, or deleting data.

## What is a NoSQL database?
A NoSQL database is a non-relational database that does not use a structured data model. It can store unstructured or semi-structured data, making it more flexible than traditional SQL databases.

## How does it work?
NoSQL databases work by using various data models, including key-value, document, graph, or column-family, to store and retrieve data. They do not use a predefined schema, so they can easily adapt to changing data requirements.

## What is inside of a MongoDB database?
A MongoDB database contains collections of documents, which are similar to records in a traditional SQL database. Each document can have its own structure and does not need to conform to a pre-defined schema.

## Which is more flexible - SQL or MongoDB? and why.
MongoDB is more flexible than SQL because it allows for the storage of unstructured and semi-structured data, while SQL requires a pre-defined schema. MongoDB also offers a more natural representation of data, allowing for faster and more efficient queries.

## What is the disadvantage of a NoSQL database?
One disadvantage of NoSQL databases is that they do not provide the same level of transactional consistency as SQL databases. They are also less mature than SQL databases, so there is less support for them in terms of development tools and libraries.
