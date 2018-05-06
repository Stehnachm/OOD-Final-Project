# Lambda expressions, closures, or functions as types

### Java [[Source]](https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html)
* Java previously had anonymous inner classes that acted close to lambda expressions

Previous anonymous inner class implementation:
```java
HelloWorld frenchGreeting = new HelloWorld() {
    
    String name = "tout le monde";
    
    public void greet() {
        greetSomeone("tout le monde");
    }
    
    public void greetSomeone(String someone) {
        name = someone;
        System.out.println("Salut " + name);
    }
};
```

> Lambda expressions let you express instances of single-method classes more compactly

Using the example from [here](https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html#use-case) to demonstrate the benefits of using lambda expressions over anonymous inner classes:
```java
public class Person {

    public enum Sex {
        MALE, FEMALE
    }

    String name;
    LocalDate birthday;
    Sex gender;
    String emailAddress;

    public int getAge() {
        // ...
    }

    public void printPerson() {
        // ...
    }
}
```
Class to print the Persons:
```java
public static void printPersons(
    List<Person> roster, CheckPerson tester) {
    for (Person p : roster) {
        if (tester.test(p)) {
            p.printPerson();
        }
    }
}
```

Java anonymous class implementation pre-lambda expressions:
```java
printPersons(
    roster,
    new CheckPerson() {
        public boolean test(Person p) {
            return p.getGender() == Person.Sex.MALE
                && p.getAge() >= 18
                && p.getAge() <= 25;
        }
    }
);
```
Java lambda expression simplification:
```java
printPersons(
    roster,
    (Person p) -> p.getGender() == Person.Sex.MALE
        && p.getAge() >= 18
        && p.getAge() <= 25
);
```

Lambda expressions also suppose chaining of commands on _Collections_:
```java
roster
    .stream() // The .stream() is opening a stream to obtain the source of objects
    .filter( // .filter() is used to filter values coming in
        p -> p.getGender() == Person.Sex.MALE
            && p.getAge() >= 18
            && p.getAge() <= 25)
    .map(p -> p.getEmailAddress()) // Map values to a new specified value
    .forEach(email -> System.out.println(email));
```

### Swift

The Swift equivalent to lambda expressions are **Closures**
> Closures are self-contained blocks of functionality that can be passed around and used in your code

Usage:
```swift
{ (parameters) -> return type in
    statements
}
```
```swift
reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in
    return s1 > s2
})
```
Short implementation:
```swift
reversedNames = names.sorted(by: { $0 > $1 } )
```
Even shorter implementation:
```swift
reversedNames = names.sorted(by: >)
```

Creating your own closures: [[Source]]()
```swift
let closure: (Int, Int) -> Int = { (number1, number2) in // Initializing a variable 'closure' and setting it to the value of a function
return number1 + number2
}
closure(8,2) // the result is 10 // When used it will act as a function
```
