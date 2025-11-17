# Trees
Non-linear data structure
Collection of Nodes
	Top node called the **root**
Every note except the **root** is a **child**, and has a **parent**
## Terms
**Path**- Sequence of connected nodes
**Length** - Number of edges in the path
	Path of one node has length 0
**Ancestor** - if there is a path downwards from this node to the other
	Descendant is the opposite
**Depth** - Distance from root to a node
	To efficiently compute, need parent link
```java
depth(v){
	if(v.parent == null){
		return 0;
	} else {
		return 1 + depth(v.parent);
	}
}
```
**Height** - Maximum length of a path from that node to a leaf
# Traversal
### Breadth First
For each level, visit all nodes at that level
### Depth First
Preorder Traversal
	Visit a node
	Preorder Traversal of each subtree (its children)
	VISIT ROOT BEFORE CHILDREN
Postorder Traversal
	Subtree traversed first
	Then node is visited
## Computing Height
```java
height(node){
	if(node has no children){
		return 0;
	} else {
		h = 0;
		for each child
			h = max(h, height(child))
		return 1 + h;
	}
}
```
# Recursive Search
