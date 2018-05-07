# Instance reference name in data type (class)
Instance reference refers to the referencing of members from within an instantiated object.

## Swift
Swift uses *self* to reference current scope.


```swift
class ExampleClass{
    var exampleVariable:Int?
    
    init(number:Int){
        print("Hello World")
        self.exampleVariable = number
    }
}

```
#### Code Explanation:
In the class, the initializer takes in an Int and using *self* will set that to the variable on the class named exampleVariable. 


## Java
Java designates the *this* keyword for referencing members of an instantiated object from within a constructor or an instance method.

```java
public class Pet {
	private String name;
	private String gender;

	/* Creates a male pet named Pete using the Pet constructor
	from the previous example */
	public Pet() {
		this("Pete", "male");
	}

	public Pet(String name, String gender) {
		this.name = name; // this.name references the current object instance
		this.gender = gender; // this.gender references the current object instance
	}
}
```

#### Code Explanation:
*An example illustrating the use of instance referencing from within a constructor in Java*

In addition to referencing class properties, the *this* keyword in Java can be used to call another constructor in the same class.
