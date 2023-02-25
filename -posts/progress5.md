---
title: "Overriding & Optional data type"
date: 2023-02-25
---

Initializers:

Initializer methods in classes ensure that a newly created object of that class is prepared for use. Additionally, customizing initializer methods allows you to set up your object according to your preferences when creating a new instance of the class.

For example, 

    class Person {
    var name = ""

    init() {          // Declare the initializer function of the specific class using "init()" keyword
    // custom init code

    init(_name:String) {
    //set name property using input parameter
    self.name = name
    }
    }

    class Employee: Person {

    var salary = 0
    var role = ""
  
    func doWork() {
      print("my name \(name)")
      salary += 1
    }
    }
 
    let myPerson = Person("priya")
    print(myPerson.name)

   Output:

    priya

If you wish to override the identical function from the person class, you can utilize the "override func(_name:String)" statement within the person() function.

Optional:
 
Utilizing the optional feature makes it possible to declare a variable or constant without initially assigning a value to it, resulting in an empty state. In other words, you can set it as nil before assigning any actual data to it. This is achieved using an optional data type, which allows the variable or constant to hold "nil" as a valid value. For instance, you could declare a variable as follows: "var a:Int? = nil"

For example, 

      class XmasPresent {

      func surprise() -> Int {
        return Int.random(in: 1...10)
      }
      }

      let present = XmasPrsent()

      // check the optional to see if it contains an object

     if present != nil{       //! Mark is used to opening the box and get whatever is inside whether it is an actual object or no.
     // it contains an object
     // call the surprise function
     print(present!.surprise())
     }

Output: 

    6

To access the object of an optional variable or constant, you need to perform an "unwrap" operation on it before use. In other words, you have to extract the actual value from the optional data type before you can work with it.
Why do we have optionals in swift?

Swift is a type-safe language, requiring programmers to be extremely precise when specifying the data type of variables and constants. As a result, Swift enforces strict rules around data types, ensuring that the correct type is used for each variable or constant.

Properties:
 
Properties are just like variables that are at the class level, they are declared at the class level, they are accessible and usable by any of the functions inside that class.

Based on the previous example, the dowork method of the employee class can access the salary property because as declared, if we had more methods in this class inside each, we would be able to access the salary.

For example, 

    class Manager: Employee {

      var teamSize = 0
      var bonus:Int {
    // This is a computed property
    //When it's accessed, the code in here will run
    //Then we'll return the value

    return teamSize = 1000
    }

    init(_name:String, _team:Int) {
    // This calls the init of the Employee class
     super.init(name)
    }
    let a = Manager("priya", 11)
    print(m.bonus)

Output:

    11000

Challenges:

While declaring properties, I have to choose a unique name if not it gonna clash with other names used in the same scope. I used multiple properties that have the same name, and then it lead to conflicts.
When using Swift, it can be challenging to work with variables or constants that are declared without initially assigning them a value, resulting in a "nil" value. This is due to the language's strict rules around data typing, requiring precise and accurate declarations of variables and constants.

References : 

    https://www.codecademy.com/learn/learn-swift
    https://www.youtube.com/watch?v=kDWDTg_RpLA
    https://www.programiz.com/swift-programming
