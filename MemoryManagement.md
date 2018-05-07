# Memory Management

## Swift
```swift
class User {
    var name: String
    
    init(name: String) {
        self.name = name
        print("User \(name) is initialized")
    }
    
    deinit {
        print("User \(name) is being deallocated")
    }
}

do {
    let user1 = User(name: "Matt")
}
```
#### Code Explanation:
When this playground is run we can see when ARC handles the allocation and deallocation of memory for the User object. Print statements fire when allocation of memory happens in the init and when deallocation of memory happens in deinit for demonstration purposes.

### How is it handled?
Swift handles much of the memory management of applications behind the scenes. Swift allocates or deallocates memory on your behalf using a method called Automatic Reference Counting or "ARC". Using ARC allows for developers to be able to reliably predict when memory will be allocated or deallocated based on reference counts.
### How does it work?
Apple Summaries how ARC works by saying: "Swift uses Automatic Reference Counting (ARC) to track and manage your app’s memory usage. In most cases, this means that memory management “just works” in Swift, and you do not need to think about memory management yourself. ARC automatically frees up the memory used by class instances when those instances are no longer needed."

### Step by step:

   -Allocation (memory taken from stack or heap)

   -Initialization (init code runs)

   -Usage (the object is used)

   -Deinitialization (deinit code runs)

   -Deallocation (memory returned to stack or heap)
   
### Garbage collection?
Swift uses ARC as opposed to garbage collection.



## Java
*Automatic Memory Management*
The Java Virtual Machine (JVM) handles all of the memory and allocates/ deallocates when necessary. The JVM and garbage collection takes this so seriously, that Java will not allow the developer to access memory.


### How is it handled?
Memory allocated on the heap is managed automatically. The heap is created when the JVM starts and increases or decreases in size while an application runs.

### How does it work?
A heap is divided into two areas called the nursery and old space. The nursery is for new objects. If the nursery becomes full then there is a special, 'young collection' that is run. If an object has lived long enough then it is moved to the old space. If the old space becomes full then there is a process of 'old collection' in which the old collection is taken out like garbage.

### Garbage collection?
When the heap becomes full, the garbage is collected. During the garbage collection objects that are no longer used are cleared - making space for new objects.

