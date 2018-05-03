# Functional programming 
* Does the language support functional programming?

## Swift
Swift supports functional programming by allowing immutability, higher-order functions, pure functions, and functions to be treated as first class citizens (can be assigned to variables). 

```swift
func hello() {
  print("Hello World!")
}
let print = hello
print()

// Other example
func print() -> Void { 
  print("Hello world!")
}
func hello(input_function: () -> Void) { 
  input_function()
}
hello(print) // prints Hello world!
```

## Java
Java supports functional programming by treating functions as first class citizens as well and is commonly seen with the use of lambda expressions. 

```java
// lambda expression
ChangeListener<Number> listener = (ObservableValue<? extends Number> observable, Number oldValue, final Number newValue) -> {
  renderBoard();
};

// Other example
Function<Integer,Integer> add_one = x -> x + 1;

Integer num = add_one.apply(10); //yields 11
```
