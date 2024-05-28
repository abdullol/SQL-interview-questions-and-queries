My Chat gpt rules :-
make its html for readme file on github
give h4 heading to line starting from $
give paragraph to line starting from %
give code script to line starting from #
wrap code around pre tag

https://www.youtube.com/watch?v=1idbrEwuh8w&list=PLysly0KYnAY08stX1R_xDayz-jlALgfAg&ab_channel=IshwarAcademy
* Views
* Temp Table
* Distinct 


<h3>SQL Concepts</h3>

<h4>Create Database</h4>
<p>Command to create database</p>
<pre><code>CREATE DATABASE Db_Concepts;</code></pre>

<h4>Datatypes</h4>
<ul>
  <li>int</li>
  <li>datetime</li>
  <li>decimal</li>
  <li>float</li>
  <li>date</li>
  <li>time</li>
  <li>bit</li>
</ul>

<p>SQL also has several character data types:</p>
<ul>
  <li>Char: A fixed-length datatype that will store a fixed number of characters, even if the input data is shorter.</li>
  <li>VarChar: A variable-length datatype that will store the input data as-is, without padding any extra space.</li>
  <li>nChar: A Unicode character datatype that can store multiple languages.</li>
  <li>nVarChar: A Unicode variable-length character datatype that can store multiple languages.</li>
</ul>

<h4>Integrity Constraint</h4>
<p>A set of rules to ensure that data integrity is not affected while CRUD</p>
<ul>
  <li>Unique</li>
  <li>NOT NULL</li>
  <li>Primary Key</li>
  <li>Foreign Key</li>
  <li>Default</li>
  <li>Check</li>
</ul>

<h4>SQL Statements</h4>
<p>There are two types of SQL statements:</p>
<ul>
  <li>DDL Statments (data definition): Used to modify or create the Object structure (database, table, views, structure) commands are (Create, Alter, Drop, Truncate, Rename)</li>
  <li>DML Statments (data manipulation): Used to insert, modify, retrieve, remove data from table commands are (Insert, Update, Delete, Select)</li>
</ul>

<h4>Create Command</h4>
<p>The following SQL command creates a table called <code>Employee_Info</code> with columns <code>empId</code>, <code>empName</code>, <code>empSalary</code>, <code>job</code>, <code>phone</code>, and <code>deptId</code>. The <code>empId</code> column is set as the primary key, <code>empName</code> and <code>empSalary</code> columns are set as <code>NOT NULL</code>, and the <code>deptId</code> column is set as <code>NOT NULL</code>.</p>
<pre><code>CREATE TABLE Employee_Info(
    empId INT PRIMARY KEY,
    empName VARCHAR(20) NOT NULL,
    empSalary DECIMAL(10, 2) NOT NULL,
    job VARCHAR(20),
    phone VARCHAR(50),
    deptId INT NOT NULL
)
</code></pre>

<h4>INSERT Command</h4>
<p>This command is used to insert new data into a table.</p>
<pre><code>INSERT INTO Employee_Info
VALUES ('Adam', 20000, 'Developer', 101190, 10)</code></pre>
<p>If you want to insert data into specific columns, you can use this syntax:</p>
<pre><code>INSERT INTO Employee_Info (empId, empName, empSalary, job, phone, deptId) VALUES
('Adam', 20000, 'Developer', 101190, 10)</code></pre>

<h4>Select Command</h4>
<p>To retrieve information from the database, you can use the SELECT command:</p>
<pre><code>SELECT * / [COLUMN_NAME] [FUNCTION_NAME] FROM TABLE_NAME
[WHERE condition]
[GROUP BY condition]
[HAVING condition]
[ORDER BY COLUMN_NAME]</code></pre>
<p>Here are some examples:</p>
<pre><code>SELECT * FROM Employee_Info
SELECT empName FROM Employee_Info
SELECT empName, empSalary FROM Employee_Info</code></pre>


<h4>Update Command</h4>
<p>Use the following SQL query to update the job title of an employee from "Developer" to "Business Man" in the Employee_Info table:</p>
<pre><code>UPDATE Employee_Info SET job = 'Business Man' WHERE job = 'Developer'</code></pre>

<h4>Delete Command</h4>
<p>Use the following SQL query to delete a record from the Employee_Info table where the empId is 2:</p>
<p>Note that DELETE can be rolled back using the ROLLBACK statement, whereas TRUNCATE cannot be rolled back.</p>
<pre><code>DELETE FROM Employee_Info WHERE empId = 2</code></pre>

<h4>Order By Clause</h4>
<p>Used to arrange data in certain format like Asc or Desc order, Always used with Select Command</p>
<pre><code>select * from Employee_Info order by empName desc</code></pre>
<pre><code>select * from Employee_Info order by empSalary asc</code></pre>
<h4>Where Clause</h4>
<p>This clause helps you to restrict query to rows that meet a specific condition</p>
<pre><code>select empName, job from Employee_Info where empId = 1015</code></pre>
<pre><code>update Employee_Info set empName = 'Umer' where empId=1014</code></pre>
<pre><code>delete from Employee_Info where empId = 1007</code></pre>

<h4>Aggregate Function/Group Function</h4>
<p>It is applied on numeric value</p>
<pre><code>SELECT SUM(empSalary) from Employee_Info</code></pre>
<pre><code>SELECT AVG(empSalary) FROM Employee_Info</code></pre>
<pre><code>SELECT COUNT(empSalary) FROM Employee_Info</code></pre>
<pre><code>SELECT MAX(empSalary) FROM Employee_Info</code></pre>
<h4>Numeric Function</h4>
<p>give positive of what is given</p>
<pre><code>SELECT ABS(-10)</code></pre>
<p>gives upper value e.g 77</p>
<pre><code>SELECT CEILING(76.12)</code></pre>
<p>gives lower end value e,g, 76</p>
<pre><code>SELECT FLOOR(76.12)</code></pre>
<p>gives square root</p>
<pre><code>SELECT SQRT(81)</code></pre>
<p>gives square</p>
<pre><code>SELECT SQUARE(16)</code></pre>
<h4>String Function</h4>
<p>upper case</p>
<pre><code>SELECT UPPER('this is our world')</code></pre>
<p>lower case</p>
<pre><code>SELECT LOWER('THIS IS OUR WORLD')</code></pre>
<p>cut the string</p>
<pre><code>SELECT SUBSTRING('CHATGPTWHAT', 3, 6)</code></pre>
<p>replace string</p>
<pre><code>SELECT REPLACE('MICROSOFTISWHATIS', 'MICRO', 'MAJOR')</code></pre>
<p>repeat that number of times</p>
<pre><code>SELECT REPLICATE('MAJOR', 5)</code></pre>
<pre><code>SELECT LTRIM('      WORLD')</code></pre>
<pre><code>SELECT RTRIM('WORLD      ')</code></pre>

<h4>Boolean Operator</h4>
<p>AND, OR, NOT</p>
<pre><code>SELECT * FROM Employee_Info WHERE empName = 'Bob Johnson' AND job = 'Intern'</code></pre>
<pre><code>SELECT * FROM Employee_Info WHERE empName = 'Ali' OR JOB = 'Analyst'</code></pre>
<pre><code>SELECT empName FROM Employee_Info WHERE NOT empName = 'Ali'</code></pre>

<h4>Datetime Function</h4>
<pre><code>SELECT GETDATE() AS TODAY_DATE</code></pre>
<pre><code>SELECT SYSDATETIME() AS SYSTEM_DATE</code></pre>
<pre><code>SELECT CURRENT_TIMESTAMP AS TODAY_DAT</code></pre>


<pre><code>SELECT DATENAME(MONTH, CURRENT_TIMESTAMP) AS 'MONTH'</code></pre>
<pre><code>SELECT DATENAME(YEAR, CURRENT_TIMESTAMP) AS 'YEAR'</code></pre>
<pre><code>SELECT DATENAME(HOUR, CURRENT_TIMESTAMP) AS 'HOUR'</code></pre>
<pre><code>SELECT DATEDIFF(YEAR, 'JANUARY 6 1996', CURRENT_TIMESTAMP) AS 'AGE'</code></pre>

<h4>Group By Clause</h4>
<p>Defines one or more columns as Group, such that all values within that groups have the same value for those column always used with Select statement</p>
<pre><code>SELECT empId, SUM(empSalary) AS 'TOTAL SALARY' FROM Employee_Info GROUP BY empId
SELECT empSalary, COUNT(*) AS 'TOTAL_RECORD' FROM Employee_Info GROUP BY empSalary
</code></pre>
<h4>Having Clause</h4>
<p>Defines the condition that is then applied to groups of rows always used with Select statement inside Group By clause</p>
<pre><code>SELECT empId, SUM(empSalary) AS 'TOTAL SALARY' FROM Employee_Info GROUP BY empId
SELECT empSalary, COUNT(*) AS 'TOTAL_RECORD' FROM Employee_Info GROUP BY empSalary
SELECT job, Employee_Info.empName, SUM(empSalary) AS 'TOTAL RECORD' FROM Employee_Info 
    GROUP BY job, Employee_Info.empName
    HAVING empName = 'Ali' AND SUM(empSalary) BETWEEN 100000 AND 200000
</code></pre>

<h4>Top Clause</h4>
<p>Specifies the first N rows of the query result that are to be retrieved.</p>
<pre><code>SELECT TOP(3) empSalary from Employee_Info ORDER BY empSalary ASC</code></pre>
<h4>Coping data from one database to another</h4>
<pre><code>SELECT * INTO STUDENTS FROM CoreCrud.dbo.Employees</code></pre>

<h4>Alter Statement</h4>
<p>The ALTER statement is used to modify existing database objects, such as tables, columns, indexes, or constraints.</p>
<pre><code>ALTER TABLE Employee_Info ADD Salary decimal</code></pre>
<pre><code>ALTER TABLE EMPLOYEE_INFO ADD employeeId INTEGER NULL </code></pre>
<pre><code>ALTER TABLE EMPLOYEE_INFO ADD REVENUE DECIMAL (10, 3) NULL, PROJECTID INTEGER CONSTRAINT PROJECTID_PK PRIMARY KEY</code></pre>
<pre><code>ALTER TABLE EMPLOYEE_INFO DROP COLUMN OFFICE, ADDRESS</code></pre>
<pre><code>ALTER TABLE EMPLOYEE_INFO DROP CONSTRAINT PK__Employee__AFB3EC0DC86E3F78, COLUMN SALARY</code></pre>
<h4>Changing datatype of column</h4>
<pre><code>ALTER TABLE EMPLOYEE_INFO ALTER COLUMN empSalary char(255)
ALTER TABLE EMPLOYEE_INFO ALTER COLUMN DEPTID DECIMAL
</code></pre>
<P>Adding foreign key in a table after table creation</p>
<pre><code> ALTER TABLE Employee_Info
ADD CONSTRAINT FK_Employee_Info_Department
FOREIGN KEY (EMP_DEPTID)
REFERENCES Department (Id);
</code></pre>

<h4>ADVANCED SQL TOPICS ONWARDS</h4>

<h4>Aliases</h4>
<p>Aliases can be used to create temporary names for columns and tables. There are two types of aliases:</p>
<h5>Column Aliases</h5>
<p>Column aliases are used to make column headings easier to read in a query:</p>
<pre><code>SELECT empName AS 'Employee Name' FROM EMPLOYEE_INFO</code></pre>
<pre><code>SELECT empName 'EMPLOYEE NAME' FROM EMPLOYEE_INFO</code></pre>
<pre><code>SELECT empName AS 'Employee Name', phone AS Phone, empSalary AS 'Employee Salary', job AS 'Employee Job Title' from Employee_Info</code></pre>
<h5>Table Aliases</h5>
<p>Table aliases are used to shorten your SQL:</p>
<pre><code>SELECT e.empName, d.deptName FROM EMPLOYEE_INFO e INNER JOIN DEPARTMENT_INFO d ON e.DEPTID = d.DEPTID;</code></pre>
<h4>Joins</h4>
<p>Joins are used to retieve data from multiple tables</p>
<p>Joins are used to combine rows from two or more tables based on a related column between them. There are different types of joins:</p>

<ul>
  <li>Inner Join/simple join/natural join</li>
  <p>Inner Join returns rows from multiple tables where the join condition is satisfied. Other types of joins are also available, such as:</p>
  <li>Outer Join</li>
  <ul>
    <li>Left Outer Join</li>
    <li>Right Outer Join</li>
    <li>Full Outer Join</li>
  </ul>
  <li>Cross Join</li>
</ul>
<p>Inner Join is used for getting records where defined properties have similar values. Here are some examples:</p>
<pre><code>SELECT * FROM Employee_Info INNER JOIN Department ON LOWER(Employee_Info.job) = LOWER(Department.dept_name)</code></pre>
<pre><code>SELECT * FROM Employee_Info INNER JOIN Department ON Employee_Info.EMP_DEPTID = Department.Id</code></pre>
<p>Alias can be used to increase code readability and to reduce table length:</p>
<pre><code>SELECT E.empName, E.empSalary, E.job, D.dept_location, D.dept_name FROM Employee_Info AS E INNER JOIN Department AS D ON E.job = D.dept_name</code></pre>

<h4>Left Outer Join</h4>
<p>Returns all rows from the left-hand table and records from the right table with only matching values.</p>
<pre>
<code>
SELECT  E.empId, E.empSalary, E.empSalary, D.dept_location, D.dept_name 
FROM Employee_Info AS E
LEFT OUTER JOIN Department AS D ON E.job = D.dept_name
</code>
</pre>
<pre>
<code>
SELECT E.empId, E.empSalary, E.empSalary, D.dept_location, D.dept_name
FROM Employee_Info AS E
LEFT OUTER JOIN Department AS D ON E.EMP_DEPTID = D.Id
</code>
</pre>

<h4>Right Outer Join</h4>
<p>Returns all records from the right-hand table and records from the left-hand table with only matching values.</p>
<pre>
<code>
SELECT D.dept_location, D.dept_name, E.empName, E.empSalary, E.job, E.phone 
FROM Employee_Info AS E 
RIGHT OUTER JOIN Department AS D ON E.EMP_DEPTID = D.Id
</code>
</pre>
<pre>
<code>
SELECT D.dept_location, D.dept_name, E.empName, E.empSalary, E.job AS 'JOB TITLE', E.phone
FROM Employee_Info AS E
RIGHT OUTER JOIN Department AS D ON E.job = D.dept_name
</code>
</pre>

<h4>Full Outer Join</h4>
<p> return all rows from left-hand and right-hand table with matching values </p>
<pre><code>SELECT E.empName, E.empSalary, E.job, E.phone, D.dept_location, D.dept_name FROM Employee_Info AS E FULL OUTER JOIN Department AS D ON E.deptId = D.Id</code></pre>

<h4>Subquery</h4>
<p>A query within another SQL query</p>
<p>A subquery is used to retrieve data that will be used in the main query's condition, expression, or from clause. If you need to filter your main query based on a subset of data that is not directly available in the main table, a subquery can be used to retrieve the required data.</p>
<pre><code>
--Display salary of employees whose salary is greater than Sarah's salary<br>
SELECT empSalary, empName FROM Employee_Info WHERE empSalary > <br>
(SELECT empSalary FROM Employee_Info WHERE empName = 'Sarah Lee' )<br>
</code></pre>
<pre><code>
--Display name, salary of employees whose salary us greater than Sarah salary and deptno same as adam<br>
SELECT empName, empSalary FROM Employee_Info WHERE empSalary >= <br>
(SELECT empSalary FROM Employee_Info WHERE empName = 'Sarah Lee') AND EMP_DEPTID = <br>
(SELECT EMP_DEPTID FROM Employee_Info WHERE empName = 'Sarah Lee')<br>
</code></pre>
<pre><code>
--Display employe info where department is located at Newyork<br>
SELECT * FROM Employee_Info AS E INNER JOIN Department AS  D ON E.EMP_DEPTID = D.Id WHERE<br>
D.dept_location = (SELECT D.dept_location WHERE D.dept_location = 'MULTAN')<br>
</code></pre>

 <h4>Introduction to T-SQL (transactional)</h4>
    <p>In Standard SQL, we are able to perform DML Statements, operators, built-in functions, and single line queries. However, in T-SQL, we get Standard SQL apart from batch or script, triggers, working with variables, user-defined functions, stored procedures, and many more.</p>
    <h4>Working with Variables</h4>
<p>Variables are generally used to store values in memory. T-SQL variables are created by using DECLARE followed by a variable name preceded with the '@' symbol and datatype.</p>
<pre>
  <code>DECLARE @NAME VARCHAR(255), @AGE INT;
  
  -- By default, the declared variable value is null. For assignment, we can use SET and SELECT statements. SET can assign a value to one variable, and SELECT can assign a value to multiple variables.
  SET @variable_name = value
  SELECT @var_name = value,@var_name = value;
  SET @age += 10;
  SET @age = @age * 10;
      </code>
</pre>
<pre>
  <code>
DECLARE @AGE INT = 100;
  SET @AGE = @AGE * 12;
  SELECT @AGE;
    </code>
</pre>
<pre>
  <code>
  DECLARE @NAME VARCHAR(255), @QTY INT = 23;
  SELECT @NAME = 'ABDULLAH', @QTY = 27 ;
  SELECT @NAME, @QTY;
  </code>
</pre>

<h4>Batch</h4>
<p>It's a group of 2 or more SQL statements or a single SQL statement. It can have DML, DDL, DCL (it contains control permissions).</p>
<p>1- Explicit Batch: 2 or more SQL statements separated by a semicolon.<br>
2- Procedure: it contains more than one SQL statement.</p>

<h4>Go Command</h4>
<p>It's not an SQL statement, but it's a command recognized by SQL Server utilities. It signals the end of a batch. You can access certain declared variables within that GO statement.</p>
<pre>
  <code>
DECLARE @NAME VARCHAR(50)
SELECT @NAME = 'ChatPT'
SELECT @NAME AS 'NAME'
GO
</code>
</pre>

<h4>Control Flow</h4>
	<p>T-SQL statements are executed in sequence one after another through control flow keywords we want to interrupt the normal flow. Control flow keywords are:</p>
	<ul>
		<li>BEGIN...END</li>
		<li>IF...ELSE</li>
		<li>WHILE</li>
		<li>BREAK</li>
		<li>CONTINUE</li>
		<li>GOTO</li>
		<li>RETURN</li>
		<li>TRY...CATCH</li>
		<li>THROW</li>
		<li>WAITFOR</li>
	</ul>
 <h4>Begin End</h4>
<p>Are used to group multiple lines into single statement. It can be nested means, they can be placed into one another.</p>
<pre><code>BEGIN 
DECLARE @NAME VARCHAR(255), @SALARY char(55), @DEPTID INT = 7;
SELECT @NAME = empName, @SALARY = empSalary FROM Employee_Info WHERE EMP_DEPTID = @DEPTID
SELECT @NAME AS 'NAME', @SALARY AS 'SALARY';
BEGIN 
	PRINT 'DEPARTMENT ID: '
END
END
GO</code></pre>
<h4>IF...Else</h4>
<pre><code>BEGIN 
DECLARE @SALARY CHAR(55);
SELECT @SALARY = AVG(empSalary) FROM Employee_Info;
SELECT @SALARY AS 'AVG SALARY';
IF @SALARY &gt; '25000'
	BEGIN 
		PRINT 'AVERAGE SALARY IS GREATER THAN 25000';
	END
ELSE 
	BEGIN 
		PRINT 'AVG SALARY IS LESS THAN 25000'
	END 
END</code></pre>
<h4>While Loop</h4>
<pre><code>WHILE [condition]
BEGIN
[SQL CODE HERE]
END</code></pre>
<h4>Try...Catch</h4>
<p>Error handling concept, SQL conditions will be grouped in Try block.</p>
<pre><code>BEGIN TRY 
[SQL CONDITION HERE]
END TRY
BEGIN CATCH
[SQL CONDITION HERE] e.g. SELECT ERROR_MESSAGE() AS 'ERROR MESSAGE', ERROR_LINE() AS 'ERROR LINE';
END CATCH</code></pre>
<h4>WAIT...FOR</h4>

<p>Blocks the execution of batch, store procedure or transaction until a specified time or time interval interval elapses or a specified statement modifies or return atleast one row.</p>

<p><b>WAITFOR</b> has 2 arguments:</p>

<ol>
  <li><b>Time:</b> It will execute query on this time after every 24 hours</li>
</ol>

<pre><code>
SELECT GETDATE() AS 'CURRENT TIME';
GO 
BEGIN 
	WAITFOR TIME '14:57:00'
	SELECT * FROM Employee_Info
END 
GO 
</code></pre>
<ol start="2">
  <li><b>Delay:</b> It will execute query after every 10 seconds</li>
</ol>
<pre><code>
SELECT GETDATE() AS 'CURRENT TIME';
GO
BEGIN 
	WAITFOR DELAY '00:00:10'
	SELECT * FROM Employee_Info
END 
GO 
</code></pre>
<h4>Stored Procedure</h4>
<p>It's a group of one or more T-SQL statements. It can accept input parameter and return multiple values. It contains programming statements to perform operations on database. It returns a value which indicates the success or failure of the program.</p>
<p><b>Benefits:</b></p>
<ul>
  <li>Reuse code</li>
  <li>Improve performance</li>
  <li>Strong security</li>
  <li>Reduce server/client network traffic</li>
</ul>
<p><b>Types:</b></p>
<ul>
  <li>System: Physically stored in the internal resource database.</li>
  <li>User-defined: It can be stored in a user-defined database or system database except the resource database.</li>
  <li>Temporary: Form of user-defined procedure, they are like permanent procedures except they are stored in tempdb.</li>
</ul>

<h4>Create Stored Procedure</h4>

<p>There are 2 ways to create a stored procedure:</p>

<h4>2 - SP without parameter</h4>
<pre><code>
CREATE PROCEDURE procedure_name
AS 
BEGIN
   [sql statements or block]
END
</code></pre>
<pre><code>
CREATE PROCEDURE proc_employeeInfo
AS 
BEGIN 
SELECT * FROM Employee_Info WHERE empId = 1003
END;
EXECUTE proc_employeeInfo
</code></pre>
<h4>1 - SP with parameter</h4>
<p>This stored procedure retrieves employee information along with their department details based on the location parameter passed to the procedure.</p>

<pre><code> 
	USE [database_name]
	GO

	CREATE PROCEDURE proc_employeeDetailJobWise(@location AS VARCHAR(100))
	AS
	BEGIN 
		SELECT * FROM Employee_Info e INNER JOIN Department d 
		ON e.EMP_DEPTID = d.Id
		WHERE d.dept_location = @location
	END;
	GO
</code></pre>

<h4>Alter SP</h4>
<p>This stored procedure retrieves all employee information along with their department details whose department ID is 5.</p>
<pre><code> 
	USE [database_name]
	GO

	ALTER PROCEDURE proc_allEmployeeInfo
	AS 
	BEGIN 
		SELECT * FROM Employee_Info AS E INNER JOIN Department AS D
		ON E.EMP_DEPTID = 5
	END;
	GO
</code></pre>

<h4>Function - User Defined Function (UDF)</h4>
<p>UDF always returns a value.</p>
<p>It has only one input parameter.</p>
<p>It cannot return multiple result sets.</p>
<p>Error handling is restricted, so you cannot use Try-Catch or @Error.</p>
<p>SET statements are not allowed in UDFs.</p>
<p>UDFs cannot call stored procedures, but stored procedures can call functions.</p>
<p>UDFs can be nested.</p>
<pre><code>
-- function syntax
CREATE FUNCTION function_name (parameter datatype, --- )
---
---
RETURNS return_datatype
[WITH  <function_option[...n]>]
[AS]
    BEGIN 
      function_body
      RETURN scalar_expression
    END;
</code></pre>
<pre><code>
-- create a function to get employee salary by passing employee name
CREATE FUNCTION salary(@name as varchar(50))
RETURNS decimal
BEGIN
    DECLARE @sal DECIMAL;
    SELECT @sal = Employee_Info.empSalary FROM Employee_Info
    WHERE Employee_Info.empName = @name;
    RETURN @sal;
END
</code></pre>

 <h4>Table-valued functions:</h4>
  <p>
    A table-valued function is a function that returns a table as its result. It can be used in a query as if it were a regular table, allowing you to join, filter, and perform other operations on its result set. Table-valued functions are useful when you need to encapsulate complex queries or perform data manipulations and return the results as a table.
  </p>
  <p>
    There are two types of table-valued functions:
  </p>
  <ul>
    <li>
      <strong>Inline table-valued functions:</strong> These functions return a table directly as the result of a single SELECT statement.
    </li>
    <li>
      <strong>Multi-statement table-valued functions:</strong> These functions use a BEGIN...END block and can have multiple statements to generate and populate the result table.
    </li>
</ul>

  <h4>Trigger</h4>
  <p>
    Special type of SP, that automatically runs when an event occurs.
    Here events are DML operations (Insert, Delete, Update).
  </p>
  <p>
    <b>Types of Trigger</b>
  </p>
  <ol>
    <li>DDL Trigger: is fired when DDL Statements like DROP Table, Create Table, or Alter Table occurs. DDL Triggers are always after triggers.</li>
    <li>DML Trigger: We can create DML Triggers on DML Statements like INSERT, UPDATE, DELETE. They are of 3 types.</li>
  </ol>
  <ul>
    <li>After Trigger: Executes after the action of Insert, delete, merge, update.</li>
    <li>Instead Of trigger:
      <ul>
        <li>Overrides the standard action of the triggering statement.</li>
        <li>Used to perform error or value checking.</li>
        <li>Performs additional action before Insert, delete, merge, update.</li>
      </ul>
    </li>
  </ul>
