# Classes

### Java
##### Declaring
> "The class body (the area between the braces) contains all the code that provides for the life cycle of the objects created from the class" [[Source]](https://docs.oracle.com/javase/tutorial/java/javaOO/classdecl.html)
- The class body is defined by curly braces
- Classes can have the Public and Private access modifiers
```java
// Class declaration
public class MyClass {
	// Constructor
    public MyClass {
    
    }
    
    // Method declaration
    public int foo(int bar) {
    	return bar;
    }
}
```

##### Creating New Instances
- Classes provide the blueprint for creating objects
* Each of these statements has three parts (discussed in detail below): [[Source]](https://docs.oracle.com/javase/tutorial/java/javaOO/objectcreation.html)
  * **Declaration**: The code set before the "=" are all variable declarations that associate a variable name with an object type.
  * **Instantiation**: The new keyword is a Java operator that creates the object.
  * **Initialization**: The new operator is followed by a call to a constructor, which initializes the new object.

```java
MyClass foo = new MyClass();
```

##### Constructing/initializing

> The new operator instantiates a class by allocating memory for a new object and returning a reference to that memory
> 
> The new operator also invokes the object constructor

```java
public class MyClass {

	private int size;
    
	public MyClass(int size) {
    	this.size = size;
    }
    
    private int getSize() {
    	return size;
    }
}
```
* The constructor, always named the same as the class name, is used to initialize objects. This is useful to make sure the programmer does not create an object with null or default values.

##### Destructing/de-initializing

* Java has automatic garbage collection
* Java was one of the first languages to feature automatic garbage collection aka automatic memory management
* Java triggers garbage collection when an object no longer has a reference to it

### Swift

##### Declaring

* Swift features both Classes and Structs
* Classes in Swift are Pass-By-Reference while Structs are Pass-By-Value
* Much like Java, Swift also defines code between curly braces
```swift
class SomeClass {
    // class definition goes here
}
struct SomeStructure {
    // structure definition goes here
}
```

##### Creating New Instances

* Swift does not require a **new** keyword to create new instances of classes or structs
* Swift's automatic type detection makes it so you do not have to declare the class type in the initialization

To create a new instances:
```swift
let someClass = SomeClass()
let someStructure = SomeStructure()
```

##### Constructing/initializing
* Swift offers two initializers **init** and **convenience init**
* The convenience initializer is an initializer that has some default values set
  * Useful for creating an object on the fly with pre-set values
```swift
class Person {
  var name: String = ""
  var age: Int = 0

  init (name: String, age: Int) {
    self.name = name
    self.age = age
  }
}

let person = Person("John", 21)
```
##### Destructing/de-initializing
> Swift automatically deallocates your instances when they are no longer needed, to free up resources
> 
> Swift handles the memory management of instances through automatic reference counting (ARC)
> 
> [[Source]](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Deinitialization.html#//apple_ref/doc/uid/TP40014097-CH19-ID142)

* To handle additional actions when a class is being deinitialized add the following code to your class
* This is useful for completing actions before the reference is trashed

```swift
deinit {

}
```
