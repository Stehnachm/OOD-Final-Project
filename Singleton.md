# Singleton 

## Swift
```swift
class Singleton {
    static let sharedInstance = Singleton()
    private init() {}
    var names : [String] = []
}

Singleton.sharedInstance.names = ["String1", "String2"]

print(Singleton.sharedInstance.names)
```
### Code Explanation:
Output: ["String1", "String2"]

In swift, A Singleton can be declared in the manner specified above. The singleton pattern is a software design pattern that restricts the instantiation of a class to one and only one object. In the code above we can see a class called Singleton is declared with a static constant called sharedInstance of type Singleton. A private init() is then created which prevents others from using the default initializer for this class. A local variable names of type string array is then declared for illustration purposes. In the lines outside of the class the contents of the Singleton names array is printed.

### Can it be made thread-safe?
Swift singleton creation is thread safe. This doesn't guarantee that the functions you call in the singleton instance will be magically thread safe. There are several methods that can be implemented to make the functions that you call within the singleton to be thread safe.

### Can the singleton instance be lazily instantiated?
In our implementation, the singleton cannot use the lazy keyword for instantiation. The singleton can have variables that are lazily instantiated.

## Java
```Java
public final class Singleton {
    private static final Singleton INSTANCE = new Singleton();

    private Singleton() {}

    public static Singleton getInstance() {
        return INSTANCE;
    }
}
```

### Code Explanation
For Java, we simply have a class that creates a single instance of the desired resources/object for us. From there we're able to access that instance that we created by calling a getter on that class.

### Can it be made thread-safe?
Yes we can make it thread safe by implementing some sort of dead-lock on the singleton in which case you could make it thread safe through that. (i.e. just make a binary variable for example that states whether it's currently "in use" - if it is being used, don't let it be called in another thread)

### Can the singleton instance be lazily instantiated?
Yes it can be lazily instantiated, we just need to check for whether the instance is null or not before it's sent to where it's called. If it is null we instantiate it - otherwise we just return the single instance of it.