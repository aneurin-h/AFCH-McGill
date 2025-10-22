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
	size = 0, size = 1 cases etc.
Exist at head and tail of an empty Linked List
Stores nothing
Helps with edge cases:
No need for if statements when removing Nodes!
```java
public Node remove(int i){
	if(size = 0 || i < 0 || i >= size){throw new Exception();}
	Node node = getNode(i);
	// Pretty Neat, erases self
	node.prev.next = node.next;
	node.next.prev = node.prev;
	
	size--;
	
	return node;
}
```
```java
public Node removeLast(){
	if(size = 0){throw new Exception();}
	Node out = dummyTail.prev;
	
	node.prev.next = node.next;
	node.next.prev = node.prev;
	
	size--;
	
	return out;
}
```
```java
public Node removeFirst(){
	if(size = 0){throw new Exception();}
	Node out = dummyHead.next;
	
	node.prev.next = node.next;
	node.next.prev = node.prev;
	
	size--;
	
	return out;
}
```
# Space Complexity
All three data structures use space O(N) for a list of size N
Linked lists use 2x (Single) or 3x (Double), the memory when compared to an array

# Java List Libraries
Disallowed on assignments
Types specified with a type parameter
## ArrayList
Uses an array as underlying data structure
Grows by 50% not 100% during a resize
## Linked List
Doubly Linked List
