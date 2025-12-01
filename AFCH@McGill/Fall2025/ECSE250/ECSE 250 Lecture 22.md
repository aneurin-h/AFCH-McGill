Recursive Sorting
# Merge Sort
## Divide
Index of middle of list: $\frac{n-1}{2}$
Get elements up to mid value for first half, and get elements from mid+1 to last index for second half
## Merge
Given two smaller lists, interleaf them such that the final list is still sorted
Choose the smallest non-added value from the 2 lists, and add to the output list
Once one list is empty, copy all remaining elements into output

# Quick Sort