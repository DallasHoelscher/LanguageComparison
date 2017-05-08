# Inheritance / extension
* Swift
  * Inheritance - Swift allows you to inherit from other classes
  ```
    class SomeSubclass: SomeSuperclass {
      // subclass definition goes here
    }
  ```
  
  * Exensions <br>
  Extensions add new functionality to an existing class, structure, enumeration, or protocol type. This includes the ability to extend types for which you do not have access to the original source code (known as retroactive modeling).
   * Extensions in swift can : 
    * Add computed instance properties and computed type properties
    ```
    //Example of adding computed property
    extension Double {
        var km: Double { return self * 1_000.0 }
        var m: Double { return self }
        var cm: Double { return self / 100.0 }
        var mm: Double { return self / 1_000.0 }
        var ft: Double { return self / 3.28084 }
    }
    ```
    * Define instance methods and type methods
    * Provide new initializers
    * Define subscripts
    * Define and use new nested types
    * Make an existing type conform to a protocol
     ```
      //Example of making existing type conform to a protocol
      extension SomeType: SomeProtocol, AnotherProtocol {
       // implementation of protocol requirements goes here
      }
     ```
  
* Java

  * Inheritance - Java allows you to inherit from other classes
  ```
    public class SomeSubclass extends SomeSuperclass {
      // subclass definition goes here
    }
  ```
  * Extensions - Java does not allow extending types.
