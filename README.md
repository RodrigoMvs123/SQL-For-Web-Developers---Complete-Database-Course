# SQL-For-Web-Developers---Complete-Database-Course

https://www.youtube.com/watch?v=KBDSJU3cGkc

https://raw.githubusercontent.com/RodrigoMvs123/SQL-For-Web-Developers---Complete-Database-Course/main/README.md



https://github.com/bootdotdev/fcc-learn-sql-assets 

Introduction to SQL ( Structured Query Language ) 

What is SQL ?
Structured query language, or SQL is the primary programming language used to manage and interact with relational databases. SQL can perform various operations such as creating, updating, reading and deleting record within a database.

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * from users;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT name, balance FROM users;


Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT id, name, is_admin FROM users;

SQL Databases
PostgreSQL
MySQL
SQLite
SQL Server
Oracle
Cockroach DB

NoSQL Databases 
Mongo DB
Redis
ElasticSearch
Firebase
Dynamo DB

Types of noSQL Databases
Document Database
Key-Value Store
Wide-Column
Graph

Questions 
1 - Each NoSQL Database tends to use different query language(s).
NoSQL
2- SQL compatible databases tend to be more similar in their functionality than NoSQL databases.
SQL and NoSQL
3- Which type of database always uses table structures ?
SQL

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE users (id INTEGER, name TEXT, age INTEGER);
INSERT into users (id, name, age) values (1,'John Doe', 21);
INSERT into users (id, name, age) values (2, 'Montgomery Burns', 33);
SELECT * FROM users;

Tables

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE people(
    id INTEGER;
    handle TEXT;
    name TEXT;
    age INTEGER;
    balance INTEGER;
    is_admin BOOLEAN
);

# TEST SUIT, DO NOT TOUCH BELOW THIS LINE 

program table_info('people');

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
ALTER TABLE people RENAME to users;

ALTER TABLE users RENAME COLUMN handle to username;

ALTER TABLE users ADD COLUMN password TEXT;

# TEST SUIT, DO NOT TOUCH BELOW THIS LINE 

program table_info('people');

Questions
1 - Which of the following statements about migrations is FALSE ?
You can be fast and loose when writing migrations - a bed migration is easy to fix.
2 - Will database migrations often be coupled with application code updates ?
Yes
3 - Why are “good” migrations written in a reversible manner ?
So that if something goes wrong the changes can be rolled…

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
ALTER TABLE transactions
    ADD COLUMN was_successeful BOOLEAN;

ALTER TABLE transactions 
    ADD COLUMN transaction_type TEXT;

# TEST SUIT, DO NOT TOUCH BELOW THIS LINE 

program table_info('people');

Questions
1 - How is a “true” boolean value stored and presented in SQLite ?
1.
2 - All SQL databases support the same data types ?
False.
3 - What type would you use to store a user's email ?
Text.

Constraints 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql

CREATE TABLE users(
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    age INTEGER NOT NULL,
    country_code TEXT NOT NULL,
    username TEXT UNIQUE,
    password TEXT NOT NULL,
    is_admin BOOLEAN
);

# TEST SUIT, DO NOT TOUCH BELOW THIS LINE 

program table_info('people');

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
INSERT into users (
    id, 
    name,
    age,
    username,
    password,
    is_admin
) values (
    0,
    "Rudolf",
    33,
    "rudolf1234",
    "thisisnotsecure",
    false
);

INSERT into users (
    id, 
    name,
    age,
    username,
    password,
    is_admin
) values (
    1,
    "Jerry",
    25,
    "jerrysmith"
    "mypasswordis1234",
    true
);

program table_info('people');

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
INSERT into users (
    id, 
    name,
   country_code 
) values (
    0,
    "Jerry",
    "US"
);

INSERT into users (
    id, 
    name,
    country_code 
) values (
    1,
    "Amit",
    "IN"
);

program table_info('people');

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE transactions(
    id INTEGER PRIMARY KEY,
    sender_id INTEGER,
    recipient_id INTEGER,
    memo TEXT NOT NULL,
    amount INTEGER NOT NULL,
    balance INTEGER NOT NULL
);

program table_info('transactions');

Questions
1 - How many courses is Sam enrolled in ?
3.
2 - How many students are in the MongoDB course ?
3.
3 - Relational databases typically do not duplicate data, while non-relational databases more often do duplicate data.
Do not, do.
4 - Non relational databases connect similar entities by using 
Nested data.

CRUD 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
INSERT INTO users
    (id, name, age, country_code, username, password, is_admin)
    VALUES 
    (1, "David", 34, "US", "DavidDev", "InsertPractice", false);

INSERT INTO users
    (id, name, age, country_code, username, password, is_admin)
    VALUES 
    (2, "Samantha", 29, "BR", "Sammy93", "addingRecords!", false);


SELECT * FROM users;

Questions 
1 - A front-end typically communicates with a database directly to add new records.
False
2 - The “Create” in CRUD maps to which SQL statement and HTTP Method ?
Inset, Post

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
INSERT INTO users
    (name, age, country_code, usernamen, password, is_admin)
    VALUES
    ("Lance", 20, "US", "LanChr", "b00tdevisbest", false);

INSERT INTO users
    (name, age, country_code, usernamen, password, is_admin)
    VALUES
    ("Tiffany", 28, "US", "Tifferoon", "autoincrement", true);

SELECT * FROM users;

Questions 
1 - Every time someone creates an account on boot.dev Allan or Lane has to manually add them to the database by hand-writing a SQL query.
False
2 - Within backend systems, SQL queries are typically 
Generated by code

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT count(*) FROM users;

Questions 
1 - The HTTP Method that generally corresponds with a SQL SELECT statement is an HTTP ?
Get
2 - Which happens first ?
A GET request is made


Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT username FROM users WHERE is_admin=true;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM transactions WHERE sender_id IS NOT NULL;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
DELETE FROM users WHERE id=2;

SELECT * from users;

Questions 
1 - You should have automated backups being taken of a production database
Almost always 
2 - A soft-delete is where you ?
Mark a row as deleted instead of actually removing the data

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
UPDATE users
     SET is_admin=TRUE
     WHERE id=9;

SELECT * from users where id = 9;

Questions 
1 - When using an ORM, you 
Call methods and functions made available via the ORM´s API
2 - One advantage of an ORM is that it …
Makes your code less verbose 
3 - Should you use an ORM ?
It depends on the project/team

Basic Queries 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT amount, note AS birthday_message 
     FROM transacions WHERE sender_id=10;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT *,
     IIF(was_successeful, "No actions required", "Perform an audit") AS audit 
     FROM transactions;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT name, age FROM users
     WHERE age BETWEEN 18 AND 30;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT DISTINCT country_code FROM users;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM users
     WHERE country_code = "CA"
     AND age < 18;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT count(*) FROM users
     WHERE (country_code="US" OR country_code"CA")
     AND age < 18;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT name, age, country_code
     FROM users WHERE 
     country_code IN ('US', 'CA', 'MX');
     

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM users
     WHERE name lIKE 'Al%';

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM users
     WHERE name LIKE 'Al___';

Questions 
1 - Which describe the values that match example 1 ?
Values that start with ‘or’, and are at least 3 characters in length 
2 - Which would not match example 2 ?
Singing

Structuring 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * from transactions 
     WHERE note LIKE '%lunch';
     LIMIT 5;

Questions 
1 - ‘LIMIT 5’ will always return 5 records ?
False
2 - Why might you use a LIMIT clause ?
To avoid selecting a huge amount of data and causing strain on the system 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM transactions 
     WHERE amount BETWEEN 10 and 80
     ORDER by amount DESC;

Questions 
1 - Example 1 is sorted in DESC order
DESC
2 - Witch query would potentially return the data in example 1 ?
SELECT * from people ORDER BY age 
DESC

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM transactions
WHERE amount BETWEEN 10 and 80
ORDER BY amount DESC
LIMIT 4;

Aggregations 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT count(*) FROM transactions 
     WHERE user_id=6
     AND was_successful = true; 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT sum(amount) FROM transactions
     WHERE user_id=9;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT max(amount), user_id FROM transactions
     WHERE user_id=4;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT min(age) FROM users
     WHERE country_code="US";
     
Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT user_id, sum(amount) AS balance
     FROM transactions
     GROUP BY user_id;

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT avg(age) FROM users WHERE country_code="US";

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT sender_id, sum(amount) AS balance FROM transactions
     WHERE note LIKE '%lunch%'
     GROUP BY sender_id
     HAVING balance > 20
     ORDER BY balance ASC;

Questions 
1 - In the example, should you user a WHERE or a HAVING clause to filter down to a specific class_id ? 
WHERE
2 - In the example, should you use a WHERE or a HAVING clause to filter down classes  of a particular size ?
Having 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT round(avg(age)) AS round_age
FROM users
WHERE country_code='US';

Subqueries 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM transactions
     WHERE user_id = (
          SELECT id FROM users
          WHEN name="David"
     );

Questions
1 - A subquery …
Allows you to query the result set of a nested query 
2 - The example will return row(s)
Potentially many 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT * FROM users
     WHERE age_in_days > (40 * 365);

Questions 
1 - SQL can only operate on data stored in tables ?
False

Normalization 

Questions
1 - Which is an example of a one-to-one relationship ?
A transaction´s ‘note’
2- How would you model the relationship between a class and its name ?
One to one 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE users (
     id INTEGER PRIMARY KEY,
     name TEXT NOT NULL,
     age INTEGER NOT NULL,
     username TEXT UNIQUE,
     password TEXT NOT NULL,
     is_admin BOOLEAN
);

CREATE TABLE countries (
     id INTEGER PRIMARY KEY,
     country_code TEXT,
     name TEXT,
     user_id INTEGER,
     FOREIGN KEY (user_id)
     REFERENCES users(id)
);

INSERT INTO users (name, age, username, password, is_admin)
…

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE users (
     id INTEGER PRIMARY KEY,
     name TEXT NOT NULL,
     age INTEGER NOT NULL,
     username TEXT UNIQUE,
     password TEXT NOT NULL,
     is_admin BOOLEAN
);

CREATE TABLE countries (
     id INTEGER PRIMARY KEY,
     country_code TEXT,
     name TEXT
);

CREATE TABLE users_country (
     country_id INTEGER,
     user_id INTEGER,
     UNIQUE (country_id, user_id)
);

INSERT INTO users (name, age, username, password, is_admin)
…

Questions 
1 - To improve data integrity, data should generally be stored in a raw form
 Raw
2 - Pick the best example of data redundancy 
A users address is stored in two different tables
3 - Which form has the most duplicate data?
1 NF ( Normal Form ) 
4 - Which form encourages the most accurate and up-to-date information ?
Boyce-Codd normal form
5 - In the context of normalization, a primary key is made up of 1-many table columns
1-many 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE companies (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    num_employees INTEGER NOT NULL
);

pragma table_info('companies');

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    age INTEGER NOT NULL
);

CREATE TABLE companies (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    num_employees INTEGER NOT NULL,
    company_revenue INTEGER
);

CREATE TABLE users_companies (
    user_id INTEGER,
    company_id INTEGER, 
    UNIQUE(user_id, comapany_id)
);

…


Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE companies (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    num_employees INTEGER NOT NULL
);

...

SELECT *, IIF(num_employess > 100, "large", "small") AS size
    FROM companies;

Questions 
1 - When can a table be in 3NF but not BCNF ?
It has multiple possible primary key combinations, and one of the columns in a possible primary key is dependent on a column outside of the primary key
2 - Which should you optimize for first ?
Reducing duplicate data
3 - When you do not need a composite key, what should the name of your primary key´s column be ?
Id
4 - Which is more important for your career in back-end development ?
Internalizing simple rules-of-thumb regarding database normalization 

Joins 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT users.name, users.age, countries.name AS country_code
FROM users
INNER JOIN countries on countries.country_code = users.country_code;
ORDER BY country_name ASC;


Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT users.name
    sum(transactions.amount) as sum,
    count(transactions.id) as count
    FROM users
    LEFT JOIN transactions
    ON users.id = transactions.user_id
    GROUP BY users.id
    ORDER BY sum DESC; 

Questions
1 - We can retrieve the same records with a RIGHT JOIN and a LEFT JOIN by…
Flipping the position os the tables in the joy statement 
2 - Select the best scenario to use a FULL JOIN ?
When you need every single row from two tables, whether or not they are related
3 - Given the tables and query, which JOIN type would produce the result ?
Left JOIN


Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
SELECT users.id, users.name, users.age, 
    users.username, countries.name as country_name,
    sum(transactions.amount) as balance 
    FROM users 
    LEFT JOIN countries on users.country_code = countries.country_code
    LEFT JOIN transactions on transactions.user_id = users.id 
    WHERE users.id = 6 
    GROUP BY users.id;

Performance 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    email TEXT,
    name TEXT,
    age INTEGER
);   

CREATE INDEX email_idx on users(email); 

SELECT name 
FROM sqlite_master
WHERE type = 'index';

Questions
1 - A binary-tree index makes lookups…
O(log(n))
2 - Add indexes to…
Columns that you frequently perform lookups
3 - Indexes slow down…
Write speed 

Visual Studio Code
EXPLORER 
OPEN EDITORS
Cashpal.sql

Cashpal.sql
CREATE TABLE transactions (
    id   INTEGER PRIMARY KEY,
    user_id INTEGER,
    recipient_id INTEGER   ,
    sender_id INTEGER,
    amount INTEGER
);   

CREATE INDEX 
    user_id_recipient_id_idx  
    ON transactions (user_id, recipient_id);

SELECT type, name, tbl_name
FROM sqlite_master
WHERE type = 'index';

Questions 
1 - Denormalizing a database can be used to…
Speed up the queries 
2 - It is smart to start with a normalized database and denormalized it as needed for speed.
Normalized and Denormalized
3 - A normalized database is easier to keep bug-free
Normalized
4 - SQL injections is best avoided by using a modem SQL package that handles a sanitization of user-provided values
True
5 - What happened in the comic ?
Every student´s data in that School´s database was deleted 
 
