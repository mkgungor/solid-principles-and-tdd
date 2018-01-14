# SOLID Principles and TDD

A collection of use cases in which I apply the SOLID principles during refactoring phase. 
Refactoring is done using the TDD (Test Driven Development) technique.

### Test Driven Development
It's a software development process that relies on the repetition of a very short development cycle:

1. Requirements are turned into very specific test cases.
2. Software is improved to pass the new tests.
3. The growing code must be cleaned up regularly during test-driven development with
the four rules of simple design:

    * Writing and running continuously all the tests.
    * Duplication must be removed.
    * Object, class, module, variable and method names should clearly represent their purpose.
    * Minimal classes and methods.
    
These rules helps our system's adherence to the primary OO goals of low coupling and high cohesion.

### Single Responsibility Principle (Actors and high level architecture)
![alt text](https://lostechies.com/derickbailey/files/2011/03/SingleResponsibilityPrinciple2_71060858.jpg)
The theoretical explanation is *There is one and only one reason to change a class*. 
This means that we should start to think small. Each complex problem cannot be easily solved as a whole.
It's much easier to divide the problem in smaller sub-problems. Each sub-problem can be tackled separately.
Now we should start thinking in tems of "divide et imperat".
*What to do:* Keep on dividing each sub-problem into sub-sub-problems until you reach
the point where such a "mini-problem" has just one single task left.
Since each class has only one single task to fulfill, there is only one reason left to change this class.
Then the code will be:

* More readable
* More robust
* Better testable
* Better maintainable and extendable

### Open Closed Principle (Class design and feature extensions)
The theoretical explanation is *software entities should be open for extension but closed for modification*.
Such an entity can allow its behavior to be altered without altering its source code.
There are several ways to extend a class/entity:

* Inheritance
* Composition
* Proxy implementation

### Liskov Substitution Principle (Subtyping and inheritance)
Functions that use references to base classes must be able to use objects of derived classes without knowing it
Child classes should never break the parent class type definitions. It's in strong relation with Open Closed Principle.
In fact a violation of LSP is a latent violation of OCP.

### Interface Segregation Principle (Business logic to clients communication)
In all modular applications there must be some kind of interface that the client rely on.
The scope is the communication to the client code on how to use the module.
We could take the approach to break the interface into pieces, specialized to each implementation.
This principle states that *no client should be forced to depend on methods it does not use*.

### Dependency Inversion Principle
The principle states:

1. High-level modules should not depend on low-level modules. Both should depend on abstractions.
2. Abstractions should not depend on details. Details should depend on abstractions.

Instead of a high-level module depending on a low-level module, both should depend on an abstraction.
While dependency inversion is more focused on the structure of your code, 
dependency injection is how the code functionally works. 
Spring is using dependency injection to assemble your application, dependency
inversion is what decouples your code so Spring can use dependency injection at run time.

# Resources

* [Test Driven Development by Example - Kent Beck](http://www.amazon.com/Test-Driven-Development-By-Example/dp/0321146530)
* [SO - Does TDD Force Me to Follow SOLID?](http://programmers.stackexchange.com/questions/111863/does-test-driven-development-force-me-to-follow-solid)
* [Principles of OOD - Robert Martin](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)
* [Design Principles and Design Patterns - Robert Martin](http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf)
* [SOLID Principles with Uncle Bob - Scott Hanselman](http://s3.amazonaws.com/hanselminutes/hanselminutes_0145.pdf)
* [Working Effectively with Legacy Code - Michael Feathers](http://www.amazon.com/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052)
* [Test Driven Development by Example - Kent Beck](http://www.amazon.com/Test-Driven-Development-By-Example/dp/0321146530)
* [Clean Code - Robert Martin](http://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
* [SOLID Motivational Pictures](http://lostechies.com/derickbailey/2009/02/11/solid-development-principles-in-motivational-pictures/)
* [30 Days of TDD: Day 5 - Make Your Code SOLID](http://blogs.telerik.com/james-bender/posts.aspx/13-09-18/30-days-of-tdd-day-five-make-your-code-solid)
* [SOLID eBook](http://lostechies.com/wp-content/uploads/2011/03/pablos_solid_ebook.pdf)