Lecture 15 Slides
# SR Latch
Set & Reset
Holds memory
![[image-42.png|239x179]]![[image-43.png]]![[image-44.png|194x179]]
$S=1, R=1$ Case will oscillate, and so that behavior is don't care
## Gated SR Latch
Has a `CLK` Input, operate as SR Latch while `CLK=1`, hold state otherwise
![[image-46.png|304x147]]![[image-47.png|181x186]]![[image-48.png]]
Level sensitive: Change depends on the *level* of `CLK`
Can be implemented using either AND and NOR gates, or simply all NAND gates
## Gated Data (D)-Latch
Has a D input, which is connected to both S and R, with a NOT gate on R
Removes $S=R=1$ case
Means that we can only read when `CLK=0`
![[image-49.png]]![[image-50.png|218x162]]
# Master-Slave D Flip-Flop
