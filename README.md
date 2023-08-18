# Library_Management_System



![POSTGRESQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=for-the-badge&logo=PostgreSQL&logoColor=white)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![Microsoft Office](https://img.shields.io/badge/Microsoft_Office-D83B01?style=for-the-badge&logo=microsoft-office&logoColor=white)
![Microsoft Word](https://img.shields.io/badge/Microsoft_Word-2B579A?style=for-the-badge&logo=microsoft-word&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

The Library Management System is a project aimed at creating an efficient system for managing a library's operations. This system allows users to issue books, search for different books and their titles, and provides detailed information about the books available in the library. By automating these processes, it eliminates the need for manual record-keeping and offers a user-friendly experience.

## Project Idea

The main objective of this project is to develop a comprehensive library management system that simplifies the management of books within a library. This system maintains a centralized database of books, including their details such as title, price, status, and the total number of books available. It streamlines the borrowing process and provides users with easy access to information, making it an efficient alternative to the traditional manual recording system.

## Project Structure

    ├── LICENSE
    ├── README.md          <- README .
    ├── reports            <- Folder containing the final reports/results of this project.
    │   │
    │   └── query_report.pdf        <- Final query report in PDF for verifying data.
    │   
    ├── src                <- Source for this project.
        │
        ├── LMS_query.sql           <- Final query for this project.
        ├── LMS_schema.sql          <- Schema for this project.
        
--------

# Library Management System - Schema created

## Table: books

The `books` table stores information about books available in the library.

### Columns

| Column Name    | Data Type    | Constraints | Description                              |
|----------------|--------------|-------------|------------------------------------------|
| id             | SERIAL       | PRIMARY KEY | Unique identifier for the book            |
| title          | VARCHAR(255) | NOT NULL    | Title of the book                         |
| author         | VARCHAR(255) | NOT NULL    | Author of the book                        |
| category       | VARCHAR(255) | NOT NULL    | Category of the book                      |
| price          | DECIMAL(10,2)| NOT NULL    | Price of the book                         |
| status         | VARCHAR(255) | NOT NULL    | Status of the book (e.g., available, sold) |
| total_copies   | INT          | NOT NULL    | Total number of copies available           |

## Table: customers

The `customers` table stores information about the library customers.

### Columns

| Column Name    | Data Type    | Constraints | Description                              |
|----------------|--------------|-------------|------------------------------------------|
| id             | SERIAL       | PRIMARY KEY | Unique identifier for the customer        |
| first_name     | VARCHAR(255) | NOT NULL    | First name of the customer                |
| last_name      | VARCHAR(255) | NOT NULL    | Last name of the customer                 |
| email          | VARCHAR(255) | NOT NULL    | Email address of the customer             |
| phone_number   | VARCHAR(20)  | NOT NULL    | Phone number of the customer              |

## Table: issued_books

The `issued_books` table stores information about the books issued by customers.

### Columns

| Column Name    | Data Type    | Constraints       | Description                             |
|----------------|--------------|-------------------|-----------------------------------------|
| id             | SERIAL       | PRIMARY KEY       | Unique identifier for the issued book    |
| book_id        | INT          | NOT NULL          | Foreign key referencing books(id)        |
| customer_id    | INT          | NOT NULL          | Foreign key referencing customers(id)    |
| issue_date     | DATE         | NOT NULL          | Date when the book was issued            |
| due_date       | DATE         | NOT NULL          | Due date for returning the book          |
| return_date    | DATE         |                   | Date when the book was returned (optional)|
----



## Features

The Library Management System is designed with the following features in mind:

- User-friendly interface for easy navigation and interaction.
- Comprehensive entry for each book, containing details such as title, price, status, and quantity.
- Efficient search functionality to allow users to find books by their titles.
- Streamlined book issuing process to facilitate borrowing and returning.
- Centralized database to store and manage book information.
- Automated tracking of available books in the library.

By incorporating these features, the Library Management System aims to provide an efficient and user-friendly solution for managing library operations.

## Conclusion

The Library Management System is an automated solution that simplifies the management of books within a library. It offers a user-friendly interface, extensive book details, and efficient search functionality. By utilizing SQL queries, it interacts with a database to store and retrieve information effectively. With this system in place, the process of book management becomes more streamlined and convenient for both library staff and users.
The `books` table stores information about books available in the library.

## Author
- <ins><b>©2023 Tushar Aggarwal. All rights reserved</b></ins>
- <b>[LinkedIn](https://www.linkedin.com/in/tusharaggarwalinseec/)</b>
- <b>[Medium](https://medium.com/@tushar_aggarwal)</b> 
- <b>[Tushar-Aggarwal.com](https://www.tushar-aggarwal.com/)</b>
- <b>[New Kaggle](https://www.kaggle.com/tagg27)</b> 

## Contact me!

If you have any questions, suggestions, or just want to say hello, you can reach out to us at [Tushar Aggarwal](mailto:info@tushar-aggarwal.com). We would love to hear from you!