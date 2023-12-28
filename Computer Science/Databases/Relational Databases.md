- A type of database that organizes data into tables, which consist of rows and cells
- SQL (Standard Query Language) is the standard language for interacting with relational databases

#### Implementation

Every cell of a table has **only one** value, so if a person has starred in **multiple** shows, to store this in a relational database, you would need at least two tables: one table for people and their attributes and one for shows and their attributes, then these tables can have **relations** with each other

```SQL
CREATE TABLE people (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    gender VARCHAR(10)
);

CREATE TABLE shows (
    id INT PRIMARY KEY,
    title VARCHAR(100),
    genre VARCHAR(50),
    release_year INT
);

CREATE TABLE stars (
    person_id INT,
    show_id INT,
    PRIMARY KEY (person_id, show_id),
    FOREIGN KEY (person_id) REFERENCES People(person_id),
    FOREIGN KEY (show_id) REFERENCES TVShows(show_id)
);
```

#### Data Types in SQL
- `INTEGER`        (int)
- `NUMERIC`        (date, time, ...)
- `VARCHAR(n)` (Variable-length character strings with a maximum length)
- `REAL`              (float)
- `TEXT`              (string)
- `BLOB`              (binary large object e.g.: images)
- `BOOLEAN`        (bool)
...

#### Main Functions of Relational Databases (CRUD)
- Creating:
	- `CREATE`, `INSERT`
- Reading
	- `SELECT` ^40ee59
- Updating
	- `UPDATE`
- Deleting
	- `DELETE`, `DROP`

#### SQL Methods
- `AVG`: Calculates the average value of a column
- `COUNT`: Counts the number of occurrences of a specific value
- `SUM`: Calculates the sum of numeric values in a column
- `MIN`: Retrieves the minimum value from a column
- `MAX`: Retrieves the maximum value from a column

#### SQL Clauses
- `WHERE`: Specifies a condition to filter the rows returned by a query
- `LIKE`: Used in a `WHERE` clause to search for a specified pattern in a column
- `ORDER BY`: Sorts the result set of a query by one or more columns in ascending (default) or descending order
- `LIMIT`: Limits the number of rows returned by a query
- `GROUP BY`: Groups rows based on the values in specified columns

#### SQL Keys
- `PRIMARY KEY`
	- A unique identifier of a table, so that it is relatable from other tables
- `SECONDARY KEY`
	- A reference to the primary key of another table, relating them

#### Joining Tables

*Example*: 
What are the Shows that Steve Carell starred in?
Tables: shows, stars, people

- **Parentheses**
```SQL
SELECT title FROM shows WHERE id IN 
(SELECT show_id FROM stars WHERE person_id = 
(SELECT id FROM people WHERE name = 'Steve Carell'));
```
- **Explicit Joining**
```SQL
SELECT title FROM people 
JOIN stars ON people.id = stars.person_id
JOIN shows ON stars.show_id = shows.id
WHERE name = 'Steve Carell';
```
- **Implicit Joining**
```SQL
SELECT title FROM people, stars, shows
WHERE people.id = stars.person_id
AND stars.show_id = shows.id
AND name = 'Steve Carell'
/* If the name attribute existed in multiple of the tables that were joined, then the table would need to be specified -> table.attribute */
```

! `.schema`: Shows all of the tables