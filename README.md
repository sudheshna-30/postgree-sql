<pre># postgree-sql
Microsoft Windows [Version 10.0.19045.5737]
(c) Microsoft Corporation. All rights reserved.

C:\Users\Minfy>psql
Password for user Minfy:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Minfy"

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# CREATE USER university_admin WITH PASSWORD 'your_secure_password';
CREATE ROLE
postgres=# CREATE USERNAME WITH PASSWORD 'Sudhu@1664';
ERROR:  syntax error at or near "USERNAME"
LINE 1: CREATE USERNAME WITH PASSWORD 'Sudhu@1664';
               ^
postgres=# CREATE USER Sudheshna WITH PASSWORD 'Sudhu@1664';
CREATE ROLE
postgres=# CREATE DATABASE university_db OWNER university_admin;
CREATE DATABASE
postgres=# CREATE DATABASE minfy_db OWNER Sudheshna;
CREATE DATABASE
postgres=# GRANT ALL PRIVILEGES ON DATABASE university_db TO university_admin;
GRANT
postgres=# GRANT ALL PRIVILEGES ON DATABASE minfy_db TO Sudheshna;
GRANT
postgres=# \q

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>/password
'/password' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# psql -U Sudheshna -d minfy_db;
ERROR:  syntax error at or near "psql"
LINE 1: psql -U Sudheshna -d minfy_db;
        ^
postgres=# psql -U Sudheshna -d minfy_db
postgres-# \l
                                                                          List of databases
     Name      |      Owner       | Encoding | Locale Provider |      Collate       |       Ctype        | Locale | ICU Rules |           Access privileges
---------------+------------------+----------+-----------------+--------------------+--------------------+--------+-----------+---------------------------------------
 minfy_db      | sudheshna        | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =Tc/sudheshna                        +
               |                  |          |                 |                    |                    |        |           | sudheshna=CTc/sudheshna
 postgres      | postgres         | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           |
 template0     | postgres         | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =c/postgres                          +
               |                  |          |                 |                    |                    |        |           | postgres=CTc/postgres
 template1     | postgres         | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =c/postgres                          +
               |                  |          |                 |                    |                    |        |           | postgres=CTc/postgres
 university_db | university_admin | UTF8     | libc            | English_India.1252 | English_India.1252 |        |           | =Tc/university_admin                 +
               |                  |          |                 |                    |                    |        |           | university_admin=CTc/university_admin
(5 rows)


postgres-# \c minfy_db
You are now connected to database "minfy_db" as user "postgres".
minfy_db-# CREATE TABLE students(
minfy_db(# student_id INTEGER,
minfy_db(# first_name VARCHAR(50),
minfy_db(# last_name VARCHAR(50),
minfy_db(# email VARCHAR(100),
minfy_db(# date_of_birth DATE);
ERROR:  syntax error at or near "psql"
LINE 1: psql -U Sudheshna -d minfy_db
        ^
minfy_db=# CREATE TABLE students (
minfy_db(#     student_id INTEGER,
minfy_db(#     first_name VARCHAR(50),
minfy_db(#     last_name VARCHAR(50),
minfy_db(#     email VARCHAR(100),
minfy_db(#     date_of_birth DATE
minfy_db(# );
CREATE TABLE
minfy_db=# \d
          List of relations
 Schema |   Name   | Type  |  Owner
--------+----------+-------+----------
 public | students | table | postgres
(1 row)


minfy_db=# \q

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db;
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql
Password for user Minfy:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Minfy"

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# psql -U Sudheshna -d minfy_db
postgres-# psql -U Sudheshna -d minfy_db;
ERROR:  syntax error at or near "psql"
LINE 1: psql -U Sudheshna -d minfy_db
        ^
postgres=# psql -U Sudheshna -d minfy_db;
ERROR:  syntax error at or near "psql"
LINE 1: psql -U Sudheshna -d minfy_db;
        ^
postgres=# psql -U Sudheshna -d minfy_db
postgres-# \q

C:\Users\Minfy>\c Sudheshna
'\c' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>\c minfy_db
'\c' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>\c minfy_db
'\c' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# \c minfy_db
You are now connected to database "minfy_db" as user "postgres".
minfy_db=# CREATE TABLE students (
minfy_db(#     student_id INTEGER,
minfy_db(#     first_name VARCHAR(50),
minfy_db(#     last_name VARCHAR(50),
minfy_db(#     email VARCHAR(100),
minfy_db(#     date_of_birth DATE
minfy_db(# );
ERROR:  relation "students" already exists
minfy_db=# \q

C:\Users\Minfy>\d
'\d' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>psql -U Sudheshna -d  minfy_db
Password for user Sudheshna:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "Sudheshna"

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  password authentication failed for user "postgres"

C:\Users\Minfy>\password
'\password' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# \q

C:\Users\Minfy>CREATE USER university_admin WITH PASSWORD 'your_secure_password';
'CREATE' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>CREATE USER university_admin WITH PASSWORD 'Suh@97050';
'CREATE' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Minfy>psql -U postgres
Password for user postgres:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

postgres=# CREATE USER university_admin WITH PASSWORD 'your_secure_password';
ERROR:  role "university_admin" already exists
postgres=# CREATE USER uni_admin WITH PASSWORD 'Suh@97050';
CREATE ROLE
postgres=# CREATE DATABASE university_db OWNER university_admin;
ERROR:  database "university_db" already exists
postgres=# CREATE DATABASE uni_db OWNER uni_admin;
CREATE DATABASE
postgres=# GRANT ALL PRIVILEGES ON DATABASE university_db TO university_admin;
GRANT
postgres=# GRANT ALL PRIVILEGES ON DATABASE uni_db TO uni_admin;
GRANT
postgres=# psql -U uni_admin -d uni_db
postgres-# psql -U uni_admin -d uni_db;
ERROR:  syntax error at or near "psql"
LINE 1: psql -U uni_admin -d uni_db
        ^
postgres=# \q

C:\Users\Minfy>psql -U uni_admin -d uni_db
Password for user uni_admin:
psql (17.5)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.

uni_db=> CREATE TABLE students (
uni_db(>     student_id INTEGER,
uni_db(>     first_name VARCHAR(50),
uni_db(>     last_name VARCHAR(50),
uni_db(>     email VARCHAR(100),
uni_db(>     date_of_birth DATE
uni_db(> );
CREATE TABLE
uni_db=> \d
           List of relations
 Schema |   Name   | Type  |   Owner
--------+----------+-------+-----------
 public | students | table | uni_admin
(1 row)


uni_db=> ALTER TABLE students ADD COLUMN enrollment_date DATE;
ALTER TABLE
uni_db=> ALTER TABLE students DROP COLUMN enrollment_date;
ALTER TABLE
uni_db=> ALTER TABLE students ALTER COLUMN email TYPE VARCHAR(150);
ALTER TABLE
uni_db=> ALTER TABLE students RENAME COLUMN date_of_birth TO dob;
ALTER TABLE
uni_db=> ALTER TABLE students ADD CONSTRAINT unique_email UNIQUE (email);
ALTER TABLE
uni_db=> ALTER TABLE students RENAME TO learners;
ALTER TABLE
uni_db=> ALTER TABLE learners RENAME TO students; -- Change it back
ALTER TABLE
uni_db=> ALTER TABLE learners RENAME TO students;
ERROR:  relation "learners" does not exist
uni_db=> ALTER TABLE students ADD COLUMN phonenumber VARCHAR(20);
ALTER TABLE
uni_db=> ALTER TABLE students DROP COLUMN phonenumber;
ALTER TABLE
uni_db=> \d
           List of relations
 Schema |   Name   | Type  |   Owner
--------+----------+-------+-----------
 public | students | table | uni_admin
(1 row)


uni_db=> DROP TABLE IF EXISTS students;
DROP TABLE
uni_db=> CREATE TABLE students (
uni_db(>     student_id INTEGER,
uni_db(>     first_name VARCHAR(50),
uni_db(>     last_name VARCHAR(50),
uni_db(>     email VARCHAR(100),
uni_db(>     date_of_birth DATE
uni_db(> );
CREATE TABLE
uni_db=> \d
           List of relations
 Schema |   Name   | Type  |   Owner
--------+----------+-------+-----------
 public | students | table | uni_admin
(1 row)


uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (1, 'Alice', 'Smith', 'alice.smith@example.com', '2003-05-15');
ERROR:  column "dob" of relation "students" does not exist
LINE 1: ...NTO students (student_id, first_name, last_name, email, dob)
                                                                   ^
uni_db=>
uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (2, 'Bob', 'Johnson', 'bob.johnson@example.com', '2002-08-22'),
uni_db->        (3, 'Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10');
ERROR:  column "dob" of relation "students" does not exist
LINE 1: ...NTO students (student_id, first_name, last_name, email, dob)
                                                                   ^
uni_db=>        (3, 'Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10');
ERROR:  syntax error at or near "3"
LINE 1: (3, 'Charlie', 'Brown', 'charlie.brown@example.com', '2003-0...
         ^
uni_db=> \d students
                         Table "public.students"
    Column     |          Type          | Collation | Nullable | Default
---------------+------------------------+-----------+----------+---------
 student_id    | integer                |           |          |
 first_name    | character varying(50)  |           |          |
 last_name     | character varying(50)  |           |          |
 email         | character varying(100) |           |          |
 date_of_birth | date                   |           |          |


uni_db=> ALTER TABLE RENAME COLUMN date_of_birth TO dob;
ERROR:  syntax error at or near "COLUMN"
LINE 1: ALTER TABLE RENAME COLUMN date_of_birth TO dob;
                           ^
uni_db=> ALTER TABLE students  RENAME COLUMN date_of_birth TO dob;
ALTER TABLE
uni_db=> \d students
                       Table "public.students"
   Column   |          Type          | Collation | Nullable | Default
------------+------------------------+-----------+----------+---------
 student_id | integer                |           |          |
 first_name | character varying(50)  |           |          |
 last_name  | character varying(50)  |           |          |
 email      | character varying(100) |           |          |
 dob        | date                   |           |          |


uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (2, 'Bob', 'Johnson', 'bob.johnson@example.com', '2002-08-22'),
uni_db->        (3, 'Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10');
INSERT 0 2
uni_db=> \d students
                       Table "public.students"
   Column   |          Type          | Collation | Nullable | Default
------------+------------------------+-----------+----------+---------
 student_id | integer                |           |          |
 first_name | character varying(50)  |           |          |
 last_name  | character varying(50)  |           |          |
 email      | character varying(100) |           |          |
 dob        | date                   |           |          |


uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (1, 'Sudheshna', 'T', 'sudheshna@gmail.com', '2003-11-30'),
uni_db->        (4, 'eswar', 'aditya', 'aditya@gmail.com', '2003-11-05');
INSERT 0 2
uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (5, 'Keerthi', 'kelam', 'keerthi@gmail.com', '2004-06-28');
INSERT 0 1
uni_db=> SELECT first_name, last_name, email FROM students;
 first_name | last_name |           email
------------+-----------+---------------------------
 Bob        | Johnson   | bob.johnson@example.com
 Charlie    | Brown     | charlie.brown@example.com
 Sudheshna  | T         | sudheshna@gmail.com
 eswar      | aditya    | aditya@gmail.com
 Keerthi    | kelam     | keerthi@gmail.com
(5 rows)


uni_db=> SELECT * FROM students;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com   | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
          1 | Sudheshna  | T         | sudheshna@gmail.com       | 2003-11-30
          4 | eswar      | aditya    | aditya@gmail.com          | 2003-11-05
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
(5 rows)


uni_db=> SELECT * FROM students WHERE student_id = 1;
 student_id | first_name | last_name |        email        |    dob
------------+------------+-----------+---------------------+------------
          1 | Sudheshna  | T         | sudheshna@gmail.com | 2003-11-30
(1 row)


uni_db=> SELECT first_name, last_name FROM students WHERE last_name = 'aditya';
 first_name | last_name
------------+-----------
 eswar      | aditya
(1 row)


uni_db=> SELECT * FROM students WHERE dob >= '2006-06-28';
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> SELECT * FROM students WHERE dob >= '2004-06-28';
 student_id | first_name | last_name |       email       |    dob
------------+------------+-----------+-------------------+------------
          5 | Keerthi    | kelam     | keerthi@gmail.com | 2004-06-28
(1 row)


uni_db=> SELECT * FROM students WHERE dob BETWEEN '2003-01-31' AND '2004-12-30';
 student_id | first_name | last_name |        email        |    dob
------------+------------+-----------+---------------------+------------
          1 | Sudheshna  | T         | sudheshna@gmail.com | 2003-11-30
          4 | eswar      | aditya    | aditya@gmail.com    | 2003-11-05
          5 | Keerthi    | kelam     | keerthi@gmail.com   | 2004-06-28
(3 rows)


uni_db=> SELECT * FROM students WHERE first_name LIKE 'A%';
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> SELECT * FROM students WHERE first_name LIKE 'S%';
 student_id | first_name | last_name |        email        |    dob
------------+------------+-----------+---------------------+------------
          1 | Sudheshna  | T         | sudheshna@gmail.com | 2003-11-30
(1 row)


uni_db=> SELECT * FROM students WHERE email ILIKE '@.com';
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> SELECT * FROM students WHERE email ILIKE '%.com';
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com   | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
          1 | Sudheshna  | T         | sudheshna@gmail.com       | 2003-11-30
          4 | eswar      | aditya    | aditya@gmail.com          | 2003-11-05
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
(5 rows)


uni_db=> SELECT * FROM students WHERE first_name = 'Sudheshna' AND last_name = 'T';
 student_id | first_name | last_name |        email        |    dob
------------+------------+-----------+---------------------+------------
          1 | Sudheshna  | T         | sudheshna@gmail.com | 2003-11-30
(1 row)


uni_db=> SELECT * FROM students WHERE student_id = 1 OR student_id = 3;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
          1 | Sudheshna  | T         | sudheshna@gmail.com       | 2003-11-30
(2 rows)


uni_db=> SELECT * FROM students WHERE student_id IN (1, 3, 5);
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
          1 | Sudheshna  | T         | sudheshna@gmail.com       | 2003-11-30
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
(3 rows)


uni_db=> INSERT INTO students (student_id, first_name, last_name, dob) VALUES (4, 'Diana', 'Prince', '2001-11-01');
INSERT 0 1
uni_db=> SELECT * FROM students WHERE email IS NULL;
 student_id | first_name | last_name | email |    dob
------------+------------+-----------+-------+------------
          4 | Diana      | Prince    |       | 2001-11-01
(1 row)


uni_db=> SELECT * FROM students WHERE email IS NOT NULL;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com   | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
          1 | Sudheshna  | T         | sudheshna@gmail.com       | 2003-11-30
          4 | eswar      | aditya    | aditya@gmail.com          | 2003-11-05
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
(5 rows)


uni_db=> SELECT * FROM students WHERE student_id = 2;
 student_id | first_name | last_name |          email          |    dob
------------+------------+-----------+-------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com | 2002-08-22
(1 row)


uni_db=> SELECT * FROM students WHERE dob <= '2003-01-01';
 student_id | first_name | last_name |          email          |    dob
------------+------------+-----------+-------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com | 2002-08-22
          4 | Diana      | Prince    |                         | 2001-11-01
(2 rows)


uni_db=> SELECT * FROM students WHERE first_name LIKE 'B%'or 'C%';
ERROR:  invalid input syntax for type boolean: "C%"
LINE 1: SELECT * FROM students WHERE first_name LIKE 'B%'or 'C%';
                                                            ^
uni_db=> SELECT * FROM students WHERE first_name LIKE 'B%' or 'C%';
ERROR:  invalid input syntax for type boolean: "C%"
LINE 1: SELECT * FROM students WHERE first_name LIKE 'B%' or 'C%';
                                                             ^
uni_db=> SELECT * FROM students WHERE first_name LIKE 'B%' OR 'C%';
ERROR:  invalid input syntax for type boolean: "C%"
LINE 1: SELECT * FROM students WHERE first_name LIKE 'B%' OR 'C%';
                                                             ^
uni_db=> SELECT * FROM students WHERE first_name LIKE 'B%' OR first_name LIKE 'C%';
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com   | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
(2 rows)


uni_db=> Find students whose email address is from example.com.
uni_db-> SELECT * FROM students WHERE email ILIKE 'example.com';
ERROR:  syntax error at or near "Find"
LINE 1: Find students whose email address is from example.com.
        ^
uni_db=> SELECT * FROM students WHERE email ILIKE 'example.com';
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> SELECT * FROM students WHERE email ILIKE '@gmail.com';
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> WHERE email LIKE '%@example.com';
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          2 | Bob        | Johnson   | bob.johnson@example.com   | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10
(2 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> WHERE email IS NULL OR email = '';
 student_id | first_name | last_name | email |    dob
------------+------------+-----------+-------+------------
          4 | Diana      | Prince    |       | 2001-11-01
(1 row)


uni_db=> UPDATE table_name
uni_db-> SET column1 = value1, column2 = value2, ...
uni_db-> WHERE condition; -- CRITICAL! Without a WHERE clause, ALL rows in the table will be updated.
ERROR:  syntax error at or near ".."
LINE 2: SET column1 = value1, column2 = value2, ...
                                                ^
uni_db=> UPDATE students
uni_db-> SET email = 'alices@example.net'
uni_db-> WHERE student_id = 1;
UPDATE 1
uni_db=> UPDATE students
uni_db-> SET first_name = 'Robert', email = 'robert.j@example.com'
uni_db-> WHERE student_id = 2;
UPDATE 1
uni_db=> SELECT * FROM students WHERE student_id IN (1,2);
 student_id | first_name | last_name |        email         |    dob
------------+------------+-----------+----------------------+------------
          1 | Sudheshna  | T         | alices@example.net   | 2003-11-30
          2 | Robert     | Johnson   | robert.j@example.com | 2002-08-22
(2 rows)


uni_db=> UPDATE students
uni_db-> SET date_of_birth = '2003-02-15'
uni_db-> WHERE first_name = 'Charlie' AND last_name = 'Brown';
ERROR:  column "date_of_birth" of relation "students" does not exist
LINE 2: SET date_of_birth = '2003-02-15'
            ^
uni_db=> UPDATE students
uni_db-> SET date_of_birth = '2003-02-15'
uni_db-> WHERE first_name = 'Charlie' AND last_name = 'Brown';
ERROR:  column "date_of_birth" of relation "students" does not exist
LINE 2: SET date_of_birth = '2003-02-15'
            ^
uni_db=> UPDATE students
uni_db-> SET date_of_birth = '2003-02-15'
uni_db-> WHERE first_name = 'Charlie' AND last_name = 'Brown';
ERROR:  column "date_of_birth" of relation "students" does not exist
LINE 2: SET date_of_birth = '2003-02-15'
            ^
uni_db=> UPDATE students
uni_db-> SET dob = '2003-02-15'
uni_db-> WHERE first_name = 'Charlie' AND last_name = 'Brown';
UPDATE 1
uni_db=> UPDATE students
uni_db-> SET email = 'diana.prince@example.org'
uni_db-> WHERE student_id = 4;
UPDATE 2
uni_db=> \d students
                       Table "public.students"
   Column   |          Type          | Collation | Nullable | Default
------------+------------------------+-----------+----------+---------
 student_id | integer                |           |          |
 first_name | character varying(50)  |           |          |
 last_name  | character varying(50)  |           |          |
 email      | character varying(100) |           |          |
 dob        | date                   |           |          |


uni_db=> SELECT * FROM students
uni_db-> SELECT * FROM students;
ERROR:  syntax error at or near "SELECT"
LINE 2: SELECT * FROM students;
        ^
uni_db=> SELECT * FROM students;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
(6 rows)


uni_db=> UPDATE students
uni_db-> SET email = 'aditya@example.org'
uni_db-> WHERE student_id = 4;
UPDATE 2
uni_db=> SELECT * FROM students;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | aditya@example.org        | 2003-11-05
          4 | Diana      | Prince    | aditya@example.org        | 2001-11-01
(6 rows)


uni_db=> UPDATE students
uni_db-> SET email = 'diana.prince@example.org'
uni_db-> WHERE student_id = 4;
UPDATE 2
uni_db=> DELETE FROM table_name
uni_db-> WHERE condition;
ERROR:  relation "table_name" does not exist
LINE 1: DELETE FROM table_name
                    ^
uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (99, 'Temp', 'User', 'temp@example.com', '2000-01-01');
INSERT 0 1
uni_db=> SELECT * FROM students WHERE student_id = 99;
 student_id | first_name | last_name |      email       |    dob
------------+------------+-----------+------------------+------------
         99 | Temp       | User      | temp@example.com | 2000-01-01
(1 row)


uni_db=> DELETE FROM students WHERE student_id = 99;
DELETE 1
uni_db=> SELECT * FROM students WHERE student_id = 99;
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (100, 'karthik', 'L', 'karthik@example.com', '2003-08-22');
INSERT 0 1
uni_db=> SELECT * FROM students WHERE student_id = 100;
 student_id | first_name | last_name |        email        |    dob
------------+------------+-----------+---------------------+------------
        100 | karthik    | L         | karthik@example.com | 2003-08-22
(1 row)


uni_db=> DELETE FROM students WHERE student_id = 100;
DELETE 1
uni_db=> SELECT * FROM students WHERE student_id = 100;
 student_id | first_name | last_name | email | dob
------------+------------+-----------+-------+-----
(0 rows)


uni_db=> SELECT * FROM students ORDER BY last_name ASC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
(6 rows)


uni_db=> SELECT * FROM students ORDER BY dob DESC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
(6 rows)


uni_db=> SELECT * FROM students ORDER BY last_name, first_name;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
(6 rows)


uni_db=> SELECT * FROM students ORDER BY dob DESC LIMIT 3;
 student_id | first_name | last_name |          email           |    dob
------------+------------+-----------+--------------------------+------------
          5 | Keerthi    | kelam     | keerthi@gmail.com        | 2004-06-28
          1 | Sudheshna  | T         | alices@example.net       | 2003-11-30
          4 | eswar      | aditya    | diana.prince@example.org | 2003-11-05
(3 rows)


uni_db=> SELECT * FROM students ORDER BY student_id LIMIT 2 OFFSET 2;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
(2 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY last_name DESC, first_name ASC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
(6 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY last_name DESC, first_name ASC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
(6 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY date_of_birth ASC;
ERROR:  column "date_of_birth" does not exist
LINE 3: ORDER BY date_of_birth ASC;
                 ^
uni_db=> SELECT * FROM students ORDER BY dob ASC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
(6 rows)


uni_db=> FROM students
uni_db-> ORDER BY last_name DESC, first_name ASC;
ERROR:  syntax error at or near "FROM"
LINE 1: FROM students
        ^
uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY date_of_birth ASC;
ERROR:  column "date_of_birth" does not exist
LINE 3: ORDER BY date_of_birth ASC;
                 ^
uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY date_of_birth ASC;
ERROR:  column "date_of_birth" does not exist
LINE 3: ORDER BY date_of_birth ASC;
                 ^
uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY dob ASC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
(6 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY last_name DESC, first_name ASC;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          1 | Sudheshna  | T         | alices@example.net        | 2003-11-30
          4 | Diana      | Prince    | diana.prince@example.org  | 2001-11-01
          5 | Keerthi    | kelam     | keerthi@gmail.com         | 2004-06-28
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
          4 | eswar      | aditya    | diana.prince@example.org  | 2003-11-05
(6 rows)


uni_db=> SELECT *
uni_db-> FROM students
uni_db-> ORDER BY date_of_birth ASC
uni_db-> LIMIT 2;
ERROR:  column "date_of_birth" does not exist
LINE 3: ORDER BY date_of_birth ASC
                 ^
uni_db=> SELECT * FROM ORDER BY dob ASC LIMIT 2;
ERROR:  syntax error at or near "ORDER"
LINE 1: SELECT * FROM ORDER BY dob ASC LIMIT 2;
                      ^
uni_db=> SELECT * FROM students ORDER BY dob ASC LIMIT 2;
 student_id | first_name | last_name |          email           |    dob
------------+------------+-----------+--------------------------+------------
          4 | Diana      | Prince    | diana.prince@example.org | 2001-11-01
          2 | Robert     | Johnson   | robert.j@example.com     | 2002-08-22
(2 rows)


uni_db=> SELECT * FROM students ORDER BY student_id ASC LIMIT 2 OFFSET 1;
 student_id | first_name | last_name |           email           |    dob
------------+------------+-----------+---------------------------+------------
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-02-15
(2 rows)


uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob)
uni_db-> VALUES (5, 'Eve', 'Smith', 'eve.smith@example.com', '2004-07-01');
INSERT 0 1
uni_db=> SELECT last_name FROM students;
 last_name
-----------
 kelam
 T
 Johnson
 Brown
 aditya
 Prince
 Smith
(7 rows)


uni_db=> SELECT DISTINCT last_name FROM students ORDER BY last_name;
 last_name
-----------
 aditya
 Brown
 Johnson
 kelam
 Prince
 Smith
 T
(7 rows)


uni_db=> SELECT DISTINCT last_name, first_name FROM students;
 last_name | first_name
-----------+------------
 Prince    | Diana
 T         | Sudheshna
 kelam     | Keerthi
 aditya    | eswar
 Smith     | Eve
 Johnson   | Robert
 Brown     | Charlie
(7 rows)


uni_db=> SELECT DISTINCT dob FROM students ORDER BY dob;
    dob
------------
 2001-11-01
 2002-08-22
 2003-02-15
 2003-11-05
 2003-11-30
 2004-06-28
 2004-07-01
(7 rows)


uni_db=> SELECT DISTINCT EXTRACT(YEAR FROM date_of_birth) AS birth_year
uni_db-> FROM students
uni_db-> ORDER BY birth_year;
ERROR:  column "date_of_birth" does not exist
LINE 1: SELECT DISTINCT EXTRACT(YEAR FROM date_of_birth) AS birth_ye...
                                          ^
uni_db=> SELECT DISTINCT EXTRACT(YEAR FROM dob) AS birth_year
uni_db-> FROM students
uni_db-> ORDER BY birth_year;
 birth_year
------------
       2001
       2002
       2003
       2004
(4 rows)


uni_db=> SELECT COUNT(*) AS total_students FROM students;
 total_students
----------------
              7
(1 row)


uni_db=> SELECT COUNT(email) AS students_with_email FROM students;
 students_with_email
---------------------
                   7
(1 row)


uni_db=> SELECT COUNT(DISTINCT last_name) AS unique_last_names FROM students;
 unique_last_names
-------------------
                 7
(1 row)


uni_db=> SELECT MIN(dob) AS oldest_student_dob FROM students;
 oldest_student_dob
--------------------
 2001-11-01
(1 row)


uni_db=> SELECT MAX(dob) AS youngest_student_dob FROM students;
 youngest_student_dob
----------------------
 2004-07-01
(1 row)


uni_db=> SELECT COUNT(*) AS total_students FROM students;
 total_students
----------------
              7
(1 row)


uni_db=> SELECT last_name, COUNT(*) AS number_of_students
uni_db-> FROM students
uni_db-> GROUP BY last_name
uni_db-> ORDER BY number_of_students DESC;
 last_name | number_of_students
-----------+--------------------
 aditya    |                  1
 kelam     |                  1
 Smith     |                  1
 T         |                  1
 Johnson   |                  1
 Prince    |                  1
 Brown     |                  1
(7 rows)


uni_db=> SELECT last_name, COUNT(*) AS number_of_students
uni_db-> FROM students
uni_db-> GROUP BY last_name
uni_db-> HAVING COUNT(*) > 1
uni_db-> ORDER BY number_of_students DESC;
 last_name | number_of_students
-----------+--------------------
(0 rows)


uni_db=> SELECT EXTRACT(YEAR FROM dob) AS birth_year, COUNT(*) AS students_in_year
uni_db-> FROM students
uni_db-> WHERE dob IS NOT NULL
uni_db-> GROUP BY birth_year
uni_db-> ORDER BY birth_year;
 birth_year | students_in_year
------------+------------------
       2001 |                1
       2002 |                1
       2003 |                3
       2004 |                2
(4 rows)


uni_db=> SELECT first_name, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY first_name
uni_db-> ORDER BY count DESC, first_name;
 first_name | count
------------+-------
 Charlie    |     1
 Diana      |     1
 eswar      |     1
 Eve        |     1
 Keerthi    |     1
 Robert     |     1
 Sudheshna  |     1
(7 rows)


uni_db=> SELECT EXTRACT(YEAR FROM date_of_birth) AS birth_year, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY birth_year
uni_db-> ORDER BY birth_year;
ERROR:  column "date_of_birth" does not exist
LINE 1: SELECT EXTRACT(YEAR FROM date_of_birth) AS birth_year, COUNT...
                                 ^
uni_db=> SELECT EXTRACT(YEAR FROM dob) AS birth_year, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY first_name
uni_db-> ORDER BY birth_year;
ERROR:  column "students.dob" must appear in the GROUP BY clause or be used in an aggregate function
LINE 1: SELECT EXTRACT(YEAR FROM dob) AS birth_year, COUNT(*) AS cou...
                                 ^
uni_db=> SELECT YEAR(date_of_birth) AS birth_year, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY YEAR(date_of_birth)
uni_db-> ORDER BY birth_year;
ERROR:  column "date_of_birth" does not exist
LINE 1: SELECT YEAR(date_of_birth) AS birth_year, COUNT(*) AS count
                    ^
uni_db=> SELECT YEAR(dob) AS birth_year, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY YEAR(dob)
uni_db-> ORDER BY dob;
ERROR:  function year(date) does not exist
LINE 1: SELECT YEAR(dob) AS birth_year, COUNT(*) AS count
               ^
HINT:  No function matches the given name and argument types. You might need to add explicit type casts.
uni_db=> SELECT YEAR(dob) AS birth_year, COUNT(*) AS count FROM students
uni_db-> GROUP BY YEAR(dob) ORDER BY birth_year;
ERROR:  function year(date) does not exist
LINE 1: SELECT YEAR(dob) AS birth_year, COUNT(*) AS count FROM stude...
               ^
HINT:  No function matches the given name and argument types. You might need to add explicit type casts.
uni_db=> SELECT first_name, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY first_name
uni_db-> ORDER BY count DESC, first_name;
 first_name | count
------------+-------
 Charlie    |     1
 Diana      |     1
 eswar      |     1
 Eve        |     1
 Keerthi    |     1
 Robert     |     1
 Sudheshna  |     1
(7 rows)


uni_db=> SELECT EXTRACT(YEAR FROM date_of_birth) AS birth_year, COUNT(*) AS count
uni_db-> FROM students
uni_db-> GROUP BY birth_year
uni_db-> ORDER BY birth_year;
ERROR:  column "date_of_birth" does not exist
LINE 1: SELECT EXTRACT(YEAR FROM date_of_birth) AS birth_year, COUNT...
                                 ^
uni_db=> SELECT EXTRACT(YEAR FROM dob) AS birth_year, COUNT(*) AS count FROM students
uni_db-> GROUP BY birth_year
uni_db-> ORDER BY birth_year;
 birth_year | count
------------+-------
       2001 |     1
       2002 |     1
       2003 |     3
       2004 |     2
(4 rows)


uni_db=> DROP TABLE IF EXISTS students;
DROP TABLE
uni_db=> CREATE TABLE students (
uni_db(>     student_id INTEGER,
uni_db(>     first_name VARCHAR(50) NOT NULL, -- first_name cannot be NULL
uni_db(>     last_name VARCHAR(50) NOT NULL,
uni_db(>     email VARCHAR(100) UNIQUE,      -- email must be unique (and can be NULL by default for UNIQUE)
uni_db(>     dob DATE,
uni_db(>     enrollment_status VARCHAR(10) CHECK (enrollment_status IN ('enrolled', 'graduated', 'dropped'))
uni_db(> );
CREATE TABLE
uni_db=> \d students
                           Table "public.students"
      Column       |          Type          | Collation | Nullable | Default
-------------------+------------------------+-----------+----------+---------
 student_id        | integer                |           |          |
 first_name        | character varying(50)  |           | not null |
 last_name         | character varying(50)  |           | not null |
 email             | character varying(100) |           |          |
 dob               | date                   |           |          |
 enrollment_status | character varying(10)  |           |          |
Indexes:
    "students_email_key" UNIQUE CONSTRAINT, btree (email)
Check constraints:
    "students_enrollment_status_check" CHECK (enrollment_status::text = ANY (ARRAY['enrolled'::character varying, 'graduated'::character varying, 'dropped'::character varying]::text[]))


uni_db=> SELECT * FROM students;
 student_id | first_name | last_name | email | dob | enrollment_status
------------+------------+-----------+-------+-----+-------------------
(0 rows)


uni_db=> SELECT * FROM students
uni_db->
uni_db-> ;
 student_id | first_name | last_name | email | dob | enrollment_status
------------+------------+-----------+-------+-----+-------------------
(0 rows)


uni_db=> INSERT INTO students (student_id, last_name, email, dob) VALUES (1, 'Test', 'test@test.com', '2000-01-01');
ERROR:  null value in column "first_name" of relation "students" violates not-null constraint
DETAIL:  Failing row contains (1, null, Test, test@test.com, 2000-01-01, null).
uni_db=> INSERT INTO students (student_id, last_name, email, date_of_birth)
uni_db-> VALUES (1, 'Test', 'test@test.com', '2000-01-01');
ERROR:  column "date_of_birth" of relation "students" does not exist
LINE 1: ...SERT INTO students (student_id, last_name, email, date_of_bi...
                                                             ^
uni_db=> INSERT INTO students (student_id, last_name, email, dob)
uni_db-> VALUES (1, 'Test', 'test@test.com', '2000-01-01');
ERROR:  null value in column "first_name" of relation "students" violates not-null constraint
DETAIL:  Failing row contains (1, null, Test, test@test.com, 2000-01-01, null).
uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob) VALUES (1, 'Test', 'User', 'test@test.com', '2000-01-01');
INSERT 0 1
uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob) VALUES (2, 'Another', 'User', 'test@test.com', '2001-01-01');
ERROR:  duplicate key value violates unique constraint "students_email_key"
DETAIL:  Key (email)=(test@test.com) already exists.
uni_db=> INSERT INTO students (student_id, first_name, last_name, email, dob, enrollment_status) VALUES (2, 'Another', 'User', 'another@test.com', '2001-01-01', 'pending');
ERROR:  new row for relation "students" violates check constraint "students_enrollment_status_check"
DETAIL:  Failing row contains (2, Another, User, another@test.com, 2001-01-01, pending).
uni_db=> DROP TABLE IF EXISTS students;
DROP TABLE
uni_db=> CREATE TABLE students (
uni_db(>     student_id SERIAL PRIMARY KEY,  -- student_id is now PK, auto-incrementing, NOT NULL
uni_db(>     first_name VARCHAR(50) NOT NULL,
uni_db(>     last_name VARCHAR(50) NOT NULL,
uni_db(>     email VARCHAR(100) UNIQUE,      -- Email should be unique; can be NULL unless NOT NULL is added
uni_db(>     dob DATE,
uni_db(>     enrollment_status VARCHAR(20) CHECK (enrollment_status IN ('enrolled', 'graduated', 'dropped', 'pending'))
uni_db(> );
CREATE TABLE
uni_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
uni_db-> VALUES ('Alice', 'Smith', 'alice.smith@example.com', '2003-05-15', 'enrolled');
INSERT 0 1
uni_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
uni_db-> VALUES ('Robert', 'Johnson', 'robert.j@example.com', '2002-08-22', 'enrolled');
INSERT 0 1
uni_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
uni_db-> VALUES ('Charlie', 'Brown', 'charlie.brown@example.com', '2003-01-10', 'pending');
INSERT 0 1
uni_db=>
uni_db=> SELECT * FROM students;
 student_id | first_name | last_name |           email           |    dob     | enrollment_status
------------+------------+-----------+---------------------------+------------+-------------------
          1 | Alice      | Smith     | alice.smith@example.com   | 2003-05-15 | enrolled
          2 | Robert     | Johnson   | robert.j@example.com      | 2002-08-22 | enrolled
          3 | Charlie    | Brown     | charlie.brown@example.com | 2003-01-10 | pending
(3 rows)


uni_db=> INSERT INTO students (first_name, last_name, dob, enrollment_status)
uni_db-> VALUES ('Dana', 'White', '2004-02-28', 'graduated');
INSERT 0 1
uni_db=> INSERT INTO students (first_name, last_name, email, dob, enrollment_status)
uni_db-> VALUES ('Eve', 'Black', 'alice.smith@example.com', '2004-06-12', 'enrolled');
ERROR:  duplicate key value violates unique constraint "students_email_key"
DETAIL:  Key (email)=(alice.smith@example.com) already exists.
uni_db=> INSERT INTO students (last_name, email, dob, enrollment_status)
uni_db-> VALUES ('Gray', 'eve.gray@example.com', '2004-06-12', 'enrolled');
ERROR:  null value in column "first_name" of relation "students" violates not-null constraint
DETAIL:  Failing row contains (6, null, Gray, eve.gray@example.com, 2004-06-12, enrolled).
uni_db=> CREATE TABLE courses (
uni_db(>     course_id SERIAL PRIMARY KEY,
uni_db(>     course_name VARCHAR(100) NOT NULL UNIQUE,
uni_db(>     credits INTEGER CHECK (credits > 0 AND credits < 10) -- Example of CHECK
uni_db(> );
CREATE TABLE
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Introduction to SQL', 3);
INSERT 0 1
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Database Design', 4);
INSERT 0 1
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Web Development', 3);
INSERT 0 1
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Data Structures', 4);
INSERT 0 1
uni_db=> CREATE TABLE enrollments (
uni_db(>     enrollment_id SERIAL PRIMARY KEY,
uni_db(>     student_id INTEGER NOT NULL,
uni_db(>     course_id INTEGER NOT NULL,
uni_db(>     enrollment_date DATE DEFAULT CURRENT_DATE, -- Sets default if not specified
uni_db(>     grade CHAR(1) CHECK (grade IN ('A', 'B', 'C', 'D', 'F', 'W', NULL)),
uni_db(> CONSTRAINT fk_student
uni_db(>         FOREIGN KEY (student_id)
uni_db(>         REFERENCES students(student_id)
uni_db(>         ON DELETE CASCADE,
uni_db(> CONSTRAINT fk_course
uni_db(>         FOREIGN KEY (course_id)
uni_db(>         REFERENCES courses(course_id)
uni_db(>         ON DELETE RESTRICT,
uni_db(>  UNIQUE (student_id, course_id)
uni_db(> );
CREATE TABLE
uni_db=> -- This will fail if student_id 999 does not exist
uni_db=> INSERT INTO enrollments (student_id, course_id)
uni_db-> VALUES (999, 1);
ERROR:  insert or update on table "enrollments" violates foreign key constraint "fk_student"
DETAIL:  Key (student_id)=(999) is not present in table "students".
uni_db=> -- This will fail if course_id 999 does not exist
uni_db=> INSERT INTO enrollments (student_id, course_id)
uni_db-> VALUES (1, 999);
ERROR:  insert or update on table "enrollments" violates foreign key constraint "fk_course"
DETAIL:  Key (course_id)=(999) is not present in table "courses".
uni_db=> INSERT INTO enrollments (student_id, course_id)
uni_db-> VALUES
uni_db-> (1, 1),
uni_db-> (1, 2);
INSERT 0 2
uni_db=> INSERT INTO enrollments (student_id, course_id, grade) VALUES (1, 1, 'A');
ERROR:  duplicate key value violates unique constraint "enrollments_student_id_course_id_key"
DETAIL:  Key (student_id, course_id)=(1, 1) already exists.
uni_db=> INSERT INTO enrollments (student_id, course_id) VALUES (1, 2); -- Grade will be NULL
ERROR:  duplicate key value violates unique constraint "enrollments_student_id_course_id_key"
DETAIL:  Key (student_id, course_id)=(1, 2) already exists.
uni_db=> INSERT INTO enrollments (student_id, course_id, grade) VALUES (2, 1, 'B');
INSERT 0 1
uni_db=> INSERT INTO enrollments (student_id, course_id, grade) VALUES (1, 1, 'A');
ERROR:  duplicate key value violates unique constraint "enrollments_student_id_course_id_key"
DETAIL:  Key (student_id, course_id)=(1, 1) already exists.
uni_db=>

Activity 4:
    -update Charlie Brown's date of birth to '2003-02-15'. Then, they update the email for the student with student_id = 4 (Diana Prince) to 'diana.prince@example.org'.
<img width="378" alt="image" src="https://github.com/user-attachments/assets/0821a9e4-eefb-43b4-b276-c35dacfcc802" />
    -Students add a new temporary student with student_id = 100, then write a DELETE statement to remove that student.
![image](https://github.com/user-attachments/assets/68a05b83-ffba-4444-8e66-dd7edd5e29a3)
    - List all students ordered by their date of birth, oldest first.
    - List all students ordered by last name descending, then by first name ascending.
<img width="454" alt="image" src="https://github.com/user-attachments/assets/8d2d3d44-9e8c-41f1-990b-dacad4d38ca4" />
    - Find the two students who were born earliest (oldest two).
    - List students, skipping the first one and showing the next two, ordered by `student_id`.
<img width="439" alt="image" src="https://github.com/user-attachments/assets/5854ba71-32b9-4e48-bafd-1f5bd963f601" />
    -Get a list of unique birth years from the students table. (Hint: You might need a function to extract the year first, or realize DISTINCT dob is different from distinct 
     birth years if times were involved). For simplicity, let's aim for SELECT DISTINCT dob FROM students ORDER BY dob; and discuss how to get just years later.
<img width="419" alt="image" src="https://github.com/user-attachments/assets/6fab8f8f-9561-4f6a-ba53-3815bd26c0e6" />
    - Count how many students are in the `students` table.
    - Find the earliest (minimum) date of birth.
    - Count how many distinct last names there are.
<img width="440" alt="image" src="https://github.com/user-attachments/assets/0b92e87f-fa59-41de-928c-c975b5ffd1b6" />
    - Count the number of students for each distinct first`_name`.
    - Find the number of students born in each year.
<img width="480" alt="image" src="https://github.com/user-attachments/assets/079dc99c-239c-4fff-91ef-7d98e31ec32c" />
     - Students re-create the students table with NOT NULL on first_name and last_name, and UNIQUE on email. They then try to insert data that violates these constraints to see the errors.
<img width="599" alt="image" src="https://github.com/user-attachments/assets/132f5f4e-5f8f-4572-86b6-8f29637ebf64" />
<img width="947" alt="image" src="https://github.com/user-attachments/assets/f1f7c392-b448-4a66-8c94-36bf35e9b6b1" />
Activity 5 :  recreate the `students` table with `student_id SERIAL PRIMARY KEY` and other constraints. They re-insert the data and observe the auto-generated `student_id`.
    - Try inserting a student without an email. (Should work if `UNIQUE` constraint on email allows NULLs, which it does by default).
    - Try inserting a student with a duplicate email to one already existing. (Should fail due to `UNIQUE` constraint).
    - Try inserting a student with a `NULL` first name. (Should fail due to `NOT NULL` constraint).
![Screenshot (29)](https://github.com/user-attachments/assets/611f8ba7-4dda-4d3e-ae29-4b81eb6ab1dc)
    1. Students create the `courses` table and insert the sample data.
    2. Students create the `enrollments` table with the foreign keys and other constraints.
    3. Try to insert an enrollment for a `student_id` that doesn't exist in `students` (e.g., student_id 999). *It should fail due to FK constraint.*
    4. Try to insert an enrollment for a `course_id` that doesn't exist in `courses`. *It should fail.*
    5. Enroll 'Alice Smith' (assume her `student_id` is 1) in 'Introduction to SQL' (assume `course_id` is 1) and 'Database Design' (assume `course_id` is 2).
uni_db=> CREATE TABLE courses (
uni_db(>     course_id SERIAL PRIMARY KEY,
uni_db(>     course_name VARCHAR(100) NOT NULL UNIQUE,
uni_db(>     credits INTEGER CHECK (credits > 0 AND credits < 10) -- Example of CHECK
uni_db(> );
CREATE TABLE
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Introduction to SQL', 3);
INSERT 0 1
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Database Design', 4);
INSERT 0 1
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Web Development', 3);
INSERT 0 1
uni_db=> INSERT INTO courses (course_name, credits) VALUES ('Data Structures', 4);
INSERT 0 1
uni_db=> CREATE TABLE enrollments (
uni_db(>     enrollment_id SERIAL PRIMARY KEY,
uni_db(>     student_id INTEGER NOT NULL,
uni_db(>     course_id INTEGER NOT NULL,
uni_db(>     enrollment_date DATE DEFAULT CURRENT_DATE, -- Sets default if not specified
uni_db(>     grade CHAR(1) CHECK (grade IN ('A', 'B', 'C', 'D', 'F', 'W', NULL)),
uni_db(> CONSTRAINT fk_student
uni_db(>         FOREIGN KEY (student_id)
uni_db(>         REFERENCES students(student_id)
uni_db(>         ON DELETE CASCADE,
uni_db(> CONSTRAINT fk_course
uni_db(>         FOREIGN KEY (course_id)
uni_db(>         REFERENCES courses(course_id)
uni_db(>         ON DELETE RESTRICT,
uni_db(>  UNIQUE (student_id, course_id)
uni_db(> );
CREATE TABLE
uni_db=> -- This will fail if student_id 999 does not exist
uni_db=> INSERT INTO enrollments (student_id, course_id)
uni_db-> VALUES (999, 1);
ERROR:  insert or update on table "enrollments" violates foreign key constraint "fk_student"
DETAIL:  Key (student_id)=(999) is not present in table "students".
uni_db=> -- This will fail if course_id 999 does not exist
uni_db=> INSERT INTO enrollments (student_id, course_id)
uni_db-> VALUES (1, 999);
ERROR:  insert or update on table "enrollments" violates foreign key constraint "fk_course"
DETAIL:  Key (course_id)=(999) is not present in table "courses".
uni_db=> INSERT INTO enrollments (student_id, course_id)
uni_db-> VALUES
uni_db-> (1, 1),
uni_db-> (1, 2);
INSERT 0 2
</pre>
