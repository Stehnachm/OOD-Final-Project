# Comparisons of references and values 

## Swift
```swift
let var1 = "red"
let var2 = "red"

if var1 == var2 {
    print("Both of the variables are the same word.")
} else {
    print("The two variables are different words.")
}

let newVar1 = ExampleClass()
let newVar2 = newVar1

if newVar1 === newVar2 {
    print("The two variables reference the same object.")
} else {
    print("The two variables reference different objects.")
}
```
### Code Explanation:
Output: "Both of the variables are the same word."
		"The two variables reference the same object."

This code declares two strings of the same value. An if else statement then uses the == operator to see if the strings are of the same **value**. In Swift, Strings are a value type. Since the value of both of the strings are the same, the if statement is true and executes the print statement declaring they are equal. In the second portion of the code above, since newVar2 is set equal to newVar1, then they are referencing the same Object (class in this instance) so when we check for the reference equality using === the print statement displays that they reference the same object. 

### How are values/references compared?
When comparing two strings we see that Swift’s String type is a value type. If you create a new String value, that String value is copied when it is passed to a function or method, or when it is assigned to a constant or variable. In Swift, using the == operator allows you to compare if two strings are the same. Swift also includes several methods of comparing strings using functions like the .contains() function.

For Swift using the === operator allows us to compare the reference of an object and compare the equality of two different variables through that method.


## Java
```java
int var1 = 1;
int var2 = 2;

if(var1 == var2)
	System.our.print("The values are the same.");
else
	System.our.print("The values are not the same."); //it will print this

//compare value in an Object by using .equals()
String string1 = new String("red");
String string2 = new String("red");
String string3 = string2;

if(string1 == string2)
	System.our.print("The references are the same.");
else
	System.our.print("he references are not the same."); //it will print this

if(string1 == string3)
	System.our.print("The references are the same."); //it will print this
else
	System.our.print("The references are the same.");

if(string1.equals(string2))
	System.our.print("The values are the same."); //it will print this
else
	System.our.print("The values are not the same.");

if(string2.equals(string3))
	System.our.print("The values are the same."); //it will print this
else
	System.our.print("The values are not the same.");
```

### Code Explanation:
Output: Noted in the comments of the above code

The code above shows examples of both value comparison through the use of the .equals method and as well as how to compare values using the == operator. When comparing objects though, the == will look at the object's reference and not the specific value itself.

### How are values/references compared?
As mentioned above in order to compare the object's actual values in Java we need to use the .equals method - to compare their references we can use the == operator. When attempting to compare values of single variables we can use the == operator to compare values.