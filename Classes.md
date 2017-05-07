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
   * Getters / Setters (example from Swift Documentation)
    ```
    struct Rect {
      var origin = Point()
      var size = Size()
      var center: Point {
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set(newCenter) {
            origin.x = newCenter.x - (size.width / 2)
            origin.y = newCenter.y - (size.height / 2)
        }
      }
    }
    ```
      Getters / Setters are built into the swift programming language
  * Computed property 
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
  * Getters / Setters
  ```
    public class Pet {
      private String type;
      public Pet(String type) {
        this.type = type;
      }
    
      public void setType(String type) {
       this.type = type;
      }
    
      public String getType() {
        return type;
      }
    }
  ```
  In java getters and setters are just regular functions implemented by the programmer.
