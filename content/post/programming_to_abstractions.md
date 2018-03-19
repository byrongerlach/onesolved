---
title: "Programming to Abstractions with Interfaces in C#"
date: 2018-03-18
tags: ["c#"]
categories: ["design patterns"]
draft: true
---




## Why program to an abstraction rather an implementation? 
Dependency injection. 
Code is less brittle. The implementation can change for an interface and not break all clients, but this is not true for a concrete type.

Consider a client which consumes an ```IEnumerable<string>``` as opposed to a ```List<string>```. If the client consumes the IEnumerable, then if the target class changes from List to an Array, then the client won't break.


Interfaces enable nonhierarchial type frameworks.

Interfaces enable mixins.

## More Resilient Designs

## References

[More Effective C#, Item 14: Prefer Defining and implementing Interfaces to Inheritance](
https://www.safaribooksonline.com/library/view/More+Effective+C+(Includes+Content+Update+Program):+50+Specific+Ways+to+Improve+Your+C,+2nd+edition/9780134579306/ch02.xhtml#ch02lev1sec4)

Interfaces are fixed: You release an interface as a contract for a set of fucntionalyity that any type can implement. In contrast, base classes can be extended over time, and those extensions become part of every derived class.

[Effective Java, Item 20: Prefer Interfaces to Abstract classes]( 
https://www.safaribooksonline.com/library/view/effective-java-third/9780134686097/ch4.xhtml#lev20)


Existing classes can easily be retrofitted to implement a new interface, while an existing class can only implement an abstract class if it's higher up in the inheritance tree.

Interfaces enable mixin definition: "A mixin is a type that a class can implement in addition to its primary type." The optional functionality can be "mixed in" to the primary functionality. IComparable, for example



Abstract class versus interface. 

Abstract class and interfaces provide compile-time checking. 



Pluralsight course [C# Interfaces](https://app.pluralsight.com/library/courses/csharp-interfaces/table-of-contents).

Notes:

Quote:

Abstract Classes | Interfaces
---------|------------
Properties | Properties
Methods | Methods
Events | Events
Indexers | Indexers
Properties | 
Constructors |
Destructors |

Abstract Classes | Interfaces
---------|------------
Implementation code | No implementation code
Single inheritance | Multiple inheritance
Members have access modifiers | Members are automatically public
May contain fields, properties, constructors, destructors, methods, events and indexers | My only contain properties, methods, events, and indexers

Abstract class and interfaces provide compile-time checking. 

Quotes: 
Program to an abstraction rather than a concrete class. 
Program to an interface rather than a concrete class.
Concrete Class: Brittle
Interface: Resilience in the face of change
Insulation from implementatoin details.