# Lecture 7 Slides
## Multiple Output Circuits & Joint Implementation
Combining multiple functions in order to save cost
Share gates between the functions

Steps to design:
- Create individual K-Maps
	- Group into prime implicants
- Identify shared implicant
- Add non-shared implicants
- Draw combined circuit diagram reusing the overlapped implicants
Won't *always* reduce cost
Don't have to always stick solely to prime implicants

Can pick selection of prime and non prime implicants to find optimal multi-output solution
There are likely multiple combinations to check
	Have to check all, and compare costs
Joint implementation can be worse than individual implementations
## Fan-In & Fan-Out
Fan-In
	Number of inputs to the gate
Fan-Out
	Number of gates connected to its output (number of gates it can drive)
	