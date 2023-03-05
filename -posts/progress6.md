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

Challenges faced:

No, my post does not demonstrate a challenge that I faced and how I addressed it or plan to address it next week. Instead, it provides examples and explanations of initializer methods, including designated and convenience initializers, and how they can be used to ensure proper object initialization and configuration.

Array:

A collection of data ordered by indexes. That means there is a specific order to list values.

For example,

    var a = "Dog"
    var b = "Cat"
    var c = "Bird"

    a = "My" + a
    ["Dog", "Cat", "Bird"] // An array of 3 items Dog has an index of 0, Cat has an index of 1, and Bird has an index of 2.

We assign an array to a constant called myArray "let myArray = ["Dog", "Cat", "Bird"]"

To access these items we use "print(myArray[0])"

Output :

    Dog 

If you have an array range as 0 to 199 we can use loops for example, 

     for counter in 0...199 {
     myArray[counter] = "My" + myArray[counter]
     print(myArray[counter])

If we do not know the range of an array. The array itself cones with handy properties one of them called as a counter. Which return how many items are in the array.

If you simply want to print out the items of the array we use

     for item in myArray {
     print(item)                //Easy way to loop through items in the array
    }

Declare a empty array :

    var emptyArray:[String]
    var emptyArray2 = [String]()    //Creating anew Array object as string type

    //Add items
    myArray.insert("pig", at:0)     //insert element in particular index not gonna override it but pushes the element

    for item in myArray {
    print(item)
    }

Output :

    Dog
    Cat
    Bird
    pig
    Dog
    Cat
    Bird

Add a number of items to the back of the array

    myArray += ["pig", "Frog"]

Output :

    Dog
    cat
    Bird
    pig
    Frog

Challenges faced: 

In terms of challenges I have faced while working with arrays, array indexes start at 0, which can sometimes lead to off-by-one errors. Another potential challenge is working with multidimensional arrays, which can require nested loops to access and manipulate elements.





















