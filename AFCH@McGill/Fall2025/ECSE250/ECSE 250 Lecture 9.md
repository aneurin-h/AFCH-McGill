## Encapsulation
Make fields `private` in general
Allows control over use/modification of data
	Can validate data before setting
Passing of a reference type field can result in it pointing to the original value, and thus being able to be mutated from outside the class

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
