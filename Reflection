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
