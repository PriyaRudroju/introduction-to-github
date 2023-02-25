---
title: "Optional"
date: 2023-02-18
---
  
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
