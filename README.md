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




