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

### instanceOf keyword
returns true or false, depending on whether object is instance of specified type
```java
Dog myDog = new Dog();
myDog instanceOf Dog // True
myDog instanceOf Beagle // False
```
Use to make sure that downcasting will not cause runtime error

## Object
Only class in Java that doesn't have a superclass
Default superclass
Has a constructor that does nothing
Has methods:
- toString
- hashCode
- equals
Overriding toString allows displaying the content of an Object with private fields
### Hash code
32 bit integer represented in hexadecimal

### equals()
```java
obj1.equals(obj2)
```
`true` if they are equal, `false` otherwise
String override: same sequence of characters
