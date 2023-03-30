---
title: "Class & Subclasses"
date: 2023-02-18
---

Class:

A class is a template or a blueprint

Syntax: 

    class name{
      
      define class
    }

For example, 

    class student {
                
         var name = ""
         var department = ""

     func changeCourse(){
       print("I'm \(name) want to change course")  
    }
    }
         let a:String = "priya"
         var b:student = student()
      c.name = "rudroju"
      c.department = "computer science"
         print(c.department)
         c.changeCourse()

Output:

    I'm rudroju want to change course

When you declare a function inside a class is called the "method of that class".

The variables defined inside a class are called "properties".

Subclassing:

It is another way to further organize classes. Subclass is a way to extend one class from the other.

For Example, (Based on the above example)

    func changeCourse(){
     print("Hi my name is (\name) and I'm doing work")
    }
    }
     class A: B{
    override func changeCourse()   //to change definition of changeCourse() can be read by using override 
     print("I'm Student")              
    }
     var m = A()
     m.name = "priya"
     m.course = "computer science"
     m.changeCourse()

Output:

    I'm Student

If you wanted to increase the functionality you can call changeCourse() method of the B class inside override by using the "Super" keyword.

    Override func changeCourse(){
     super.changeCorse()


Output:

    Hi my name is priya and I'm doing work
    I'm student

UI-Kit:

UI-Kit is an iOS framework created by Apple that offers a vast collection of pre-designed classes required to create iOS applications. 
Designing each user interface element from scratch when creating an application can be a tedious and time-consuming task. However, UI-Kit provides a library of pre-built elements that developers can use, saving significant time and effort.
UI-Kit contains lots of user interface elements. It also uses some inheritance and subclassing.

Apple has addressed the issue of time-consuming UI design in app development by providing a collection of pre-built libraries, which they have named UI-Kit. 
This library contains numerous user interface elements, and employs inheritance and subclassing to organize and structure these elements. Through this organization, UI-Kit demonstrates how each of these elements are derived from other, more general elements.

UI-Kit has several subclasses, including UI Button, which is a subclass of UI Control. UI Control, in turn, is a subclass of UI View, which is a subclass of UI Responder. UI Responder is a subclass of NsObject. This hierarchical structure is employed in UI-Kit to organize and categorize user interface elements.

Challenging part:

Mastering the syntax of subclassing and comprehending the workings of UI-Kit can be quite challenging. UI-Kit has a hierarchical structure of classes, and gaining an understanding of how these classes are interrelated is essential. When working with subclassing, it's crucial to be meticulous and pay attention to small details to ensure error-free coding. Properly subclassing a class and overriding its methods can be a daunting task, as it necessitates a deep understanding of how the parent and child classes interact.
