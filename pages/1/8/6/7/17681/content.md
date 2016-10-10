#Contents#
* table of contents
{:toc}


*stub*


##Idea

A **monad transformer** is a type constructor which takes a [[monad]] as an argument and returns a monad as a result. The concept is typically treated in the literature on [[monad (in computer science)|monads in computer science]].

Monad transformers generally derive from ordinary monads and allow a modular composition, so that the action on the identity monad of the associated transform $M T$ of a monad $M$ is equivalent to $M$.

This construction is sometimes viewed (see [#HP07](#HP07), [[Eff]]) as a complication resulting from passing from the setting of [[Lawvere theories]], where any two theories may be naturally combined.

##References

* Bryan O'Sullivan, Don Stewart, and John Goerzen, _Monad transformers_, [Chapter 18](http://book.realworldhaskell.org/read/monad-transformers.html) of Real World Haskell.

* Chung-Chieh Shan, _Monad transformers_, [blog post](http://conway.rutgers.edu/~ccshan/wiki/blog/posts/Monad_transformers/)

* Mauro Jaskelioff, Eugenio Moggi, _Monad Transformers as Monoid Transformers_, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/tcs10.pdf)

* Oleksandr Manzyuk, _Calculating monad transformers with category theory_, [pdf](https://oleksandrmanzyuk.files.wordpress.com/2012/02/calc-mts-with-cat-th1.pdf)