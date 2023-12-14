Dear Raj,



Hope this mail finds you well. Here are my designs foe the databases based on the information you provided and attached is my exported mars database.

***

1) *We are building a newspaper website. We need to keep track of the stories the newspaper site publishes, who wrote the stories, the comments that our readers leave on the stories, and which section the stories are part of (news, sports, etc.).* 

   | **Stories**                                               |
   | --------------------------------------------------------- |
   | `storyID` (Primary Key): ID for each story.               |
   | `title`: The title of the story.                          |
   | `content`: The main content/body of the story.            |
   | `publishDate`: Date and time the story was published.     |
   | `authorID` (Foreign Key): References the Authors table.   |
   | `sectionID` (Foreign Key): References the Sections table. |

   | **Authors**                                   |
   | --------------------------------------------- |
   | `authorID` (Primary Key): ID for each author. |
   | `firstName`: The first name of the author.    |
   | `lastName`: The last name of the author.      |
   | `email`: The email address of the author.     |

   | **Comments**                                           |
   | ------------------------------------------------------ |
   | `commentID` (Primary Key): ID for each comment.        |
   | `commentText`: The content of the comment.             |
   | `storyID` (Foreign Key): References the Stories table. |
   | `commentDate`: Date and time the comment was posted.   |

   | Sections                                                 |
   | -------------------------------------------------------- |
   | `sectionID` (Primary Key): ID for each section.          |
   | `sectionName`: Name of the section (e.g., news, sports). |

2) *We are helping a library create a new circulation system. They need to be able to track books, patrons, and circulation records. Use your best guess to identify the fields to track on a book, and for each patron record (patrons are users of the library). The circulation records will link a book to a patron with a check-in and check-out date. (Do this in 3 tables) If you think you need more tables, you can either draw them out, or write about them.* 

   | **Books**                                                |
   | -------------------------------------------------------- |
   | `bookID` (Primary Key): ID for each book.                |
   | `title`: The title of the book.                          |
   | `author`: The author of the book.                        |
   | `ISBN`: International Standard Book Number.              |
   | `genre`: Genre of the book (e.g., fiction, non-fiction). |
   | `publicationYear`: The year the book was published.      |

   | **Patrons**                                   |
   | --------------------------------------------- |
   | `patronID` (Primary Key): ID for each patron. |
   | `firstName`: First name of the patron.        |
   | `lastName`: Last name of the patron.          |
   | `email`: Email address of the patron.         |
   | `address`: Physical address of the patron.    |
   | `phone`: Phone number of the patron.          |

   | **CirculationRecords**                                    |
   | --------------------------------------------------------- |
   | `recordID` (Primary Key): ID for each circulation record. |
   | `bookID` (Foreign Key): References the Books table.       |
   | `patronID` (Foreign Key): References the Patrons table.   |
   | `checkOutDate`: Date the book was checked out.            |
   | `checkInDate`: Date the book was returned.                |

3) *We would like to keep track of our internal employee training information. We need to keep track of which employees have taken which classes they have taken and when. We also need to keep track of who teaches those classes, as well as the learning objective for each class. (This is a bonus example, it is not required)* 

   | **Employees**                                     |
   | ------------------------------------------------- |
   | `employeeID` (Primary Key): ID for each employee. |
   | `firstName`: First name of the employee.          |
   | `lastName`: Last name of the employee.            |
   | `email`: Email address of the employee.           |

   | **Classes**                                                  |
   | ------------------------------------------------------------ |
   | `classID` (Primary Key): ID for each class.                  |
   | `className`: Name of the class.                              |
   | `learningObjective`: Description of what the class aims to teach or the skills it imparts. |
   | `instructorID` (Foreign Key): References the Employees table, denoting the employee who teaches the class. |

   | **Records**                                                  |
   | ------------------------------------------------------------ |
   | `recordID` (Primary Key): ID for each enrollment record.     |
   | `employeeID` (Foreign Key): References the Employees table, indicating who took the class. |
   | `classID` (Foreign Key): References the Classes table, indicating which class was taken. |
   | `dateTaken`: Date when the employee took or completed the class. |

*Also please make a copy of the "world" database. It should be called mars. I should be able to run "use mars" and show tables and see the same tables that are in world. You will need to add **--set-gtid-purged=OFF** to your mysql dump command.* 

Here is the screenshot of my command:

![image-20231105210534400](/Users/julienne_hu/Library/Application Support/typora-user-images/image-20231105210534400.png)

***

Hope above will be helpful.



Regards,

Jun