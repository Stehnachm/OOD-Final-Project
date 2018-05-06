# Multi-Threading

### Java
* There are two ways to multi-thread in Java
  * Extend **Thread** or implement **Runnable** on a class
  * Multi-threading is useful for GUI applications and making applications feel more responsive
  * Multi-threading allows concurrent execution
  * Threads are light-weight processes within a _Process_

Thread usage:
```java
class ElipsesThread extends Thread
{
    public void run()
    {
        try
        {
            // Code here 
        }
        catch (Exception e)
        {
            System.out.println ("Exception is caught");
        }
    }
}
 
public class Main
{
    public static void main(String[] args)
    {
        int size = 100;
        for (int i = 0; i < size; i++)
        {
            ElipsesThread elipses = new ElipsesThread();
            elipses.start();
        }
    }
}
```

Runnable implementation differs slightly in the instantiation of a new thread:
```java
class Multithread
{
    public static void main(String[] args)
    {
        int size = 100;
        for (int i = 0; i < size; i++)
        {
            Thread elipses = new Thread(new ElipsesThread());
            elipses.start();
        }
    }
}
```

When multi-threading you may use the **join()** method on the thread.  This will make it so the first thread will finish before continuing on to the second. This is useful if you need results returned back in order.  Ex [[Source]](https://stackoverflow.com/a/18480296):
```java
class Demo {
   Thread t1 = new Thread(new Runnable() {
       public void run () {
           //do something
       }
   });
   Thread t2 = new Thread(new Runnable() {
       public void run () {
           //do something
       }
   });
   
   t1.start();
   t1.join();
   t2.start();
}
```

### Swift
* Utilizes service called **Grand Central Dispatch (GCD)** to manage multi-threading
* Task are put onto the queue to be handled off of the main thread
* For iOS, and other UI applications, you normally cannot update the main thread from another thread
  * Multi-threading gives you the ability to run additional functionality without halting the main thread

Example of multi-threading in Swift:
```swift 
DispatchQueue.global(qos: .userInitiated).async {
    // Download file or perform expensive task
	
    DispatchQueue.main.async { // When the process is complete update the UI with results
        // Update the UI  
    }
}
```

A comparable multi-threading technique to Java is the usage of **Operation Queues**.  These function much like Java's multi-threading.  Created like so:
```swift
let operationQueue: OperationQueue = OperationQueue() // Creates an OperationQueue
operationQueue.addOperations([operation1], waitUntilFinished: false) // operation1 can a fuction 
```
```swift
class CustomOperation: Operation {
    override func main() {
        guard isCancelled == false else {
            finish(true)
            return
        }
        
        // Do something
        
        finish(true)
    }
}
```
Like Java's **join()** method, Swift has the ability to set dependencies which acts the same as join()
```swift
operation2.addDependency(operation1) //execute operation1 before operation2
```
