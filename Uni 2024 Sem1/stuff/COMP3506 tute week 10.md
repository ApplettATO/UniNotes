Shortest Path
- given vertices u and v
- shortest path: minimum total weight between u & v
- Subpath of a shortest path is itself a shortest path
Tree of shortest path

Dijkstra's Algorithm
- Greedy Algorithm: relax the vertices cloud
	- takes best option at present, ignores future consequences
- Edge relaxation
- Run Time: O((n + m) + log(n))
	- adjacency list, proof p658 java, p66 python
- Assumptions
	- something
	- something
- Method
	- Start at a vertex
- Example
	- Dijkstras(A)
		- label A as 0, everything else as infinite
		- replace infinite with the costs, update as you go to other nodes with costs that are lower

DAG-Based Alogrithm
- Works with negative weights, Dijkstra's doesn't
- Run Time: O(n+m)
- Topological Order
- Start weight 0, everything else infinity

Minimum Spanning Tree
- Spanning Subgraph
- Tree
- Spanning Tree
- Minimum Spanning Tree
	- Cycle Property
		- MST should have **no cycles**
	- Partition Property

Prim-Jarnik's Algorithm
- Purpose: Find MST
- Greedy algorithm
- Run time: O((n + m) log(n))
	- Proof: pg673 python
- First edge: find the smallest weighted edge
	- (from arbitrary node)
- Until you create an MST:
	- find the next minimum weighted edge that is already connected to the current tree. Ensure the edge you select does not produce a cycle (violates the concept of a tree)

Kruskal's Algorithm
- Purpose: Find MST
- Greedy algorithm
- Run time: O((n + m) log(n))
	- Proof: pg679 python
- Does not require a starting node unlike Prim-Jarnik's
	- Discard the edge if it forms a cycle

Kruskal's VS Prim-Jarnik's
- Kruskal's looks at the smallest edge disregarding the current node
- Prim-Jarnik's looks at the smallest edge connected to nodes in the cloud

#TuteSheet 
Question 1:
![[Pasted image 20231003134353.png]]
(a) yes
(b) dense
	(c)
(d)
![[Pasted image 20231003134721.png]]
(e)
![[Pasted image 20231003134544.png]]

Question 2:
(a) 
![[Pasted image 20231003124406.png]]

(b)
![[Pasted image 20231003124455.png]]
(c)
![[Pasted image 20231003123848.png]]

Question 3:
(a)
Run Time: O((n + m) + log(n))
Adj List: O((v + e) log(v))

(b) DFS(G,u)
Adj List: O(v + e)
- Deg(v) times for one vertex -> O(e) overall
- Overall complexity for:
	- edge list: O(v + ve) euro alpha ve 
	- adj list: O(v + e)

Question 4:
![[Pasted image 20231003133654.png]]
Algorithms only:
(a) BFS
(b) MST Algorithm
(c) Topological Algorithm
(d) Test for Strong Connectivity
(e) Shortest Path Algorithm, but optimizing for highest probability rather than path length