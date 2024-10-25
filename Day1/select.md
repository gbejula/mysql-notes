To get all details in a table

-- The use command is used to select a database

USE name_of_db;

-- SELECT STATMENT
-- * helps to select all the rows in the table.
-- Retrieve data from a single table


SELECT column FROM table
select * from table_name

-- The order to get info from a table

SELECT column, ...
FROM table_name
WHERE condition(s)
ORDER BY column


# SELECT CLAUSE
-- Arithmetic operations can also be done during a select.

SELECT last_name, first_name, points * 10 + 100
FROM customers

# USING ALIAS

SELECT 
    last_name, 
    first_name, 
    (points + 10) * 100 AS Discount_Factor
FROM customers

** To use space in between the ALIAS, it should be in parenthesis.

e.g AS 'Discount Factor'


# Working with duplicates in a select table.

DISTINCT keyword is used to remove duplicates

SELECT DISTINCT state 
FROM customers