HAR(30) NOT NULL,
done boolean DEFAULT' at line 1
mysql> desc todos;
+-------+------------+------+-----+---------+----------------+
| Field | Type       | Null | Key | Default | Extra          |
+-------+------------+------+-----+---------+----------------+
| id    | int(11)    | NO   | PRI | NULL    | auto_increment |
| name  | char(30)   | NO   |     | NULL    |                |
| done  | tinyint(1) | YES  |     | 0       |                |
+-------+------------+------+-----+---------+----------------+
3 rows in set (0.09 sec)

mysql> insert into todos(name,done) values("tarek",true);
Query OK, 1 row affected (0.07 sec)

mysql> show todos;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'todos' at line 1
mysql> select * from todos;
+----+---------------+------+
| id | name          | done |
+----+---------------+------+
|  1 | column values |    1 |
|  2 | tarek         |    1 |
+----+---------------+------+
2 rows in set (0.00 sec)

mysql> insert into todos(name,done)values("tarek tarho",false);
Query OK, 1 row affected (0.07 sec)

mysql> select * from todos;
+----+---------------+------+
| id | name          | done |
+----+---------------+------+
|  1 | column values |    1 |
|  2 | tarek         |    1 |
|  3 | tarek tarho   |    0 |
+----+---------------+------+
3 rows in set (0.00 sec)

mysql> insert into todos(name,done) values("wake up",true);
Query OK, 1 row affected (0.10 sec)

mysql> insert into todos(name,done) values("eat breakfast",true);
Query OK, 1 row affected (0.05 sec)

mysql> insert into todos(name,done) values("go to gym",true);
Query OK, 1 row affected (0.06 sec)

mysql> insert into todos(name,done) values("take a shower",true);
Query OK, 1 row affected (0.09 sec)

mysql> insert into todos(name,done) values("eat other meal",true);
Query OK, 1 row affected (0.07 sec)

mysql> insert into todos(name,done) values("go to work",true);
Query OK, 1 row affected (0.05 sec)

mysql> select * from todos;
+----+----------------+------+
| id | name           | done |
+----+----------------+------+
|  1 | column values  |    1 |
|  2 | tarek          |    1 |
|  3 | tarek tarho    |    0 |
|  4 | wake up        |    1 |
|  5 | eat breakfast  |    1 |
|  6 | go to gym      |    1 |
|  7 | take a shower  |    1 |
|  8 | eat other meal |    1 |
|  9 | go to work     |    1 |
+----+----------------+------+
9 rows in set (0.02 sec)
