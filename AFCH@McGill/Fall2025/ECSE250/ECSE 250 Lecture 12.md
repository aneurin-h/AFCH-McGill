# Doubly Linked List
Each node stores references to both previous and next nodes
## Definitions and Implementation
### Node Class
```java
class Node {
	Object element;
	Node next;
	Node prev;
}
```
### Functions
#### Remove Last
O(1)
```java
public Node removeLast(){
	if(size == 0){
		// Throw Error
	}
	Node out;
	if(size == 1){
		out = head;
		head = null;
		tail = null;
		return out;
	}
	
	out = tail;
	tail = tail.prev;
	tail.next = null;
	return out;
}
```
#### Get Node
```java
private getNode(int i){
	Node node = head;
	for(int k = 0; k < i; k++){
		node = node.next;
	}
	return node;
}
```