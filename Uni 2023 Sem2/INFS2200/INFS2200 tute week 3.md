#Question3
D C TOTAL_S

| D | C | Total_S | Average_S | 
| -------- | -------- | -------- | -------- | 
| 1 | 1 | 55000 | 55000 |   
| 5 | 4 | 133000 | 33250 |
| 4 | 3 | 93000 | 31000 |

#Question4
A) INSERT INTO EMP VALUES(101, 'John Doe', 32, 15000);

B) UPDATE EMP SET SALARY=SALARY x 1.1;

C) DELETE 
	FROM EMP 
	WHERE dname='Toy';

D) SELECT E.name, E.salary
	FROM Emp E, Dept D
	WHERE D.managerid = E.eid AND D.dname = 'IT';

E) Select w.did, Count(ASTERISK), AVG(E.Salary)
	From Emp E, Works W
	Where E.eird = W.eid
	Group by W.did
	Having Count(ASTERISK) > 20;

F)
- Computer cross product of Emp and Work
- Apply condition E.eid = W.eid (remove rows that don't meet this condition)
- Keep W.did and E.salary, and remove the other columns
- Sort the table based on W.did
- Calculate ciybt for each group (ie W.did) and remove group with count less than 20
- Calculate AVG(salary) for each remaining group

G) 
Select ename
From Empp
Where age > 50 and salary > 100000l

H) It is not updatable, because it does not contain the primary key and we can just include the primary key to make it updatable

I) No it is not because it contains aggregate functions

#Question5
1) Select p#, weight, colour
	from p
	where weight > 14 and colour = 'green'

2) Select p#, weight + 5
	from o
	where weight > 14
	order by 2;

3) Update p
	set colour = 'white'
	where weight > 14 and weight = 18;

4) Delete
	from p
	where weight > 14 and weight < 10;

5) Insert into P(p#, weight, colour)
	values ('P99', 12, 'Purple');
