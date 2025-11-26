# Graph Definition
Rootless Tree
Edges can be both weighted and directed
A **Directed Graph** has a set of vertices $V = \{vi : i \in \{1,\dots, n\}\}$
	& a set of edges $E = \{(v_{i},v_{j}) : i,j \in \{1,\dots,n\}\}$
**Path**: Sequence of edges such that the end of one edge is the start of the next
**Graph ADT**:
Methods
```
addVertex(), addEdge()
containsVertex(), containsEdge()
getVertex(), getEdge()
removeVertex(), removeEdge()
numVertex(), numEdge()
```
Store using an adjacency list, for each element, store the elements it is adjacent to
For small graphs can also store an adjacency matrix (w/ all elements as row/col (from/to) indices)
## Implementation
Graph Class:
	ArrayList of Vertex : vertices
Vertex Class:
	T : element
	ArrayList of Edges : adjacency list
Edge Class:
	Vertex : end vertex
	double : weight
# Graph Traversal (Recursive)
```java
depthFirstGraph(v) // Preorder
	mark v as visited
	visit v
	for all unvisited adjacents
		traverse those vertex
```
# Graph Traversal (Non Recursive)
```java
graphTraversalUsingStack(v)
	stack push v
	while(stack isnt empty)
		v1 = stack pop
		visit v1
		mark v1 as visited
		for all unvisited adjacents of v1 that havent already been added to stack
			add to stack
```
Also works with Queue and Priority Queue
# Single Source Shortest Path Problem
Input 
	Directed Graph $G=(V,E)$
	Weight Function for edges $w(v_{i},v_{j})$
	Source $s$
Weight of a path
	Sum of edge weights on a path
	$\sum_{k=1}^{n}w(v_{k-1},v_{k})$
Shortest Path from $s$ to $v$
	find $min(w(v))$ if $w(v)$ exists
	Not necessarily unique
	For each vertex v
		`dist[v]` is the estimate of the shortest path
		`pred[v]` is the predecessor of the estimated shortest path
## Dijkstra
Initialization
	All vertices `dist[v]` to $\infty$, `pred[v]` = null, add to the priority queue
1. Remove smallest from priority queue
2. Relax the adjacent vertices
	1. Adjust their `dist`