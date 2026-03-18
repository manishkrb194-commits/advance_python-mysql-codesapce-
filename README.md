# advance_python-mysql-codesapce-

mysql> select * from gietudb;
+---------+--------+----------+-------------+--------+--------+
| Roll_no | name   | address  | designation | salary | gender |
+---------+--------+----------+-------------+--------+--------+
| 101     | Aman   | Delhi    | Doctor      |  25000 | M      |
| 102     | manish | Delhi    | teacher     |  20000 | M      |
| 103     | Raman  | Rayagada | Plumber     |  15000 | M      |
| 104     | Navi   | Raipur   | Nurse       |  15000 | F      |
| 105     | Pavi   | Raigarh  | Police      |  25000 | F      |
| 106     | Ankit  | China    | Singer      |  45000 | M      |
| 107     | Umesh  | Vizag    | Dancer      |  45000 | M      |
| 108     | Ramesh | Bihar    | Manager     |  25000 | M      |
| 109     | Mahesh | Patna    | Thief       |  55000 | M      |
| 110     | Sita   | Kolkata  | Teacher     |  30000 | F      |
+---------+--------+----------+-------------+--------+--------+
10 rows in set (0.00 sec)

mysql>
mysql>
mysql>
mysql>
mysql>
mysql>
mysql> ^C
mysql> CREATE DATABASE giet_db;
Query OK, 1 row affected (0.03 sec)

mysql> USE giet_db;
Database changed
mysql> CREATE TABLE giet (
    ->     roll INT PRIMARY KEY,
    ->     name VARCHAR(50),
    ->     address VARCHAR(50),
    ->     desig VARCHAR(50),
    ->     salary INT,
    ->     gender CHAR(1)
    -> );
Query OK, 0 rows affected (0.06 sec)

mysql> INSERT INTO giet VALUES
    -> (101, 'aman', 'delhi', 'doctor', 25000, 'M'),
    -> (102, 'naman', 'gunupur', 'teacher', 15000, 'M'),
    -> (103, 'raman', 'rayagada', 'plumber', 15000, 'M'),
    -> (104, 'Navi', 'raipur', 'nurse', 15000, 'F'),
    -> (105, 'Pavi', 'raigarh', 'police', 25000, 'F'),
    -> (106, 'Ankit', 'china', 'singer', 45000, 'M'),
    -> (107, 'Umesh', 'vizag', 'dancer', 45000, 'M'),
    -> (108, 'ramesh', 'bihar', 'manager', 25000, 'M'),
    -> (109, 'mahesh', 'patna', 'thied', 55000, 'M');
Query OK, 9 rows affected (0.01 sec)
Records: 9  Duplicates: 0  Warnings: 0

mysql> SELECT * FROM giet;
+------+--------+----------+---------+--------+--------+
| roll | name   | address  | desig   | salary | gender |
+------+--------+----------+---------+--------+--------+
|  101 | aman   | delhi    | doctor  |  25000 | M      |
|  102 | naman  | gunupur  | teacher |  15000 | M      |
|  103 | raman  | rayagada | plumber |  15000 | M      |
|  104 | Navi   | raipur   | nurse   |  15000 | F      |
|  105 | Pavi   | raigarh  | police  |  25000 | F      |
|  106 | Ankit  | china    | singer  |  45000 | M      |
|  107 | Umesh  | vizag    | dancer  |  45000 | M      |
|  108 | ramesh | bihar    | manager |  25000 | M      |
|  109 | mahesh | patna    | thied   |  55000 | M      |
+------+--------+----------+---------+--------+--------+
9 rows in set (0.00 sec)

mysql> select  name from giet;
+--------+
| name   |
+--------+
| aman   |
| naman  |
| raman  |
| Navi   |
| Pavi   |
| Ankit  |
| Umesh  |
| ramesh |
| mahesh |
+--------+
9 rows in set (0.00 sec)

mysql> SELECT name, address FROM giet;
+--------+----------+
| name   | address  |
+--------+----------+
| aman   | delhi    |
| naman  | gunupur  |
| raman  | rayagada |
| Navi   | raipur   |
| Pavi   | raigarh  |
| Ankit  | china    |
| Umesh  | vizag    |
| ramesh | bihar    |
| mahesh | patna    |
+--------+----------+
9 rows in set (0.00 sec)

mysql> SELECT roll, salary FROM giet;
+------+--------+
| roll | salary |
+------+--------+
|  101 |  25000 |
|  102 |  15000 |
|  103 |  15000 |
|  104 |  15000 |
|  105 |  25000 |
|  106 |  45000 |
|  107 |  45000 |
|  108 |  25000 |
|  109 |  55000 |
+------+--------+
9 rows in set (0.00 sec)

mysql> SELECT * FROM giet WHERE name = 'aman';
+------+------+---------+--------+--------+--------+
| roll | name | address | desig  | salary | gender |
+------+------+---------+--------+--------+--------+
|  101 | aman | delhi   | doctor |  25000 | M      |
+------+------+---------+--------+--------+--------+
1 row in set (0.00 sec)

mysql> SELECT * FROM giet WHERE address = 'delhi';
+------+------+---------+--------+--------+--------+
| roll | name | address | desig  | salary | gender |
+------+------+---------+--------+--------+--------+
|  101 | aman | delhi   | doctor |  25000 | M      |
+------+------+---------+--------+--------+--------+
1 row in set (0.00 sec)

mysql> select *from giet where gender = 'M';
+------+--------+----------+---------+--------+--------+
| roll | name   | address  | desig   | salary | gender |
+------+--------+----------+---------+--------+--------+
|  101 | aman   | delhi    | doctor  |  25000 | M      |
|  102 | naman  | gunupur  | teacher |  15000 | M      |
|  103 | raman  | rayagada | plumber |  15000 | M      |
|  106 | Ankit  | china    | singer  |  45000 | M      |
|  107 | Umesh  | vizag    | dancer  |  45000 | M      |
|  108 | ramesh | bihar    | manager |  25000 | M      |
|  109 | mahesh | patna    | thied   |  55000 | M      |
+------+--------+----------+---------+--------+--------+
7 rows in set (0.00 sec)

mysql> SELECT *FROM  giet where desig ='doctor';
+------+------+---------+--------+--------+--------+
| roll | name | address | desig  | salary | gender |
+------+------+---------+--------+--------+--------+
|  101 | aman | delhi   | doctor |  25000 | M      |
+------+------+---------+--------+--------+--------+
1 row in set (0.00 sec)

mysql> select *from giet where salary = 15000;
+------+-------+----------+---------+--------+--------+
| roll | name  | address  | desig   | salary | gender |
+------+-------+----------+---------+--------+--------+
|  102 | naman | gunupur  | teacher |  15000 | M      |
|  103 | raman | rayagada | plumber |  15000 | M      |
|  104 | Navi  | raipur   | nurse   |  15000 | F      |
+------+-------+----------+---------+--------+--------+
3 rows in set (0.00 sec)

mysql> select *from giet where salary < 20000;
+------+-------+----------+---------+--------+--------+
| roll | name  | address  | desig   | salary | gender |
+------+-------+----------+---------+--------+--------+
|  102 | naman | gunupur  | teacher |  15000 | M      |
|  103 | raman | rayagada | plumber |  15000 | M      |
|  104 | Navi  | raipur   | nurse   |  15000 | F      |
+------+-------+----------+---------+--------+--------+
3 rows in set (0.00 sec)

mysql>  select *from giet where salary > 20000;
+------+--------+---------+---------+--------+--------+
| roll | name   | address | desig   | salary | gender |
+------+--------+---------+---------+--------+--------+
|  101 | aman   | delhi   | doctor  |  25000 | M      |
|  105 | Pavi   | raigarh | police  |  25000 | F      |
|  106 | Ankit  | china   | singer  |  45000 | M      |
|  107 | Umesh  | vizag   | dancer  |  45000 | M      |
|  108 | ramesh | bihar   | manager |  25000 | M      |
|  109 | mahesh | patna   | thied   |  55000 | M      |
+------+--------+---------+---------+--------+--------+
6 rows in set (0.00 sec)

mysql>  select *from giet where salary < 30000;
+------+--------+----------+---------+--------+--------+
| roll | name   | address  | desig   | salary | gender |
+------+--------+----------+---------+--------+--------+
|  101 | aman   | delhi    | doctor  |  25000 | M      |
|  102 | naman  | gunupur  | teacher |  15000 | M      |
|  103 | raman  | rayagada | plumber |  15000 | M      |
|  104 | Navi   | raipur   | nurse   |  15000 | F      |
|  105 | Pavi   | raigarh  | police  |  25000 | F      |
|  108 | ramesh | bihar    | manager |  25000 | M      |
+------+--------+----------+---------+--------+--------+
6 rows in set (0.00 sec)

mysql> select *from giet where gender = 'M' AND SALARY >20000;
+------+--------+---------+---------+--------+--------+
| roll | name   | address | desig   | salary | gender |
+------+--------+---------+---------+--------+--------+
|  101 | aman   | delhi   | doctor  |  25000 | M      |
|  106 | Ankit  | china   | singer  |  45000 | M      |
|  107 | Umesh  | vizag   | dancer  |  45000 | M      |
|  108 | ramesh | bihar   | manager |  25000 | M      |
|  109 | mahesh | patna   | thied   |  55000 | M      |
+------+--------+---------+---------+--------+--------+
5 rows in set (0.00 sec)

mysql> SELECT*FROM GIET WHERE GENDER = 'F' OR ADDRESS = 'raipur';
+------+------+---------+--------+--------+--------+
| roll | name | address | desig  | salary | gender |
+------+------+---------+--------+--------+--------+
|  104 | Navi | raipur  | nurse  |  15000 | F      |
|  105 | Pavi | raigarh | police |  25000 | F      |
+------+------+---------+--------+--------+--------+
2 rows in set (0.00 sec)

mysql> select *from giet where name = 'a';
Empty set (0.00 sec)

mysql> SELECT * FROM GIETUdb
    -> WHERE name LIKE 'a%';
ERROR 1146 (42S02): Table 'giet_db.gietudb' doesn't exist
mysql> select * from giet where name like 'a%';
+------+-------+---------+--------+--------+--------+
| roll | name  | address | desig  | salary | gender |
+------+-------+---------+--------+--------+--------+
|  101 | aman  | delhi   | doctor |  25000 | M      |
|  106 | Ankit | china   | singer |  45000 | M      |
+------+-------+---------+--------+--------+--------+
2 rows in set (0.00 sec)

mysql> select*from giet where name like'%h';
+------+--------+---------+---------+--------+--------+
| roll | name   | address | desig   | salary | gender |
+------+--------+---------+---------+--------+--------+
|  107 | Umesh  | vizag   | dancer  |  45000 | M      |
|  108 | ramesh | bihar   | manager |  25000 | M      |
|  109 | mahesh | patna   | thied   |  55000 | M      |
+------+--------+---------+---------+--------+--------+
3 rows in set (0.00 sec)

mysql> select *from giet where address like '%pur';
+------+-------+---------+---------+--------+--------+
| roll | name  | address | desig   | salary | gender |
+------+-------+---------+---------+--------+--------+
|  102 | naman | gunupur | teacher |  15000 | M      |
|  104 | Navi  | raipur  | nurse   |  15000 | F      |
+------+-------+---------+---------+--------+--------+
2 rows in set (0.00 sec)

mysql> select *from giet order by name asc;
+------+--------+----------+---------+--------+--------+
| roll | name   | address  | desig   | salary | gender |
+------+--------+----------+---------+--------+--------+
|  101 | aman   | delhi    | doctor  |  25000 | M      |
|  106 | Ankit  | china    | singer  |  45000 | M      |
|  109 | mahesh | patna    | thied   |  55000 | M      |
|  102 | naman  | gunupur  | teacher |  15000 | M      |
|  104 | Navi   | raipur   | nurse   |  15000 | F      |
|  105 | Pavi   | raigarh  | police  |  25000 | F      |
|  103 | raman  | rayagada | plumber |  15000 | M      |
|  108 | ramesh | bihar    | manager |  25000 | M      |
|  107 | Umesh  | vizag    | dancer  |  45000 | M      |
+------+--------+----------+---------+--------+--------+
9 rows in set (0.00 sec)

mysql>  select *from giet order by salary dsc;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'dsc' at line 1
mysql>  select *from giet order by salary des;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'des' at line 1
mysql> select *from giet order by salary desc;
+------+--------+----------+---------+--------+--------+
| roll | name   | address  | desig   | salary | gender |
+------+--------+----------+---------+--------+--------+
|  109 | mahesh | patna    | thied   |  55000 | M      |
|  106 | Ankit  | china    | singer  |  45000 | M      |
|  107 | Umesh  | vizag    | dancer  |  45000 | M      |
|  101 | aman   | delhi    | doctor  |  25000 | M      |
|  105 | Pavi   | raigarh  | police  |  25000 | F      |
|  108 | ramesh | bihar    | manager |  25000 | M      |
|  102 | naman  | gunupur  | teacher |  15000 | M      |
|  103 | raman  | rayagada | plumber |  15000 | M      |
|  104 | Navi   | raipur   | nurse   |  15000 | F      |
+------+--------+----------+---------+--------+--------+
9 rows in set (0.00 sec)

mysql> select count(*) from giet;
+----------+
| count(*) |
+----------+
|        9 |
+----------+
1 row in set (0.01 sec)

mysql> select count(*) from giet where gender = 'M';
+----------+
| count(*) |
+----------+
|        7 |
+----------+
1 row in set (0.00 sec)

mysql>
