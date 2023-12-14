

Dear Kelly,



Hope this mail finds you well! It is my pleasure to be a part contributing to the acqusition and the following are my answers with you questions:

***

**Part One**

1. *The cost of the company we are thinking about buying is \$30,000,000.  However, the owner is on our board and will give a discount of $15,210,000.  We will be buying a share of this company with 6 other investors.  The board member is wiling to give all of us the discount on the purchase price.  What is the price that each investor will pay?* 
   
   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008223949705.png" alt="image-20231008223949705" style="zoom:50%;" />
   
   Each investor supposed to pay $\$2112857.1429$.

**Part Two**

1. *How many accounts does company1 have?  (Optional)*

   There are 24 accounts.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008224109902.png" alt="image-20231008224109902" style="zoom:50%;" />

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008224126699.png" alt="image-20231008224126699" style="zoom:50%;" />

2. *What is the primary key of the accounts table?*

   'account_id' is the primary key. 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008224159627.png" alt="image-20231008224159627" style="zoom:50%;" />

3. *What are the possible values that could be in the status field in the account table?*  

   'ACTIVE','CLOSED','FROZEN' are possible values that could be in the status field in the account table.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008224227362.png" alt="image-20231008224227362" style="zoom:50%;" />

   However, in current table, there is only 'ACTIVE' in it.
   
   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230915194424587.png" alt="image-20230915194424587" style="zoom:50%;" />

<u>Table Documentation</u>

*Account*

|     Field Name     |           Data Type           |                Values                 | Note        |
| :----------------: | :---------------------------: | :-----------------------------------: | ----------- |
|     account_id     |              int              |             id of account             | primary key |
|     product_id     |              int              |             id of product             |             |
|     open_date      |             date              |           account open date           |             |
|     close_date     |             date              |          account close date           |             |
| last_activity_date |             date              |       account last active date        |             |
|       status       | enum('ACTIVE'CLOSED''FROZEN') |     three kinds of account status     |             |
|   open_branch_id   |              int              |   id of branch where account opened   |             |
|    open_emp_id     |              int              | id of employee who opened the account |             |
|   avail_balance    |             float             |       account available balance       |             |
|  pending_balance   |             float             |        account pending balance        |             |

**Part Three**

1. *Which employee ID has opened the most company accounts? (look at the account table for this one)*

   The employee with id 1 is the person who opened the most company accounts since in the open_emp_id 1 has the most appearance.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008231451619.png" alt="image-20231008231451619" style="zoom:50%;" />

2. *When did the  employee who has opened the most accounts start working at the company? (optional)*

   The empoyee1 started to work for the company since June 22nd, 2001.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230915195412678.png" alt="image-20230915195412678" style="zoom:50%;" />

**Part Four**

1. *Write a query that returns only the date of the transaction and the account id (in that order) from the transaction table sort this by the most recent transaction.* 

   The following is my query:

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230915195623763.png" alt="image-20230915195623763" style="zoom:50%;" />

   <u>Table Documentation</u>

   *Transaction*

   |     Field Name      |    Data Type     |                   Values                    | Note        |
   | :-----------------: | :--------------: | :-----------------------------------------: | ----------- |
   |       txn_id        |       int        |              id of transaction              | primary key |
   |      txn_date       |     datetime     |     transaction date and specific time      |             |
   |     account_id      |       int        |                id of account                |             |
   |     txn_type_cd     | enum('DBT','CDT) |  transaction via debit card or credit card  |             |
   |    teller_emp_id    |       int        |            id of teller employee            |             |
   | execution_branch_id |       int        | id of branch where the transaction executed |             |
   |  funds_avial_date   |     datetime     |        time when the fund available         |             |

   

2. *What is the primary key in the transaction table?*

   'txn_id' is the primary key.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230915195652181.png" alt="image-20230915195652181" style="zoom:50%;" />

3. *What are the unique product types that are offered?  (optional)*

   'ACCOUNT', 'INSURANCE', 'LOAN' are the unique product types.('product_type_cd' is the primary key.)

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230915195938617.png" alt="image-20230915195938617" style="zoom:50%;" />

**Part Five**

1. *How many branches are located in MA?  (optional)*

   There are 3 branches located in MA.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231008231952140.png" alt="image-20231008231952140" style="zoom:50%;" />

2. *Can you write a query will list the name of each branch, the address of each branch, the zip code of each branch, and a field that indicates the current date and time you made the query that shows in the query as a field called "querytime"?  I want to make sure that when I view the data, I am seeing when (date, time) you made the query to validate if you are correct.* 

   The following is my query:

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20230915200339084.png" alt="image-20230915200339084" style="zoom:50%;" />
   
   <u>Table Documentation</u>
   
   *Branch*
   
   | Field Name | Data Type |          Values           | Note        |
   | :--------: | :-------: | :-----------------------: | ----------- |
   | branch_id  |    int    |       id of branch        | primary key |
   |    name    |  varchar  |      name of branch       |             |
   |  address   |  varchar  |     address of branch     |             |
   |    city    |  vrachar  | city where branch located |             |
   |   state    |  varchar  |   state where branch in   |             |
   |    zip     |  varchar  |     zipcode of branch     |             |
   

***

Best regards,

Jun