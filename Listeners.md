# Listeners

* Swift
  * In swift you use targets and tell them what method to call and when you'd like it called, for example with a button
    ```
      button.addTarget(self, action: #selector(self.buttonClicked), for: .touchUpInside)
      @objc private func buttonClicked() {
          // called when button tapped
      }
    ```
  * A lot of things you would use a listener for in Java you would add a delegate for in swift, i.e if you wanted to know when a view changed size, you would call delegate methods to let the delegate know you are going to change the size.
  * You can also add a willSet and didSet properties to a variable, for example : 
    ```
      var myProperty: Int = 0 {
          didSet {
              print("The value of myProperty became \(myProperty)")
          }
      }
    ```
* Java
  * In java you use lamdas / anonymous inner class for event listeners
    ```
      button.addActionListener(e -> {
          // called when button tapped
      });
    ```
  * You can also add these listeners to all sorts of things, like if a width / height changes.
