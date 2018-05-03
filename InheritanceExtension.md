# Inheritance / extension

## Swift
#### Inheritance
A class can inherit methods, properties, and other characteristics from another class. Classes in Swift can call and access methods, properties, and subscripts belonging to their superclass and can provide their own overriding versions of those methods, properties, and subscripts to refine or modify their behavior.  
> Swift classes do not inherit from a universal base class. Classes you define without specifying a superclass automatically become base classes for you to build upon. 
```swift
// Bicycle is a subclass of the superclass Vehicle
// format = class subclass: superclass { subclass implementation }
class Bicycle: Vehicle {
  var hasBasket = false
}
```

Swift **doesn't allow** the declaration of a class with *multiple* base classes or superclasses, so there is **no support for multiple inheritance of classes**. A subclass can inherit just from *one* class.

#### Extension
Swift allows the addition of new functionality to existing classes, structures, enumerations, or protocol types. Swift extensions do not have names.
> Extensions can add new functionality to a type, but they cannot override existing functionality.

Swift Extensions can:
* Add computed instance properties and computed type properties 
* Define instance methods and type methods 
* Provide new initializers
* Define subscripts 
* Define and use new nested types
* Make an existing type conform to a protocol
```swift
// sample format = extension some_type { new functionality of some_type }
// another sample format = extension some_type: a_protocol, b_protocol { new protocol requirements }

extension Double {
  var km: Double { return self * 1_000.0 }
  var m: Double { return self }
  var cm: Double { return self / 100.0 }
  var mm: Double { return self / 1_000.0 }
  var ft: Double { return self / 3.28084 }
}

let threeFeet = 3.ft
print("Three feet is \(threeFeet) meters")
// Prints "Three feet is 0.914399970739201 meters"
```

## JAVA
#### Inheritance

#### Extension
