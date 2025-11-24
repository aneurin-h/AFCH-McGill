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

