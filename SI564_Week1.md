Dear Raj,



Hope this mail finds you well. It is my pleasure to work with you and I am willing to help you gain a basic understanding of the current database Borromean has in place. And here are my answers with you confusions about the database:

***

**Part 1**

1. *From the reading what are the 3 types of relationships the author defines.*  

   one-to-one, one-to-many, and many-to-many.

2. *Can you define a few different entities that could be related. For example, Class<->professor.* 

   Community<->Building     Buiding<->Room     Room<->Resident;

   University<->School    School<->Department    Department<->Division    Division<->Faculty.

3. *The author defines 2 different types of databases, in what use case at might you use each type?*

   Hierarchical Database:

   The university is a kind of hierarchical system. A university have sevral schools. Each School have several departments. Under each department there are different divisions. And under each division there are corresponding employees.

   Relational Database: 

   In warehouse management database system, we can use customer id as unique id in each tables(order table, payment table, address table) to connect them. And this is a typical one-to-many relationship between customer and other entities since a customer can make several payments, order several times  and have multiple addresses.

   

**Part 2**

1. *What databases are you able to see?*

   There are 14 databases, they are:

   bikes, information_schema, kubedb_system, mysql, performance_schema, ro_company1, ro_employees    , ro_query, ro_recipes, ro_research1, ro_twitter, sakila, sys, world.        

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230907194145241.png" alt="image-20230907194145241" style="zoom:50%;" />

2. *If you look at the ro_query database, how many tables are in this database?  Sales indicates there should be 4. I think there are 5? Help us decide who is correct.* 

   There are two tables(home_value_by_zip, taxdata) in the ro_query database. None of you is correct.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230907195731538.png" alt="image-20230907195731538" style="zoom:50%;" />

3. *What columns are there in the tax table?* 

   There are 12 columns in the tax table, they are: id, ein, name, year, revenue, expenses, purpose, ptid, ptname, city, state, url.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230907200049198.png" alt="image-20230907200049198" style="zoom:50%;" />

4. *Inside the ro_employees database, how many rows are in the titles table.* 

   There are 443308 rows in the titles table.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230907201011368.png" alt="image-20230907201011368" style="zoom:50%;" />

***

Thank you!



Best,

Jun