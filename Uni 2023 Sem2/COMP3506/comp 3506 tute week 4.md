#define Sorting
	- merge sort, bucket sort, radix sort

Merge Sort
- imagine arrows pointing to the first elements of each list
- compare the arrowed elements add the smaller element into the merged list
- the arrow that was pointing to the added element moves to the next item in that list

Bucket Sort
- Sort objects by a key into buckets
- Stable sort
	- e.g Key range: [0, 9]
		- [7, d], [1, c], [3, a], [7, g], [3, b], [7, e]
	- Element d, with key 7 [7, d]
	- iterate through a list, put(indexing into the array) elements into "buckets"
	- *insert image*
- O(n + N) where n is the amount of items

Radix Sort for Binary Numbers
- Stable sort
- Sorting for binary numbers
- Repeated bucket sort
- Run time O(b x n)
	- where b is the number of digits in each binary number
	- where n is the number of numbers to sort
- *insert image*

#define Linked lists
- wa i zoned out

#define Static and Dynamic array (array list)
Statiic List (Array)
- cannot be resized

Dynamic List (Array List)
- Grows dynamically 
- push(object) adds an element at the end of the array
- if the array is full the list will need to grow (wao but how)
	- Incremental Strategy
		- Increase array size by c
	- Doubling Strategy
		- Double the array size
		- Performance Analysis
			- Every nth push, you must resize the array
				-> push(o) is O(n)
			- All other push calls are constant (when not resizing)
			- We distribute that one O(n) over all n pushes, for an **Average** time complexity of O(1)
			$$
			O(n)/n something
			$$

Dynamic List and Achievable Run Time

| Method | Big O | 
| -------- | -------- | 
| size() | O(1) |  
| isEmpty() | O(1) |
| get(i) | O(1) |
| set(i,e) | O(1) |
| add(i,e) | O(n) |
| remove(i) | O(n) |


#define Amortization

