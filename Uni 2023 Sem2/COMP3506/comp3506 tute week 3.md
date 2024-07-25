#define Analysing Recursive Functions
Count the opearations in a single recursive step

#define selection sort
O(n^2)

scans the unsorted part of the list
selects the smallest element out of the unsorted portion and then places it at the beginning/end of the sorted portion

#define insertion sort
O(n^2)

goes through the unsorted portion 1 by 1
inserts each unsorted element into the the correct spot in the sorted position

#definte merge sort
O(n log n)

#define quick sort
worst case O(n^2)
expected case O(n log n)

#define Tute Sheet
Question 1
2^10
3 log (log n)
100 log n
4n
4n log n + 2n
n^2 + 10n
n^2 log n
n^3
2^n
2^log n

Question 2
O(n) O(1)

O(n)
println(i) -> O(dn) where dn = no. of digits being printed
d(n) = FLOOR(log10 n) + 1

O(n log n)


Question 3
![[Pasted image 20230808132244.png]]

In recursive call addition is being done O(1)
T(n) = {
	O(1)
	O(1) + 2T(n/2)
}

Recursion run time analysis tree
- each node shows O(1)
- no. nodes = logBASE2 n sigma i=0 (2^i)
		     = 2n - 1

Question 7
3 Situations
- 


(a) O(n) 
T(n-1) + O(1)
if input size of n
- n => n-1 => n-2 ... => 1
- work done is determined by the ... + O(1) part

(b) O(n log n)
input size of n
- n => (n/2), (n/2) => (n/4), (n/4), (n/4), (n/4) => 1 (O(n))
- Work done at n/2 is O(n/2) therefore the work done at second level is O(n) => O(n/2) + O(n/2)
- Every time we go down a level the input size is x 1/2

(c) O(n^2)
