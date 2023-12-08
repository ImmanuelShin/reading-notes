# Class 11

## SQL vs NoSQL

|SQL   |  NoSQL |
|---|---|
| Relational databases | Non-relational/Distributed  |
| Predefined schema  |  Dynamic schema |
| Vertically scalable (i.e faster hardware)  | Horizontally scalable (i.e more hardware) |
| Table based data  | Key-value/Documents/Graph/Wide-column stores  |
| Better for complex query intensive environments  | Better for big data (i.e HBase) |
| MySql, Oracle, Sqlite, Postgres  | MongoDB, BigTable, Redis  |
| Better refined data search  | Better for hierarchical data storage |

SQL stands for Structured Query Language. You create keywords that search specific data and combine them to form a powerful search function. After a certain amount of keywords, you create so many relations between keys and data that you can saturate a lot of information.  
This relational database works in a table structure. Each table will have multiple fields, or columns, and each field will have multiple records, or rows. This organizational structure lays out the schema. Every record follows this schema. That means that any new record added and any record retrieved will have to be referred to by this schema.  
Once we have multiple tables, we can create a relation with another table that connects multiple tables together.  
Types of relations include:

- One to One: One table's info relates directly to only one other table's.
- One to Many: One table's info can relate to multiple of another table's info.
- Many to Many: Multiple tables can relate to multiple tables.

NoSQL. In this case MongoDB. MongoDB stands for humongous. It's because it is usually used for big data.
MongoDB organizes data in a hierarchical structure. It doesn't have any schema, which means some records might not have the same information as other info. This makes it harder to search for, but more flexible. There isn't really relations in NoSQL, which means that data needs to merged manually. Instead, NoSQL puts all the information into one place.

Both SQL and NoSQL has their pros and cons.
SQL uses schemas and relations that restrict flexibility, but promote organization and ease of change. Disadvantage comes from lots of reads where the structure slows down the read.
NoSQL doesn't use schema and all the data will be in one place. This makes it faster to read, but harder to update and will sometimes create duplicates.

## Things I want to know more about
