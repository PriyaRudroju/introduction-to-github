---
title: "Mini-project reflection"
date: 2023-03-29
---

## Skills/Knowledge  
The mini-project involves developing an iOS application that simulates a coin toss.

1. Swift programming language: Understanding the basics and concepts of swift programming language which is further used to write the code for the app, implementing and connecting user interface elements(labels, buttons, etc) to the code.

2. User interface: Designing user interface using UIKit. The user interface includes auto layout and UI elements(labels, buttons, etc). A user interface can build using a storyboard with the drag-and-drop method.

3. Handling Application: Managing user-interactive applications can be challenging, especially when it comes to keeping track of important data such as the number of coin tosses in an application.

4. Debugging: Identifying and resolving errors during the development process is essential, and this process is significantly aided by keeping track of important data.

These main skills/knowledge are crucial for building effective and functional iOS applications.


## Additional skills/knowledge  
Additional Skills that may need to be learned to complete the task include knowledge of the swift language, Xcode, and iOS frameworks. These tools help to create apps that are user-friendly and compatible with different iOS versions.

Understanding delegates and protocols in swift which are used to communicate between different modules within the app.

for example, 

    public class CoinToss {
    var coin: Coin?
    public weak var delegate: CoinTossDelegate?
    
Viewcontroller.swift: This module contains the view controller, which is responsible for managing the app's user interface. It will communicate with the model classes and update the view based on the state of the model. 

For example, 

     tossCounter = TossCounter()
        coinToss = CoinToss()
        coinToss?.delegate = self
    }

    @IBAction func onButtonClick(_ sender: Any) {
        tossCounter?.increment()
        tossCount.text = "Toss Count: \(tossCounter?.count ?? 0)"
        coinToss?.tossCoin()
    }

    @IBAction func refreshCount(_ sender: Any) {
        tossCounter?.count = 0
        tossCount.text = "Toss Count: \(tossCounter?.count ?? 0)"
    }
    }

The concept of state handling/managing to keep track of the number of coin tosses when the user clicks the button("Flip coin"). 

for example,

    public class TossCounter {
    public var count = 0
    
    public func increment() {
        count += 1
    }
    }

To ensure the randomness of the coin toss results, it is necessary to implement a random number generation algorithm in the "coin toss" app using Swift programming language.

for example,

    public func tossCoin() {
        let random = Int.random(in: 0...1)
        coin = random == 0 ? .heads : .tails
        delegate?.didTossCoin(self)
    }
    }


## Challenges  

The biggest challenge is making sure an iOS app works as intended including making sure it is compatible with all iOS devices and versions. Implementing user interface elements could be another obstacle.
