# 0x0E. SQL - More queries

This project is about learning how to use SQL to perform more complex queries on databases.

## Learning Objectives

- How to create a new MySQL user
- How to manage privileges for a user to a database or table
- What’s a PRIMARY KEY
- What’s a FOREIGN KEY
- How to use NOT NULL and UNIQUE constraints
- How to retrieve data from multiple tables in one request
- What are subqueries
- What are JOIN and UNION

## Requirements

- All files are executed on Ubuntu 14.04 LTS using MySQL 5.7 (version 5.7.8-rc)
- All files are written in SQL (Structured Query Language)
- All SQL queries end with a semicolon
- The first line of all files is a comment indicating what each script is doing

## Tasks

### [0. My privileges!](./0-privileges.sql)

Write a script that lists all privileges of the MySQL users `user_0d_1` and `user_0d_2` on your server.

### [1. Root user](./1-create_user.sql)

Write a script that creates the MySQL server user `user_0d_1`.

Requirements:

* The user `user_0d_1` should have all privileges on your MySQL server
* The password of `user_0d_1` should be set to `user_0d_1_pwd`

### [2. Read user](./2-create_read_user.sql)

Write a script that creates the database `hbtn_0d_2` and the user `user_0d_2`.

Requirements:

* The database `hbtn_0d_2` should be accessible by the user `user_0d_2`
* The user `user_0d_2` should only have SELECT privilege in the database `hbtn_0d_2`
* The password of `user_0d_2` should be set to `user_0d_2_pwd`

### [3. Always a name](./3-force_name.sql)

Write a script that creates the table force_name on your MySQL server.

Requirements:

* The table force_name should have attributes id (int, auto increment, primary key), name (varchar(256), not null) and score (int)
* If you try to insert a record without specifying a value for name, it should fail

### [4. ID can't be null](./4-never_empty.sql)

Write a script that creates the table id_not_null on your MySQL server.

Requirements:

* The table id_not_null should have attributes id (int, auto increment, primary key), name (varchar(256)) and score (int)
* If you try to insert an empty record in this table, it should fail

### [5. Unique ID](./5-unique_id.sql)

Write a script that creates the table unique_id on your MySQL server.

Requirements:

* The table unique_id should have attributes id (int, auto increment, primary key), name (varchar(256)) and score (int)
* If you try to insert an already existing record in this table, it should fail

### [6. States table](./6-states.sql)

Write a script that creates the database hbtn\_0c\_usa and the table states (in hbtn\_0c\_usa) on your MySQL server.

Requirements:

* The table states should have attributes id (int, auto increment, primary key), name (varchar(256), not null) and capital_city_id(int)
* capital_city_id is referencing cities.id which will be created later


### [7. Cities table](./7-cities.sql)

Write a script that creates the database hbtn\_0c\_usa and the table cities (in hbtn\_0c\_usa) on your MySQL server.

Requirements:

* The table cities should have attributes id(int ,auto increment ,primary key ), state_id(int ,not null )and name(varchar(256) ,not null )
* state_id is referencing states.id which will be created later


### [8. Cities of California](./8-cities_of_california_subquery.sql)

Write a script that lists all cities contained in California from hbtn\_0c_usa database.

Requirements:

* Your query result must contain only two columns: city names sorted by alphabetical order followed by their corresponding state names.
* You must use subqueries.


### [9. Cities by States](./9-cities_by_state_join.sql)

Write a script that lists all cities contained in California from hbtn\_0c_usa database.

Requirements:

* Your query result must contain only two columns: city names sorted by alphabetical order followed by their corresponding state names.
* You must use JOIN.


### [10. Genre ID by show](./10-genre_id_by_show.sql)

Write a script that lists all shows contained in hbtn\_0d_tvshows that have at least one genre linked.

Requirements:

* Your query result must contain only two columns: tv show title and genre id
* You must use a LEFT JOIN


### [11. Genre ID for all shows](./11-genre_id_all_shows.sql)

Write a script that lists all shows contained in the database hbtn\_0d_tvshows.

Requirements:

* Your query result must contain three columns: tv show title, number of genres linked to the show and genre id
* If a show doesn’t have a genre, display NULL
* You must use a LEFT JOIN


### [12. No genre](./12-no_genre.sql)

Write a script that lists all shows contained in hbtn\_0d_tvshows without a genre linked.

Requirements:

* Your query result must contain only one column: tv show title
* You must use a LEFT JOIN


### [13. Number of shows by genre](./13-count_shows_by_genre.sql)

Write a script that lists all genres from hbtn\_0d_tvshows and displays the number of shows linked to each.

Requirements:

* Your query result must contain two columns: the genre name and the number of shows linked to this genre
* You must use a LEFT JOIN


### [14. My genres](./14-my_genres.sql)

Write a script that uses the hbtn_0d_tvshows database to list all genres of the show Dexter.

Requirements:

* Your query result should display only one column with the genre name
* You must use the shows table as reference (not the show_genres)


### [15. Only Comedy](./15-comedy_only.sql)

Write a script that lists all Comedy shows in the database hbtn_0d_tvshows.

Requirements:

* Your query result should display only one column with the tv show name
* You must use the genres table as reference (not the show_genres)


### [16. List shows and genres](./16-shows_by_genre.sql)

Write a script that lists all shows, and all genres linked to that show, from the database hbtn_0d_tvshows.

Requirements:

* If a show doesn’t have any genres, display NULL in front of it
* Your query result should display two columns: tv show name and its corresponding genres name (even if it is NULL).
