# Singleton

* Swift 
  * In swift a singleton is implemented by : 
    ```
    class mySingletonClass {
      static sharedInstance = new mySingletonClass();
      
      private init() {
        //Prevent further creations. 
      }
    }
    ```
   * In swift, by default this singleton will be lazy and thread safe. This doesnt mean that the methods inside are thread safe, and will still need more work to make sure that they are also thread safe.
   
* Java
  * In java a singleton can be implemented by : 
  ```
   public class Singleton {
       public static Singleton sharedInstance = new Singleton( );
       private Singleton() { }
    }
  ```
  * In java a lazy singleton is implemented by : 
  ```
  public class LazyInitializedSingleton {

        private static LazyInitializedSingleton instance;

        private LazyInitializedSingleton(){}

        public static LazyInitializedSingleton getInstance(){
            if(instance == null){
                instance = new LazyInitializedSingleton();
            }
            return instance;
        }
    }
  ```
  * In java the singleton can be made thread safe by adding these methods : 
     ```
     private static class SingletonHolder { 
          public static final Singleton instance = new Singleton();
      }

      public static Singleton getInstance() {
          return SingletonHolder.instance;
      }
     ```
  
