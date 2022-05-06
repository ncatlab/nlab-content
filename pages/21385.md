
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _object_ in the sense of _object-oriented_ [[programming languages]] (OOP) is an encapsulated unit of state and behavior that operates on this state. Given an object, you cannot directly access its state, but only invoke its behavior by calling its "methods". When constructing an object (or defining a class that constructs objects), you have direct access to the state when implementing the methods.

OOP should be contrasted with the use of [[abstract data types]] (ADTs), since they are deceptively similar. Both involve a distinction between a private implementation and a public interface, but with ADTs, the implementation is "private to the type", while with OOP it's "private to the object", and an object is not a type. Assuming the language in question has [[types]], different objects of the same type generally have different implementations of the same interface.

Many OOP languages allow class definitions, which are a way to share the implementations of methods among the objects "instantiated" from the class (constructed by it). In some languages, classes are treated as types, while in others, they're only used for object construction.

Often there is an emphasis on the possibility of constructing objects successively ("inheritance"), with one object inheriting the implementation and interface from another one, and then typically adding more. This is usually managed via the class definitions, which can have a "superclass". But in some languages it can be done directly between objects, where an object can have a "prototype". Some languages also support multiple inheritance, which tends to greatly complicate the semantics.

Sometimes [[subtyping]] is thought of as inheritance of an interface, with no associated implementation. Accordingly, typed object-oriented languages often support subtyping. Multiple inheritance of interfaces has less complicated semantics than multiple inheritance of implementations, since there are no coherence issues.


There exist various different frameworks for OOP, including the class-based approach of [Java](https://en.wikipedia.org/wiki/Java_(programming_language), the prototype-based approach of [Self](https://en.wikipedia.org/wiki/Self_(programming_language), and the 'everything is an object'-approach of [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk). Alan Kay, one of the creators of Smalltalk, famously said "I made up the term 'object-oriented', and I can tell you I did not have C++ in mind."

## Relation to category theory

Henry Story has [noted](https://www.quora.com/Why-is-functional-programming-seen-as-the-opposite-of-OOP-rather-than-an-addition-to-it/answer/Henry-Story) that, since OOP is coalgebraic and [[functional programming]] (FP) is algebraic, OOP and FP can in some sense be regarded as dual to each other. 

Although, in the context of [[computer science]], [[category theory]] is perhaps most often associated with [[functional programming]], there has been work on analysing object-oriented programming from a category-theoretic viewpoint, e.g. in the work of [[Bart Jacobs]] (e.g [Jacobs 2003](#Jacobs2003)).

## Related concepts

* [[functional programming]]

* [[imperative programming]]

* [[programming language]]

## References

* Wikipedia, _[Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming)_

* Alan Kay, _[The Computer Revolution hasn't happened yet](https://www.youtube.com/watch?v=oKg1hTOQXoY)_, OOPSLA Keynote, 1997

* {#Jacobs1995a} [[Bart Jacobs]], _Inheritance and Cofree Constructions_, 1995 ([pdf](https://ir.cwi.nl/pub/4938/4938D.pdf))

* {#Jacobs1995b} [[Bart Jacobs]], _Objects and Classes, Co-algebraically_, Object Orientation with Parallelism and Persistence, 1995 ([pdf](https://static.aminer.org/pdf/PDF/000/137/588/objects_and_classes_co_algebraically.pdf))

* {#Jacobs2003} [[Bart Jacobs]], Erik Poll, _Coalgebras and monads in the semantics of Java_, Theoretical Computer Science Volume 291 Issue 3, 2003 ([doi:10.1016/S0304-3975(02)00366-3](https://www.sciencedirect.com/science/article/pii/S0304397502003663))

* {#Story2018} Henry Story, _[Why is functional programming seen as the opposite of OOP rather than an addition to it?](https://www.quora.com/Why-is-functional-programming-seen-as-the-opposite-of-OOP-rather-than-an-addition-to-it/answer/Henry-Story)_, 2018

[[!redirects object-oriented program]]
[[!redirects object-oriented programs]]
