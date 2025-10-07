# Lecture 8 Slides
## Functional Decomposition of Five Variable Functions
Patterns can be either vertical or horizontal

Find subfunction that identifies where Pattern A is

Repeat for Pattern B, ... etc

Extract $f$ by summing products of the subfunctions with their patterns
# Lecture 9 Slides
## Base Conversions
![[image-5.png|407x192]]
Conversions from base $b$ to decimal
![[image-6.png|400x184]]

## Dynamic Operation of Logic Gates
Logic Gates use transistors
	0 and 1 are low and high voltage respectively, actual voltage depends on tech
Changing states -> moving charge around -> capacitors
Voltage over a capacitor does not change instantaneously!
```math
||{"id":850565890036}||
I_C(t) = C {dV_C(t)}/{dt}
```
It takes time to preform logic calculations
In reality, timing diagrams are not perfect
![[image-7.png|356x155]]
Both smooth changes in level, and delay between input and output

## Latency
Time it takes for change at input to propagate to output
Latency varies for each input, output, and direction of change
Latency also varies for gate type
	Different implementations of transistors have different capacitances
Faster not always better
	Setup time and hold time
	