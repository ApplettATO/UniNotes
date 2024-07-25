Graph Basics & Terminology
- Possesses a vertices and an edge
- Terminology
	- Undirected Edge
	- Undirected Graph
	- Directed Edge
	- Degree of a verted
	- Parallel Edges
	- Self-Loop
	- Path
		- Alternating sequence of vertices and edges
	- Cycle
		- Path that starts and ends on the same vertex
	- Connectivity
		- Graph
		- Component
	- Properties
		- Sigma(v) deg(v) = 2m
		- m <= n (n - 1) / 2
			- for this to hold needs undirected graph
	- Density
		- *a whole lot of definitions*

Graph Traversals
- Breadth first travel
- Depth first travel

Adjacency Matrix Structure
- 2D Array
- Performance
	- outgoing/incomingEdges(v) - O(n)
		- iterating the list
	- getEdge, removeVertex - O(n)

Digraphs

Directed Graph Algorithms

Depth First Search (DFS)
- Run time O(n+1)
- Example:
	- add A to visited -> visited[A, ...]
	- frontier [E, D, C, B]
	- add E to visited ->
	- terminate search when frontier empty

Breadth First Search: 
- Example

Strong connectivity

Transitive Closure

Topological Sort


#TuteSheet 
Question 1:
a) no
b) 3
c) no
d) yes
e) *insert image*
- x goes to y
- y goes to z
- z goes to y
f) 5


Drawbacks of adjacent matrices
- Slow
	- good for how many walks for vertices

Question 2:
a) V(V-1) x 1/2 = (n-1) + (n-2) + (n-3) + (n-3) + ... + 1 + 0
b) V(v-1)
c) Yes

Question 3:
a) 
frontier{numbers you see} always take the number at the top but put the smallest numbers at the start
visited {1, 2, 3, 4, 7, 6, 9, 10, 8, 5}

b)
frontier{numbers you see} take the number at the bottom
visited {1, 2, 3, 5, 4, 6, 8, 7, 9, 10}

Question 4:
a) visited {a, c, d, b, e}
b) yes
c) remove a-c 
d) any edge that introduces a circle/loop
- eg: make b-a or b-d
e)
i) A -> B -> C -> D
	add A to B, B to D
