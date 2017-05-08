# Unique Features

* Swift <br>
  * ARC (Automatic Reference Counting) - ARC keeps track of how many references there are to an object and whether they are strong or weak, if there is no strong reference to an object, it is deallocated. 
  * Optionals - Swift handles nil objects in a convenient way, by using Optionals. An Optional is data type that is known to possibly be nil, so in Swift I could have an optional integer,
  ```
  var x: Int? = 7
  ```
  and this Integer can be set to nil ```x = nil``` with no errors. Now if I want to use this variable I can easily check to make sure that its safe by doing ```if let x = x {//Use x}```
  * Guard statement - The guard statement is a way to permanently unwrap a value inside a function, basically if the value cant be unwrapped you leave the function. This saves you from putting all your code inside an if let.
  ```
  guard let x = x else {
        return
    }
    //If x wasn't nil, notice there is no need to unwrap x
    print(x)
    ```
* Java <br>
Java is old enough that any unique features have now been used in many other languages as well. Java's features that make it viable to code in include being simple, object oriented, and portable. Another great feature to Java is that bugs that could crash the system are easily caught, allowing the program not to crash on users. 

<br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
