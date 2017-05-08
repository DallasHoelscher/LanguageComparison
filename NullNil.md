# Null vs Nil

* Swift 
  * Swift uses nil
  * Swift has features using nil
    * Optionals - Swift will handle calling a function if the reference is null
      ```
      x?.callSomeMethod() //Wont crash if x is nil
      ```
    * nil coalescing operator - 
      ```
      let x = someOptional ?? 7 //let x be the optional value or 7 if the optional is nil
      ```
* Java
  * Java uses null
    * Doesn't have features to handle if something is null, but you can manually check if something is null i.e
      ```
       if( x != null) {
          x.callSomeMethod() //Wont crash because we checked x
       }
      ```
       if x is null, and you just do ```x.callSomeMethod()``` the program will throw an Exception

<br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
