---
title: "Designated Initializer & Convenience initializer"
date: 2023-03-04
---
Revisit initializer methods and designated versus convenience initializer

For example, 

    class Person {
      var name = "None"
    }

Here is a person class and it has one property called name which is initialized to the string "none".

All the classes will have a default init initializer. So, you can create a new person object like "person()".

The initialization process of a class guarantees that the object is properly configured and functional. This includes tasks such as memory allocation and other necessary operations required for object creation and return. Additionally, the initializer ensures that all properties of the object are initialized appropriately.

For example,

    class Person {

      var name = "None"
      var netWorth:Int?   //Optional integer. By default, the optional integer is assigned with "Nil"
      var gender:String!

    // By default all the properties of the person class are already initialized.
    }

    Person()

For example, If one of the properties is not initialized. 

    class Person {

      var name:String
      var netWorth:Int?   
      var gender:String!

    init() {

      name = "None"    
    // Class needs an initializer explicitly where you initialize the name property. So, in this case, we ass init and assign a value to the property.
    }
    }

    let a = Person()
 
    print(a.name)

Output :

    None
   
Designated Initializer:

A designated initializer is responsible for ensuring that an object is prepared for use and that all of its properties are properly initialized. By using a designated initializer method, you can be confident that the object will be returned and ready for use, with all its properties initialized.

Convenience Initializer:

A convenience initializer is a type of initialization method that is used to pre-configure an object in a specific manner. These types of initializers may depend on a designated initializer to ensure that the object is properly configured and ready to be used.

For example, 

    class Person {

      var name:String
      var netWorth:Int?   
      var gender:String!
    // Designated initializer because it makes sure that all properties are initialized

    init() {
       name = "None"
    }

    convenience init(_gender:String, _netWorth) {
    //Call the designated initializer to ensure that the object is ready to go 

       init()

    //Set any other properties or custom code to initialize for this scenario

       self.gender = gender
       self.netWorth = netWorth
    }

    }

    let a = Person()    //Creating a new person object


















