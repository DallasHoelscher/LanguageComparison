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
