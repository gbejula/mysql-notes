# IN OPERATOR

It is used when comparing an operator with a list of values.

e.g

SELECT *
FROM Customers
WHERE state = 'VA' OR state = 'GA' OR state = 'FL'

equivalent

WHERE state IN ('VA', 'FL', 'GA')

**Another example**

WHERE state NOT IN ('VA', 'FL', 'GA')


# BETWEEN OPERATOR

It is used when comparing an attribute with a range of values.

SELECT * 
FROM Customers
WHERE points >= 1000 AND points <= 3000

equivalent 

WHERE points BETWEEN 1000 AND 3000

|**Another example**

SELECT *
FROM Customers
WHERE birth_date BETWEEN '1990-01-01' AND '2000-01-01'


# LIKE OPERATOR

This is used to get roles that match a specific string pattern

SELECT * 
FROM customers
WHERE last_name LIKE 'b%'

**% -- it is used to represent any number of characters after b and the b is checks for both lower or upper case.**

WHERE last_name LIKE '%b%'

**'%b%' -- the double %% means that any string that contains b in any string.**

WHERE last_name LIKE '%y'

**-- this means any surname that contains y.**

WHERE last_name LIKE '_y'

**this means any last that has only 2 characters and the last character is y**

WHERE last_name LIKE '_____y'

**this means that there are 5 characters but it ends with y.**

-- % any number of characters
-- _ single character.



e.g Get the customers whose addresses contain TRAIL or AVENUE

SELECT *
FROM customers
WHERE address LIKE '%trail%' OR address LIKE '%avenue%'

-- customer phone numbers end with 9

WHERE phone LIKE '%9'