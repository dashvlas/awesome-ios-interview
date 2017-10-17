* [UIKit](#uikit)
  * [Live Rendering](#how-could-you-setup-live-rendering)
  * [What are different ways that you can specify the layout of elements in a UIView?](#what-are-different-ways-that-you-can-specify-the-layout-of-elements-in-a-uiview)
  * [Autolayout formula](#formula-of-autolayout)
  * [Size Classes](#size-classes)
  * [Intrinsic Content Size](#intrinsic-content-size)
  * [Difference between the frame and the bounds?](#whats-the-difference-between-the-frame-and-the-bounds)
* [Testing](#testing)
  * [Test types](#testing)
  	  * [Unit Tests](#unit-tests)
  	  * [Integration Tests](#integration-tests)
  	  * [Functional Tests](#functional-tests)
     * [Acceptance Tests](#acceptance-tests)
  * [Writing tests for iOS apps](#what-is-the-benefit-writing-tests-in-ios-apps)
  * [Please explain “Arrange-Act-Assert”](#please-explain-arrange-act-assert)
  * [Test Driven Development](#what-is-the-test-driven-development-of-three-simple-rules)
* [Tasks](#tasks)
  * [Explain why a compile time error occurs](#explain-why-a-compile-time-error-occurs-how-can-you-fix-it)
  * [Consider the following code](#consider-the-following-code)
  * [Determine the value of “x” in the Swift code](#determine-the-value-of-x-in-the-swift-code-below)
* [SDK](#sdk)
  * [Application States](#application-states)
  * [What happens when you call autorelease on an object?](#can-you-explain-what-happens-when-you-call-autorelease-on-an-object)
  * [iBeacons](#what-are-ibeacons)
  * [JSONSerialization](#what-kind-of-jsonserialization-have-readingoptions)
* [Patterns](#patterns)
  * [Adapter Pattern](#what-is-adapter-pattern)
  * [B-Trees](#what-are-b-trees)
  * [Memento Pattern](#what-is-memento-pattern)
  * [Responder Chain](#what-is-responder-chain)
  * [Observer Pattern](#what-is-observer-pattern)
  * [Singleton Pattern](#what-is-singleton-pattern)
  * [Decorator Design Pattern](#what-is-decorator-design-pattern)
  * [Facade Design Pattern](#what-is-facade-design-pattern)
* [Architecture](#acrhitecture)
  * [MVC](#mvc)
  * [MVVM](#mvvm)
  * [MVP](#mvp)
  * [Viper](#viper)
* [OOP](#oop)
  * [Inheritance](#inheritance)
  * [Polymorphism](#polymorphism)
  * [Encapsulation](#encapsulation)
  * [What is the abstract class?](#what-is-the-abstract-class)
* [Language](#language)
  * [What is the difference fileprivate and private access level?](#what-is-the-difference-fileprivate-and-private-access-level)
  * [What is final class?](#what-is-final-class)
  * [Structs vs Classes](#structs-vs-classes)
  * [Swift Standard Library Protocol](#swift-standard-library-protocol)
  * [What is Downcasting?](#what-is-downcasting)
  * [What are “strong” and “weak” references?](#what-are-strong-and-weak-references)
  * [Explain [weak self] and [unowned self]?](#explain-weak-self-and-unowned-self)
  * [Lazy in Swift](#lazy-in-swift)
  * [Raw and associated values in Swift](#difference-between-raw-and-associated-values-in-swift)
  * [Swift vs Objective-C](#can-you-briefly-describe-differences-between-swift-and-objective-c)
  * [Non-Escaping and Escaping Closures](#what-is-the-difference-non-escaping-and-escaping-closures)
  * [Method Swizzling](#please-explain-method-swizzling)
  * [Error handling in Swift](#how-should-one-handle-errors-in-swift)
  * [Difference strong, weak, readonly and copy?](#what-is-the-difference-strong-weak-readonly-and-copy)
  * [Guard benefits](#what-are-benefits-of-guard)
  * [When applied to strings, what’s the complexity of the countElements function and why?](#when-applied-to-strings-whats-the-complexity-of-the-countelements-function-and-why)
  * [In Swift enumerations, what’s the difference between raw values and associated values?](#in-swift-enumerations-whats-the-difference-between-raw-values-and-associated-values)
  * [Swift Transforming Array functions](#swift-transforming-array-functions)
  * [What is dynamic in Objective-C?](#what-is-dynamic-in-objective-c)
  * [What is made up of NSError object?](#what-is-made-up-of-nserror-object)
  * [Extensions](#extensions)
  * [KVO](#kvo)
  * [KVC ](#kvc)
  * [By calling performSelector:withObject:afterDelay: is the object retained?](#by-calling-performselectorwithobjectafterdelay-is-the-object-retained)
  * [What is defer?](#what-is-defer)
  * [Selectors](#selectors)
  * [What is the difference Any and AnyObject?](#what-is-the-difference-any-and-anyobject)
* [General](#general)
  * [HTTP request types](#http-request-types)
  * [Communication protocols](#communication-protocols)
   	* [Sokets](#sokets)
   	* [Web Sockets](#web-sokets)
   	* [TCP](#tcp)
   	* [UDP](#udp)
   	* [CFStream](#cfstream)
    * [NSStream](#nsstream)
  * [REST](#rest)
  * [Deep and shallow copy](#deep-and-shallow-copy)
  * [Protocol Oriented Programming](#protocol-oriented-programming)
* [Data](#data)
  * [How does NSManagedObjectContext work?](#how-does-nsmanagedobjectcontext-work)
  * [NSFetchedResultsController](#nsfetchedresultscontroller)
  * [NSPersistentContainer](#nspersistentcontainer)
  * [Managed object context and the functionality that it provides](#managed-object-context-and-the-functionality-that-it-provides)
  * [What is NSFetchRequest?](#what-is-nsfetchrequest)
* [Concurrency](#concurrency)
  * [Different ways of achieving concurrency in OS X and iOS](#different-ways-of-achieving-concurrency-in-os-x-and-ios)
  * [What is DispatchGroup?](#what-is-dispatchgroup)
  * [Synchronized](#synchronized)
  * [What is the difference between Synchronous &amp; Asynchronous task?](#what-is-the-difference-between-synchronous--asynchronous-task)

# UIKit
### How could you setup Live Rendering?
The attribute `@IBDesignable` lets Interface Builder perform live updates on a particular view

## What are different ways that you can specify the layout of elements in a UIView?
Here are a few common ways to specify the layout of elements in a UIView:

Using `Interface Builder`, you can add a `XIB file` to your project, layout elements within it, and then load the XIB in your application code (either automatically, based on naming conventions, or manually). Also, using InterfaceBuilder you can create a storyboard for your application.
You can your own code to use NSLayoutConstraints to have elements in a view arranged by Auto Layout.
You can create CGRects describing the exact coordinates for each element and pass them to UIView’s  
```objectivec  
  - (id)initWithFrame:(CGRect)frame method.
```
## Formula of Autolayout
Attribute 1 = Multiplier * Attribute 2 + Constant

## Size Classes
A size class is a new technology used by iOS to allow you to custom your app for a given device class, based on its orientation and screen size.
There are presently four size classes:  
- Horizontal Regular   
- Horizontal Compact  
- Vertical Regular  
- Vertical Compact  

## Intrinsic Content Size
The Intrinsic Content Size is one of the most powerful features you gain when you opt-in to using Auto Layout to describe your interfaces. When a view has an intrinsic content size, it is promising Auto Layout that it will have a predefined size that the engine can use to calculate and lay out its views

## What’s the difference between the frame and the bounds? 
`The bounds` of an UIView is the rectangle, expressed as a location (x,y) and size (width,height) relative to its own coordinate system (0,0)   
`The frame` of an UIView is the rectangle, expressed as a location (x,y) and size (width,height) relative to the superview it is contained within.  

# TESTING
  
### Test types

### Unit Tests
Tests the smallest unit of functionality, typically a method/function (e.g. given a class with a particular state, calling x method on the class should cause y to happen). Unit tests should be focussed on one particular feature (e.g., calling the pop method when the stack is empty should throw an InvalidOperationException). Everything it touches should be done in memory; this means that the test code and the code under test shouldn't:

1.	Call out into (non-trivial) collaborators
2.	Access the network
3.	Hit a database
4.	Use the file system
5.	Spin up a thread

Any kind of dependency that is slow / hard to understand / initialise / manipulate should be stubbed / mocked / whatevered using the appropriate techniques so you can focus on what the unit of code is doing, not what its dependencies do.
In short, unit tests are as simple as possible, easy to debug, reliable (due to reduced external factors), fast to execute and help to prove that the smallest building blocks of your program function as intended before they're put together. The caveat is that, although you can prove they work perfectly in isolation, the units of code may blow up when combined which brings us to ...

### Integration Tests
Integration tests build on unit tests by combining the units of code and testing that the resulting combination functions correctly. This can be either the innards of one system, or combining multiple systems together to do something useful. Also, another thing that differentiates integration tests from unit tests is the environment. Integration tests can and will use threads, access the database or do whatever is required to ensure that all of the code and the different environment changes will work correctly.
If you've built some serialization code and unit tested its innards without touching the disk, how do you know that it'll work when you are loading and saving to disk? Maybe you forgot to flush and dispose filestreams. Maybe your file permissions are incorrect and you've tested the innards using in memory streams. The only way to find out for sure is to test it 'for real' using an environment that is closest to production.
The main advantage is that they will find bugs that unit tests can't such as wiring bugs (e.g. an instance of class A unexpectedly receives a null instance of B) and environment bugs (it runs fine on my single-CPU machine, but my colleague's 4 core machine can't pass the tests). The main disadvantage is that integration tests touch more code, are less reliable, failures are harder to diagnose and the tests are harder to maintain.
Also, integration tests don't necessarily prove that a complete feature works. The user may not care about the internal details of my programs, but I do!

### Functional Tests
Functional tests check a particular feature for correctness by comparing the results for a given input against the specification. Functional tests don't concern themselves with intermediate results or side-effects, just the result (they don't care that after doing x, object y has state z). They are written to test part of the specification such as, "calling function `Square(x)` with the argument of `2` returns `4`".

### Acceptance Tests
Acceptance testing seems to be split into two types:
Standard acceptance testing involves performing tests on the full system (e.g. using your web page via a web browser) to see whether the application's functionality satisfies the specification. E.g. "clicking a zoom icon should enlarge the document view by 25%." There is no real continuum of results, just a pass or fail outcome.
The advantage is that the tests are described in plain English and ensures the software, as a whole, is feature complete. The disadvantage is that you've moved another level up the testing pyramid. Acceptance tests touch mountains of code, so tracking down a failure can be tricky.
Also, in agile software development, user acceptance testing involves creating tests to mirror the user stories created by/for the software's customer during development. If the tests pass, it means the software should meet the customer's requirements and the stories can be considered complete. An acceptance test suite is basically an executable specification written in a domain specific language that describes the tests in the language used by the users of the system.

## What is the benefit writing tests in iOS apps?
Tests gives us a clear perspective on the API design, by getting into the mindset of being a client of the API before it exists.
Good tests serve as great documentation of expected behavior.
It gives us confidence to constantly refactor our code because we know that if we break anything our tests fail.
If tests are hard to write its usually a sign architecture could be improved. Following RGR ( Red — Green — Refactor ) helps you make improvements early on.

## Please explain “Arrange-Act-Assert”
AAA is a pattern for arranging and formatting code in Unit Tests. If we were to write XCTests each of our tests would group these functional sections, separated by blank lines:
Arrange all necessary preconditions and inputs.
Act on the object or method under test.
Assert that the expected results have occurred.


## What is the Test Driven Development of three simple rules?
You are not allowed to write any production code unless it is to make a failing unit test pass.
You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
You are not allowed to write any more production code than is sufficient to pass the one failing unit test.


# TASKS
### Explain why a compile time error occurs. How can you fix it?
Task:
The following code snippet results in a compile time error:
```objectivec  
struct IntStack {
  var items = [Int]()
  func add(x: Int) {
    items.append(x) // Compile time error here
  }
}
``` 

Solution:
Structures are value types. By default, the properties of a value type cannot be modified from within its instance methods.
However, you can optionally allow such modification to occur by declaring the instance methods as ‘mutating’:
```objectivec  
struct IntStack {
  var items = [Int]()
  mutating func add(x: Int) {
    items.append(x) // All good!
  }
}
``` 


## Consider the following code:
Task:
```objectivec  
var defaults = UserDefaults.standard()
var userPref = defaults.stringForKey("userPref")!
printString(userPref)
 
func printString(string: String) {
    print(string)
}
``` 


Solution:
The second line uses the stringForKey method of UserDefaults, which returns an optional, to account for the key not being found, or for the corresponding value not being convertible to a string.

During its execution, if the key is found and the corresponding value is a string, the above code works correctly. But if the key doesn’t exist, or the corresponding value is not a string, the app crashes with the following error:

fatal error: unexpectedly found nil while unwrapping an Optional value
The reason is that the forced unwrapping operator ! is attempting to force unwrap a value from a nil optional. The forced unwrapping operator should be used only when an optional is known to contain a non-nil value.

The solution consists of making sure that the optional is not nil before force-unwrapping it:
```objectivec  

let userPref = defaults.stringForKey("userPref")
if userPref != nil {
    printString(userPref!)
}
``` 
## Determine the value of “x” in the Swift code below
Task: 
```swift  
var a1 = [1, 2, 3, 4, 5]
var a2 = a1
a2.append(6)
var x = a1.count
```

Solution:
In Swift, arrays are implemented as structs, making them value types rather than reference types (i.e., classes). When a value type is assigned to a variable as an argument to a function or method, a copy is created and assigned or passed. As a result, the value of “x” or the count of array “a1” remains equal to 5 while the count of array “a2” is equal to 6, appending the integer “6” onto a copy of the array “a1.” The arrays appear in the box below.
```swift
a1 = [1, 2, 3, 4, 5]  
a2 = [1, 2, 3, 4, 5, 6]  
``` 

# SDK
### Application States
The iOS application states are as follows:

Not running state: The app has not been launched or was running but was terminated by the system.  

Inactive state: The app is running in the foreground but is currently not receiving events. (It may be executing other code though.) An app usually stays in this state only briefly as it transitions to a different state. The only time it stays inactive for any period of time is when the user locks the screen or the system prompts the user to respond to some event (such as an incoming phone call or SMS message).  

Active state: The app is running in the foreground and is receiving events. This is the normal mode for foreground apps.  

Background state: The app is in the background and executing code. Most apps enter this state briefly on their way to being suspended. However, an app that requests extra execution time may remain in this state for a period of time. In addition, an app being launched directly into the background enters this state instead of the inactive state.  

Suspended state: While suspended, an app remains in memory but does not execute any code. When a low-memory condition occurs, the system may purge suspended apps without notice to make more space for the foreground app.

## Can you explain what happens when you call autorelease on an object?
When you send an object a autorelease message, its retain count is decremented by 1 at some stage in the future. The object is added to an autorelease pool on the current thread. The main thread loop creates an autorelease pool at the beginning of the function, and release it at the end. This establishes a pool for the lifetime of the task. However, this also means that any autoreleased objects created during the lifetime of the task are not disposed of until the task completes. This may lead to the taskʼs memory footprint increasing unnecessarily. You can also consider creating pools with a narrower scope or use NSOperationQueue with itʼs own autorelease pool. (Also important – You only release or autorelease objects you own.)

## What are iBeacons?
iBeacon.com defines iBeacon as Apple’s technology standard which allows Mobile Apps to listen for signals from beacons in the physical world and react accordingly. iBeacon technology allows Mobile Apps to understand their position on a micro-local scale, and deliver hyper-contextual content to users based on location. The underlying communication technology is Bluetooth Low Energy.

## What kind of JSONSerialization have ReadingOptions?
- MutableContainers specifies that arrays and dictionaries are created as variables objects, not constants    
- MutableLeaves specifies that leaf strings in the JSON object graph are created as instances of variable String   
- AllowFragments specifies that the parser should allow top-level objects that are not an instance of Array or Dictionary   

# PATTERNS
### What is Adapter Pattern? 
An Adapter allows classes with incompatible interfaces to work together. It wraps itself around an object and exposes a standard interface to interact with that object.

## What Are B-Trees? 
B-trees are search trees that provide an ordered key-value store with excellent performance characteristics. In principle, each node maintains a sorted array of its own elements, and another array for its children

## What is Memento Pattern? 
In Memento Pattern saves your stuff somewhere. Later on, this externalized state can be restored without violating encapsulation; that is, private data remains private. One of Apple’s specialized implementations of the Memento pattern is Archiving.

## What is Responder Chain? 
A ResponderChain is a hierarchy of objects that have the opportunity to respond to events received.

## What is Observer Pattern?
In the Observer pattern, one object notifies other objects of any state changes.

## What is Singleton Pattern?
The Singleton design pattern ensures that only one instance exists for a given class and that there’s a global access point to that instance. It usually uses lazy loading to create the single instance when it’s needed the first time.

## What is Decorator Design Pattern?
The Decorator pattern dynamically adds behaviors and responsibilities to an object without modifying its code. It’s an alternative to subclassing where you modify a class’s behavior by wrapping it with another object.

## What is Facade Design Pattern? 
The Facade design pattern provides a single interface to a complex subsystem. Instead of exposing the user to a set of classes and their APIs, you only expose one simple unified API.

# ARCHITECTURE

### MVC
`Model` —   responsible for the domain data or a data access layer which manipulates the data, think of ‘Person’ or ‘PersonDataProvider’ classes.
`Views`  —  responsible for the presentation layer (GUI), for iOS environment think of everything starting with ‘UI’ prefix.
`Controller/Presenter/ViewModel` —  mediator between the Model and the View, in general responsible for altering the Model by reacting to the user’s actions performed on the View and updating the View with changes from the Model.

## MVVM

The MVVM defines the following
·      The View , which is generally passive, corresponds to the Presentation Layer
·      The Model , corresponds to the Business Logic Layer and is identical to the MVC pattern
·      The View Model sits between the View and the Model , corresponds to the Application Logic Layer

The key aspect of the MVVM pattern is the binding between the View and the View Model.  In other words, the View is automatically notified of changes to the View Model.

In iOS, this can be accomplished using Key-Value-Observer (KVO) Pattern. In the KVO Pattern (https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/KeyValueObserving/KeyValueObserving.html) , one object is automatically notified of changes to the state of another object. In Objective C, this facility is built into the run-time. However, it’s not as straightforward in Swift. One option would be to add the “dynamic” modifiers to properties that need to be dynamically dispatched. However, this is limiting as objects now need to be of type NSObject.  The alternate is to simulate this behavior by defining a generic type that acts as a wrapper around properties that are observable.

## MVP
The MVP defines the following
·      The View , which is generally passive, corresponds to the  Presentation Layer
·      The Model , corresponds to the  Business Logic Layer and is identical to the MVC pattern
·      The Presenter sits between the View and the Model , corresponds to the Application Logic Layer.
A View is typically associated with one Presenter.

In iOS, the interaction between the View and Presenter can be implemented using the Delegation Pattern (https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/Delegation.html). The Delegation Pattern allows one object to delegate tasks to another object. In iOS, the pattern is implemented using a Protocol. The Protocol defines the interface that is to be implemented by the delegate.

In the MVP pattern, the View and Presenter are aware of each other. The Presenter holds a reference to the view it is associated with.

The PresenterProtocol defines the base set of methods that any Presenter must implement. Applications must extend this Protocol to include application specific methods.

```swift
protocol PresenterProtocol: class{
    func attachPresentingView(_view:PresentingViewProtocol)
    func detachPresentingView(_view:PresentingViewProtocol)
}
```

The PresentingViewProtocol  defines the base set of methods that View must implement. By providing default implementation of the methods in this interface, the conformant view does not have to provide its own implementation. This interface can be extended to define application specific methods.

```swift
protocol PresentingViewProtocol: class{
    func dataStartedLoading()
    func dataFinishedLoading()
    func showErrorAlertWithTitle(_title:String?, message:String)
    func showSuccessAlertWithTitle(_title:String?, message:String)
}
```

## Viper

This architecture is based on Single Responsibility Principle which leads to a clean architecture.

- View: The responsibility of the view is to send the user actions to the presenter and shows whatever the presenter tells it.
- Interactor: This is the backbone of an application as it contains the business logic.
- Presenter: Its responsibility is to get the data from the interactor on user actions and after getting data from the interactor, it sends it to the view to show it. It also asks the router/wireframe for navigation.
- Entity: It contains basic model objects used by the Interactor.
- Router: It has all navigation logic for describing which screens are to be shown when. It is normally written as a wireframe.

# OOP
### Inheritance
It allows a class to be defined that has a certain set of characteristics (such as methods and instance variables) and then other classes to be created which are derived from that class. The derived class inherits all of the features of the parent class and typically then adds some features of its own.

## Polymorphism
The word polymorphism means having many forms. Typically, polymorphism occurs when there is a hierarchy of classes and they are related by inheritance.

Objective-C polymorphism means that a call to a member function will cause a different function to be executed depending on the type of object that invokes the function.

Consider the example, we have a class Shape that provides the basic interface for all the shapes. Square and Rectangle are derived from the base class Shape.

## Encapsulation
Encapsulation is an Object-Oriented Programming concept that binds together the data and functions that manipulate the data and that keeps both safe from outside interference and misuse. Data encapsulation led to the important OOP concept of data hiding.

Data encapsulation is a mechanism of bundling the data and the functions that use them, and data abstraction is a mechanism of exposing only the interfaces and hiding the implementation details from the user.

## What is the abstract class?
An abstract class is a class that contains at least one abstract method, which is a method without any actual code in it, just the name and the parameters, and that has been marked as "abstract".

The purpose of this is to provide a kind of template to inherit from and to force the inheriting class to implement the abstract methods.

An abstract class thus is something between a regular class and a pure interface. Also interfaces are a special case of abstract classes where ALL methods are abstract

# LANGUAGE
### What is the difference fileprivate and private access level?
`Fileprivate` is accessible within the current file, private is accessible within the current declaration.

## What is final class?
By adding the keyword final in front of the method name, we prevent the method from being overridden

## Structs vs Classes
1. Inheritance.

Structures can't inherit in swift. If you want 

class Vehicle {
}

class Car : Vehicle {
}

Go for an class.

2. Pass By

Swift structures pass by value and class instances pass by reference.

3. Thread Safety

Structs are thread-safe

## Swift Standard Library Protocol
There are a few different protocol. Equatable protocol, that governs how we can distinguish between two instances of the same type. That means we can analyze. If we have a specific value is in our array. The comparable protocol, to compare two instances of the same type and sequence protocol: prefix(while:) and drop(while:) [SE-0045].
Swift 4 introduces a new Codable protocol that lets us serialize and deserialize custom data types without writing any special code.

## What is Downcasting?
When we’re casting an object to another type in Objective-C, it’s pretty simple since there’s only one way to do it. In Swift, though, there are two ways to cast — one that’s safe and one that’s not .
as used for upcasting and type casting to bridged type
as? used for safe casting, return nil if failed
as! used to force casting, crash if failed. should only be used when we know the downcast will succeed.

## What are “strong” and “weak” references?
By default, any variable that points to another object does so with what is referred to as a “strong” reference. A retain cycle occurs when two or more objects have reciprocal strong references (i.e., strong references to each other). Any such objects will never be destroyed by ARC (iOS’ Automatic Reference Counting). Even if every other object in the application releases ownership of these objects, these objects (and, in turn, any objects that reference them) will continue to exist by virtue of those mutual strong references. This therefore results in a memory leak.

Reciprocal strong references between objects should therefore be avoided to the extent possible. However, when they are necessary, a way to avoid this type of memory leak is to employ weak references. Declaring one of the two references as weak will break the retain cycle and thereby avoid the memory leak.

To decide which of the two references should be weak, think of the objects in the retain cycle as being in a parent-child relationship. In this relationship, the parent should maintain a strong reference (i.e., ownership of) its child, but the child should not maintain maintain a strong reference (i.e., ownership of) its parent.

For example, if you have Employer and Employee objects, which reference one another, you would most likely want to maintain a strong reference from the Employer to the Employee object, but have a weak reference from the Employee to thr Employer.

## Explain [weak self] and [unowned self]?
unowned does the same as weak with one exception: The variable will not become nil and therefore the variable must not be an optional.
But when you try to access the variable after its instance has been deallocated. That means, you should only use unowned when you are sure, that this variable will never be accessed after the corresponding instance has been deallocated.
However, if you don’t want the variable to be weak AND you are sure that it can’t be accessed after the corresponding instance has been deallocated, you can use unowned.
By declaring it [weak self] you get to handle the case that it might be nil inside the closure at some point and therefore the variable must be an optional. A case for using [weak self] in an asynchronous network request, is in a view controller where that request is used to populate the view.

## Lazy in Swift
An initial value of the lazy stored properties is calculated only when the property is called for the first time. There are situations when the lazy properties come very handy to developers.

## Difference between raw and associated values in Swift
This question tests the developer’s understanding of enumeration in Swift. Enumeration provides a type-safe method of working with a group of related values. Raw values are compile time-set values directly assigned to every case within an enumeration, as in the example detailed below:
enum Alphabet: Int {
case A = 1
case B
case C
}

In the above example code, case “A” was explicitly assigned a raw value integer of 1, while cases “B” and “C” were implicitly assigned raw value integers of 2 and 3, respectively. Associated values allow you to store values of other types alongside case values, as demonstrated below:
enum Alphabet: Int {
case A(Int)
case B
case C(String)
}


## Can you briefly describe differences between Swift and Objective-C?
When Swift was first launched in 2014, it was aptly described as “Objective-C without the C.” By dropping the legacy conventions that come with a language built on C, Swift is faster, safer, easier to read, easier to maintain, and designed specifically for the modern world of consumer-facing apps. One of the most immediately visible differences is the fact that Objective-C lacks formal support for namespaces, which forces Objective-C code to use two- or three-letter prefixes to differentiate itself. Instead of simple names like “String,” “Dictionary,” and “Array,” Objective-C must use oddities like “NSString,” “NSDictionary,” and “NSArray.”
Another major advantage is that Swift avoids exposing pointers and other “unsafe” accessors when referring to object instances. That said, Objective-C has been around since 1983, and there is a mountain of Objective-C code and resources available to the iOS developer. The best iOS developers tend to be pretty well versed in both, with an understanding that Swift is the future of iOS development.

## What is the difference Non-Escaping and Escaping Closures?
The lifecycle of a non-escaping closure is simple:
Pass a closure into a function
The function runs the closure (or not)
The function returns
Escaping closure means, inside the function, you can still run the closure (or not); the extra bit of the closure is stored some place that will outlive the function. There are several ways to have a closure escape its containing function:
Asynchronous execution: If you execute the closure asynchronously on a dispatch queue, the queue will hold onto the closure for you. You have no idea when the closure will be executed and there’s no guarantee it will complete before the function returns.
Storage: Storing the closure to a global variable, property, or any other bit of storage that lives on past the function call means the closure has also escaped.

## Please explain Method Swizzling

Method swizzling allows the implementation of an existing selector to be switched at runtime for a different implementation in a classes dispatch table. Swizzling allows you to write code that can be executed before and/or after the original method. For example perhaps to track the time method execution took, or to insert log statements.  

```objectivec
#import "UIViewController+Log.h"
@implementation UIViewController (Log)
    + (void)load {
        static dispatch_once_t once_token;
        dispatch_once(&once_token,  ^{
            SEL viewWillAppearSelector = @selector(viewDidAppear:);
            SEL viewWillAppearLoggerSelector = @selector(log_viewDidAppear:);
            Method originalMethod = class_getInstanceMethod(self, viewWillAppearSelector);
            Method extendedMethod = class_getInstanceMethod(self, viewWillAppearLoggerSelector);
            method_exchangeImplementations(originalMethod, extendedMethod);
        });
    }
    - (void) log_viewDidAppear:(BOOL)animated {
        [self log_viewDidAppear:animated];
        NSLog(@"viewDidAppear executed for %@", [self class]);
    }
@end
```

## How should one handle errors in Swift?
The method for handling errors in Swift differ a bit from Objective-C. In Swift, it's possible to declare that a function throws an error. It is, therefore, the caller's responsibility to handle the error or propagate it. This is similar to how Java handles the situation.

You simply declare that a function can throw an error by appending the throws keyword to the function name. Any function that calls such a method must call it from a try block.

func canThrowErrors() throws -> String
 
//How to call a method that throws an error
try canThrowErrors()
 
//Or specify it as an optional
let maybe = try? canThrowErrors()

## What is the difference strong, weak, readonly and copy?
- `Strong` means that the reference count will be increased and the reference to it will be maintained through the life of the object
- `Weak` means that we are pointing to an object but not increasing its reference count. It’s often used when creating a parent child relationship. The parent has a strong reference to the child but the child only has a weak reference to the parent.
- `Readonly`, we can set the property initially but then it can’t be changed.
- `Copy` means that we’re copying the value of the object when it’s created. Also prevents its value from changing.

## What are benefits of Guard?
There are two big benefits to guard. One is avoiding the pyramid of doom, as others have mentioned — lots of annoying if let statements nested inside each other moving further and further to the right. The other benefit is provide an early exit out of the function using break or using return.


## When applied to strings, what’s the complexity of the countElements function and why?
Comments: The String struct doesn’t provide a count or length property or method to count the number of characters it contains. Instead a global countElements<T>() function is available.


Solution: Swift strings support extended grapheme clusters. Each character stored in a string is a sequence of one or more unicode scalars that, when combined, produce a single human readable character. Since different characters can require different amounts of memory, and considering that an extreme grapheme cluster must be accessed sequentially in order to determine which character it represents, it’s not possible to know the number of characters contained in a string upfront, without traversing the entire string. For that reason, the complexity of the countElements function is O(n).

## In Swift enumerations, what’s the difference between raw values and associated values?
Raw values are used to associate constant (literal) values to enum cases. The value type is part of the enum type, and each enum case must specify a unique raw value (duplicate values are not allowed).

The following example shows an enum with raw values of type Int:

enum IntEnum : Int {
    case ONE = 1
    case TWO = 2
    case THREE = 3
}
An enum value can be converted to its raw value by using the rawValue property:

var enumVar: IntEnum = IntEnum.TWO
var rawValue: Int = enumVar.rawValue
A raw value can be converted to an enum instance by using a dedicated initializer:

var enumVar: IntEnum? = IntEnum(rawValue: 1)
Associated values are used to associate arbitrary data to a specific enum case. Each enum case can have zero or more associated values, declared as a tuple in the case definition:

enum AssociatedEnum {
    case EMPTY
    case WITH_INT(value: Int)
    case WITH_TUPLE(value: Int, text: String, data: [Float])
}
Whereas the type(s) associated to a case are part of the enum declaration, the associated value(s) are instance specific, meaning that an enum case can have different associated values for different enum instances.

## Swift Transforming Array functions  
→ map and flatMap— how to transform element. 
→ filter— should an element be included?  
→ reduce— how to fold an element into an aggregate value  
→ sort and lexicographicCompare—in what order should two elements come?  
→ indexOf and contains—does this element match?  
→ minElement and maxElement—which is the min/max of two elements?  
→ elementsEqual and startsWith—are two elements equivalent?  
→ split—is this element a separator?  

## What is dynamic in Objective-C?
`@dynamic` used to delegate the responsibility of implementing the accessors.
Dynamic for properties means that it setters and getters will be created manually and/or at runtime.

## What is made up of NSError object?
There are three parts of NSError object a domain, an error code, and a user info dictionary. The domain is a string that identifies what categories of errors this error is coming from.


## Extensions
Extensions add new functionality to an existing class, structure, enumeration, or protocol type. This includes the ability to extend types for which you do not have access to the original source code. Extensions are similar to categories in Objective-C

Extensions in Swift can:  
- Add computed instance properties and computed type properties  
- Define instance methods and type methods  
- Provide new initializers  
- Define subscripts  
- Define and use new nested types  
- Make an existing type conform to a protocol  

## KVO
KVO stands for `Key-Value Observing` and allows a controller or class to observe changes to a property value. In KVO, an object can ask to be notified of any changes to a specific property; either its own or that of another object.

## KVC 
KVC adds stands for `Key-Value Coding`. It’s a mechanism by which an object’s properties can be accessed using string’s at runtime rather than having to statically know the property names at development time.


## By calling performSelector:withObject:afterDelay: is the object retained?
Yes, the object is retained. It creates a timer that calls a selector on the current threads run loop. It may not be 100% precise time-wise as it attempts to dequeue the message from
the run loop and perform the selector

## What is defer?
`defer` keyword which provides a block of code that will be executed in the case when execution is leaving the current scope.


## Selectors
In Objective-C, selector has two meanings. It can be used to refer simply to the name of a method when it’s used in a source-code message to an object. It also, though, refers to the unique identifier that replaces the name when the source code is compiled. Compiled selectors are of type SEL. All methods with the same name have the same selector. You can use a selector to invoke a method on an object—this provides the basis for the implementation of the target-action design pattern in Cocoa

[friend performSelector:@selector(gossipAbout:) withObject:aNeighbor]
is equivalent to
 [friend gossipAbout:aNeighbor]

## What is the difference Any and AnyObject?
According to Apple’s Swift documentation:
Any can represent an instance of any type at all, including function types and optional types.
AnyObject can represent an instance of any class type.


# GENERAL
### HTTP request types
An HTTP request is a class consisting of HTTP style requests, request lines, request methods, request URL, header fields, and body content. The most common methods that are used by a client in an HTTP request are as follows:

1) GET:- Used when the client is requesting a resource on the Web server.

2) HEAD:- Used when the client is requesting some information about a resource but not requesting the resource itself.

3) POST:- Used when the client is sending information or data to the server—for example, filling out an online form (i.e. Sends a large amount of complex data to the Web Server).

4) PUT:- Used when the client is sending a replacement document or uploading a new document to the Web server under the request URL.  

## Communication protocols
### Network socket
__Network socket__ is an internal endpoint for sending or receiving data at a single node in a computer network. Concretely, it is a representation of this endpoint in networking software (protocol stack), such as an entry in a table (listing communication protocol, destination, status, etc.), and is a form of system resource.
The term "socket" is analogous to physical female connectors, communication between two nodes through a channel being visualized as a cable with two male connectors plugging into sockets at each node. Similarly, the term "port" (another term for a female connector) is used for external endpoints at a node, and the term "socket" is also used for an internal endpoint of local inter-process communication (IPC) (not over a network). However, the analogy is strained, as network communication need not be one-to-one or have a channel.
### WebSocket
__WebSocket__ is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. The WebSocket protocol was standardized by the IETF as RFC 6455 in 2011, and the WebSocket API in Web IDL is being standardized by the W3C.
WebSocket is a different TCP protocol from HTTP. Both protocols are located at layer 7 in the OSI model and, as such, depend on TCP at layer 4. Although they are different, RFC 6455 states that WebSocket "is designed to work over HTTP ports 80 and 443 as well as to support HTTP proxies and intermediaries" thus making it compatible with the HTTP protocol. To achieve compability, the WebSocket handshake uses the HTTP Upgrade header[1] to change from the HTTP protocol to the WebSocket protocol.
The WebSocket protocol enables interaction between a browser and a web server with lower overheads, facilitating real-time data transfer from and to the server. This is made possible by providing a standardized way for the server to send content to the browser without being solicited by the client, and allowing for messages to be passed back and forth while keeping the connection open. In this way, a two-way (bi-directional) ongoing conversation can take place between a browser and the server. The communications are done over TCP port number 80 (or 443 in the case of TLS-encrypted connections), which is of benefit for those environments which block non-web Internet connections using a firewall. Similar two-way browser-server communications have been achieved in non-standardized ways using stopgap technologies such as Comet.
### TCP Stream Socket
Is much more commonly used, as it provides the framework for a complete, structured "conversation" to occur between the two endpoints. TCP connections provide a means to ensure the message was received, and guarantees that packets are received in order. TCP is used by protocols including HTTP, FTP, and others where data must be reliably sent and received in order. To keep track of the ordering of packets, TCP employs a sequence number, which identifies the sequence of each packet. This not only keeps your conversation in order, but also adds a basic level of protection against some forms of spoofing (data forgery by a malicious party).

* Dedicated & point-to-point channel between server and client.
* Reliable and Lossless.
* Data sent/received in the similar order.
* Long time for recovering lost/mistaken data
* Web, SSH, FTP, TELNET, SMTP, IMAP/POP
### UDP Datagram Socket

Is used for sending short messages called datagrams to the recipient. Datagrams are single packets of data that are sent and received without any "return postage." There is no guarantee that the recipient will receive a particular packet, and multiple packets may be received out of order. Datagrams are generally thought of as unreliable, in the same way that a carrier pigeon can be unreliable. This form of communication is used for sending short query/response-type messages that do not require authentication, such as DNS (name resolution) lookups, as well as by some protocols where lost packets are irrelevant; such as live video streams and online multiplayer games, where an interruption can be ignored.

* No dedicated & point-to-point channel between server and client.
* Not 100% reliable and may lose data.
* Data sent/received order might not be the same
* Don't care or rapid recovering lost/mistaken data
* Tunneling/VPN (lost packets are ok - the tunneled protocol takes care of it)
* Media streaming
* Games that don't care if you get every update
* Local broadcast mechanisms (same application running on different machines "discovering" each other)
***
```c
CFSocketRef CFSocketCreate (
    CFAllocatorRef allocator,
    SInt32 protocolFamily,
    SInt32 socketType,
    SInt32 protocol,
    CFOptionFlags callBackTypes,
    CFSocketCallBack callout,
    const CFSocketContext *context
);
```
### CFStream

Socket streams provide an easy interface for reading and writing data to or from a socket. Each socket can be bound to a read and write stream, allowing for synchronous or asynchronous communication. Streams encapsulate most of the work needed for reading and writing byte streams, and replace the traditional `send()` and `recv()` functions used in C. Two different stream objects are used with sockets: `CFReadStream` and `CFWriteStream`
### NSStream

__`NSStream`__ is an abstract class that defines the fundamental interface and properties for all stream objects. `NSInputStream` and `NSOutputStream` are subclasses of `NSStream` and implement default input-stream and output-stream behavior. `NSStream` is built on the `CFStream` layer of Core Foundation. This close relationship means that the concrete subclasses of `NSStream`, `NSOutputStream` and `NSInputStream`, are toll-free bridged with their Core Foundation counterparts `CFWriteStream` and `CFReadStream`. Although there are strong similarities between the Cocoa and Core Foundation stream APIs, their implementations are not exactly coincident. The Cocoa stream classes use the delegation model for asynchronous behavior (assuming run-loop scheduling) while Core Foundation uses client callbacks. Despite their strong similarities, __`NSStream` does give you a major advantage over `CFStream`. Because of its Objective-C underpinnings, it is extensible.__ You can subclass `NSStream`, `NSInputStream`, or `NSOutputStream` to customize stream attributes and behavior. For example, you could create an input stream that maintains statistics on the bytes it reads; or you could make a `NSStream` subclass whose instances can seek through their stream, putting back bytes that have been read. `NSStream` has its own set of required overrides, as do `NSInputStream` and `NSOutputStream`.

## REST 
An architectural style called REST (Representational State Transfer) advocates that web applications should use HTTP as it was originally envisioned. Lookups should use GET requests. PUT, POST, and DELETE requests should be used for *mutation, creation, and deletion respectively *.

REST proponents tend to favor URLs, such as

server.com/catalog/thing/1723
but the REST architecture does not require these “pretty URLs”. A GET request with a parameter

server.com/catalog?thing=1723
is every bit as RESTful.

GET requests should never be used for updating information. For example, a GET request for adding an item to a cart

server.com/addToCart?cart=314159&thing=1723

would not be appropriate. GET requests should be idempotent. That is, issuing a request twice should be no different from issuing it once. That’s what makes the requests cacheable. An “add to cart” request is not idempotent—issuing it twice adds two copies of the item to the cart. A POST request is clearly appropriate in this context. Thus, even a RESTful web application needs its share of POST requests.

## Deep and shallow copy
There are two kinds of object copying: shallow copies and deep copies. The normal copy is a shallow copy that produces a new collection that shares ownership of the objects with the original. Deep copies create new objects from the originals and add those to the new collection.

## Protocol Oriented Programming

Protocol-Oriented Programming is a new programming paradigm ushered in by Swift 2.0. In the Protocol-Oriented approach, we start designing our system by defining protocols. We rely on new concepts: protocol extensions, protocol inheritance, and protocol compositions. The paradigm also changes how we view semantics. In Swift, value types are preferred over classes. However, object-oriented concepts don’t work well with structs and enums: a struct cannot inherit from another struct, neither can an enum inherit from another enum. So inheritancefa - one of the fundamental object-oriented concepts - cannot be applied to value types. On the other hand, value types can inherit from protocols, even multiple protocols. Thus, with POP, value types have become first class citizens in Swift.

__Protocol Extensions__

You can extend a protocol and provide default implementation for methods, computed properties, subscripts and convenience initializers.

__Protocol Inheritance__

A protocol can inherit from other protocols and then add further requirements on top of the requirements it inherits.

__Protocol Composition__

Swift types can adopt multiple protocols.

# DATA
### How does NSManagedObjectContext work?
`Managed object context` exists for three reasons: life-cycle management, notifications, and concurrency. It allows the developer to fetch an object from a persistent store and make the necessary modifications before deciding whether to discard or commit these changes back to the persistent store. The managed object context tracks these changes and allows the developer to undo and redo changes.

## NSFetchedResultsController
`NSFetchedResultsController` is a controller, but it’s not a view controller. It has no user interface. Its purpose is to make developers’ lives easier by abstracting away much of the code needed to synchronize a table view with a data source backed by Core Data.
Set up an NSFetchedResultsController correctly, and your table will mimic its data source without you have to write more than a few lines of code.

## NSPersistentContainer
The persistent container creates and returns a container, having loaded the store for the application to it. This property is optional since there are legitimate error conditions that could cause the creation of the store to fail.

## Managed object context and the functionality that it provides
A managed object context (represented by an instance of NSManagedObjectContext) is basically a temporary “scratch pad” in an application for a (presumably) related collection of objects. These objects collectively represent an internally consistent view of one or more persistent stores. A single managed object instance exists in one and only one context, but multiple copies of an object can exist in different contexts.

You can think of a managed object context as an intelligent scratch pad. When you fetch objects from a persistent store, you bring temporary copies onto the scratch pad where they form an object graph (or a collection of object graphs). You can then modify those objects however you like. Unless you actually save those changes, though, the persistent store remains unchanged.

Key functionality provided by a managed object context includes:

Life-cycle management. The context provides validation, inverse relationship handling, and undo/redo. Through a context you can retrieve or “fetch” objects from a persistent store, make changes to those objects, and then either discard the changes or commit them back to the persistent store. The context is responsible for watching for changes in its objects and maintains an undo manager so you can have finer-grained control over undo and redo. You can insert new objects and delete ones you have fetched, and commit these modifications to the persistent store.
Notifications. A context posts notifications at various points which can optionally be monitored elsewhere in your application.
Concurrency. Core Data uses thread (or serialized queue) confinement to protect managed objects and managed object contexts. In OS X v10.7 and later and iOS v5.0 and later, when you create a context you can specify the concurrency pattern with which you will use it using initWithConcurrencyType:

## What is NSFetchRequest?
`NSFetchRequest` is the class responsible for fetching from Core Data. Fetch requests are both powerful and flexible. You can use fetch requests to fetch a set of objects meeting the provided criteria, individual values and more.

# CONCURRENCY
### Different ways of achieving concurrency in OS X and iOS
There are basically three ways of achieving concurrency in iOS:  
1. threads  
2. GCD 
3. NSOperationQueue  

The disadvantage of threads is that they relegate the burden of creating a scalable solution to the developer. You have to decide how many threads to create and adjust that number dynamically as conditions change. Also, the application assumes most of the costs associated with creating and maintaining the threads it uses.

OS X and iOS therefore prefer to take an asynchronous design approach to solving the concurrency problem rather than relying on threads.

One of the technologies for starting tasks asynchronously is Grand Central Dispatch (GCD) that relegates thread management down to the system level. All the developer has to do is define the tasks to be executed and add them to the appropriate dispatch queue. GCD takes care of creating the needed threads and scheduling tasks to run on those threads.

All dispatch queues are first-in, first-out (FIFO) data structures, so tasks are always started in the same order that they are added.

An operation queue is the Cocoa equivalent of a concurrent dispatch queue and is implemented by the NSOperationQueue class. Unlike dispatch queues, operation queues are not limited to executing tasks in FIFO order and support the creation of complex execution-order graphs for your tasks.

## What is DispatchGroup?
`DispatchGroup` allows for aggregate synchronization of work. We can use them to submit multiple different work items and track when they all complete, even though they might run on different queues. This behavior can be helpful when progress can’t be made until all of the specified tasks are complete. 

## Synchronized
The `@synchronized` directive is a convenient way to create mutex locks on the fly in Objective-C code.

`Synchronized` guarantees that only one thread can be executing that code in the block at any given time.

Syntax:
```objectivec  
 @synchronized(key) 
 { 
  // thread-safe code 
 }
 ```

Example:
```objectivec  
 -(void)AppendExisting:(NSString*)val
{
  @synchronized (oldValue) {
      [oldValue stringByAppendingFormat:@"-%@",val];
  }
}
```
Now the above code is perfectly thread safe..Now Multiple threads can change the value.


## What is the difference between Synchronous & Asynchronous task?
`Synchronous`: waits until the task has completed
`Asynchronous`: completes a task in background and can notify you when complete
