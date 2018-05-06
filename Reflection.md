# Reflection

Reflection is used by programs to examine or modify the runtime behavior of applications

### Java
* Using Reflection in Java you can:
  * Finding Out About Methods of a Class
  * Obtaining Information About Constructors
  * Finding Out About Class Fields
  * Invoking Methods by Name
  * Creating New Objects
  * Changing Values of Data Fields
  * Creating or Manipulating Arrays

This function will obtain all of the methods from the **Class c** and print them out [[Source]](http://www.oracle.com/technetwork/articles/java/javareflection-1536171.html)
```java
import java.lang.reflect.*;
 
   public class DumpMethods {
      public static void main(String args[])
      {
         try {
            Class c = Class.forName(args[0]);
            Method m[] = c.getDeclaredMethods();
            for (int i = 0; i < m.length; i++)
            System.out.println(m[i].toString());
         }
         catch (Throwable e) {
            System.err.println(e);
         }
      }
   }
```
Output
```java
public java.lang.Object java.util.Stack.push(java.lang.Object)
public synchronized java.lang.Object java.util.Stack.pop()
public synchronized java.lang.Object java.util.Stack.peek()
public boolean java.util.Stack.empty()
public synchronized int java.util.Stack.search(java.lang.Object)
 ```
     
 ### Swift
 * Reflection is known as **Mirror** in Swift
 > A representation of the substructure and display style of an instance of any type
 > 
 > A mirror describes the parts that make up a particular instance, such as the instance’s stored properties, collection or tuple elements, or its active enumeration case

Usage of Mirror in Swift:
```swift
let myClass = MyClass()
let myMirror = Mirror(reflecting: myClass)
```

