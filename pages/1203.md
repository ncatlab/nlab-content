
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In the [[foundations]] of [[mathematics]], the [[axiom of infinity]] asserts that [[infinite set]]s exist.  Infinite sets cannot be constructed from finite sets, so their existence must be posited as an extra axiom.  Further axioms in this vein which assert the existence of even larger sets that cannot be constructed from smaller ones are called [[large cardinal]] axioms.


## Statements

One common form of the axiom of infinity says that the particular set $N$ of [[natural number]]s exists.  In material [[set theory]] this often takes the form of asserting that the von Neumann [[ordinal number]] $\omega$ exists, where $\omega$ is characterized as the smallest set such that $\emptyset\in\omega$ and whenever $a\in \omega$ then $a\cup \{a\}\in \omega$.  In structural set theory the usual form of the axiom of infinity is the existence of a [[natural numbers object]].

In the form of an NNO, the axiom of infinity generalises to the existence of [[inductive type]]s or [[W-type]]s.  These can be constructed from a NNO if [[power set]]s exist, but in [[predicative mathematics|predicative]] theories they can be added as additional axioms.

One could also posit the existence of the set of [[extended natural numbers]] instead of the set of natural numbers, as the set of extended natural numbers have [[countable|countably infinite]] cardinality and is the categorical [[duality|dual]] of the natural numbers in Set, a [[terminal coalgebra]] for the endofunctor $F(X) = 1 + X$ in Set. This generalises to the existence of [[coinductive types]] or [[M-types]], which can be added as additional axioms. 

## Alternatives

Broadly speaking, [[finite mathematics]] is mathematics that does not use or need the axiom of infinity; a finitist is an extreme breed of [[constructive mathematics|constructivist]] that believes that mathematics is better without the axiom of infinity, or even that this axiom is false.

A more extreme case is to *deny* the axiom of infinity with an __axiom of finiteness__: every set is [[finite set|finite]].  There is one of these for every definition of 'finite' given on that page; here is the strongest stated directly in terms of [[set theory]] as an axiom of [[induction]]:

* Any property of sets that is invariant under [[isomorphism]] and holds for the [[empty set]] must hold for all sets if, whenever it holds for a set $X$, it holds for the [[disjoint union]] $X \uplus \{*\}$.

In [[material set theory]], this is equivalent given the [[axiom of foundation]] (which guarantees that $X$ and $\{X\}$ are [[disjoint sets|disjoint]]):

* Any property of sets that holds for the empty set must hold for all sets if, whenever it holds for a set $X$, it holds for the [[union]] $X \cup \{X\}$.


category: foundational axiom

[[!redirects axiom of infinity]]
[[!redirects axioms of infinity]]

[[!redirects axiom of finiteness]]
[[!redirects axioms of finiteness]]
[[!redirects axiom of finity]]
[[!redirects axioms of finity]]
