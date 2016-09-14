## Postgresql
http://www.tutorialspoint.com/postgresql/index.htm


## Basic Traning
http://www.dofactory.com/sql/tutorial

### standard silly question 
## finding N th higest salary 
```
SELECT * /*This is the outer query part */
FROM Employee Emp1
WHERE (N-1) = ( /* Subquery starts here */
SELECT COUNT(DISTINCT(Emp2.Salary))
FROM Employee Emp2
WHERE Emp2.Salary > Emp1.Salary)
```
## Finding duplicate values in a SQL table
```
SELECT name, COUNT(email) 
FROM users
GROUP BY email
HAVING ( COUNT(email) > 1 )
```
## FAQ 

https://www.toptal.com/sql/interview-questions

http://www.programmerinterview.com/

