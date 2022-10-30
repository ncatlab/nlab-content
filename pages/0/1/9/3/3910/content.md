
#Contents#
* table of contents
{:toc}

## Idea

An __integer__ is an element of $\mathbb{Z}$, which may defined as the [[free group]] on one generator or as the [[initial object|initial]] [[ring]].

As a group, $\mathbb{Z}$ is [[abelian group|abelian]] and is the [[Grothendieck group]] of the [[monoid]] (or [[semigroup]]) $\mathbb{N}$ of [[natural numbers]].

$$
  \mathbb{Z} = \{0\} \cup \{n, -n | n \in \mathbb{N}, n \gt 0\} = \{ \ldots, -3, -2, -1, 0, 1, 2, 3, \ldots \}
  \,.
$$

The group of natural numbers is naturally even a [[rig]] -- in fact the [[initial object|initial]] rig -- and this multiplicative structure extends to $\mathbb{Z}$ to make it a [[ring]] -- in fact the initial ring.


## Terminology

The underlying [[sets]] $\mathbb{Z}$ and $\mathbb{N}$ are [[isomorphic]]. Some subcultures of mathematics (and not only [[set theory|set theorists]]) use the term 'integer' synonymously for a natural number.  Computer scientists distinguish between 'unsigned integers' (natural numbers) and 'signed integers' (integers as described here).  Translations can also cause confusion with the term 'whole number'.

In [[number theory]], one generalises integers to [[algebraic integers]], an instance of the [[red herring principle]].  Accordingly, some number theorists will call the integers 'rational integers' to clarify; $\mathbb{Z}$ is the ring of algebraic integers in the [[number field]] $\mathbb{Q}$ of [[rational numbers]].

The symbol '$\mathbb{Z}$' derives from the German word 'Zahlen', which is a generic word for 'numbers'.  (Compare [[Richard Dedekind|Dedekind]]\'s use of that word in the title of his famous book on the [[foundations]] of [[real numbers]].)

## References

A formalization in terms of [[homotopy type theory]], using a unary notation, is in 

* [[Mike Shulman]], _[Integers.v](https://github.com/HoTT/HoTT/blob/master/Coq/HIT/Integers.v)_

(A different common formalization of integers in type theory is in a binary notation, as in the [Coq standard library](http://coq.inria.fr/stdlib/Coq.ZArith.BinInt.html).  Binary notation is exponentially more efficient for performing computations, but the unary notation was convenient for calculating $\pi_1(S^1)$.)

[[!redirects integer]]
[[!redirects integers]]
[[!redirects ring of integers]]
