Dear Raj,



Hope you had a lovely weekend! It is my pleasure to help with decision making in our company's non-profit investment. Here are my answers for your questions:

***

<u>**Part 1 - Revenue**</u>

1. *2014 was a key year for generating revenue. How many Ann Arbor-based companies (rows) are listed in the database that year?*

   There are 247 Ann Arbor-based companies are listed in the database in 2014.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231012221049585.png" alt="image-20231012221049585" style="zoom:50%;" />

   <u>taxdata</u>
   
   | Field Name | Data Type |           Values            | Note        |
   | :--------: | :-------: | :-------------------------: | ----------- |
   |     id     |    int    |      if of the company      | primary key |
   |    ein     |    int    | ein arrnaged to the company |             |
   |    name    |  varchar  |     name of the company     |             |
   |    year    |    int    |           taxyear           |             |
   |  revenue   |    int    |   revenue of the company    |             |
   |  expenses  |    int    |   expense of the company    |             |
   |  purpose   |   text    |   purpose of the company    |             |
   |    ptid    |  varchar  |     ptid of the company     |             |
   |   ptname   |  varchar  |    ptname of the company    |             |
   |    city    |  varchar  | city where company located  |             |
   |   state    |  varchar  |   cstate where company in   |             |
   |    url     |  varchar  |       url of company        |             |
   
2. *To get a broader picture, we also need a list of the names of ALL of the companies that generated more than $10,000,000,000 (ten billion dollars) in 2014.*

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230923144223637.png" alt="image-20230923144223637" style="zoom:50%;" />

3. *How does this compare to how many unique companies generated a revenue of more than $1,000,000,000 (one billion dollars) in any year?*

   There are 404 unique companies made revenue more than $1,000,000,000$ in any year.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230923150716400.png" alt="image-20230923150716400" style="zoom:50%;" />

   

<u>**Part 2 - Expenses**</u>

1. *We are looking for the top 20 unique companies by expenses (as in: who had the most expenses?). Your query should provide the name of the company and their expenses in 2013.* 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230923150255310.png" alt="image-20230923150255310" style="zoom:50%;" />

2. *We also need to know the EINs and cities for each company that made between \$1-100,000 in revenue and between $10000-200,000 in expenses. (If this list is long, just give us a random selection of 20 and your query)* 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230923151729686.png" alt="image-20230923151729686" style="zoom:50%;" />

<u>**Part 3 - Specific Words**</u>

1. *First, we are interested in the number of companies with the word "toy" anywhere in the ‘purpose’ field.*

   There are 378 companies with the word 'toy' anywhere in the 'purpose' field.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231012222137732.png" alt="image-20231012222137732" style="zoom:50%;" />

2. *Additionally, we need data on how many rows have both the word ‘smith’ in the ‘ptname’ field and have reported revenue (e.g. revenue is not empty or 0).*

   There are 2796 rows meet the above requirements.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231012222304135.png" alt="image-20231012222304135" style="zoom:50%;" />

<u>**Part 4**</u>

1. *First, we need to know the company name and length of the name for 50 random companies with a ptid of P01345770.*

   The following is my query and part of the output table;

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230923153133388.png" alt="image-20230923153133388" style="zoom:50%;" />

2. *Second, we need the number of companies that have a ‘purpose’ field containing less than 10 characters. Keep in mind that the value of the ‘purpose’ field should never be an empty string.*

   There are 917 companies meet the requirement.

<img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231012222531217.png" alt="image-20231012222531217" style="zoom:50%;" />

<u>**Part 5 - Employee's**</u> 

1. *What shortest WHERE clause can you write to query the number of folks that got hired in 1994, 1995 and 1990. (You can do this using the count(1) syntax as discussed in class, or a query that returns all the records and you just count). I want the shortest WHERE query possible.* 

   The following is my query:

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231012222819273.png" alt="image-20231012222819273" style="zoom:50%;" />

2.  *What query will provide a count of all 'Senior Engineer' that were at the company on 1986-06-26. (Hint, this is not a simple where date=1)* 

   The following is my query:

<img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231012223202876.png" alt="image-20231012223202876" style="zoom:50%;" />

<u>employees</u>

| Field Name |   Data Type    |         Values         | Note        |
| :--------: | :------------: | :--------------------: | ----------- |
|   emp_no   |      int       |    employee number     | primary key |
| birth_date |      date      | birthdate of employee  |             |
| first_name |    varchar     | first name of employee |             |
| last_name  |    varchar     | last name of employee  |             |
|   gender   | enum('M', 'F') |   gender of employee   |             |
| hire_date  |      date      |  employee hired date   |             |

3. *Can you give me a list of unique names of folks that have had a title of "Engineer". We have not covered joins yet, so please make sure to do this without a join and in a single query.* 

   There are 11930 names meet the requirements showed in the following picture, to give a short preview I added 'limit 10' command at the last:
   
   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230923202544149.png" alt="image-20230923202544149" style="zoom:50%;" />
   
   <u>Title</u>
   
   | Field Name | Data Type |           Values           | Note        |
   | :--------: | :-------: | :------------------------: | ----------- |
   |   emp_no   |    int    |      employee number       | primary key |
   |   title    |  varchar  |     title of employee      |             |
   | from_date  |   date    |  employee hired from date  |             |
   |  to_date   |   date    | employee left company date |             |

***

Hopefully my analytics will be helpful! Thank you!



Best regards,

Jun
