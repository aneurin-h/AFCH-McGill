# Computational Complexity
Running Time: The number of steps/operations executed

Running Time depends on input size
	N = input size
	t(N) = running time as a function of input size
Operation times can vary between operations
## Expressing Running Time
In worst case, algorithm takes O(N)
1. Find running time as function of input size
2. Use asymptotic notation to express running time (remove constants)
## Example: Array List Add Method
Worst case: Resizing

```java
private void resize(){
	Dog[] bigger = new Dog[arr.length * 2] // Takes time c_1, run once
	
	for(int i = 0; i < size; i++){
		bigger[i] = arr[i]; // Takes time c_2, run N times
	}
	
	arr = bigger // Takes time c_3, run once
}
```
$O_{resize}(N)=c_1+c_2N+c_3$
`add()` is thus also $O(N)$

**Add method with index:**
Worst Case: Resizes ($O(N)$) & Shifts array N times ($O(N)$)
Overall method is $O(N)$

**Remove method:**
Worst case: Remove first element
Runs shifting $N$ times
Overall is $O(N)$

# Singly Linked Lists