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
  * Computed property

* Java
