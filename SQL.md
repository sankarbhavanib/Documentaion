## Postgresql
http://www.tutorialspoint.com/postgresql/index.htm


## Basic Traning

https://www.youtube.com/watch?v=7Vtl2WggqOg

http://www.dofactory.com/sql/tutorial

### Standard SQL question 

## finding N th higest salary 
```
SELECT * /*This is the outer query part */
FROM Employee Emp1
WHERE (N-1) = ( /* Subquery starts here */
SELECT COUNT(DISTINCT(Emp2.Salary))
FROM Employee Emp2
WHERE Emp2.Salary > Emp1.Salary)
```
## finding duplicate values in a SQL table
```
SELECT name, COUNT(email) 
FROM users
GROUP BY email
HAVING ( COUNT(email) > 1 )
```
## FAQ 

https://www.toptal.com/sql/interview-questions

http://www.programmerinterview.com/

