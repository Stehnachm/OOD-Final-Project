# Errors and exception handling

## Swift
Swift provides first-class support for throwing, catching, propagating, and manipulating recoverable errors at runtime. In Swift, errors are represented by values of types that conform to the *Error* protocol. This empty protocol indicates that a type can be used for error handling. 

There are four ways to handle errors in Swift: You can propagate the error from a function to the code that calls that function, handle the error using a do-catch statement, handle the error as an optional value, or assert that the error will not occur. 

```swift
var vendingMachine = VendingMachine()
vendingMachine.coinsDeposited = 8

do {
  try buyFavoriteSnack(person: "Alice", vendingMachine: vendingMachine)
  print("Success! Yum.")
} catch VendingMachineError.invalidSelection {
  print("Invalid Selection.")
} catch VendingMachineError.outOfStock {
  print("Out of Stock.")
} catch VendingMachineError.insufficientFunds(let coinsNeeded) {
  print("Insufficient funds. Please insert an additional \(coinsNeeded) coins.")
} catch {
  print("Unexpected error: \(error).")
}
// Prints "Insufficient funds. Please insert an additional 2 coins."

```

## Java
Some paragraph.

```java
import nothing;
```
