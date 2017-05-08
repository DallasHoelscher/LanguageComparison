# Reflection
* Swift
  * Swift doesnt really allow reflection, although they did add some support to make playgrounds work. 
  ```
    class Fruit {
      var name="Apple"
    }

    reflect(Fruit()).count         // 1
    reflect(Fruit())[0].0          // "name"
    reflect(Fruit())[0].1.summary  // "Apple"
    
    //From what ive read all reflection is read only.
  ```

* Java
  * Java allows reflection
   ```
    Method method = foo.getClass().getMethod("doSomething", null); //Get the method named "doSomething"
    method.invoke(foo, null); //Invoke the method if there was one
   ```
   * Uses
     * A major use for reflection is to look for @Test annotations for unit test cases
     * An application may make use of external, user-defined classes by creating instances of extensibility objects using their fully-qualified names.
     * Class Browsers and Visual Development Environments

<br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
