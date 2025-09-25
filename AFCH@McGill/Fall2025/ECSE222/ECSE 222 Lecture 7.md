# Lecture 6 (cont)
## POS & SOP Forms
Resulting expression from POS & SOP can be different
- Count number of ones and zeros in K-Map, reason about groupings of either to determine which to use
SOP
- Consider cells that are 1
- Use minterms
- Use variables to represent 1, and variables complements to represent 0s
- OR terms together
POS
- Consider cells that are 0
- Use Maxterms
- Use variables to represent 0, and variables complements to represent 1s
- AND terms together
Output of either can be minimized further in some cases
*In exam setting, anything below minimal cost is accepted*
K-Maps give minimal form, not minimum form

Cost Comparison
- Costs can differ
- ![[Pasted image 20250925090124.png]]
DeMorgan (TODO)
- Can take the complement, $\bar{f}$ by switching 0s and 1s, finding SoP of this will find PoS of the the normal $f$
	- Complementing $f$ switches PoS and SoP

## Incompletely Specified Functions
If certain input combinations of a function cannot occur or do not matter, the function is called incompletely specified/
- The input combinations that cannot occur or do not matter are called don't care
Notation in a truth table:
![[Pasted image 20250925091447.png]]
Notation in a Karnaugh Map:
![[Pasted image 20250925091707.png]]

Can choose which to consider as 0s and which to consider as 1s
- Can pick combinations of 0s and 1s to provide optimum/simplest logic function
---
# Lecture 7
## Minimization Design
BCD
- Binary coded digit (0-9)
	- 4 bits (Not consider a BCD after 9/1001)
	- 001100110011 -> 333, because 3->0011, so 333 -> 0011 0011 0011
Function $f$
- Input: A digit in BCD
- Output: 1 if the digit is divisible by 3
Minimization of $f$
Truth Table:

| x1  | x2  | x3  | x4  | digit | f     |
| --- | --- | --- | --- | ----- | ----- |
| 0   | 0   | 0   | 0   | 0     | ==1== |
| 0   | 0   | 0   | 1   | 1     | 0     |
| 0   | 0   | 1   | 0   | 2     | 0     |
| 0   | 0   | 1   | 1   | 3     | ==1== |
| 0   | 1   | 0   | 0   | 4     | 0     |
| 0   | 1   | 0   | 1   | 5     | 0     |
| 0   | 1   | 1   | 0   | 6     | ==1== |
| 0   | 1   | 1   | 1   | 7     | 0     |
| 1   | 0   | 0   | 0   | 8     | 0     |
| 1   | 0   | 0   | 1   | 9     | ==1== |
| 1   | 0   | 1   | 0   |       | ==Ø== |
| 1   | 0   | 1   | 1   |       | ==Ø== |
| 1   | 1   | 0   | 0   |       | ==Ø== |
| 1   | 1   | 0   | 1   |       | ==Ø== |
| 1   | 1   | 1   | 0   |       | ==Ø== |
| 1   | 1   | 1   | 1   |       | ==Ø== |
Karnaugh Map

| x3x4**\\**x1x2 | 00  | 01  | 11  | 10  |
| -------------- | --- | --- | --- | --- |
| 00             | 1   | 0   | Ø   | 0   |
| 01             | 0   | 0   | Ø   | 1   |
| 11             | 1   | 0   | Ø   | Ø   |
| 10             | 0   | 1   | Ø   | Ø   |
$f=\bar{x_1}\bar{x_2}\bar{x_3}\bar{x_4}+\bar{x_2} x_3 x_4+x_2 x_3\bar{x_4}+x_1x_4$

## Multiple Output Functions
![[Pasted image 20250925094842.png]]
Merging two circuits to save complexity
- Fewer gates, etc
