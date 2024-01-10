# create database studentdb
# create table tblstudent
## columns are
1.studentId  datatyepe integer , make it as primary key and it shiuld be auto incremented,
2.studentName datatyepe varchar, range 64
3.dob datatyp date,
4. address datatyp varchar range 64

## Add atlead three entries (3 rows) into the table




mysql> CREATE DATABASE studentdb;
Query OK, 1 row affected (0,01 sec)

mysql> USE studentdb;
Database changed

mysql> CREATE TABLE tblstudent (studentId INT NOT NULL PRIMARY KEY AUTO_INCREMENT, studentName VARCHAR(64), dop DATE, address VARCHAR(64));
Query OK, 0 rows affected (0,03 sec)

mysql> INSERT INTO tblstudent (studentName, dop, address)
    -> VALUES
    -> ('Fritz the Fly', '2022-05-12', 'Munich'),
    -> ('Gabi Gobby', '2023-08-25', 'New York'),
    -> ('Sebastian Sebby', '1991-07-30', 'Madrid');
Query OK, 3 rows affected (0,02 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> SELECT * FROM tblstudent;
+-----------+-----------------+------------+----------+
| studentId | studentName     | dop        | address  |
+-----------+-----------------+------------+----------+
|         1 | Fritz the Fly   | 2022-05-12 | Munich   |
|         2 | Gabi Gobby      | 2023-08-25 | New York |
|         3 | Sebastian Sebby | 1991-07-30 | Madrid   |
+-----------+-----------------+------------+----------+
3 rows in set (0,00 sec)

mysql> ALTER TABLE tblstudent RENAME COLUMN dop TO dob;
Query OK, 0 rows affected (0,03 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> SELECT * FROM tblstudent;
+-----------+-----------------+------------+----------+
| studentId | studentName     | dob        | address  |
+-----------+-----------------+------------+----------+
|         1 | Fritz the Fly   | 2022-05-12 | Munich   |
|         2 | Gabi Gobby      | 2023-08-25 | New York |
|         3 | Sebastian Sebby | 1991-07-30 | Madrid   |
+-----------+-----------------+------------+----------+
3 rows in set (0,00 sec)
