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
DeMorgan
- Can take the complement, $\bar{f}$ by switching 0s and 1s, finding SoP of this will find PoS of the the normal $f$ 