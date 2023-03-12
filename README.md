My Chat gpt rules :-
make its html for readme file on github
give h4 heading to line starting from $
give paragraph to line starting from %
give code script to line starting from #


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
<p>Joins are used to combine rows from two or more tables based on a related column between them. There are different types of joins:</p>

