# Bubble Sort
Iteration 1
	Compare all adjacent elements
	If needed, swap
After first iteration,
	Smallest element is anywhere except final (N-1) position
	Largest element is at the end
Can stop one step earlier, because we know the last element
Count number of swaps, if none preformed, end
	Track using boolean initialized to false, and set to true on swap
$\Omega(N)\:\&\:O(N^2)$
# Selection Sort
Iterate through list looking for smallest element, place that first
Repeat by iterating though smaller section of list
Don't need to check on iteration N-1, as 1 element is sorted on its own
$\Omega(N^2)\:\&\:O(N^2)$
# Insertion Sort
Takes next element, moves down until it is in correct space using a sequence of swaps
Must do all loops
$\Omega(N)\:\&\:O(N^2)$

# Operations Needed
Bubble & Selection -> swap
Insertion -> insertion

## Swap
ArrayList
```java
	tmp = list[i];
	list[i] = list[j];
	list[j] = tmp;
	```

# Best Case Time Complexity
Big Omega, ex: $\Omega{}(N),\:\Omega{}(N^2),\:\Omega{}(Nlog(N)),\:etc$ 