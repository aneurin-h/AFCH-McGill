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
	stack add v
	while(stack isnt empty)
		v1 = stack pop
		visit v1
		mark v1 as visited
		for all unvisited adjacents of v1
			add to stack
```
# Single Source Shortest Path Problem