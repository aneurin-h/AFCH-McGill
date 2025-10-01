## Encapsulation
Make fields `private` in general
Allows control over use/modification of data
	Can validate data before setting

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

