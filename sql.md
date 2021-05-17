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

## SQL AGGREAGATE FUNCTIONS
* Aggregate functions take multiple rows from the table and return a value according to the query.
* All the aggregate functions are used in Select statement.


Syntax - 
```sql    
SELECT <FUNCTION NAME> (<PARAMETER>) FROM <TABLE NAME>
```

**AVG Function :**
This function returns the average value of the numeric column that is supplied as a parameter.

><B>Example:</B> Write a query to select average salary from employee table.

```sql
Select AVG(salary) from Employee
```

**COUNT Function :**   The count function returns the number of rows in the result. It does not count the null values.

><B>Example:</B> Write a query to return number of rows where salary > 20000.

```sql
Select COUNT(*) from Employee where Salary > 20000;
```

#### Types:
* COUNT(*): Counts all the number of rows of the table including null.

* COUNT( COLUMN_NAME): count number of non-null values in column.

* COUNT( DISTINCT COLUMN_NAME): count number of distinct values in a column.

**MAX FUNCTION :**
The MAX function is used to find maximum value in the column that is supplied as a parameter. It can be used on any type of data.

><B>Example − </B> Write a query to find the maximum salary in employee table.
```sql
Select MAX(salary) from Employee
```
**SUM Function :**
This function sums up the values in the column supplied as a parameter.

><B>Example:</B> Write a query to get the total salary of employees.
```sql
Select SUM(salary) from Employee
```

**STDDEV Function:**
The STDDEV function is used to find standard deviation of the column specified as argument.

><B>Example − </B> Write a query to find standard deviation of salary in Employee table.
```sql
Select STDDEV(salary) from Employee
```
**VARIANCE Function:**
The VARIANCE Function is used to find variance of the column specified as argument.

><B>Example −</B>
```sql

Select VARIANCE(salary) from Employee
```




## SQL JOINS
<p>
A SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are:
</p>

  * INNER JOIN
  * LEFT JOIN
  * RIGHT JOIN
  * FULL JOIN
  
  consider two tables below:

#### Students:
            
![tables](https://media.geeksforgeeks.org/wp-content/cdn-uploads/table1-3.png)

#### StudentCourse:

![tables](https://media.geeksforgeeks.org/wp-content/uploads/table5.png)

<B>1. INNER JOIN:</B>The INNER JOIN keyword selects all rows from both the tables as long as the condition satisfies. This keyword will create the result-set by combining all rows from both the tables where the condition satisfies i.e value of the common field will be same.

![INNER join images](https://www.w3schools.com/sql/img_innerjoin.gif)


##### Syntax:

```sql
SELECT StudentCourse.COURSE_ID, Student.NAME, Student.AGE FROM Student
INNER JOIN StudentCourse
ON Student.ROLL_NO = StudentCourse.ROLL_NO;
```

#### output:
![output](https://media.geeksforgeeks.org/wp-content/uploads/table22.png)

<B>2.LEFT JOIN:</B>This join returns all the rows of the table on the left side of the join and matching rows for the table on the right side of join. The rows for which there is no matching row on right side, the result-set will contain null. LEFT JOIN is also known as LEFT OUTER JOIN.

![LEFT join](https://www.w3schools.com/sql/img_leftjoin.gif)

#### Syntax:
```sql
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
LEFT JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
```
#### output:
![output](https://media.geeksforgeeks.org/wp-content/uploads/table31.png)

<B>3.RIGHT JOIN:</B> RIGHT JOIN is similar to LEFT JOIN. This join returns all the rows of the table on the right side of the join and matching rows for the table on the left side of join. The rows for which there is no matching row on left side, the result-set will contain null. RIGHT JOIN is also known as RIGHT OUTER JOIN.

![Rigth Join](https://www.w3schools.com/sql/img_rightjoin.gif)

#### Syntax:
```sql
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
RIGHT JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
```
#### Output:
![Right Table](https://media.geeksforgeeks.org/wp-content/uploads/table6.png)

<B>4. FULL JOIN:</B> FULL JOIN creates the result-set by combining result of both LEFT JOIN and RIGHT JOIN. The result-set will contain all the rows from both the tables. The rows for which there is no matching, the result-set will contain NULL values.


![FULL OUTER join](https://www.w3schools.com/sql/img_fulljoin.gif)

#### Syntax:
```sql
SELECT Student.NAME,StudentCourse.COURSE_ID 
FROM Student
FULL JOIN StudentCourse 
ON StudentCourse.ROLL_NO = Student.ROLL_NO;
```
#### Output:
![output](https://media.geeksforgeeks.org/wp-content/uploads/table7.png)



<u>References </u>:

[1.SQL Tutorialspoint](https://www.tutorialspoint.com/sql/index.htm)

[2.Artical in geekforgeeks](https://www.geeksforgeeks.org/sql-join-set-1-inner-left-right-and-full-joins/)


