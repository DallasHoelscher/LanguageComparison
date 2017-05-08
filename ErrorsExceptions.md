# Errors / Exceptions

* Swift
  * In Swift, errors are represented by values of types that conform to the Error protocol.
  * You can indicate that a function throws an exception
  ```
    func canThrowErrors() throws -> String
  ```
  * You can do many way combinations of do / try / catch, such as passing the error up from the function as long as you show that it throws, or you can do a do try catch. 
  ```
  //Example from apple docs
  do {
      try buyFavoriteSnack(person: "Alice", vendingMachine: vendingMachine)
  } catch VendingMachineError.invalidSelection {
      print("Invalid Selection.")
  } catch VendingMachineError.outOfStock {
      print("Out of Stock.")
  } catch VendingMachineError.insufficientFunds(let coinsNeeded) {
      print("Insufficient funds. Please insert an additional \(coinsNeeded) coins.")
  }
  ```
  * You can also assign a try to a function, if it throws an error the value is nil, otherwise its the returned value
  ```
  let x = try? someThrowingFunction()
  ```
* Java
  * In Java, errors are typically subclasses of Exception or Exception itself.
  * Example of do try catch when accessing an element out of bounds
  ```
      try {
         int a[] = new int[2];
         System.out.println("Access element three :" + a[3]);
      }catch(ArrayIndexOutOfBoundsException e) {
         System.out.println("Exception thrown  :" + e);
      }
  ```
  * Java does allow you to use multiple catch blocks in a row, starting with the most specific and working all the way out to Exception
  
  * If you do not want to directly handle the error, you can show that your function throws. 
    ```
      public void withdraw(double amount) throws RemoteException, 
        InsufficientFundsException {
        // Method implementation
      }
    ```
  * You can also use a finally block at the end to run some code whether there was something caught or not.
  ```
      try {
         int a[] = new int[2];
         System.out.println("Access element three :" + a[3]);
      }catch(ArrayIndexOutOfBoundsException e) {
         System.out.println("Exception thrown  :" + e);
      } finally {
           System.out.println("Finally was called");
      }
  ```
  <br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
