# Types

* Swift <br>
  * In swift, both reference types and value types are supported. 
  ```
    // Value type example
    struct S { var data: Int = -1 }
    var a = S()
    var b = a						// a is copied to b
    a.data = 42						// Changes a, not b
    println("\(a.data), \(b.data)")	// prints "42, -1"
  ```

  ```
    // Reference type example
    class C { var data: Int = -1 }
    var x = C()
    var y = x						// x is copied to y
    x.data = 42						// changes the instance referred to by x (and y)
    println("\(x.data), \(y.data)")	// prints "42, 42"
  ```
  Swift goes a step further to categorize into two data types, named types and compound types.
  * A named type is a type that can be given a particular name when it is defined. Named types include classes, structures, enumerations, and protocols
  * A compound type is a type without a name, defined in the Swift language itself. There are two compound types: function types and tuple types.
* Java
  * Value types
    * Java has 8 value types, and you cannot create your own.
      * 8 value types : byte, short, int, long, float, double, boolean, char
  * Reference types
    * All value types made by users are reference types, meaning we as programers can only create objects. 
    ```
      // Reference type example
      public class Bicycle {
        //Methods / variables go in here
      }
    ```
    * To be clear, users cannot create value types in Java, unlike swift.
<br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
