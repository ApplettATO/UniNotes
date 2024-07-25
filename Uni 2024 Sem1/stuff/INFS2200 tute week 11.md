MidSem Exam:
Question 3:

CHECK (SELECT E.age FROM EMP E, DEP D where E.eid = D.managerid > 30);

Question 4:
(a)
Cylinder:
	Cylinder with tracks inside it
Platter:
	Circle with tracks inside it

(b)
- In DBMS I/O operation will read or write data blocks
- A block is a unit of data transfer between hard disk and memory
- A disk block is an adjacent sequence of sectors from a platter
- Block size typically range from 512 byes to 4kbytes
4 marks

c)
2 marks for each correct explanation
Heap file:
- Unordered and stored randomly
- Access records are based on *linked list*
- Can fixed length or variable length
Ordered File:
- Sequentially in order based of a sorted key
Hash File:
- Records are distributed in different blocks according to the hash function that the key returns
- The overflow buckets may be used to store records as well

d)
4 marks
Seek time and relational delay are the dominating factors as they both *manipulate the physical parts* of the disk and are at least three orders of magnitude slower than mechanically done disk

Question 5)
6 marks
Identify three bottle neck problems: Queueing, Hot Spots, Read/Write Latency

7 marks
Queueing: Multiple users access the same database in the server at the same time
Hot Spot: Set of records in a database are simultaneously requests by many users with a high frequency for both read/write operation
Read/Write: Seek time + rotation delay + block transfer time for read and write data from/to the hard disk. It is dominated by the seek time and rotational delay


Question 7:
+2 for each dot points mentioned