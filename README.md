 select * from ecommerce.customers;
+-------------+---------+-------------------+
| customer_id | name    | email             |
+-------------+---------+-------------------+
|           1 | smitha  | smi3@gmail.com    |
|           2 | shreeja | srija14@gmail.com |
+-------------+---------+-------------------+
2 rows in set (0.015 sec)

mysql> select name from ecommerce.customers;
+---------+
| name    |
+---------+
| smitha  |
| shreeja |
+---------+
2 rows in set (0.006 sec)
 select price from ecommerce.products;
+-------+
| price |
+-------+
| 45.00 |
| 42.00 |
+-------+
2 rows in set (0.007 sec)

mysql> select * from ecommerce.products where product_id=5;
+------------+---------+-------+
| product_id | name    | price |
+------------+---------+-------+
|          5 | colgate | 20.00 |
+------------+---------+-------+
1 row in set (0.011 sec)
 select name from ecommerce.products where price>40;
+---------------+
| name          |
+---------------+
| basumati rice |
| sugar         |
+---------------+
2 rows in set (0.006 sec)

mysql> select * from products where name=egg and price=5;
ERROR 1054 (42S22): Unknown column 'egg' in 'where clause'
mysql> select * from products where name='egg' and price=5;
+------------+------+-------+
| product_id | name | price |
+------------+------+-------+
|          3 | egg  |  5.00 |
+------------+------+-------+
1 row in set (0.010 sec)

mysql> select name from products where product_id=3 or price=20;
+---------+
| name    |
+---------+
| egg     |
| colgate |
+---------+
2 rows in set (0.008 sec)
