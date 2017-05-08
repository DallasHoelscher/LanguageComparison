# Multithreading

* Swift
  * In swift, multithreading can be quite easy becuase of something called Grand Central Dispatch which handles all of the multithreading for you.
  ```
    DispatchQueue.global(attributes: [.qosDefault]).async { 
        // Background thread
        DispatchQueue.main.async(execute: { 
            // UI Updates on main thread
        })
    }
  ```
  
* Java
  * Multi threading isn't neccessarily harder in Java, but requires a lot more steps.
    * Multithreading by extending the Thread class
      ```
      class MultithreadingDemo extends Thread{  
        public void run(){  
          System.out.println("My thread is in running state.");  
        }   
        public static void main(String args[]){  
           MultithreadingDemo obj=new MultithreadingDemo();   
           obj.start();  
        }  
      }
      ```
    * and by implementing Runnable
    ```
    class MultithreadingDemo implements Runnable{  
      public void run(){  
        System.out.println("My thread is in running state.");  
      }   
      public static void main(String args[]){  
         MultithreadingDemo obj=new MultithreadingDemo();  
         Thread tobj =new Thread(obj);  
         tobj.start();  
     }  
    }
    ```
