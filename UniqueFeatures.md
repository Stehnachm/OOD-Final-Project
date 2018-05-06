# Unique features of the language

## Swift
```swift
var var1:String?
var var2:Int?

if let unWrap:String = var1{
    //Assuming that "var1" is not nil, then we would be able to access the contents of "var1" through the variable "unWrap"
}

guard let testVar:Int = var2 else{
    //By using "guard" we are able to test whether "var2" is nil - if it is, then we'll handle it here
}

//If variable2 is not nil, its data will not be in "testVar" and you can access it where needed below the "guard"

```
#### Code Explanation:
One of the cool features of Swift is the ability to create Optional Variables. Essentially what that means is that we wrap the contents of the data in a container that can be set equal to nil. This is unique in that we can wrap any data-type in a container instead of just classes like other Object Oriented Languages. In the code above, there are two variables both created as "optional" by appending a question mark to the end of the data-type. From there, we have an "if let" statement that will set "unWrap" equal to the contents of var1 if and only if var1 is **not** nil. Then next conditional statement is a "guard let" which if "var2" is nil will then go into the block of code to handle that case. If the optional variable is not nil, then we can access the contents of "var2" below the "guard let."

## Java
#### Unique Features:
With Java, since it was one of the first main Object Oriented Programming languages, there aren't as many specific "unique" features with Java as there are with other languages since many of the newer OO languages took from specific aspects of Java and built on them. Thus some of the things that make Java more Java-esque are that it is:
* Simple
* Secure
* **Portable**
* Robust (large set of libraries available to it)
* Architecture-neutral (to a degree)
* High Performance
* Distributed
* Dynamic 