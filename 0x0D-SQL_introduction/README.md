# 0x0D. SQL - Introduction

This project is an introduction to SQL (Structured Query Language), a standard language for accessing and manipulating databases.

## Learning Objectives

By the end of this project, you will be able to:

- Explain what a database is and how it differs from a spreadsheet
- Explain what SQL is and how it differs from other programming languages
- Explain what DDL (Data Definition Language) and DML (Data Manipulation Language) are
- Create databases and tables using SQL commands
- Insert, update, delete, and query data using SQL commands
- Use subqueries and functions in SQL queries
- Use indexes to optimize database performance

## Requirements

To complete this project, you will need:

- A MySQL server running on your local machine or on a remote server
- A MySQL client such as mysql or mysqlsh to interact with the MySQL server
- A text editor such as vim or emacs to write your SQL scripts

## Installation

To install MySQL server on your local machine (Ubuntu 18.04), follow these steps:

1. Update your system packages: `sudo apt update`
2. Install MySQL server: `sudo apt install mysql-server`
3. Secure your MySQL installation: `sudo mysql_secure_installation`
4. Start MySQL service: `sudo service mysql start`
5. Check MySQL status: `sudo service mysql status`

To install MySQL client on your local machine (Ubuntu 18.04), follow these steps:

1. Update your system packages: `sudo apt update`
2. Install MySQL client: `sudo apt install mysql-client`

## Usage

To use this project's files:

1. Clone this repository: `git clone https://github.com/brainstorma/0x0D-SQL_introduction.git`
2. Change directory to the project folder: `cd 0x0D-SQL_introduction`
3. Connect to your MySQL server using your username and password: `mysql -u brainstorma -p`
4. Execute each SQL script using the source command followed by the file name: `source file_name.sql`

To insert a new record into the customers table:
INSERT INTO customers (id, name, email, phone) VALUES (1, 'Alice', 'alice@example.com', '1234567890');
To query all the records from the customers table:
SELECT * FROM customers;
To query only the name and email columns from the customers table:
SELECT name, email FROM customers;
To query only the records where the name starts with ‘A’ from the customers table:
SELECT * FROM customers WHERE name LIKE 'A%';
To update the phone number of a record in the customers table:
UPDATE customers SET phone = '0987654321' WHERE id = 1;
To delete a record from the customers table:
DELETE FROM customers WHERE id = 1;

## Tasks

This project consists of 17 tasks that cover various aspects of SQL.

### Task 0: List databases

[0-list_databases.sql](./0-list_databases.sql): A SQL script that lists all databases.

### Task 1: Create a database

[1-create_database_if_missing.sql](./1-create_database_if_missing.sql): A SQL script that creates the database hbtn_0c_0 if it does not exist.

### Task 2: Delete a database

[2-remove_database.sql](./2-remove_database.sql): A SQL script that deletes the database hbtn_0c_0 if it exists.

### Task 3: List tables

[3-list_tables.sql](./3-list_tables.sql): A SQL script that lists all tables.

### Task 4: First table

[4-first_table.sql](./4-first_table.sql): A SQL script that creates a table first_table with two columns:

- id INT PRIMARY KEY AUTO_INCREMENT NOT NULL
- name VARCHAR(256) NOT NULL


### Task 5: Full description 

[5-full_table.sql](./5-full_table.sql): A SQL script that prints the full description of the table first_table.

### Task 6: List all in table 

[6-list_values.sql](./6-list_values.sql): A SQL script that lists all rows of the table first_table.

### Task 7: First add 

[7-insert_value.sql](./7-insert_value.sql): A SQL script that inserts a new row in the table first_table with values:

- id = 89 
- name = Best School


### Task 8: Count 89 

[8-count_89.sq
l](./8-count_89.sq l): A SQL script that displays the number records with id = 89 in the table first_table.

### Task 9: Full creation 

[9-full_creation.sq l](./9-full_creation.sq l): A SQL script that creates and fills a table second_table with three columns:

- id INT PRIMARY KEY AUTO_INCREMENT NOT NULL 
- name VARCHAR(256) NOT NULL 
- score INT NOT NULL 

Records:

| id | name   | score |
|----|--------|-------|
| 1  | John   |    10 |
| 2  | Alex   |     3 |
| 3  | Bob    |    14 |
| 4  | George |     8 |

### 10. List by best**
  * [10-top_score.sql](./10-top_score.sql): MySQL script that lists the `score` and `name` of all
  records of the table `second_table` in order of descending `score`.

### 11. Select the best**
  * [11-best_score.sql](./11-best_score.sql): MySQL script that lists the `score` and `name` of all
  records with a `score >= 10` in the table `second_table` in order of descending score.

### 12. Cheating is bad**
  * [12-no_cheating.sql](./12-no_cheating.sql): MySQL script that updates the score of Bob to 10
  the table `second_table`.

### 13. Score too low**
  * [13-change_class.sql](./13-change_class.sql): MySQL script that removes all records with a
  `score <= 5` in the table `second_table`.

### 14. Average**
  * [14-average.sql](./14-average.sql): MySQL script that computes the average `score` of all
  records in the table `second_table`.

### 15. Number by score**
  * [15-groups.sql](./15-groups.sql): MySQL script that lists the `score` and number of records
  with the same score in the table `second_table` in order of descending count.

### 16. Say my name**
  * [16-no_link.sql](./16-no_link.sql): MySQL script that lists the `score` and `name` of all
  records in the table `second_table` in order of descending `score`.
  * Does not display rows without a `name` value.

### 17. Go to UTF8**
  * [100-move_to_utf8.sql](./100-move_to_utf8.sql): MySQL script that converts the `hbtn_0c_0`
  database to UTF8.

### 18. Temperatures #0**
  * [101-avg_temperatures.sql](./101-avg_temperatures.sql): MySQL script that displays the average
  temperature (Fahrenheit) by city in descending order.

### 19. Temperatures #1**
  * [102-top_city.sql](./102-top_city.sql): MySQL script that displays the three cities with the
  highest average temperature from July to August in descending order.

### 20. Temperature #2**
  * [103-max_state.sql](./103-max_state.sql): MySQL script that displays the max temperature of each
  state in order of state name.

## Tasks

### 0. List databases
Write a script that lists all databases of your MySQL server.

### 1. Create a database 
Write a script that creates the database `hbtn_0d_tvshows` in your MySQL server.

### 2. Delete a database
Write a script that deletes the database `hbtn_0d_tvshows` in your MySQL server.

### 3. List tables
Write a script that lists all the tables of a database in your MySQL server.

### 4. First table
Write a script that creates a table `shows` in the database `hbtn_0d_tvshows` in your MySQL server.

### 5. Full description
Write a script that prints the full description of the table `shows` from the database `hbtn_0d_tvshows` in your MySQL server.

### 6. List all in table
Write a script that lists all rows of the table `shows` from the database `hbtn_0d_tvshows` in your MySQL server.

### 7. First table status
Write a script that displays the `status` of the table `shows` in the database `hbtn_0d_tvshows` in your MySQL server.

### 8. List by best 
Write a script that lists all records of the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 9. Delete by genre
Write a script that deletes all records of the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 10. List by genre
Write a script that lists all records with a `genre` of `Drama` in the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 11. Select the best
Write a script that lists all records with a `rating` equal or greater than `8` in the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 12. Cheating is bad 
Write a script that updates the `rating` of `The-Big-Bang-Theory` to `8` in the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 13. Update grade
Write a script that updates the `rating` of `The-Big-Bang-Theory` to `9` in the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 14. Delete by shows
Write a script that deletes the `The-Big-Bang-Theory` show from the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server.

### 15. Multiple deletions
Write a script that deletes all `shows` in the table `shows` of the database `hbtn_0d_tvshows` in your MySQL server that have a `rating` equal or lower than `5`.
