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
	size--;
	return out;
}
```
#### Get Node
O(N)
```java
public get(int i){
	if(/* i is outside range*/){
		//Throw Exception
	}
	
	
	Node node = head;
	for(int k = 0; k < i; k++){
		node = node.next;
	}
	return node;
	
	//OR 
	
	Node node;
	if(i > size/2){
		node = tail
		for(int k = size -1; k>i; k--){
			node = node.prev;
		}
	} else {
		for(int k = 0; k<i; k++){
			node = node.next;
		}
	}
	return node;	
}
```
# Dummy Node
Edge cases require more code
	size = 0, size = 1 cases etc
Exist at head and tail of an empty Linked List
Stores nothing
Helps with edge cases:
```java
public Node remove(int i){
	Node node = getNode(i);
	// Pretty Neat, erases self
	node.prev.next = node.next;
	node.next.prev = node.prev;
	
	size--;
	
	return node;
}
```