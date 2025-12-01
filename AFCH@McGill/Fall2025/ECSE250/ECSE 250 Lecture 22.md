Recursive Sorting
# Merge Sort
## Divide
Index of middle of list: $\frac{n-1}{2}$
Get elements up to mid value for first half, and get elements from mid+1 to last index for second half
## Merge
Given two smaller lists, interleaf them such that the final list is still sorted
Choose the smallest non-added value from the 2 lists, and add to the output list
Once one list is empty, copy all remaining elements into output
![[image-85.png|373x251]]
## Pseudocode
```java
mergesort(list)
	if(list.size() <= 1)
		return list
	else
		mid = (list.size() -1)/2
		list1 = list.getElements(0,mid)
		list2 = list.getElements(mid+1,list.size()-1)
		list1 = mergesort(list1);
		list2 = mergesort(list2);
		return merge(list1, list2);
```
$O(n\log_{2}(n))$
# Quick Sort
Pick an element of the array (the pivot)
Partition by moving the pivot
	All smaller elements are on one side
	All larger elements are on the other
	Implemented with swapping
Multiple ways to pick pivot
	For example, using the last element
**Example**
	Pick Pivot
	Set the wall on the left
	Go through all elements that are not the pivot, if the element is smaller than the pivot, move the wall right by one, and place the element just behind the wall
	Move the pivot next to the wall
	Recur using the left section, and with the right section
In order to implement we need:
- Swap function
- Partition function
	- Places pivot correctly
	- Moves the elements around so that all the lower elements are on the left and all the larger elements are on the right
- quickSort
	- pick a pivot
	- partition
	- recursive calls to left and right
