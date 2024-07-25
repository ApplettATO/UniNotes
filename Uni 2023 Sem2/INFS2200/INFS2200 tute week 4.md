
#Question1
A) insert into employee values('Robert', 'F', 'Scott', 943775543, '21-JUN-42', '2365 Newcastle Rd, Bellaire, TX', 'M', 58000, 888665555, 1);

No violation

C) 
- Key constraint violation
- Referential integrity violation

E)
- No violation

G)
- Referential integrity violation

I)
- No violation

K)
- No violation

#Question2

C)
Create TableDept (
did INTEGER,
dname CHAR(10),
budget REAL,
managerid INTEGER NOT NULL,
PRIMARY KEY (did),
FOREIGN KEY (managerid) REFERENCES EMP);

E)
Create Table Emp (
eid INTEGER,
ename CHAR(10),
salary REAL,
PRIMARY KEY (eid),
CHECK(salary <= 1000));

G)
Create ASSERTION Emp (
CHECK (NOT EXIST ())
SELECT &x
FROM works
GROUP BY eid
HAVING SUM (pcttime) > 100));

H)
*insert image from solution*

#Question3 
2)
Let Table be person(name, weekly_income, repay_amount).
Assume repay_amount is 15% of weekly_income if no repay_amount is given in update or insert

*insert image from solution*

Create TRIGGER

5)
Assume we have 2 tables: staff(name, dname, salary) and dept(name, budget). staff.dname reference dept.name. Sum of salaries of the staff in any department cannot exceed the budget of the department

*insert image from solution*

#Question4 
*did not go through this in the tute*


