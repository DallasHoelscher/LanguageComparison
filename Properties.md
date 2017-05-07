# Properties

* Swift
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
  * Computed property <br>
  Swift has computed properties built into the language
   ```
   struct XY {
    var x = 9
    var y = 15
    
    var yMinusX: Int {
        return y - x   //Computed property
    }
   }

   var xy = XY()
   var this = xy.yMinusX //Returns 6
   xy.x = 14
   this = xy.yMinusX //Returns 1
   ```
   
* Java
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
   * Computed property <br>
   Java does not have built in computed properties, but can technically be made through using functions similar to a getter.
