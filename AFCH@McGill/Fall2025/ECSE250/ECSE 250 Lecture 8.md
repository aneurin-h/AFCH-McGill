## Polymorphism
Valid declarations
```java
Beagle snoopy1 = new Beagle();
Dog snoopy2 = new Beagle();
Animal snoopy3 = new Beagle();
```
Can label with the type of the class or any superclass
Label type does not affect what type an object is, that depends on the class used to instantiate

![[Pasted image 20250929162521.png]]
Compile checks label, interpreter (JVM) checks object type

![[Pasted image 20250929163430.png]]
