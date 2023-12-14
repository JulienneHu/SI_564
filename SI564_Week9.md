Dear Raj,



Hope this mail finds you well. It is so exciting to hear that you are happy with our work last week. In the following queries, you can see I have inserted 8 rows sample data for each table and did the deletion and update queires as you required:

***

**Newspaper Database**

```sql
INSERT INTO People (firstName, lastName, email) VALUES
('John', 'Doe', 'johndoe@example.com'),
('Jane', 'Smith', 'janesmith@example.com'),
('Alice', 'Johnson', 'alicejohnson@example.com'),
('Bob', 'Brown', 'bobbrown@example.com'),
('Charlie', 'Davis', 'charliedavis@example.com'),
('Diana', 'Miller', 'dianamiller@example.com'),
('Ethan', 'Wilson', 'ethanwilson@example.com'),
('Fiona', 'Taylor', 'fionataylor@example.com');

INSERT INTO Sections (sectionName) VALUES
('Politics'),
('Technology'),
('Sports'),
('Entertainment'),
('Science'),
('Health'),
('Business'),
('Travel');

INSERT INTO Stories (title, content, publishDate, authorID, sectionID) VALUES
('Story 1', 'Content of story 1', '2023-01-01', 1, 1),
('Story 2', 'Content of story 2', '2023-01-02', 2, 2),
('Story 3', 'Content of story 3', '2023-01-03', 3, 3),
('Story 4', 'Content of story 4', '2023-01-04', 4, 4),
('Story 5', 'Content of story 5', '2023-01-05', 5, 5),
('Story 6', 'Content of story 6', '2023-01-06', 6, 6),
('Story 7', 'Content of story 7', '2023-01-07', 7, 7),
('Story 8', 'Content of story 8', '2023-01-08', 8, 8);

INSERT INTO Comments (commentText, storyID, commentDate, commenterID) VALUES
('Great article!', 1, '2023-01-09', 1),
('Very informative', 2, '2023-01-10', 2),
('Loved this story', 3, '2023-01-11', 3),
('Interesting perspective', 4, '2023-01-12', 4),
('Thanks for sharing', 5, '2023-01-13', 5),
('Good read', 6, '2023-01-14', 6),
('Informative piece', 7, '2023-01-15', 7),
('Well written', 8, '2023-01-16', 8);
```

**Library Database**

```sql
INSERT INTO Authors (firstName, lastName, email) VALUES
('John', 'Doe', 'johndoe@example.com'),
('Jane', 'Smith', 'janesmith@example.com'),
('Alice', 'Johnson', 'alicejohnson@example.com'),
('Bob', 'Brown', 'bobbrown@example.com'),
('Charlie', 'Davis', 'charliedavis@example.com'),
('Diana', 'Miller', 'dianamiller@example.com'),
('Ethan', 'Wilson', 'ethanwilson@example.com'),
('Fiona', 'Taylor', 'fionataylor@example.com');

INSERT INTO Genres (name) VALUES
('Fiction'),
('Non-Fiction'),
('Science Fiction'),
('Fantasy'),
('Mystery'),
('Historical'),
('Romance'),
('Biography');

INSERT INTO Books (title, authorID, ISBN, genreID, publicationYear) VALUES
('Book Title 1', 1, 'ISBN-1', 1, '2023-01-01'),
('Book Title 2', 2, 'ISBN-2', 2, '2023-02-01'),
('Book Title 3', 3, 'ISBN-3', 3, '2023-03-01'),
('Book Title 4', 4, 'ISBN-4', 4, '2023-04-01'),
('Book Title 5', 5, 'ISBN-5', 5, '2023-05-01'),
('Book Title 6', 6, 'ISBN-6', 6, '2023-06-01'),
('Book Title 7', 7, 'ISBN-7', 7, '2023-07-01'),
('Book Title 8', 8, 'ISBN-8', 8, '2023-08-01');


INSERT INTO Patrons (firstName, lastName, email, address, phone) VALUES
('Liam', 'Anderson', 'liamanderson@example.com', '123 Main St', '123-456-7890'),
('Olivia', 'Wilson', 'oliviawilson@example.com', '456 Elm St', '234-567-8901'),
('Noah', 'Brown', 'noahbrown@example.com', '789 Oak St', '345-678-9012'),
('Emma', 'Jones', 'emmajones@example.com', '101 Pine St', '456-789-0123'),
('James', 'Miller', 'jamesmiller@example.com', '102 Maple St', '567-890-1234'),
('Ava', 'Davis', 'avadavis@example.com', '103 Birch St', '678-901-2345'),
('William', 'Garcia', 'williamgarcia@example.com', '104 Cedar St', '789-012-3456'),
('Sophia', 'Rodriguez', 'sophiarodriguez@example.com', '105 Spruce St', '890-123-4567');

INSERT INTO CirculationRecord (bookID, patronID, checkOutDate, checkInDate) VALUES
(1, 1, '2023-09-01 10:00:00', '2023-09-15 10:00:00'),
(2, 2, '2023-09-02 10:00:00', '2023-09-16 10:00:00'),
(3, 3, '2023-09-03 10:00:00', '2023-09-17 10:00:00'),
(4, 4, '2023-09-04 10:00:00', '2023-09-18 10:00:00'),
(5, 5, '2023-09-05 10:00:00', '2023-09-19 10:00:00'),
(6, 6, '2023-09-06 10:00:00', '2023-09-20 10:00:00'),
(7, 7, '2023-09-07 10:00:00', '2023-09-21 10:00:00'),
(8, 8, '2023-09-08 10:00:00', '2023-09-22 10:00:00');

```

**Modification Queries**

```sql
DELETE FROM CirculationRecord
WHERE recordID IN (
    SELECT recordID
    FROM (
        SELECT recordID
        FROM CirculationRecord
        ORDER BY RAND()
        LIMIT 3
    ) AS RandomRows
);

UPDATE CirculationRecord
SET checkInDate = '2023-10-01 10:00:00'
WHERE recordID = (
    SELECT * FROM (
        SELECT MAX(recordID) FROM CirculationRecord
    ) AS SubQuery
);
```

***

Hopefully above will be helpful!



Regards,

Jun