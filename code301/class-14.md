# DB Normalization 

> process used to organize a database into tables and columns.

- By limiting a table to one purpose you reduce the number of duplicate data contained within your database.

### Reasons for Database Normalization
- minimize duplicate data
- minimize or avoid data modification issues
- simplify queries

Having the table serve many purposes introduces many of the challenges; namely, data duplication, data update issues, and increased effort to query data.

### Data Duplication and Modification Anomalies
There are three modification anomalies that can occur:
- Insert Anomaly
- Update Anomaly 
- Deletion Anomaly 

### Definition of Database Normalization

- First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
- Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
- Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key