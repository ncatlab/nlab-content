
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In purely [[functional programming languages]] (such as [[Haskell]]) all would-be side effects are [[data type|data typed]] in terms of *[[monads in computer science]]* which make the side effects look like and hence be formally treated like [[type checking|verifiable]] deterministic pure functions. If the actual side effect operations of reading input from or writing output to actual physical devices is [[data type|typed]] in this [[monad in computer science|monadic]] way, one speaks of an **I/O-monad**.

So to the programming language an IO-monad looks just like a [[state monad]] or similar, but when run on an actual computer the bind operation does cause actual physical effects.

## References

In [[Haskell]]: 

* [A Gentle Introduction to Haskell](https://www.haskell.org/tutorial/), Section 7: *[Input/Output](https://www.haskell.org/tutorial/io.html)*

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Monad_(functional_programming)#IO_monad_(Haskell)">IO monad (Haskell)</a>*

(...)

[[!redirects IO-monads]]

[[!redirects IO monad]]
[[!redirects IO monads]]

[[!redirects I/O-monad]]
[[!redirects I/O-monads]]

[[!redirects I/O monad]]
[[!redirects I/O monads]]

[[!redirects input]]
[[!redirects inputs]]

[[!redirects output]]
[[!redirects outputs]]

[[!redirects input and output]]
[[!redirects inputs and soutput]]

[[!redirects output and input]]
[[!redirects outputs and inputs]]

