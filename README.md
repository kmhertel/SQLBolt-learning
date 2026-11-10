# SQLBolt-learning

SQL allows both technical and non-technical users to query, manipulate and transform data from a relational database. popular
SQL model is like an excel table

---writing SQL queries
SELECT - retrieve data from SQL database, refered to as *queries*
query - a statement which declares what data we are looking, where and possibly how to transform it before return
SYNTAX:
  SELECT column, another_column, ...
  FROM mytable;
results in 2D set of rows and columns of selected columns requested
  
for all columns
SYNTAX:
  SELECT *
  FROM mytable;
simple way to inspect table by dumpinng all data at once

EXERCISE:
SELECT * FROM movies; to
SELECT Title FROM movies; to 
SELECT director FROM movies; to
SELECT Title, director FROM movies; to
SELECT Title, year FROM movies; to
SELECT * From movies;

---queries with constraints (pt1.)
WHERE - filter certain results, applied to each row of data by checking specific column values
SYNTAX:
  SELECT column, ...
  FROM mytable
  WHERE condition
        AND/OR another_condition
        ...;

OPERATORS:
  BETWEEN... AND... - number is within range of two values (inclusive)
  NOT BETWEEN... AND... - number is not within range of two values (inclusive)
  IN (...) - number exists in a list
  NOT IN (...) - number does not exist in a list

EXERCISE:
SELECT * FROM movies;
  to
SELECT Title FROM movies
WHERE id == 6;
  to
SELECT Title FROM movies
WHERE year BETWEEN 2000 AND 2010;
  to
SELECT Title FROM movies
WHERE year NOT BETWEEN 2000 AND 2010;
  to
SELECT Title, year FROM movies
WHERE id BETWEEN 1 AND 5;

---queries with constraints (pt2)
MORE OPERATORS:
  = - case sensitive exact string comparison
  != or <> - case sensitive exact string inequality comparison
  LIKE - case insensitive exact string comparison
  NOT LIKE - case insensitive exact string inequality comparison
  % - anywhere in string to match a sequence of zero or more characters (only with (NOT) LIKE)
  - - anywhere in string to match a single character
  IN (...) - string exists in a list
  NOT IN (...) - string does not exists in a list

strings must be in quotations

EXERCISE:
SELECT * FROM movies;
  to
SELECT * FROM movies
WHERE Title LIKE "Toy Story%";
  to
SELECT * FROM movies
WHERE director = "John Lasseter";
  to
SELECT Title, director FROM movies
WHERE director != "John Lasseter";
  to
SELECT * FROM movies
WHERE Title LIKE "WALL-%";

---filtering and sorting query results




