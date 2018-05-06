# Interfaces / Protocols
## Swift
#### What does the language support?
Swift uses protocol declared  by using the protocol keyword.
#### What abilities does it have?
A protocol defines a blueprint of methods, properties, and other requirements that suit a particular task or piece of functionality.
#### How is it used?
The protocol can then be adopted by a class, structure, or enumeration to provide an actual implementation of those requirements. Any type that satisfies the requirements of a protocol is said to conform to that protocol.
~~~
protocol SomeProtocol {
    var mustBeSettable: Int { get set }
    var doesNotNeedToBeSettable: Int { get }
}
~~~

## Java
#### What does the language support?
Java uses interfaces declared by interface keyword.
#### What abilities does it have?
An interface in java is a blueprint of a class. It has static constants and abstract methods.
#### How is it used?
It is used to achieve abstraction. By interface, we can support the functionality of multiple inheritance. It can be used to achieve loose coupling.

~~~
interface printable{  
void print();  
}  
~~~
