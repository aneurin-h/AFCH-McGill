# Balanced & Unbalanced Trees
Difference in height is at most 1 between children
Aims to prevent BST from being essentially a linear data structure (and thus slower)

## Complete Binary Tree
Binary tree of height $h$ such that every level less than $h$ is full, and all elements in level $h$ are as far to the left as possible.
# Priority Queue
Add whatever elements we want
Remove the element with the highest priority first
`poll` means to remove the highest priority element
Options to implement
	Use binary search tree to store in order of priority
	Heaps
# Heap
A **complete binary tree with comparable keys**
DOES NOT HAVE TO ADHERE TO THE LEFT < RIGHT RULE FROM BINARY SEARCH TREE
![[image-63.png|348x130]]
Ordering of elements in a level don't matter for heapness
## Add
Put in next available spot, and then **heapify** (swap with parent until inequalities are satisfied (IE child is greater than parent in min heap))
**Timing:**
	Worst Case:
	$O(\lfloor \log(n) \rfloor)$ More efficient over BST due to our placement rules
	Best Case:
	$\Omega(1)$
## Remove
Remove the root, replace with the latest added element, heapify
- SWAP WITH SMALLEST CHILD NODE
![[image-64.png|147x102]]Put at root
![[image-65.png|147x135]]Swap with smallest child
No More Swaps needed
## Implementation
Most commonly implemented using an array
Put into array using the priority numberings (except for index 0)
![[image-66.png|319x186]]
Incomplete tree would cause a gap in the array (hence we can't use them)
From Parent
	$\text{Left Child at index } 2i$
	$\text{Right Child at index }2i+1$
From Child
	$\text{Parent at index}\lfloor \frac{i}{2} \rfloor$
### Pseudocode
```java
class minHeap
	int size
	T[] heap

add()
	size++
	heap[size] = key
	
	i = size;
	while(i > 1 & heap[i] < heap[i/2])
		// Swap upwards
		T temp = heap[i]
		heap[i] = heap[i/2]
		heap[i/2] = temp
		i = i/2 //INTEGER DIVISION IMPORTANT

removeMin()
	temp = heap[1]
	heap[1] = heap[size]
	size--
	heapifyDown()

heapifyDown(i)
	while(2i <= size)
		smallerIndex = smallerChildIndex(i)
		
		if(heap[smallerIndex] < heap[i])
			swap(i, smallerIndex)
			i = smallerIndex
		else
			break

getSmallerChildIndex(i)
	leftChildIndex = 2i
	if(2i+1 <= size)
		rightChildIndex = 2i + 1
		if(heap[rightChildIndex] < heap[leftChildIndex])
			return rightChildIndex
		return leftChildIndex
```
## Finding