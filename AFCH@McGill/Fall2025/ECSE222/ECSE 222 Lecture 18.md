Lecture 16 Slides
# Timing in Sequential Circuits
## Timing Parameters and Violations
Clock-to-Q time $t_{cq}$ : changes to Q occur after the positive edge of CLK
Setup time $t_{su}$ : D must be stable for $t_{su}$ before the positive edge of CLK
	Important because CLK edge may vary by a few nanoseconds
	Violation: D changes less than $t_{su}$ before the positive edge of the CLK
Hold time $t_{h}$ : D must be stable for $t_{h}$ *after* the positive edge of the CLK
	Important for same reasons as $t_{su}$
	Violation: D changes less than $t_{h}$ after the positive edge of the CLK
## Avoiding Violations
1. Make sure that clock period is sufficiently long to avoid setup time violations
2. Check for hold time violations
Two Flip Flop Example
![[image-55.png|441x209]]
$T\geq t_{su} + t_{cq}+t_{gates}$ Minimum clock period is the sum of setup, clock-to-Q time, and any gates between flipflops
$t_{cq}+t_{NOT}\geq t_{h}$
