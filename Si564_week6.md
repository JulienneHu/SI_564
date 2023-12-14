Dear Lawrence,



Hope you had a lovely honeymoon! It is my pleasure to answer your questions and here are my answers with your questions:

***

**Part 1: From the employee database**

1. How many employees do we have born in each month? *

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018152419515.png" alt="image-20231018152419515" style="zoom:50%;" />

   <u>employees</u>

   | Field Name |   Data Type    |         Values         | Note        |
   | :--------: | :------------: | :--------------------: | ----------- |
   |   emp_no   |      int       |    employee number     | primary key |
   | birth_date |      date      | birthdate of employee  |             |
   | first_name |    varchar     | first name of employee |             |
   | last_name  |    varchar     | last name of employee  |             |
   |   gender   | enum('M', 'F') |   gender of employee   |             |
   | hire_date  |      date      |  employee hired date   |             |

   

2. What day(as in day of the month) on average do we hire the most people* ?

   3 is the day in a month hired most people.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018154623160.png" alt="image-20231018154623160" style="zoom:50%;" />

3. What is the average salary by job title currently for all staff? *

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018160635503.png" alt="image-20231018160635503" style="zoom:50%;" />

   <u>Title</u>

   | Field Name | Data Type |           Values           | Note        |
   | :--------: | :-------: | :------------------------: | ----------- |
   |   emp_no   |    int    |      employee number       | primary key |
   |   title    |  varchar  |     title of employee      |             |
   | from_date  |   date    |  employee hired from date  |             |
   |  to_date   |   date    | employee left company date |             |

   <u>Salaries</u>	

   | Field Name | Data Type |           Values           | Note        |
   | :--------: | :-------: | :------------------------: | ----------- |
   |   emp_no   |    int    |      employee number       | primary key |
   |   salary   |    int    |     salary of employee     |             |
   | from_date  |   date    |  employee hired from date  |             |
   |  to_date   |   date    | employee left company date |             |

   

4. What is the average salary for all folks that are currently employed by year of hire? *

<img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018162213943.png" alt="image-20231018162213943" style="zoom:50%;" />



<img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018162810305.png" alt="image-20231018162810305" style="zoom:50%;" />

**Part 2: From the research1 database**

1. By username what is the average number of steps for July. *

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018164635978.png" alt="image-20231018164635978" style="zoom:50%;" />

   <u>fitbit_day_detail</u>

   |  Field Name  | Data Type |           Values            | Note        |
   | :----------: | :-------: | :-------------------------: | ----------- |
   |      id      |    int    |        id of detail         | primary key |
   |   user_id    |    int    |  id of corresponding user   |             |
   | fitbit_steps |    int    |       steps of detail       |             |
   |   created    |    int    | person who chreated the api |             |
   |   changed    |    int    | person who changed the api  |             |
   | fitbit_date  |   date    |     date of the detail      |             |

   <u>users_field_data</u>	

   | Field Name | Data Type |             Values             | Note        |
   | :--------: | :-------: | :----------------------------: | ----------- |
   |    uid     |    int    |           id of user           | primary key |
   |  langcode  |  varchar  | corresponding langcode of user |             |
   |    name    |  varchar  |          name of user          |             |
   |    mail    |  varchar  |          mail of user          |             |
   |  timezone  |  varcahr  |        timezone of user        |             |

   

2. For the user with the name 'f9f67f5beddc05e72d4c1715c26df95d', what is the average number of minutes they sleep each month.  Remember to write this as one query. *

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018171550125.png" alt="image-20231018171550125" style="zoom:50%;" />

   <u>fitbit_sleep</u>	

   |     Field Name     | Data Type |          Values           | Note        |
   | :----------------: | :-------: | :-----------------------: | ----------- |
   |         id         |    int    |       id of detail        | primary key |
   |      user_id       |    int    | id of corresponding user  |             |
   |        name        |  varchar  |       name of user        |             |
   |    fitbit_date     |   date    |      date of active       |             |
   |  fitbit_duration   |    int    |    duration of fitbit     |             |
   | fitbit_efficiency  |    int    |   efficiency of fitbit    |             |
   |  fitbit_timeinbed  |    int    |      sleep of fitbit      |             |
   | fitbit_ismainsleep |    int    | whether fitbit main sleep |             |
   |      created       |    int    | user who created the api  |             |

3. Please write a query that lists each user_id and the max steps they walked in a single day for each month. 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018171959763.png" alt="image-20231018171959763" style="zoom:50%;" />

4. Please provide a listing of each user_id and the if they met their goal on average per month (This is a quote from one of our researchers, figure out how to answer it and describe how you answered it) 

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018193431149.png" alt="image-20231018193431149" style="zoom:50%;" />

   <u>goal_entity</u>

   | Field Name | Data Type |          Values          | Note        |
   | :--------: | :-------: | :----------------------: | ----------- |
   |     id     |    int    |       id of detail       | primary key |
   |  user_id   |    int    | id of corresponding user |             |
   |    goal    |    int    |      goal of steps       |             |
   |    date    |  varchar  |     date of goal set     |             |

5. What days did users get more than 8 hours of sleep?  Please provide me a sample of the user_id's, the names and the days if the list is too long. Your query should NOT contain any numbers above 100. * 

   The output table is too long so I showed randomly 10 rows.

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018194042823.png" alt="image-20231018194042823" style="zoom:50%;" />

6. For user with the name of 82c8ca7904fea3535400823529ade611, what were the average number of steps taken per month per min?

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018195640661.png" alt="image-20231018195640661" style="zoom:50%;" />

   <img src="/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231018200239504.png" alt="image-20231018200239504" style="zoom:50%;" />

***

I hope these insights are of value to you! On a side note, I haven't been informed about our leader's promotion. If this is accurate, do you think there will be any changes within our team?



Regards,

Jun