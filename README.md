<p align="center">
<img src="https://i.imgur.com/3X7Lk0a.png" alt="Linux file permissions"/>
</p>

<h1>Apply filters to SQL queries</h1>

<h2>Project Description</h2>

My company is attempting to strengthen the security of their system. It is my responsibility to make sure the system is secure, look into any possible security vulnerabilities, and update staff PCs as required. The steps that follow demonstrate how I carried out security-related activities using SQL and filters.

<h3>Retrieve after hours failed login attempts</h3>

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated. 

The following code demonstrates how to used SQL query to filter for failed login attempts that occurred after business hours. 

<img src="https://i.imgur.com/toii3zg.png" alt="sql1"/>

The first part of the screenshot is my query and the second part is the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and that were unsuccessful. The first condition is login_time > '18:00', which filters for records after 18:00. The second condition is success = 0 (false) for the failed login attempts. 

<h2>Retrieve login attempts on specific dates</h2>

A suspicious even occurred on 2022-05-09. Any login attempts which occurred on this day and the day before needs to be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates. 

<img src="https://i.imgur.com/YzVtjFG.png" alt="sql2"/>

This query returns all login attempts that occurred on 2022-05-08 or 2022-05-09. First I selected all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts which occurred on either of those two dates.

<h2>Retrieve login attempts outside of Mexico</h2>

After investigating the suspicious login attempts, I believe there is an issue with the login attempts that occurred outside of the USA. These login attempts should be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of the USA.

<img src="https://i.imgur.com/EqJ16Df.png" alt="sql3"/>

This query returns all login attempts that occurred in countries outside of the USA. First, I selected all data from the log_in_attempts table. Then, I used the WHERE NOT clause to filter for countries that is outside the USA. I used LIKE with 'US%' as the pattern to match because the dataset represents USA as US and USA. The % sign represents any number of unspecified characters after US when used with the LIKE operator. 

<h2>Retrieve employees in Marketing</h2>

My team wants to perform security updates on employee machines in the Marketing department. To do this, I have to get information on which employee machines to update. The following code demonstrates how I created a SQL query to employee machines from employees in the Marketing department in the East building. 

<img src="https://i.imgur.com/mJxKG8G.png" alt="sql4"/>

This query returns all employees who is in the Marketing department and is located in the East office building. First, I selected all data from the employees table. Then, I used the WHERE clause with AND to filter for employees who work in the Marketing department and in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. 

<h2>Retrieve employees in Finance or Sales</h2>

The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments. The following code demostrates how I created a SQL query to filter for employee machines from the Finance and Sales departments.

<img src="https://i.imgur.com/tIbHlLa.png" alt="sql5"/>

This query returns all employees who work in the Finance and Sales departments. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for employees who are in the Finance and Sales departments. I used the OR operator instead of AND because I want all employees who are in either department.

<h2>Retrieve all employees not in IT</h2>

My team needs to make one more security update to employee machines who are not in the Information Technology department. To make this update, I first have to get information on these employees. The following code demostrates how I created a SQL query to filter for employee machines from employees not in the Information Technology department. 

<img src="https://i.imgur.com/KGQtk2f.png" alt="sql6"/>

This query returns all employee machines not in the Information Technology department. First, I selected all data from the employees table. Then, I used the WHERE with the != operator to filter for employees not in this department. Using != or <> is an alternative of using the NOT operator. 

<h2>Summary</h2>

I applied filters to SQL queries to get specific data on login attempts and employee machines. I used two different tables to retrieve this information (log_in_attempts and employees). I used the AND, OR, NOT operators to filter results to retreieve data needed for each task. I also used the LIKE and the % wildcard to filter for patterns within the results. 
