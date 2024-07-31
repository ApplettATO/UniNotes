Functional Dependency: X -> Y
Superkey: Set of attributes where no two tuples have the same 
- R(A B C D)
- A -> B
- B -> C
Non prime " : Not
INF:
2NF:
- INF
- Every non-prime is fully dependent on the whole of every candidate key
	- R(A B C D)
	- A -> B, AC -> D
3NF
- 2NF
- non-prime -> non-prime
- no transitive dependencies
BCNF
- Every determinant is a superkey

# Questions
**Question 1**
- i
	- candidate key: BC
	- 1NF

- ii
	- candidate key: BC
	- highest NF:
		- 1NF 
		- 2NF:
			- prime: B, C
			- non-prime: A, D
		- 3NF
		- BCNF
- iii
	- candidate key: BC, CA, CD
	- highest NF: 
		- 1NF 
		- 2NF:
			- prime {A, B, C, D}
			- non-prime {}
		- 3NF
		- BCNF -> not

**Question 3**
a) 
SELECT Puzzle **

e)
SELECT Name
FROM SOLVERS
WHERE Type = "Student"
AND RegNo IN (
	SELECT RegNo
	FROM Student
	WHERE Year = "First Year"
	) AND RegNo IN (
	SELECT RegNo
	FROM Solved
	WHERE DateSolved iS NOT NULL
		AND PName IN (
			SELECT PName
			FROM Puzzle
			WHERE Difficulty = "Hard"
		)
	)