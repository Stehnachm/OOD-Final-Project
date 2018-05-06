# Null Or Nill References
## Swift
#### Which does the language use? (null/nil/etc)
Swift uses nil. Optionals are a type that represents either a wrapped value or nil, the absence of a value.
#### Does the language have features for handling null/nil references?
The Optional type is an enumeration with two cases. Optional.none is equivalent to the nil literal. Optional.some(Wrapped) stores a wrapped value. You must unwrap the value of an Optional instance before you can use it in many contexts. 
~~~
let number: Int? = Optional.some(42)
let noNumber: Int? = Optional.none
print(noNumber == nil)
// Prints "true"
~~~

## Java
#### Which does the language use? (null/nil/etc)
Java uses null.
#### Does the language have features for handling null/nil references?
Null is a reference type and its value is the only reference value which doesn't refer to any object. Therefore, there is no representation of null in memory.
~~~
Object obj = null;
obj.toString();  // This statement will throw a NullPointerException
~~~
