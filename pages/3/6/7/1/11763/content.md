+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea


The principle of _identity of indiscernibles_ states that two objects are [[identical]] if they have all the same [[properties]].

This is also known as "[[Leibniz]]'s Law"

## In homotopy type theory
 {#InHomotopyTypeTheory}

In the presence of an [[identity type]], identity of indiscernibles is trivial because of [[haecceities]]; but extensionality principles like [[function extensionality]], [[propositional extensionality]], and [[univalence]] ("typal extensionality") are naturally regarded as a stronger form of identity of indiscernibles. In particular, the [[consistency]] of [[univalence]] means that in [[Martin-Löf type theory]] without univalence, one cannot define any [[predicate]] that provably distinguishes isomorphic [[types]]; thus isomorphic types are "externally indiscernible", and univalence incarnates that principle internally by making them identical.


"There are several ways to think about the axiom of [[univalence]]. One can see it as a sophisticated updating of Leibniz's principle of the identity of indiscernibles." --[[John Baez]] [nCaf&#233;](http://golem.ph.utexas.edu/category/2013/11/categories_for_the_working_phi.html)

## In topology

A [[topology|topological]] or geometrical version of the idea of identity of indiscernibles is [[separation axioms|separation]]: if two points are distinct, then they are separated in some sense. This means in turn that if two points in a space subject to a given separation axiom can not be separated by any admissible separation condition then they are identical.

## References

* [Wikipedia](http://en.wikipedia.org/wiki/Identity_of_indiscernibles)
* [SEP](http://plato.stanford.edu/entries/identity-indiscernible/)

Formalization in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 1.12 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013)

* [Ladyman & Presnell (2016)](https://academic.oup.com/philmat/article/doi/10.1093/philmat/nkw023/2593919/Identity-in-Homotopy-Type-Theory-Part-II-The) formulate four variants of this principle in [[homotopy type theory]].


* {#Favonia17} [[Favonia]], appendix B of _Higher-Dimensional Types in the
Mechanization of Homotopy Theory_, PhD thesis 2017, ([pdf](https://www.cs.cmu.edu/~kuenbanh/files/thesis.pdf))



[[!redirects Leibniz's Law]]
[[!redirects Leibniz's law]]
