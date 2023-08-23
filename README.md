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

