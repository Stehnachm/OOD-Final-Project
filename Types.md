# Types
* What types does the language support?
* Are both reference and value types supported?
* Can new value types be created?
## Swift
#### What types does Swift support?
Swift allows two kinds of types:
1. **named types** - types that can be given a particular name when defined.
    * Data types that are normally considered basic or primitive in other languages (such as types that represent numbers, characters, and strings) are actually named types in Swift.
    * Named types also include classes, structures, enumerations, and protocols.

```swift
// Named Type Examples:
var name: String = 'Hello World'
var number: Int = 42

```

2. **compound types** - types without a name, defined in the Swift language itself
    * There are two compound types: function types and tuple types.
        * **tuple type** - a comma-separated list of types, enclosed in parentheses. 
        * **function type** - A function type represents the type of a function, method, or closure and consists of a parameter and return type separated by an arrow (->). `(parameter_type) -> return_type`
```swift
// Compound Type Examples:

// tuple type
var tuple = (x: 2, y: 4)      // tuple is of type (x: Int, y: Int)
tuple = (x: 12, y: 55)        // Valid - names are correct
tuple = (100,1)               // Valid - names are inferred
tuple = (red: 13, blue: 87)   // Error - wrong names used

// function type
func someFunction(left: Int, right: Int) {}
var f = someFunction // The type of f is (Int, Int) -> Void, not (left: Int, right: Int) -> Void.
```
### Special Features
Swift uses type inference extensively, allowing you to omit the type or part of the type of many variables and expressions in your code. For example, instead of writing `var x: Int = 0`, you can write `var x = 0`, omitting the type completely; the compiler correctly infers that *x* names a value of type *Int*.

Swift also allows **optional types** which represent a variable that can hold either a value or no value. ex: 
```swift 
var num: Int?
```

#### Are both reference and value types supported?
Yes both reference and value types are supported.

#### Can new value types be created?
You can create a new name for an existing type using **typealias** in Swift. `typealias newname = type`
```swift
typealias Feet = Int
var distance: Feet = 100
print(distance)
//output: 100
```

## JAVA
Some paragraph.

```java
import nothing;
```
