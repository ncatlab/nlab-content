
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

\section{Idea}

Object oriented [[programming language|programming languages]] are, roughly speaking, ones in which the programmer works primarily with 'objects' which have the following characteristic aspects:

1. One constructs an object by providing certain input. E.g. one might construct an object of type 'mathematician' with input: 'name', 'university', 'research field'. This input is typically 'stored' inside the object.
1. One defines for an object certain 'methods', which, given an object and optionally some further input, a programmer may call on that object, to obtain certain output. These methods typically use the 'stored' input. E.g. for our object of type 'mathematician', we may define a method 'worksInSameCountryAs' which takes as additional input some other university X, and which returns a [[boolean]] according to whether the stored university is in the same country as university X. (And to do this, university itself should be an object which has a method providing as output the country to which the university belongs, etc).
1. The input (which may be mutable or immutable) stored inside the object is not typically exposed directly when a programmer uses the object, although one often provides a 'getter' method to return this stored variable at a given point in time (if it is mutable, it may have changed since the object was constructed). This is known as 'encapsulation'. One idea behind this is that the internals of an object can change without a programmer using an object needing to change their code accordingly.

Often, an object oriented programming language admits a notion of blueprint for an object, i.e. a description of the input needed to construct one and possibly also of the methods which the programmer may call given one, as well as the definition of these methods: a language construct known for example as a 'class' or 'prototype'. An object is then simply an 'instance' of this class or 'extension' of this prototype, i.e. it is what one obtains by actually providing some input to the blueprint (class, prototype, ...). Often 'classes' or similar play the role of 'types' in a typed object oriented language.  

One may also often 'extend' objects and their blueprints to make them more specific, adding methods which rely on this greater specificity. This is known as 'inheritance'. In the case that an object blueprint is a prototype, inheritance can even be viewed as involved in _construction_ of an object. It is, however, a tricky implementation problem to have an object extend (inherit from) more than one blueprint, and many languages (e.g. Java) forbid this.

Often object oriented languages have further levels of abstraction, e.g. the notion of an 'interface' or, in a slightly different way, of an 'abstract class' in Java. These typically can be thought as blueprints for classes, or of blueprints of objects which do not provide the details of how methods are defined, describing only the type of the input to the method and the type of the output. One says that a class 'implements' an interface. This is entirely distinct from 'inheritance'. When the language has them, interfaces can also be used as types in the language, although classes are often still types too: it is usually good programming practise to 'code to an interface', e.g. use as interface as the output type of a method, rather than use a class which implements the interface, as this provides greater flexibility. 

For a discussion of how object oriented programming languages may be able to be thought of type theoretically, see the section 'Examples' below.

Proponents of object oriented programming often argue that code in this style is more 'readable' and more 'flexible' than code in other styles, though often also more verbose. These points are, naturally, fiercely contended. 

As touched upon above, there exist various different approaches to object oriented programming, including the class-based approach of [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), the prototype-based approach of [Self](https://en.wikipedia.org/wiki/Self_(programming_language)) or JavaScript, and the 'everything is an object'-approach of [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk). 

\section{Relation to category theory}

Henry Story has [noted](https://www.quora.com/Why-is-functional-programming-seen-as-the-opposite-of-OOP-rather-than-an-addition-to-it/answer/Henry-Story) that, since OOP is coalgebraic and [[functional programming]] (FP) is algebraic, OOP and FP can in some sense be regarded as dual to each other. 

Although, in the context of [[computer science]], [[category theory]] is perhaps most often associated with [[functional programming]], there has been work on analysing object-oriented programming from a category-theoretic viewpoint, e.g. in the work of [[Bart Jacobs]] (e.g [Jacobs 2003](#Jacobs2003)).

\section{Examples}

Let us give here an implementation of a 'natural number' in a couple of object oriented programming languages. First, in Java, we can define a class as follows.

    public final class NaturalNumber {
        private final NaturalNumber successorOf;

        private NaturalNumber(final NaturalNumber successorOf) {
            this.successorOf = successorOf;
        }
 
        public static NaturalNumber zero() {
            return new NaturalNumber(null);
        }

        public NaturalNumber successor() {
            return new NaturalNumber(this);
        }

        public boolean isZero() {
            return successorOf == null;
        }

        public NaturalNumber getSuccessorOf() {
            return successorOf;
        }

        public NaturalNumber add(final NaturalNumber n) {
            NaturalNumber remainingPartToAdd = n;
            NaturalNumber withAddedPart = this;
            while (!remainingPartToAdd.isZero()) {
                withAddedPart = withAddedPart.successor();  
                remainingPartToAdd = remainingPartToAdd.getSuccessorOf();   
            }
            return withAddedPart;
        }    
    }

There are number of aspects to this which illustrate aspects of object oriented programming in languages such as Java. Firstly, if we try to see past the code itself and understand what is being expressed in terms of [[type theory]], we can observe the following.

1. A class corresponds roughly to a [[type]]. In other words, the class 'NaturalNumber' here corresponds roughly to a [[natural numbers type]]. 
1. An object of this class corresponds roughly to a [[term]] of this type. In other words, a 'NaturalNumber' object corresponds roughly to a term of a natural numbers type, i.e. to a natural number.
1. There is no sense in which this class 'NaturalNumber' is defined in terms of a canonical type construction, such as an [[inductive type]]. We are simply introducing a type in the empty context, and then defining [[natural deduction|rules]] for working with that type. This a common theme in object oriented programming: the core language typically provides very few canonical type constructions, but the programmer (or standard library!) has freedom and flexibility for introducing types and their rules. Java for example does not even have a 'pair' or 'product' type in its standard library, though it is easily implemented.   
1. In this particular example, there are roughly speaking two [[introduction rule|introduction rules]]: one given by the method 'zero', and one given by the method 'successor'. The method zero occurs in the empty context, i.e. corresponds to a rule of the form 
$$
\frac{}{zero : \mathbb{N}}
$$ 
whilst the method successor corresponds to a rule of the following form.
$$
\frac{n : \mathbb{N}}{successor(n) : \mathbb{N}}
$$ 
1. The method getSuccessorOf is roughly akin to a [[computation rule]]. Indeed, it can be thought of as being of the following form. 
$$
\frac{n : \mathbb{N} \vdash successor(n) : \mathbb{N}}{getSuccessorOf(successor(n)) = n : \mathbb{N}}
$$
1. The method add is roughly akin to an [[elimination rule]] combined with two computation rules. Indeed, the elimination rule can be thought of as being of the form 
$$
\frac{n : \mathbb{N} \vdash m : \mathbb{N}}{n + m : \mathbb{N}},
$$ 
and the computation rules can be thought of as being of the form 
$$
\frac{n : \mathbb{N}, zero : \mathbb{N} \vdash n + zero : \mathbb{N}}{n + zero = n : \mathbb{N}}
$$ 
and of the following form. 
$$
\frac{n : \mathbb{N}, m : \mathbb{N}, successor(m) : \mathbb{N} \vdash n + successor(m) : \mathbb{N}}{n + successor(m) = successor(n + m): \mathbb{N}}
$$

Secondly, if we look at the code itself, we can observe a few typical features.

1. The distinction between private and public methods and variables is often important in object oriented programming ('encapsulation'). Private methods and variables are those which can only be used internally in an object, i.e. they are 'implementation details' which cannot be seen by any code using an object. In this example, both of the two introduction rules (the methods zero and successor) actually rely on a third, purely internal, introduction rule, namely the class constructor. The code for a constructor is often 'boilerplate', i.e. almost always follows exactly or almost exactly the pattern used here: it instantiates the private variables of the class. The same goes for 'getters' like 'getSuccessorOf'. The idea is that by only exposing certain methods for public use, one controls more precisely how an object can be used, reducing the possibility for bugs, making code more predictable and easier/quicker to read.
1. The fact that 'add' is a method of the class NaturalNumber rather than a static method of form `public static NaturalNumber add(final NaturalNumber n, final NaturalNumber m)`
in some other class is archetypical object oriented programming. For another example, observe in the [Java API documentation](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html#concat-java.lang.String-) that concatenation of two strings is implemented in the Java standard library as a method `concat` in a String class which takes as input a single string, not as a static method which takes as input two strings. This is a fundamental difference in design from the way things are done in a [[functional programming|functional programming language]]. Use of static methods (ones not associated to an object of a class) is often a 'code smell' in Java and other object oriented programming languages, though there are exceptions, such as in the factory method 'zero' in the example above. We can see in the example above why this pattern is used in object oriented programming languages: it allows us to use the 'internal' private variables of an object, in this case successorOf. Though in this case it doesn't make much difference since we could have used the getter getSuccessorOf, the principle in general is that this allows for greater code flexibility: we can change the internals of our class without breaking code which uses objects of the class.  
1. Observe that 'add' relies on mutability (the variables remainingPartToAdd and withAddedPart) and a while loop rather than recursion. This is again very typical for an object oriented programming language vs a functional programming language.

We can carry out the same kind of implementation in Javascript. Javascript is not statically typed, i.e. has no explicit types or compile time type checking, and also has no explicit concept of class, relying instead on a notion of prototyping of objects. Nevertheless, the fundamental principles are the same, and in particular we claim that if we see past the code and try to understand things type theoretically, the story is exactly the same as for Java.

    function NaturalNumber(successorOf) {
      if (successorOf == undefined) {
        this.successorOf = null;
      } else if (!(successorOf instanceof NaturalNumber)) {
        throw "A natural number must be constructed either as zero or as the successor of a natural number";
      }
      this.successorOf = successorOf;
    }
    
    NaturalNumber.prototype.isZero = function () {
      return this.successorOf == null;
    }
    
    NaturalNumber.prototype.successor = function () {
      return new NaturalNumber(this);
    }
    
    NaturalNumber.prototype.add = function(n) {
      if (!(n instanceof NaturalNumber)) {
        throw "Can only add a natural number to a natural number";
      }
      var remainingPartToAdd = n;
      var withAddedPart = this;
      while (!remainingPartToAdd.isZero()) {
        withAddedPart = withAddedPart.successor();
        remainingPartToAdd = remainingPartToAdd.successorOf;
      }
      return withAddedPart;
    }

\section{Comparison with abstract data types}

Object oriented programming languages (OOP) should be contrasted with the use of [[abstract data types]] (ADTs), since they are deceptively similar. Both involve a distinction between a private implementation and a public interface, but with ADTs, the implementation is "private to the type", while with OOP it's "private to the object", and an object is not a type. Assuming the language in question has [[types]], different objects of the same type generally have different implementations of the same interface.

As a general rule, it's easy to add new data variants with OOP, because that just involves adding more objects, while it's harder to add new operations, as that involves adding to the implementations of all the existing objects. With ADT's, the reverse is true, as new operations are easy to add, while adding data variants involve changing the definition of the ADT and the implementations of all existing operations. See also [William R. Cook's essay](#Cook2009) on the differences between objects and ADTs.

This tension leads to the so-called [expression problem](http://homepages.inf.ed.ac.uk/wadler/papers/expression/expression.txt) in programming: How to design a language that makes both kinds of extension simultaneously easy.

The complementarity between user-defined types and objects was observed already by [Reynolds in 1978](#Reynolds1978).

\section{Related concepts}

* [[functional programming]]

* [[imperative programming]]

* [[programming language]]

\section{References}

* Wikipedia, _[Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming)_

* {#Cook2009} [[William R. Cook]], _[On  Understanding  Data  Abstraction,  Revisited](https://www.cs.utexas.edu/~wcook/Drafts/2009/essay.pdf)_, OOPSLA, 2009

* Alan Kay, _[The Computer Revolution hasn't happened yet](https://www.youtube.com/watch?v=oKg1hTOQXoY)_, OOPSLA Keynote, 1997

* {#Jacobs1995a} [[Bart Jacobs]], _Inheritance and Cofree Constructions_, 1995 ([pdf](https://ir.cwi.nl/pub/4938/4938D.pdf))

* {#Jacobs1995b} [[Bart Jacobs]], _Objects and Classes, Co-algebraically_, Object Orientation with Parallelism and Persistence, 1995 ([pdf](https://static.aminer.org/pdf/PDF/000/137/588/objects_and_classes_co_algebraically.pdf))

* {#Jacobs2003} [[Bart Jacobs]], Erik Poll, _Coalgebras and monads in the semantics of Java_, Theoretical Computer Science Volume 291 Issue 3, 2003 ([doi:10.1016/S0304-3975(02)00366-3](https://www.sciencedirect.com/science/article/pii/S0304397502003663))

* {#Reynolds1978} [[John C. Reynolds]], _[User-Defined Types and Procedural Data Structures as Complementary Approaches to Data Abstraction](https://www.cs.tufts.edu/~nr/cs257/archive/john-reynolds/procedural-data-structures.pdf)_, In: Gries D. (eds) Programming Methodology. Texts and Monographs in Computer Science. Springer, New York, NY

* {#Story2018} Henry Story, _[Why is functional programming seen as the opposite of OOP rather than an addition to it?](https://www.quora.com/Why-is-functional-programming-seen-as-the-opposite-of-OOP-rather-than-an-addition-to-it/answer/Henry-Story)_, 2018

* [[Anton Setzer]], _Object-oriented programming in dependent type theory_, in Henrik Nilsson (Ed.): Trends in Functional Programming. Volume 7, Series Trends in Functional Programming, Intellect, Intellect, Bristol and Chicago, 2007, pp. 91 -- 108. ISBN 978-184150-188-8, ([pdf](http://www.cs.swan.ac.uk/~csetzer/articles/objectOrientedProgrammingInDepTypeTheoryTfp2006PostProceedings.pdf))

[[!redirects object-oriented program]]
[[!redirects object-oriented programs]]
