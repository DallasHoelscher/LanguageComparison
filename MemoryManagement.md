# Memory Management

* Swift
  * ARC - Automatic Referance counting
>Every time you create a new instance of a class, ARC allocates a chunk of memory to store information about that instance. >This memory holds information about the type of the instance, together with the values of any stored properties associated >with that instance.
>
>Additionally, when an instance is no longer needed, ARC frees up the memory used by that instance so that the memory can be >used for other purposes instead. This ensures that class instances do not take up space in memory when they are no longer >needed.

>However, if ARC were to deallocate an instance that was still in use, it would no longer be possible to access that >instance’s properties, or call that instance’s methods. Indeed, if you tried to access the instance, your app would most >likely crash.

>To make sure that instances don’t disappear while they are still needed, ARC tracks how many properties, constants, and >variables are currently referring to each class instance. ARC will not deallocate an instance as long as at least one active >reference to that instance still exists
* Java
