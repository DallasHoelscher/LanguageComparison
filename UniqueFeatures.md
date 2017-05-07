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
Java is old enough that any unique features have now been used in many other languages as well. Java's features that make it viable to code in include being simple, object oriented, and portable.
