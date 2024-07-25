Tute sheet 2 - Exercise 2 -> Try A - C (revision on 1200)
D - H)
E)
Create Table(
	...
	...
	...
	check (salary => 10000)
);

Create Assertion ...
	Check(Not Exist
		Select x
		From Emp E, Dept D
		Where E.eid = D.managerid
		and E.age <= 30
		)
	)
G
Create Assertion ...
	Check(Not Exist
		Select all (*)*
		From Work
		Group by eid
		Having sum 
		)

I) What's the diff between trigger & assertion
Trigger runs 
Assertion double checks if the relation is working correctly


Tute Sheek 3
Heap File -> unsorted
Hash File -> Dictionary

Binary Sort: [2, 3, 8, 14, 18, 21] -> len() = 6

Exercise 6
Heap File: M -> 0.5 -> M -> 2
Sorted File: M -> log base2 M -> log base2 M + mot -> log base2 M + M
Hash File: M -> 1 + overflow -> rnage size -> 2 + overflow

Exercise 9: cylinder shapes or smth
A) 20 x 512 = 10240 bytes
B) 400
C) 10240 x 2(double sided) x 15(platters) = 307200
D) 400 x 307200 = 122.88 MB

Tute Sheet 4:

Cluster: Deptcode

C)
part a
What's the size of 1 index
Index entry size (Ri) = SSN + P = 9 + 6 = 15bytes
Index blocking factor (bfr) = floor (512/15) = 34 index entries per block
	bfr = floor(size of block / size of index)
part b
No. of index entries (Ni) = number of file blocks(b) = 7500 entries
No. of index / no. of index per block = 

E) distinct departmentcode (!!!) = 1000

F)
(a) 34
(b) 30 blocks
Try solve a and b
(a)
log base(bfr) size = log base34 1000
(b)
first level of index = 30 blocks
ceil(30/34) = 1
number. of blocks = 30 + 1 = 30

(c) Calculate the no. of block accesses
Suppose IT[wa] followed by IT[wa] followed by IT[wa] wtc

no. of access to search for the first block in the cluster of blocks = ...

There are 1000 distinct values of DepartmentCode so the average number of records ... 
each value is: (N/1000) = 30000/1000 = 30 records

next step records/bfr = ceil(30/4) = 8

number is 10




