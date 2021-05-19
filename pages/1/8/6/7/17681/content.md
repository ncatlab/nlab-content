
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In [[computer science]] and specifically in [[type theory]], a **monad transformer** is a [[type]] constructor which takes a [[monad]] as an argument and returns a monad as a result. The concept is typically treated in the literature on [[monad (in computer science)|monads in computer science]].

Monad transformers generally derive from ordinary monads and allow a modular composition, so that the action on the identity monad of the associated transform $M T$ of a monad $M$ is equivalent to $M$.

This construction is sometimes viewed (see [HP07](#HP07), [[Eff]]) as a complication resulting from passing to monads from the setting of [[Lawvere theories]], where any two theories may be naturally combined.

## References

Textbook account:

* {#Winitzki} [[Sergei Winitzki]], Section 14 of: *The Science of Functional Programming -- A tutorial, with examples in Scala* ([leanpub:sofp](https://leanpub.com/sofp))

See also

* Bryan O'Sullivan, Don Stewart, and John Goerzen, _Monad transformers_, [Chapter 18](http://book.realworldhaskell.org/read/monad-transformers.html) of Real World Haskell.

* Chung-Chieh Shan, _Monad transformers_, [blog post](http://conway.rutgers.edu/~ccshan/wiki/blog/posts/Monad_transformers/)

* Mauro Jaskelioff, [[Eugenio Moggi]], _Monad Transformers as Monoid Transformers_, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/tcs10.pdf)

* Oleksandr Manzyuk, _Calculating monad transformers with category theory_, [pdf](https://oleksandrmanzyuk.files.wordpress.com/2012/02/calc-mts-with-cat-th1.pdf)

* {#HP07} [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_, Electronic Notes in Theoretical Computer Science (ENTCS) archive Volume 172, April, 2007 Pages 437-458  ([pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf))