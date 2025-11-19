# Binary Search Tree
Each node has at most 2 children
	Stores 2 children: left & right
Adds **inorder** traversal, where node is visited between left and right child

## Definition
Elements are comparable and UNIQUE
For each node, all descendants in left subtree are less than the node's element
	likewise the opposite is true for the right subtree
```java
class BSTNode<K>{
	K key;
	BSTNode<K> leftNode;
	BSTNode<K> rightNode;
}
```
In-order traversal sorts the list
	Thus sorting algorithm is unnecessary (an improvement over $O(N)$)
## Finding Elements in BST
**Find Min** - Always descend to the left child, until not present
```java
findMin(node){
	if(node == null) return null
	if(node.left == null) return node;
	
	return findMin(node.left);
}
```
$\Omega(1), O(n)$
**Find Max** - Always descend to the right child, until not present
```java
findMax(node){
	if(node == null) return null
	if(node.right == null) return node;
	
	return findMax(node.right);
}
```
$\Omega(1), O(n)$
**Find Key** - finds the node containing key
```java
find(node, key){
	if(node == null) return null
	if(node.key == key) return node
	
	if(node.key.compareTo(key) < 0) return find(node.left, key)
	else return find(node.right, key)
}
```
$\Omega(1),O(n)$
**Add** - Add element, while respecting ordering rules
```java
add(root, n)
add(node, key){
	if(node == null) node.element = key
	if(key < node.key) node.left = add(node.left, key)
	if(key > node.key) node.right = add(node.right)
}
```