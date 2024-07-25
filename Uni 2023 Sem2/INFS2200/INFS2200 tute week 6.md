Exercise 1
A) Sum of box (Employee table) + 1 = 115 -> Size of record

B) records/block = block size / record size = 512/115 = 4
	size of record = 115
	block size = 512
No file = ceil (30000/4) = ceil(7500) = 7500
45.6 -> 46

C) Primary indexing
[1, 2, 3] , [4, 5, 6]
[1, 2, 3, 4, 5, 6] (draw arrows to representative number)
**Part A** - Index blocking factor (bfri)
size of 1 index = number of fields + block pointer = 9 + 6 = 15
	No. of entry = 512 (block size)
	How many blocks of indexes can we store = floor(512/15) = 34 indexes per block
**Part B** - Index entries & Index blocks 
No. entry = 7500
No. of block needed = ceil(7500/34) = 221 blocks

Consider: wa = [1, 2, 3], [2, 3, 4], [3, 4, 5]
Primary Index -> pointing to block
	points to each block
	wa[0], wa[1], wa[2]
Secondary Index -> pointing each index
	points to each individual number
	wa[0],[2]

D)
a) bfr = floor(512/12) = 34 index/block
b) no. of entry = 30000
	no. of block = ceil(30000/34) = 883 blocks

Department code -> Block -> Record
Each gets more specific

E)
a) size of index = 9 + 6 = 15
	bfr = floor(blocking size/size of index) = floor(512/15) = 34
b) no. entry = 1000
	no. blocks = ceil(1000/34) = 30 blocks

F)
a) ceil(10000/34) = 30 block
	ceil(30/34) = 1 block
		:. 2 levels

  Alternatively:
	level = ceil(logBASE(bfr)(N department codes) = ceil(log34(1000)) = 2

b) no.blocks 
	30 + 1 = 31
c) 1000 distinct dept codes
	30000 records
	30000/1000 = 30 employees per code
	ceil(30/4) = 8 blocks of each individual dept code per employee
	-> Total blocks = blocks + levels = 8 + 2 = 10

Exercise 2
A)
entry = bytes + bps (block pointer size) = 10
bfr = floor(N/entry size) = floor (10000/10) = 100 index/block
No. block = no. of entries / bfr = 10000/100 = 100 blocks
:. total no. of blocks = log[base2]100 + 1 = 8

B) Max height of Bt tree
	Note: max height when node is half full
	bfr = (0.5N / R) = (1000 x 0.5 / 10) = 50 index/block
	

Exercise 4
A) N1, N2, N5
B) N1, N2, N6, N7, N8, N9, N10, N11
