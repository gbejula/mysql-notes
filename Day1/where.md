# WHERE CLAUSE

-- The following are the operators used with the where clause

>
>=
<=
=
!=
<>

__Example__

SELECT * 
FROM Customers
WHERE state = 'va'

e.g 2

SELECT *
FROM orders
WHERE order_date >= '2019-01-01'


# NOT, OR, and AND
-- The AND has a higher precedence. Then followed by the OR


WHERE birth_date > '1990-01-01' OR (points > 1000 AND state = 'VA')

# NOT CLAUSE

SELECT *
FROM Customers
WHERE NOT (birth_date > '1990-01-01' OR points > 1000)

When NOT is applied to the following, they change:

NOT > -- <=
NOT < -- >=
NOT OR -- AND

e.g

From the order_items table, get the items for order #6 where the total price is greater than 30

SELECT *
FROM order_items
WHERE order_id = 6 AND unit_price * quantity > 30 AS 'Total Price'