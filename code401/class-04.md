# Advanced Mongo/Mongoose

### Why would a developer choose to make data models?
A developer would choose to make data models to define how data is connected to each other and how they are processed and stored inside the system.

### What purpose do CRUD operations serve?
It serves the basic functions that an application must conventionally be able to fulfill in order to be considered “complete.”

### What kind of database is Postgres? What kind of database is MongoDB?
Postgres is a SQL database. MongoDB is a NoSQL databse.

### What is Mongoose and why do we need it?
Mongoose is a MongoDB object modeling tool. We need it to design the collection, define the shape of the documents within that collection.

### Describe how NoSQL Databases scale horizontally


### Give one strong argument for and against NoSQL Databases


### Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.
For a recipe app, you will have recipes by cuisine or main ingredient category and each recipe will have its list of ingredients and instructions. 

### Name 3 cloud based NoSQL Databases
- DynamoDB
- Google Cloud Datastore
- Couchbase

| Term | Definition |
| ---| --- |
| database | organized collection of structured information, or data, typically stored electronically in a computer system.Typically modeled in rows and columns in a series of tables to make processing and data querying efficient. The data can then be easily accessed, managed, modified, updated, controlled, and organized.  [Oracle](https://www.oracle.com/database/what-is-database.html) |
| Data Model | A data model documents and organizes data, how it is stored and accessed, and the relationships among different types of data. |
|CRUD|When building APIs, we want our models to provide four basic types of functionality: Create, Read, Update, and Delete. [Rapid API](https://rapidapi.com/blog/api-glossary/crud/)|
|Schema|A database schema represents the logical configuration of all or part of a relational database. [lucidchart](https://www.lucidchart.com/pages/database-diagram/database-schema)|
|Sanitize|means removing vulgarities & odd symbols from text, also removing potentially damaging contents to avoid intrusion attempts. [Medium](https://medium.com/@abderrahman.hamila/what-sanitize-mean-and-why-sanitize-in-code-data-5c68c9f76164)|
|Structured Query Language (SQL)|SQL is a programming language used by nearly all relational databases to query, manipulate, and define data, and to provide access control. [Oracle](https://www.oracle.com/database/what-is-database.html)|
|Non SQL (NoSQL)|non-relational database. They provide flexible schemas and scale easily with large amounts of data and high user loads. [MongoDB](https://www.mongodb.com/nosql-explained), [AWS](https://aws.amazon.com/nosql/)|
|MongoDB|MongoDB is a NonSQL database that stores data in flexible, JSON-like documents, meaning fields can vary from document to document and data structure can be changed over time. [MongoDB](https://www.mongodb.com/nosql-explained)|
|Mongoose|Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment. Mongoose supports both promises and callbacks. It provides a straight-forward, schema-based solution to model your application data. [mongoosejs](https://mongoosejs.com/)|
|record|A record is a set of data stored in a table, it is an object that can contain one or more values.|
|document|A document database is a type of nonrelational database that is designed to store and query data as JSON-like documents. Document databases make it easier for developers to store and query data in a database by using the same document-model format they use in their application code. [AWS](https://aws.amazon.com/nosql/document/#:~:text=The%20document%20database%20defined,use%20in%20their%20application%20code.)|
|Object Relation Mapping (ORM)|allows us to query and manipulate data stored in a relational database using an object-oriented approach. [Medium](https://medium.com/@codeshifu/object-relational-mapping-concepts-e2ff0838590c), [MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Web_frameworks)|

