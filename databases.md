# Databases

## Cardinality

+ Cardinality (or data cardinality) : A measure on how many unique records are
there in a column/table.
+ Relationship cardinality : The relationship between the tables like
one-to-many etc.

In data modeling, most of the times, relationship cardinality is refered by the word
"cardinality".

Generally (in db query optimization), "Cardinality" refers to data cardinality, 
i.e number of distinct values in a column or table. If a column has 3 unique values, 
it's said to have cardianality of 3.

+ High cardinality
    - Refers to columns with high uniqueness like email or usernames.
+ Normal cardinality 
    - Not uniques as high cardinality, but fairly unique, like in names,
    vehical types etc.
+ Low cardinality
    - Refers to columns with very low uniqueness like in boolean values
    such as gender, status flags etc.

Refer to [this SO answer](https://stackoverflow.com/a/25548661).

## Degree of a table

The degree of a relation is the number of attributes (columns) in the given
table. It is also called as Arity. In some books, each row of the table is
called as degree-tuple, for example, in a table with 3 attributes each row is a
3-tuple.

For example, a table with 5 columns (5 attr) has a degree of 5.

## Relationship between a primary key and a foreign key in a relational DB

Primary key of a table act as a foreign key in another table. Primary key of a table and 
a foreign key of another table establishes a relationship between those two tables.

+ Primary key: Identifies each record in a table uniquely.
+ Foreign key: A primary key of another table.

## Advantages of replacing a manual database with an electronic one

+ Accuracy
+ Efficiency
+ Easy to take backups
+ Easy to query, filter and search data
+ Data security is high
+ Scalability

## Advantages of normalisation

Note: ACID stands for Atomicity, Consistency, Isolation, Durability

+ **Data integrity and consistancy is maintained** hence DB is ACID complient.
+ **No data duplication** (**Smaller size database**).
+ **Data modification anamalies are reduced.**
+ **Better performance** (faster access speeds)
+ **Cleaner and easier to maintain and change.**
+ **Updates run quickly** as no data is being duplicated in multiple locations.
+ **Insert operations run quickly** as there are duplication is not required.
+ **Smaller tables.**
