
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

## Related concepts

* [[monad in computer science]]

* [[quantum IO monad]]

## References

Original discussion:

* [[Simon L. Peyton Jones]], [[Philip Wadler]], *Imperative functional programming*, Principles of programming languages (1993) 71–84 &lbrack;[doi:10.1145/158511.158524](https://doi.org/10.1145/158511.158524), [pdf](https://www.microsoft.com/en-us/research/wp-content/uploads/1993/01/imperative.pdf)&rbrack;

Review and exposition:

* {#BentonHughesMoggi02} [[Nick Benton]], [[John Hughes]], [[Eugenio Moggi]], §5.1 in: *Monads and Effects*, in: *Applied Semantics*, Lecture Notes in Computer Science **2395**, Springer (2002) 42-122 &lbrack;[doi:10.1007/3-540-45699-6_2](https://doi.org/10.1007/3-540-45699-6_2)&rbrack;

* {#Milewski19} [[Bartosz Milewski]], §21.2.8 & §21.29 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;


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

