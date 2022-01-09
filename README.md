

# DATABASE
## What is database?
Any collection of related information like phonebook , shopinglist etc.    
Database can be stored in different ways like on paper,on a computer etc.
## Database management system(DBMS)
A special software program that helps user to create and maintain a database.
- makes it easy to manage large amount of data.
- Handles security
- Backups
### Major operations of DBMS
- Create
- Read/Retrieve
- Update
- Delete
## Two types of database
1. Relational database(SQL)
2. Non-relational database (No sql/not just sql)
### Relational database
RDMS help user to create and maintain a relational database. Mysql,oracle,postgrade,mariadb etc.
- organize data into one row or more table.
- Each row has row and column.
- A unique key identifies each row.
### Non-relational database
NRDBMS help user tto create and maintain a non-relational database. mongodb,dynamodm,apache etc. 

Organize data in anything but a traditional table.

=> key:value store

### Implementaion specific
Most NRDBMS will implemented there own language for performing C.R.U.D and administrative operations on database.
## Structure Query Language(SQL)
- Standaridized language for interacting with database.
- Used to performe C.R.U.D operation as well as other administrative tasks.
 
Sql is a actually a hybrid language.Its basically 4 typess of language in one.
### Data Query language(DQL)
- used a query the database for information.
### Data Defination language(DDL)
- used for defining database schemas.
### Data Conttrol language(DCL)
- used for controlling access the data in the database.
### Data Manipulation language(DML)
- used foe inserting,updating and deleting data from the database.

## TABLES AND KEYS

| Student-id | Name | Major |
| -------- | ---- |------ |
| 1  | sanny | ECE |
| 2  | sunny | Biology |
|3     |Rahul | CSe |
### COLUMN
Column is defined a single attribute.
### Row
In row which a horizontal entry which represent a single student or entry.
### Primary key
Its basically a attribute which primary defines the row in the database.
### Surgate key
It is primary key that has not mapping ato real world.
### Natural ley
It is primary key that has  mapping ato real world.
##3 Foregin key
It is basically a attribute that we can store on a database table that will link us to another database table.
### Coposite key
when primary key consist of two column is called composite key.
## Common database used in SQL
| INT| whole number |
| ------------- | ------------- |
| DECIMAL(M,N)  | Decimal numbers - Exact Value |
| VARCHAR(I)  | string of text of length l |
| BLOB      | Binary large object,stores large data |
| DATE | YYYY-MM-DD |
| TIMESTAMP  | YYYY-MM-DD  HH:MM:SS |
# CREATE TABLE
    CREATE TABLE student (
    student-id INT PRIMARY KEY,
    Name VARCHAR(20),
    MAJOR VRCHAR(20),
    );
    DESCRIBE student;
    DROP TABEL student;                         //delete tha tabel
    ALTER TABEL tb_name ADD (anything);         //modify tabel
    ALTER TABEL tb_name DROP row\coumn_name;    // remove row/column on modify tabel
    
   # INSERT DATA INTO TABEL
    INSERT INTO tb_name VALUES(value1 , value2 , ....)
    INSERT INTO tb_name VALUES(value1 , value2 , ....)
 
 # CONSTRAINTS
 - NOT null - Ensure that a column cannot have a null value.
 - UNIQUE - Ensure that a column are different. 
 - PRIMARY KEY - A combination of a NOT NULL and UNIQUE.uniquely identify each row in a column.
 - CHECK - Ensures that value in a column satisfy a certain condition.
 - FOREIGN KEY - It links the relationship between tabel.
 # UPDATE AND DELETE
        -  UPDATE tb_name 
           SET  major = "biology"  
          WHERE major = "sociology"     //update the tabel
        
        
     -  DELETE FROM tb_name
        WHERE major = "sociology"   //delete thr tabel
 # Basic queries
      -  SELECT*FROM tb-name
       
      - SELECT name, major
        FROM student(tb-name)
        ORDER BY major DEsc;
       
       
        - SELECT name, major
          FROM student(tb-name)
          ORDER BY student-id DESC;
          LIMIT 2;
 # SQL OPERATORS
| =    | Equal to |
| ---      | ---       |
| > |  Greater than        |
| <  | Less than        |
| >= |  Greater than equal t0       |
| <=  | Less than equal to       |
|  <> | Not equat to        |

# FUNCTIONS
- SELECT COUNT FROM employee;
- SELECT AVG(salary) FROM employee;
- SELECT SUM(salary) FROM employee;
- SELECT MAX(salary) FROM employee;
# WILDCARDS
There are two wildcard used in conjuction with the like operator.
- (%)  It represent zero , one or multiple operator.
- ( _ )  It represent only sibgle caracter.

| WHERE name LIKE "a%"| Find any values that starts with "a" |
| ------------- | ------------- |
| WHERE name LIKE "%a"  | Find any values that ends with "a" |
| WHERE name LIKE "%or%"  | Find any values that have or in any position |
| WHERE name LIKE "a_%"     | Find any values that starts with "a" and are at least 2 character in length |
| WHERE name LIKE "a%o" | Find any values that starts with "a" and ends with o |
# UNIONS
Find a list of all client and branch supplier

      SELECT client_name
      FROM client
      UNION
      SELECT supplier_name
      FROM branch-suppier
# JOINTS
It is used to join two table or combine rows from two or more tabe.
## INNER JOIN
Returns rows where there is match in both tabel.
    
    SELECT column_name
    FROM table1
    INNER JOIN table2
    ON table1.column_name = table2.columnn_name;
## LEFT OUTER JOIN
Returns all rows from the left tabel even there are no matches in right tabel.

      SELECT column_name
      FROM table1
      LEFT JOIN table2
     ON table1.column_name = table2.columnn_name;
## RIGHT OUTER JOIN
Returns all rows from the right tabel even there are no matches in left tabel.

    SELECT column_name
    FROM table1
    RIGHT JOIN table2
    ON table1.column_name = table2.columnn_name;
## FULL OUTER JOIN
Returns rows where there is match in one of the tabel.
  
    SELECT column_name
    FROM table1
    FULL OUTER JOIN table2
    ON table1.column_name = table2.columnn_name;
# NESTED QUERIES
It is used a multiple selest statement in order to get a specific piece pf information






