Exercise 1 **go through the ones that you did not cover in tutorial**
a)
SELECT E.Fname, E.Lname
	//Join employee (ssn) to works on (essn) and
	works on (Pno) to project (Pnumber)
	**There's more than the line beneath this look at tute sheet answers**
	EMP_ID <- [Employee]⋈(ESSN=SSN) [select? Hour>10 (EMP_W_P)]
FROM EMPLOYEE E, PROJECT P, WORKS_ON W
WHERE E.Dno = 5

b)
E <- Employee JOINS(SSN = ESSN AND FNAME = DEPENDENT_NAME) DEPENDENT
RESULT <- PROJECT (LNAME, FNAME)(E)

e)
*half of the soln form tute sheet*
PROJ_EMPS(SSN,PNO) <- PROJECT(ESSN,PNO)(WORKS_ON)
ALL_PROJS(PNO) <- PROJECT(PNUMBER)(PROJECT)
*tutor solution*
EMP_ALL_P <- PROJECT(pno,ESSN)(WorkOn) / PROJECT(pnumber)(PROJECT)
PROJECT(Lname, Fname)(EMPLOYEE x EMP_ALL_P)

Exercise 3
A)
= No. Bout + (Rout x Bin)
= 200 + (2000 x 1000)
= 2000200
B)
= No. Bout + (Bout x Bin)
= 200 + (200 x 1000)
= 200200
C)
= Bout + (Bout / (S-2)) x 
= 200 + (200/52-2) x 100
= 4200
D)
=
= 2000
E)
= Bout + (Nout x (Bin/2))
= 1001000