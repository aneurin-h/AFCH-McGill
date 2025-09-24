[Slides](https://mycourses2.mcgill.ca/d2l/le/lessons/800870/topics/8711937)

# OOP Part 3:
## Abstract
**Abstract methods** are not defined in superclass
	Uses `abstract` keyword, and not implementation block
**Abstract classes** contain abstract methods (and fields and other methods)
	Also uses `abstract` keyword
	Cannot be instantiated
		Constructors will be called when subclass is instantiated
	Subclasses must implement all abstract methods or be `abstract` themselves
## ArrayList
Datastructures
	Ways of handling a list of elements
Typical Functionalities
	```get(i)
	set(i,e)
	add(e)
	add(i,e)
	remove(i)
	remove(e)
	clear()
	isEmpty()
	size()```
![[Pasted image 20250924163159.png]]
Initial Capacity: size of underlying array when object created
Simple Function implementations:
```java
public class DogList{}
	private Dog[] arr;
	private int size;
	
	public DogList(){
		arr = new Dog[10] //Some initial guess for size
		size = 0;
	}
	
	public Dog get(int i){
		if(i >= 0 && i < size){
			return arr[i];
		} else {
			//Throw an exception
		}
	}
	
	public Dog set(int i, Dog d){
		if(i >= 0 && i < size){
		Dog temp = arr[i];
		arr[i] = d;
		return temp
		}
	}
	
	public void add(Dog d){
		if(arr.length == size){
			resize();
		}
		arr[size] = d;
		size = size + 1;
	}

	private void resize(){
		Dog[] bigger = new Dog[2*arr.length];
		for(int i = 0; i < arr.length; i++){
			bigger[i] = arr[i];
		}
		this.arr = this.bigger;
	}
	
	public void add(int i, Dog d){
		if(arr.length == size){
			resize();
		}
		
		shiftDown(i);
		
		arr[i] = d;
		size++;
	}
	
	private void shiftDown(int i){
		for(int j = size; j > i; j--){
			arr[j] = arr[j-1];
		}
	}
	
	public Dog remove(int i){
		for(int j = i; j < size-1; j++){
			arr[j] = arr[j+1];
		}
		
		size--;
		
		return arr[size];
	}
}
```
