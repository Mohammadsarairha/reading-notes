# Databases and ERDs

## Entity Data Model

The Entity Data Model (EDM) is a set of concepts that describe the structure of data, regardless of its stored form. The EDM borrows from the Entity-Relationship Model described by Peter Chen in 1976, but it also builds on the Entity-Relationship Model and extends its traditional uses.




## What is a Schema?

A schema is a cognitive framework or concept that helps organize and interpret information. Schemas can be useful because they allow us to take shortcuts in interpreting the vast amount of information that is available in our environment.

Why do we use them?

People use schemata (the plural of schema) to categorize objects and events based on common elements and characteristics and thus interpret and predict the world. New information is processed according to how it fits into these mental structures, or rules.

## What do they look like?

![Schema](https://database.guide/wp-content/uploads/2016/06/MySQL_Schema_Music_Example.png)
### Database Keys

A key in database is an attribute or a set of attributes that help to uniquely identify a tuple (or row) in a relation (or table). Keys are also used to establish relationships between the different tables and columns of a relational database. Individual values in a key are called key values.

### What is a Primary Key?

A primary key is a column of a table or a set of columns that helps to identify every record present in that table uniquely. There can be only one primary Key in a table. Also, the primary Key cannot have the same values repeating for any row. Every value of the primary key has to be different with no repetitions.

### What is a Foreign Key?

Foreign Key is used to establish relationships between two tables. A foreign key will require each value in a column or set of columns to match the Primary Key of the referential table. Foreign keys help to maintain data and referential integrity. 

### What is a Composite Key?

Composite Key is a set of two or more attributes that help identify each tuple in a table uniquely. The attributes in the set may not be unique when considered separately. However, when taken all together, they will ensure uniqueness.

## How are they different? When do you use 1 over the others?

- SQL keys are used to uniquely identify rows in a table.
- SQL keys can either be a single column or a group of columns.
- Super key is a single key or a group of multiple keys that can uniquely identify tuples in a table.
- Super keys can contain redundant attributes that might not be important for identifying tuples.

## What is a 1:1 relationship?

A one-to-one (1:1) relationship means that each record in Table A relates to one, and only one, record in Table B, and each record in Table B relates to one, and only one, record in Table A.

## What is a Many: Many relationship?

A many-to-many relationship occurs when multiple record in a table are associated with multiple records in another table. For example, a many-to-many relationship exists between customers and products: customers can purchase various products, and products can be purchased by many customers.

## Things I want to know more about

- Should i need DBMS  form creating database and tables database in C# ?

- Did i need LINQ to excite SQL query ?

- Why i need Data moble ?




