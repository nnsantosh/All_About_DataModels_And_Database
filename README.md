# All_About_DataModels_And_Database
Read about different kind of data models and databases

SQL DB(Example: MySQL)
1. If you have structured schema and you are clear as to which data needs to go to which table. All the records in the table need to adhere to that schema.
Schema is defined by fields(Columns).
2. You will need to normalize data to make it adhere to your defined schema.
3. Tables can have relations with each other. The relations can be of type one-to-many, many-to-many and one-to-one.
4. SQL language is capable of querying these relations. Joins can be used to retrieve connected data in one result set even if data is stored across multiple tables.
Example: Users table, Products table and Orders table.

NOSQL DB(Example: MongoDB)
1. Instead of tables we have Collections. In such a collection we have so called Documents. You can corelate them to Rows in a table. But they don't have to use the same schema. So in same collection you can have documents with different schema. So there is no schema imposed.
2. There is no relations between the collections. So the idea is that every document in a collection will hold all the information.
Example: Orders collection every document can contain user data and product data.
{id:1, user:{id:1,email:'test@gmail.com'},product:{id:2,price:9.99}}
But this results in duplicate data and also if the product price changes you will have to update that in multiple documents and collections. But if you have lot of reads and not many writes for Products then this would be a good set up.

When to choose between SQLDB vs NoSQL DB?
It depends on the kind of application you are building and the kind of data that you are storing. 

SQL                                                                       | No SQL
--------------------------------------------------------------------------|-----------------------------------------------------------------------
Data Uses Schemas                                                         | Schema-less
Relations                                                                 | No Relations
Data is distributed across multiple tables                                | Data is typically merged/nested in few collections.
Horizantal scaling is difficult or impossible.                            | Both horizontal and vertical scaling is possible.
Vertical scaling is possible.                                             
Limitations for lots of read and write queries per second                 | Greate performance for mass read and writes.Except for cases where we will update lot                                                                             of collections regularly.
                                                                                                                       

