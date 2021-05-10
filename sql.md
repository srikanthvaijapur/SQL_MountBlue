![sql logo](https://blog.stoneriverelearning.com/wp-content/uploads/2016/02/Introduction-to-SQL.png)
># SQL OVERVIEW
* SQL is a language to operate databases; it includes database creation, deletion, fetching
rows, modifying rows, etc. 
* SQL is an <b>ANSI</b> (American National Standards Institute)
standard language, but there are many different versions of the SQL language.



### 1. What is SQL?
<p>
SQL is Structured Query Language, which is a computer language for storing, manipulating
and retrieving data stored in a relational database.
<br></br>
SQL is the standard language for Relational Database System. All the Relational Database
Management Systems (RDMS) like MySQL, MS Access, Oracle, Sybase, Informix, Postgres
and SQL Server use SQL as their standard database language.
<br></br>
</p>

### 2. Why SQL?
SQL is widely popular because it offers the following advantages:
* Allows users to access data in the relational database management systems.
* Allows users to describe the data
* Allows users to define the data in a database and manipulate that data.
* Allows users to create and drop databases and tables
* Allows users to set permissions on tables, procedures and views.

### 3.SQL Commands 

<p>The standard SQL commands to interact with relational databases are <B>CREATE, SELECT,
INSERT, UPDATE, DELETE and DROP. </B><br>
These commands can be classified into the following
groups based on their nature:</p>


|
>#### DDL - Data Defination Language
| Command |Description|
|----------|----------|
| CREATE|Creates a new table, a view of a table, or other object in the database.|
| ALTER |Modifies an existing database object, such as a table.|
| DROP |Deletes an entire table, a view of a table or other objects in the database.|
>#### DML - Data Manipulation LANGUAGE
| Command | Description |
|--------|-------------|
|SELECT |Retrieves certain records from one or more tables.|
|INSERT|Creates a Record|
|UPDATE|Modifies the Data|
|Delete|Delete records|

>#### DCL - Data Control Language
|Command | Description |
|--------|-------------|
|GRANT|Gives a previliage to user|
|REVOKE|Takes back privilage granted for user

## SQL AGGRIGATIONS
* Aggregate functions take multiple rows from the table and return a value according to the query.
* All the aggregate functions are used in Select statement.

Syntax - 
    
    SELECT <FUNCTION NAME> (<PARAMETER>) FROM <TABLE NAME>
> **AVG Function**
This function returns the average value of the numeric column that is supplied as a parameter.

Example: Write a query to select average salary from employee table.

```Select AVG(salary) from Employee```
> **COUNT Function**The count function returns the number of rows in the result. It does not count the null values.

Example: Write a query to return number of rows where salary > 20000.
```Select COUNT(*) from Employee where Salary > 20000;```

>#### Some of the Aggrigation functions are "<u>MAX,SUM,VARIANCE </u> etc..



## SQL JOINS
<p>
A SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are:
</p>


>* INNER JOIN: Returns records that have matching values in both tables
>* LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
>* RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
>* FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table
![INNER join images](https://www.w3schools.com/sql/img_innerjoin.gif)
![LEFT join](https://www.w3schools.com/sql/img_leftjoin.gif)
![Rigth Join](https://www.w3schools.com/sql/img_rightjoin.gif)
![FULL OUTER join](https://www.w3schools.com/sql/img_fulljoin.gif)





<u>References </u>:

[1.SQL Tutorialspoint](https://www.tutorialspoint.com/sql/index.htm)

[2.Artical in geekforgeeks](https://www.geeksforgeeks.org/sql-join-set-1-inner-left-right-and-full-joins/)
