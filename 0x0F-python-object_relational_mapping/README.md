# 0x0F. Python - Object-relational mapping

## Description
This repository contains practical coding exercises and examples for the Python programming language that illustrate how to use Object-Relational Mapping (ORM) or Object-DataBase Mapping (ODM) to interact with databases.

The concepts of ORM or ODM can be explained in simple terms as a programming technique that defines a mapping between our database tables and the classes or objects that we use in our application. In other words, ORM helps us to avoid writing raw SQL queries and provides a more convenient high-level interface to work with the database without the need to know the underlying database technology.

ORM is a useful tool that enables developers to focus on the main functionality of their application without worrying about the details of the database management, allowing them to create, read, update, and delete (CRUD) data from the database using Python code.

## Learning objectives
In this project, we will learn how to:
* How to connect to a database from a Python script or program.
* How to perform CRUD (create-read-update-delete) operations on the database.
* How to map database tables to Python classes.
* How to use SQLalchemy to perform ORM in Python.
* How to join database tables using SQLalchemy.
* How to use Flask web framework to build a simple web application that interacts with the database.

## Repository Files

| File | Description |
| ------------- | ------------- |
| `0-select_states.py` | Python script that lists all states from the database |
| `1-filter_states.py` | Python script that filters all states that contain a given letter |
| `2-my_filter_states.py` | Python script that takes in an argument and displays all values in the states table of our `hbtn_0e_0_usa` database where `name` matches the argument |
| `3-my_safe_filter_states.py` | Python script that takes in arguments and displays all values in the states table of our `hbtn_0e_0_usa` database where `name` matches the argument. But this time, it is safe from MySQL injection attacks. |
| `4-cities_by_state.py` | Python script that lists all `cities` from the database that belong to a given `state`. |
| `5-filter_cities.py` | Python script that takes in the name of a `state` as an argument and lists all `cities` of that `state`. |
| `model_state.py` | Python file that contains the `State` class and an instance `Base` = `declarative_base()`. |
| `7-model_state_fetch_all.py` | Python script that lists all `State` objects from the database using SQLAlchemy. |
| `8-model_state_fetch_first.py` | Python script that prints the first `State` object from the database using SQLAlchemy. |
| `9-model_state_filter_a.py` | Python script that lists all `State` objects that contain the letter `a` from the database using SQLAlchemy. |
| `10-model_state_my_get.py` | Python script that prints a `State` object by name from the database using SQLAlchemy. |
| `11-model_state_insert.py` | Python script that adds the `State` object “Louisiana” to the database using SQLAlchemy. |
| `12-model_state_update_id_2.py` | Python script that changes the name of a `State` object from the database using SQLAlchemy. |
| `13-model_state_delete_a.py` | Python script that deletes all `State` objects that contain the letter `a` from the database using SQLAlchemy. |
| `model_city.py` | Python file that contains the `City` class and an instance `Base` = `declarative_base()` that is linked to the MySQL database. |
| `14-model_city_fetch_by_state.py` | Python script that lists all `City` objects from a database given a `state` name using SQLAlchemy. |
| `relationship_city.py` | Python file that contains the `City` class and the `State` class, and creates a relationship between them using SQLAlchemy. It is used for task 15. |
| `relationship_states_cities.py` | Python script that creates the `State` “California” with the `City` “San Francisco” linked to it, and prints the “`id`” attribute of both of them using SQLAlchemy. |
| `web_flask` | Contains routes to access the MySQL database from a web browser. Initialize a web application, connects to the MySQL server and displays the content of the states and the cities tables. |
| `100-relationship_states_cities.py` | Similar to `relationship_states_cities.py`, but this file creates the State “California” with the City “San Francisco” linked to it, as well as the City “San Francisco” with the State “California” linked to it, and prints the “`id`” attribute of both new City objects. |
| `101-relationship_states_cities_list.py` | Lists all `City` objects from the database using SQLAlchemy. |
| `102-relationship_cities.py` | Python file that contains the `City` class, the `State` class, and the `City` relationship with the `State`. |

1. [0-select_states.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/0-select_states.py)
2. [1-filter_states.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/1-filter_states.py)
3. [2-my_filter_states.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/2-my_filter_states.py)
4. [3-my_safe_filter_states.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/3-my_safe_filter_states.py)
5. [4-cities_by_state.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/4-cities_by_state.py)
6. [5-filter_cities.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/5-filter_cities.py)
7. [model_state.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/model_state.py)
8. [7-model_state_fetch_all.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/7-model_state_fetch_all.py)
9. [8-model_state_fetch_first.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/8-model_state_fetch_first.py)
10. [9-model_state_filter_a.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/9-model_state_filter_a.py)
11. [10-model_state_my_get.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/10-model_state_my_get.py)
12. [11-model_state_insert.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/11-model_state_insert.py)
13. [12-model_state_update_id_2.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/12-model_state_update_id_2.py)
14. [13-model_state_delete_a.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/13-model_state_delete_a.py)
15. [model_city.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/model_city.py)
16. [14-model_city_fetch_by_state.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/14-model_city_fetch_by_state.py)
17. [relationship_city.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/relationship_city.py)
18. [relationship_states_cities.py](https://github.com/brainstorma/alx-higher_level_programming/blob/master/0x0F-python-object_relational_mapping/relationship_states_cities.py)


## How to use
* Clone the repository to your local directory:
```sh
git clone https://github.com/brainstorma/alx-higher_level_programming.git
```
* Change into the `0x0F-python-object_relational_mapping` directory:
```sh
cd 0x0F-python-object_relational_mapping
```

## Author
* **Brainstorma** - [Brainstorma](https://github.com/brainstorma) 

## Acknowledgements
* This project was undertaken as part of the curriculum for the ALX High-Level programme, (Software Engineering).
