# Lambdas / Closures

* Swift
  * Swift uses closures
  * Closures are written in many ways
    * As a normal function
      ```
      func backward(_ s1: String, _ s2: String) -> Bool {
          return s1 > s2
      }
      var reversedNames = names.sorted(by: backward)
      ```
   * In closure expression syntax
     ```
     reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in
          return s1 > s2
      })
     ```
   * Which can then be reduced further to 
    ```
    reversedNames = names.sorted(by: { s1, s2 in return s1 > s2 } )
    ```
   * Which can be even further reduced to 
    ```
    reversedNames = names.sorted(by: { $0 > $1 } )
    ```
   * Which can be once more reduced down to
     ```
     reversedNames = names.sorted(by: >)
     ```
     
   * If you need to pass a closure expression to a function as the function’s final argument and the closure expression is long, it can be useful to write it as a trailing closure instead.
   ```
    reversedNames = names.sorted() { $0 > $1 }
   ```
   * If a closure needs to be called later, such as when a networking task is happening, you can put escaping to allow this to happen
   ```
    var completionHandlers: [() -> Void] = []
    func someFunctionWithEscapingClosure(completionHandler: @escaping () -> Void) {
        completionHandlers.append(completionHandler)
    }
   ```
* Java
  * In java it is best to use a lamda expression, which is basically a better looking version of an anonymous inner class.
    * You can create a runnable by itself and then run it by calling it
      ```
       Runnable r = () -> System.out.println("Hello world two!");
       r.run();
      ```
    * Inner class sorting vs lambda
     ```
      // Sort with Inner Class
      Collections.sort(personList, new Comparator<Person>(){
      public int compare(Person p1, Person p2){
      return p1.getSurName().compareTo(p2.getSurName());
      }
      });

      //Sort with lambda expression
      Collections.sort(personList, (Person p1, Person p2) -> p1.getSurName().compareTo(p2.getSurName()));

     ```
    * Lambdas can also be used as listeners, you can read more about that under <u>Listeners</u>
    
<br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
