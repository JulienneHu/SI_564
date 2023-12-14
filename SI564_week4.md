Hi Sarah,



Hope this mail finds you well. It has been a long time not to see you. Here are my answers with your questions.

***

**Part 1**

I have a database of recipes, and I could really use your help in finding out some information. This is called **ro_recipes**.

1. What are the recipe titles that are either a vegetable or a salad? I want to provide this information to my friend; please give me a SINGLE query that does this without any numbers in the query. 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231001214610711.png" alt="image-20231001214610711" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>Recipes</u>	

   |  Field Name   | Data Type |               Values               | Note                                |
   | :-----------: | :-------: | :--------------------------------: | ----------------------------------- |
   |   RecipeID    |    int    |         ID for the Recipe          | primary key                         |
   |  RecipeTitle  |  varchar  |        Title for the Recipe        |                                     |
   | RecipeClassID |    int    |    Class ID the recipe belongs     | foregin key with Recipe_Class table |
   |  Preparation  |   text    | Preparation Process for the Recipe |                                     |
   |     Notes     |   text    |        Tips for the recipe         |                                     |

   <u>Recipe_Classes</u>

   |       Field Name       | Data Type |                    Values                     | Note        |
   | :--------------------: | :-------: | :-------------------------------------------: | ----------- |
   |     RecipeClassID      |    int    |           Recipe Class ID category            | primary key |
   | RecipeClassDescription |  varchar  | Corresponding text description with number ID |             |

2. I have someone that is allergic to seafood coming over; please list all the dishes that contain seafood. Once again, one query with no numbers in it, please. (optional, this could be hard depending on how you try to do it) 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231001234150515.png" alt="image-20231001234150515" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>Recipe_Ingredients</u>	

   |   Field Name    | Data Type |          Values           | Note        |
   | :-------------: | :-------: | :-----------------------: | ----------- |
   |    RecipeID     |    int    |     ID for the Recipe     | primary key |
   |   RecipeSeqNo   |    int    | sequence number of recipe |             |
   |  IngredientID   |    int    |   id of the ingredient    |             |
   | MeasureAmountID |    int    | id of measurement amount  |             |
   |     Amount      |   float   |   amount of the recipe    |             |

   <u>Ingredient_Classes</u>

   |         Field Name         | Data Type |                    Values                     | Note        |
   | :------------------------: | :-------: | :-------------------------------------------: | ----------- |
   |     IngredientClassID      |    int    |         Ingredient Class ID category          | primary key |
   | IngredientClassDescription |  varchar  | Corresponding text description with number ID |             |

3. Raj and the rest of the database team are coming over next week, and they really like beef and garlic; what can I make for everyone that contains beef and garlic? (If you're not a fan of Raj, you don't have to answer this question). (Please note, this is the most challenging question on this homework and will require some time and complexity. We will be happy to discuss in a future week of office hours. Once again, this is a very very very very hard question. You do not have to answer it. ) 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002000609582.png" alt="image-20231002000609582" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>Ingredients</u>	

   |    Field Name     | Data Type |          Values          | Note        |
   | :---------------: | :-------: | :----------------------: | ----------- |
   |   IngredientID    |    int    |   id of the ingredient   | primary key |
   |  IngredientName   |  varchar  |    name of ingredient    |             |
   | IngredientClassID |    int    |  class ID of ingredient  |             |
   |  MeasureAmountID  |    int    | id of measurement amount |             |

**Part 2**

While you are helping out, I have a few more questions... I want to send cards to a few of my co-workers.

1. In the **ro_company1** database, can you give me the names of those employees who work in the Operations department? Once again, please don't put any numbers in your query. 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002001424083.png" alt="image-20231002001424083" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>employee</u>	

   |    Field Name     | Data Type |            Values             | Note        |
   | :---------------: | :-------: | :---------------------------: | ----------- |
   |      emp_id       |    int    |      id of the employee       | primary key |
   |       fname       |  varchar  |          first name           |             |
   |       lname       |  varchar  |           last name           |             |
   |    start_date     |   date    | start date of the employement |             |
   |     end_date      |   date    |  end_date of the employement  |             |
   |  superior_emp_id  |    int    |   employment id of superior   |             |
   |      dept_id      |    int    |     id of the department      |             |
   |       title       |  varchar  |     title in the company      |             |
   | assigned_brach_id |    int    |     id of assigned branch     |             |

   <u>department</u>

   | Field Name | Data Type |         Values         | Note        |
   | :--------: | :-------: | :--------------------: | ----------- |
   |  dept_id   |    int    |  id of the department  | primary key |
   |    name    |  varchar  | name of the department |             |

2. Also, employee Paula Roberts has opened a large number of accounts. Can you let me know on what dates she opened accounts on and what the address of those customers are? (one query) 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002002719489.png" alt="image-20231002002719489" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>customer</u>	

   |  Field Name  |   Data Type   |            Values            | Note        |
   | :----------: | :-----------: | :--------------------------: | ----------- |
   |   cust_id    |      int      |        id of customer        | primary key |
   |    fed_id    |    varchar    |      fed id of customer      |             |
   | cust_type_id | enum('I','B') |     type id of customer      |             |
   |   address    |    varchar    |     address of customer      |             |
   |     city     |    varchar    | city where customer located  |             |
   |    state     |    varchar    | state where customer located |             |
   | Postal_code  |    varchar    | zipcode of customer address  |             |

   <u>account</u>

   |     Field Name     |            Data Type             |                Values                 | Note        |
   | :----------------: | :------------------------------: | :-----------------------------------: | ----------- |
   |     account_id     |               int                |           id of the account           | Primary key |
   |     product_id     |               int                |             id of product             |             |
   |      cust_id       |               int                |            id of customer             |             |
   |     open_date      |               date               |           account open date           |             |
   |     close_date     |               date               |          account close date           |             |
   | last_activity_date |               date               |      last account activity date       |             |
   |       status       | enum('ACTIVE','CLOSED','FROZEN') |            account status             |             |
   |   open_branch_id   |               int                |   id of brach where account opened    |             |
   |    open_emp_id     |               int                | id of employee who opened the account |             |
   |   avail_balance    |               int                |   avilable balance for the account    |             |
   |  pending_balance   |               int                |    pending balance for the account    |             |

3. Can you provide me a list of _all_ our employees and their manager's ID?

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002004203078.png" alt="image-20231002004203078" style="zoom:50%;" />

4. Can you give me a list of all accounts that have not been closed, the available balance, the state the customer is located in, and the name of the customer's business if they have one? 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002010440686.png" alt="image-20231002010440686" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>business</u>	

   | Field Name  | Data Type |        Values         | Note        |
   | :---------: | :-------: | :-------------------: | ----------- |
   |   cust_id   |    int    |    id of customer     | primary key |
   |    name     |  varchar  |   name of business    |             |
   |  state_id   |  varchar  |      id of state      |             |
   | incorp_date |   date    | date of incorporation |             |

5. Can you provide a list of employees that work at a branch with the address of "422 Maple St."?

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002010948386.png" alt="image-20231002010948386" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>branch</u>	

   | Field Name | Data Type |           Values           | Note        |
   | :--------: | :-------: | :------------------------: | ----------- |
   | branch_id  |    int    |       id of customer       | primary key |
   |    name    |  varchar  |       name of branch       |             |
   |  address   |  varchar  |     address of branch      |             |
   |    city    |  varchar  | city where branch located  |             |
   |   state    |  varchar  |    state of the branch     |             |
   |    zip     |  varchar  | zip code of branch address |             |

**Part 3** 

My partner and I are trying to find some exciting places to visit for our upcoming vacation. Using the **world** database, can you find:

1. 5 random cities that have a population above 13,000 and below 500,000 and are not located in North America? 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002012721990.png" alt="image-20231002012721990" style="zoom:50%;" />

   *Table Ducumentation:*

   <u>city</u>	

   | Field Name | Data Type |                 Values                 | Note        |
   | :--------: | :-------: | :------------------------------------: | ----------- |
   |     ID     |    int    |             id of the city             | primary key |
   |    name    |   char    |            name of the city            |             |
   | CountrCode |   char    | code of the country where city located |             |
   |  District  |   char    |    district where the city belongs     |             |
   | Population |    int    |         population of the city         |             |

   <u>country</u>	

   |   Field Name   |                          Data Type                           |            Values             | Note        |
   | :------------: | :----------------------------------------------------------: | :---------------------------: | ----------- |
   |      Code      |                             char                             |      code of the country      | primary key |
   |      Name      |                             char                             |      name of the country      |             |
   |   Continent    | enum('Asia','Europe','North America','Africa','Oceania','Antarctica','South America') | continent the country located |             |
   |     Region     |                             char                             | region where country located  |             |
   |  SurfaceArea   |                           decimal                            |  surface area of the country  |             |
   |   IndepYear    |                             int                              |       Independence year       |             |
   |   Population   |                             int                              |          Population           |             |
   | LifeExpectancy |                           decimal                            |        life expectancy        |             |
   |      GNP       |                           decimal                            |              GNP              |             |
   |     GNPOld     |                           decimal                            |            GNPOld             |             |
   |   LocalName    |                             char                             |   local name of the country   |             |
   | GovernmentForm |                             char                             |    form the government in     |             |
   |  HeadOfState   |                             char                             |   president of the country    |             |
   |    Capital     |                             int                              |            capital            |             |
   |     Code2      |                             char                             |     code2 of the country      |             |

2. How many cities are in a Constitutional Monarchy?

   There are 611 cities meet the requirement.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002014005951.png" alt="image-20231002014005951" style="zoom:50%;" />

3. 5 random cities that a population above 13000 and below 500,000 that don't speak English as an official language and are not a Republic? 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002015550476.png" alt="image-20231002015550476" style="zoom:50%;" />

*Table Ducumentation:*

<u>country language</u>	

| Field Name  |   Data Type   |          Values           | Note |
| :---------: | :-----------: | :-----------------------: | ---- |
| CountryCode |     char      |    code of the country    |      |
|  Language   |     char      |  language of the country  |      |
| IsOfficial  | enum('T','F') | whether language official |      |
| Percantage  |    decimal    |  percent of language use  |      |

**Part 4**

Using the **ro_employee** database:

1. From 1985-01-01 to 1986-01-01, how many people were on payroll with a title that contained the word "Engineer"? (Optional) 

   There are 16749 people meet the requirement.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002020825580.png" alt="image-20231002020825580" style="zoom:50%;" />

2. How many people work in the Production department anytime between 1985-01-01 to 1992-01-01? (Optional) 

   There are 31700 people meet the requirement.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002021547091.png" alt="image-20231002021547091" style="zoom:50%;" />

3. Can you give a list of the names of 20 random employees, their current salary, and their current title? (Optional) 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231002022306403.png" alt="image-20231002022306403" style="zoom:50%;" />

***

Can't wait to see you and talk with you! See you next week!



Best,

Jun