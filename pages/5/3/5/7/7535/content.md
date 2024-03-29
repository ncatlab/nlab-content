
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Exactness properties
* table of contents
{: toc}

## Idea

An **exactness property** of a [[category]] asserts the existence of certain [[limits]] and [[colimits]], and moreover that the limits and colimits interact in a certain way.  Frequently, this includes stability of the colimits under [[pullback]], and also a condition expressing that some of the input data can be recovered from the colimit.

Many types of exactness can be expressed in terms of "colimits in the left-exact world". 

Exactness properties of a functor refer to preservation of limits or colimits of certain kind, existence of adjoints and possibly their exactness properties.

## Examples

* As particular cases of [[familial regularity and exactness]] we have:
  * A [[regular category]] has [[quotient object|quotients]] of [[kernel pairs]] that are stable under pullback.
  * An [[exact category]] has [[quotient object|quotients]] of [[congruences]] that are stable under pullback.
  * A [[coherent category]] is regular and has finite [[unions]] of [[subobjects]] that are stable under pullback.
  * A [[pretopos]] is coherent and also extensive (see below).
  * A [[Grothendieck topos]] is an infinitary-pretopos that also has a [[generating set]].  Toposes play a universal role for lex colimits; see [Garner-Lack](#GarnerLack).

* An [[extensive category]] has [[coproducts]] that are disjoint and stable under pullback.

* An [[adhesive category]] has pushouts of monomorphisms that are stable under pullback and "van Kampen".

* An [[exhaustive category]] has colimits of sequences of monomorphisms that are pullback-stable and "exhaust" the colimit.

* More generally, having colimits of some class which are [[van Kampen colimit|van Kampen]] is an exactness property.

* Having [[filtered colimits]] which commute with [[finite limits]] is also an exactness property.

* Exact categories with pullback-stable [[reflexive coequalizers]] are an exactness notion.

* The various types of [[additive and abelian categories]] are [[Ab-enriched]] exactness properties. See also [[AT-category]].

* A [[site]] can be considered as a category with "exactness [[structure]]", or as a way of specifying certain exactness conditions which ought to hold after "completion".  See [[postulated colimit]] and [[exact completion]].

## References

* [[Richard Garner]] and [[Steve Lack]], *Lex colimits* ([arXiv:1107.0778](http://arxiv.org/abs/1107.0778))
 {#GarnerLack}

[[!redirects exactness properties]]
[[!redirects exactness properties of categories]]
[[!redirects lex colimit]]
[[!redirects lex colimits]]
[[!redirects exactness notion]]
[[!redirects exactness notions]]
[[!redirects notion of exactness]]
[[!redirects notions of exactness]]
