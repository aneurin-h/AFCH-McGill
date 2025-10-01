## Encapsulation
Make fields `private` in general
Allows control over use/modification of data
	Can validate data before setting
Passing of a reference type field can result in it pointing to the original value, and thus being able to be mutated from outside the class

## Deep Copying
Uses `new` keyword
Then fills all indices (array) with their respective data
	Or equivalent for Objects

### Getter and Setters
Public methods to access or change data
Most Getters look like this:
```java
public <type> getName(){
	return this.name;
}```
Most Setters look like this:
```java
public void setName(<type> name){
	this.name = name;
}
```


## Final keyword
Value cannot be changed
`final` instance variables (Fields) must be initialized in every constructor
`final` class variables (static) must be initialized in place

`final` classes cannot be extended
`final` methods cannot be overriden
