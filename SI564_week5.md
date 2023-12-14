Dear Lawrence,



Hope this mail finds you well. It is my pleasue to make contributions with our acquistion plan and I will obey the NDA rule not to talk this with anyone. Here are my answers with you questions:

***

1. *What is the average customer's credit limit?* 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008234833009.png" alt="image-20231008234833009" style="zoom:50%;" />

   <u>Table Documentation</u>

   *customers*

   |       Field Name       | Data Type |                 Values                  | Note        |
   | :--------------------: | :-------: | :-------------------------------------: | ----------- |
   |     customerNumber     |    int    |           number of customer            | primary key |
   |      customerName      |  varchar  |            name of customer             |             |
   |    contactLastName     |  varchar  |          last name of contact           |             |
   |    contactFirstName    |  varchar  |          first nme of contact           |             |
   |         phone          |  varchar  |        phone number of customer         |             |
   |      addressLine1      |  varchar  |          first line of address          |             |
   |      addressLine2      |  varchar  |         second line of address          |             |
   |          city          |  varchar  |            city of customer             |             |
   |         state          |  varchar  |        state where customer live        |             |
   |       postalCode       |  varchar  |       zipcode of customer address       |             |
   |        country         |  varchar  |           country of customer           |             |
   | salesRepEmployeeNumber |    int    | number of employee sales representative |             |
   |      creditLimit       |  decimal  |       credit limit of of customer       |             |

   

2. *Please provide a list of each customer, their phone number and the payments they have made.* 

   There are 273 rows, so I screenshot part of it.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008235607819.png" alt="image-20231008235607819" style="zoom:50%;" />

   <u>Table Documentation</u>

   *Payments*

   |   Field Name   | Data Type |          Values           | Note        |
   | :------------: | :-------: | :-----------------------: | ----------- |
   | customerNumber |    int    |    number of customer     | primary key |
   |  checkNumber   |  varchar  | number of chcking account |             |
   |  paymentDate   |   pate    |      date of payment      |             |
   |    ammount     |  decimal  |     amount of payment     |             |

3. *We have a customer that has a phone number of 2125558493. Please provide the total this customer has paid us. Write your query so that you don't have to do any math. (You will need to use joins and an aggregate function. )*

   The total amount is $\$69214.33$.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009005222030.png" alt="image-20231009005222030" style="zoom:50%;" />

4. *Please provide the average payment for customers who are in the state of New York and customers who are NOT in the state of New York.  You will need 2 queries to do this.* 

   Average Payments in NY:

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009005649277.png" alt="image-20231009005649277" style="zoom:50%;" />

   Average Payments **NOT** in NY:

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009011844065.png" alt="image-20231009011844065" style="zoom:50%;" />

5. *For orders that have shipped, what is the average spent per item.*

   Average Spent Per Item: $\$91.03358$.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009010436967.png" alt="image-20231009010436967" style="zoom:50%;" />

   <u>Table Documentation</u>

   *orders*

   |   Field Name   | Data Type |            Values             | Note        |
   | :------------: | :-------: | :---------------------------: | ----------- |
   |  orderNumber   |    int    |        number of order        | primary key |
   |   orderDate    |   date    |         date of order         |             |
   |  requiredDate  |   date    |    date required for order    |             |
   |  shipped date  |   date    |    date when order shipped    |             |
   |     status     |  varchar  | current status for the order  |             |
   |    comments    |   text    |  comments left for the order  |             |
   | customerNumber |    int    | corresponding customer number |             |

   *orderdetails*

   |   Field Name    | Data Type |         Values          | Note        |
   | :-------------: | :-------: | :---------------------: | ----------- |
   |   orderNumber   |    int    |     number of order     | primary key |
   |   productCode   |  varchar  |     code of product     |             |
   | quantityOrdered |    int    | number of items ordered |             |
   |    priceEach    |  decimal  |  price of each product  |             |
   | orderLineNumber |    int    |  number of order line   |             |

6. *Please provide a list of all employees and who they report to (I want names).  I am told there are 23 people that work at this company.* 

   

   

   

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009035658992.png" alt="image-20231009035658992" style="zoom:50%;" />

   <u>Table Documentation</u>

   *employees*

   |   Field Name   | Data Type |              Values              | Note        |
   | :------------: | :-------: | :------------------------------: | ----------- |
   | employeeNumber |    int    |        number of employee        | primary key |
   |    lastName    |  varchar  |      last name of employee       |             |
   |   firstName    |  varchar  |      first name of employee      |             |
   |   extension    |  varchar  |      extension of employee       |             |
   |     email      |  varcahr  |        email of employee         |             |
   |   officeCode   |  varchar  |     office code of employee      |             |
   |   reportsTo    |    int    | if of person employee reports to |             |
   |    jobTitle    |  varchar  |       jobtitle of employee       |             |

7. *MSRP is the manufacturer's suggested retail price. Buy price is the price the classic models is charged. Our markup on a product is the difference. Please create a query that shows the buyprice, the MSRP, the markup (labeled markup) and the first 5 characters of the product line textDescription. You should order this by the markup and limit it to 5, so that I can show our board the 5 most marked up products.* 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009022504414.png" alt="image-20231009022504414" style="zoom:50%;" />

   <u>Table Documentation</u>

   *Products*

   |     Field Name     | Data Type |        Values        | Note        |
   | :----------------: | :-------: | :------------------: | ----------- |
   |    productCode     |  varchar  |   code of product    | primary key |
   |    productName     |  varchar  |   name of product    |             |
   |    productScale    |  varchar  |   scale of product   |             |
   |   productVendor    |  varchar  |  vendor of product   |             |
   | productDescription |   text    | product description  |             |
   |  quantityInStock   |    int    |   stock of product   |             |
   |      buyPrice      |  decimal  | buy price of product |             |
   |        MSRP        |  decimal  |   MSRP or product    |             |

   *ProductLines*

   |   Field Name    | Data Type |              Values              | Note        |
   | :-------------: | :-------: | :------------------------------: | ----------- |
   |   productLine   |  varchar  |           product line           | primary key |
   | textDescription |  varchar  |   description of product line    |             |
   | htmlDescription |   text    | html description of product line |             |
   |      image      |   blob    |       img of product line        |             |

8. *Please provide a list of employees that had an order in 2005.* 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009024257995.png" alt="image-20231009024257995" style="zoom:50%;" />

9. *Please provide a total of all orders with customers who are in postalCodes of 97562, 80686 and 44000*

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009024829410.png" alt="image-20231009024829410" style="zoom:50%;" />

*Also, I have been trying to teach myself SQL. Can you help me with joins. If I want records from 2 tables where there is a match on the left table and the right table, what type of join do I want.* 

**INNER JOIN**

*If I want records from 2 tables where I get ALL the records on the right table and only matching records from the left table, what type of Join do I want?*

**RIGHT JOIN**

***

Also I have attached my ERD for the classicmodels database at the end. Hopfully that will be helpful.



Regards,

Jun





# ERD



<img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231009031133171.png" alt="image-20231009031133171" style="zoom:50%;" />