# LogicComparisons

* Swift
  * To compare two references you use ===. This will tell you if two variables are the same reference. 
  ```
  let dogOne = Dog()
  let dogTwo = dogOne
  
  if dogOne === dogTwo {
    print("Same reference") //Prints Same reference
  }
  ```
  * To compare two value types you use ==. 
  ```
  let x = 7
  let y = 7
  if x == y {
    print("same") // Prints same
  }
  ```


* Java
  * To compare two references you use ==.
  * To compare two value types you use the .equals method on the class.
  
  ```
    Integer intOne = 176;
    Integer intTwo = 176;

    if(intOne == intTwo) {
        System.out.println("Same");    
    } else {
        System.out.println("Not same");    //Prints not same, because the references are not the same
    }

    if (intOne.equals(intTwo)) {
        System.out.println("Same");       //Prints same, becuase values are the same
    } else {
        System.out.println("Not same");
    }
  ```
<br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
