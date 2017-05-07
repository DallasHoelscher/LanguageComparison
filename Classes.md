# Classes

* Swift
  * Defining
  ```
    class Pet {
      var type: String
      init (type: String) {
        self.type = type
      }
    }
  ```
  * Initializing
  ```
    var myDog = Pet(type: "Dog") //Creates new pet with type dog
  ```
  * Deinitializing<br>
    If the variable is of optional type, you can deallocate the object by setting the reference to nil. If this is the only reference to the object, it will be deallocated. If there is another reference that isnt weak, the object will not be deallocated this way.
    ```
      //In this instance, myDog will be deallocated
    var myDog:Pet? = Pet(type: "Dog")
    myDog = nil 
    ```
    
    ```
      //In this instance, myDog will NOT be deallocated
    var myDog:Pet? = Pet(type: "Dog")
    var otherDog = myDog
    myDog = nil 
    ```
    
    ```
      //In this instance, myDog will be deallocated
    var myDog:Pet? = Pet(type: "Dog")
    weak var otherDog = myDog
    myDog = nil 
    ```
   You can test this code in playground by doing this: 
   ```
   class Pet {
    var type: String
    init (type: String) {
        self.type = type
    }
    
    deinit {
        print("Going away now")
      }
    }

    var myDog:Pet? = Pet(type: "Dog")
    print(myDog!.type)

    weak var otherDog = myDog

    myDog = nil
   ```
   * Instance reference name in data type
      * Swift uses "self"
* Java
  * Defining
    ```
    public class Pet {
      String type;
      public Pet(String type) {
        this.type = type;
      }
    }
    ```
   * Initializing
   ```
    Pet myDog = new Pet("Dog"); //Creates new pet with type dog
   ```
   * Deinitializing
    * Because Java is a garbage collected language you cannot predict when (or even if) an object will be destroyed. But for it to be destroyed, you can set the variable to be null, similar to swift. 
  ```
    myDog = null; 
  ```
  * Instance reference name in data type
    * Java uses "this"
