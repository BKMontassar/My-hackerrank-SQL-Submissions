### Employee Salaries 

<img src="../PIc/20.png" alt="solution">


#### Topic:
Write a query that prints a list of employee names (i.e.: the name attribute) for employees in Employee having a salary greater than $2000 per month who have been employees for less than 10 months. Sort your result by ascending employee_id.
where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is their monthly salary.
Sample Output:
Angela 
Michael 
Todd 
Joe

Explanation:
Angela has been an employee for 1 month and earns $3443 per month.
Michael has been an employee for 6 months and earns $2017 per month.
Todd has been an employee for 5 months and earns $3396 per month.
Joe has been an employee for 9 months and earns $3573 per month.
We order our output by ascending employee_id.



#### Language : MS SQL
```sql
select name from Employee where
salary > 2000 and months < 10 
order by employee_id asc
```
