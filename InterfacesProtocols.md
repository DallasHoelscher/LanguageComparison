# Interfaces / protocols

* Swift
  * Interfaces
    * Swift does not have interfaces
  * Protocols
    * Swift does have protocols
    ```
    //Creating the protocol
    protocol FullyNamed {
      var fullName: String { get }
    }
    //Conforms to the FullyNamed protocol, meaning it has a fullName variable
    struct Person: FullyNamed {
      var fullName: String
    }
    let john = Person(fullName: "John Appleseed") //Ass
    ```
     Protocols can also be used for more complicated reasons, like delegating. (Code used in maply)
     ```
      protocol DataDelegate: class {
        func eventAddedToCurrentData(event: CellInfos)
        func eventRemovedFromData(eventID: String)
      }
      
      class Data {
        weak var dataDelegate: DataDelegate? //Weak so that the delegate doesnt force Data to never deallocate.
        ...
        dataDelegate?.eventAddedToCurrentData(event: eventUpdate) //Telling the delegate something happened
      }
      
      class HomeViewController: UIViewController, DataDelegate {
        Data.sharedInstance.dataDelegate = self //Assign this view controller as the delegate
        
        //Implement delegate methods
        func eventAddedToCurrentData(event: CellInfos) {
          addAnnotation(forEvent: event)
        }
        func eventRemovedFromData(eventID: String) {
            removeAnnotationWithID(eventId: eventID)

        }
      }
     
     ```
* Java
  * Interfaces
    * Java does have interfaces, typically used as a blueprint for what a class needs to follow
    ```
    //Code borrowed from the Java Docs
    
    interface Bicycle {

        //  wheel revolutions per minute
        void changeCadence(int newValue);

        void changeGear(int newValue);

        void speedUp(int increment);

        void applyBrakes(int decrement);
    }
    
    class ACMEBicycle implements Bicycle {

        int cadence = 0;
        int speed = 0;
        int gear = 1;

       // The compiler will now require that methods
       // changeCadence, changeGear, speedUp, and applyBrakes
       // all be implemented. Compilation will fail if those
       // methods are missing from this class.

        public void changeCadence(int newValue) {
             cadence = newValue;
        }

        public void changeGear(int newValue) {
             gear = newValue;
        }

        public void speedUp(int increment) {
             speed = speed + increment;   
        }

        public void applyBrakes(int decrement) {
             speed = speed - decrement;
        }

        public void printStates() {
             System.out.println("cadence:" +
                 cadence + " speed:" + 
                 speed + " gear:" + gear);
        }
    }
    ```
    <br><br>
[Home](README.md) | [Classes](Classes.md) | [ErrorsExceptions](ErrorsExceptions.md) | [InheritanceExtension](InheritanceExtension.md) | [InterfacesProtocols](InterfacesProtocols.md) | [LamdasClosures](LamdasClosures.md) | [LanguagePurpose](LanguagePurpose.md) | [Listeners](Listeners.md) | [LogicComparisons](LogicComparisons.md) | [MemoryManagement](MemoryManagement.md) | [Multithreading](Multithreading.md) | [NameSpaces](NameSpaces.md) | [NullNil](NullNil.md) | [Procedural&Functional](Procedural&Functional.md) | [Properties](Properties.md) | [Reflection](Reflection.md) | [Singleton](Singleton.md) | [Types](Types.md) | [UniqueFeatures](UniqueFeatures.md)
  
