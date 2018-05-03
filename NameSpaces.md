
# NameSpace

## Swift

#### How are name spaces implemented?
In Swift, classes are in scoped by the modules that they are in. Therefore, namespacing is implicit and not needed. 

#### How are name spaces used?
Once the class is imported all methods will be available in classes inside the module.   

After importing a class you will have access to all its methods, for example you import ClassA with a method called doSomething(), you can simply call doSomething() and swift will think you are calling ClassA.doSomething().


```import  Animals
//In Animals there is a method of age
//Both do the same thing
var age = age(16)
var age2 = Animals.age(5)
```
## Java

#### How are name spaces implemented?
In Java, a package is a namespace that organizes a set of related classes and interfaces.

#### How are name spaces used?
Packages are used in each file that belongs to the package. If no package is defined then it belongs to the default package. The package is defined at the top of the page by using the package keyword and then the package it belongs to.
```
package animals;

interface Animal {
   public void eat();
   public void travel();
}

package animals;

public class MammalInt implements Animal {

   public void eat() {
      System.out.println("Mammal eats");
   }

   public void travel() {
      System.out.println("Mammal travels");
   } 

   public int noOfLegs() {
      return 0;
   }

   public static void main(String args[]) {
      MammalInt m = new MammalInt();
      m.eat();
      m.travel();
   }
} 
```
