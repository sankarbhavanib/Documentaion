## Basic Traning
http://www.dofactory.com/sql/tutorial

## standard silly question 
```
SELECT * /*This is the outer query part */
FROM Employee Emp1
WHERE (N-1) = ( /* Subquery starts here */
SELECT COUNT(DISTINCT(Emp2.Salary))
FROM Employee Emp2
WHERE Emp2.Salary > Emp1.Salary)
```
## FAQ 

https://www.toptal.com/sql/interview-questions

http://www.programmerinterview.com/

