# Properties

## Swift:
Below is an example of how to create a property class within Swift as well as what the getters and setters might look like within a class. We're using temperature here to give a simple example.
```Swift
class Temperature {
    var celsius: Float = 0.0
    var fahrenheit: Float {
    get {
        return (celsius * 1.8) + 32.0
        }
    set {
        celsius = (newValue - 32)/1.8
    }
    }    
}

var temp = Temperature()

temp.fahrenheit = 89
```
A Swift property does not have a corresponding instance variable, and the backing store for a property is not accessed directly. This avoids any confusion when accessing the variable and allows us to declare the property in a single statement. All information about the property - including its name, type, and memory management characteristic - is defined in a single location as part of the type’s definition.
In addition to stored properties, classes, structures, and enumerations can define computed properties, which do not actually store a value. Instead, they provide a getter and an optional setter to retrieve and set other properties and values indirectly.

## Java:
In order to define a property in any class (we'll use a bean as an example) - supply the public getter and setter methods in that class. For example, the following methods define an int property called joggingDistance:
```Java
public class JogBean {
	    private int joggingDistance = 90;

	    public int getJoggingDistance() {
	        return joggingDistance;
	    }

	    public void setJoggingDistance(int joggingDistance) {
	        this.joggingDistance = joggingDistance;
	    }
	}
```
Java has no backing variables use in the property store and set.

No computed properties exist within Java.