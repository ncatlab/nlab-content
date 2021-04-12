
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Bishop sets
* table of contents
{: toc}

## Idea

A _Bishop set_ is a notion of _[[set]]_ in [[constructive mathematics]], commonly used in [[Bishop's constructive mathematics]].

In ([Bishop](#Bishop)) the notion of _[[set]]_ is specified by stating that a set has to be given by a description of how to build [[elements]] of this set and by giving a binary [[relation]] of [[equality]], which has to be an [[equivalence relation]]. 

A [[function]] from a set $A$ to a set $B$ is then given by an operation, which is compatible with the equality (i.e. two elements which are equal in A are mapped to two elements which are equal in B), and is described as "a finite routine $f$ which assigns an element $f(a)$ of $B$ to each given element $a$ of $A$". This notion of routine is left informal but must "afford an explicit, finite, mechanical reduction of the procedure for constructing $f(a)$ to the procedure for constructing $a$."

These ideas have been formalized in [[type theory]], where they serve to set up [[set theory]] in an ambient type theoretic [[logical framework]]. See _[Formalization in type theory](#FormalizationInTypeTheory)_ below.


## Formalization in type theory
 {#FormalizationInTypeTheory}

Formally, the definition of Bishop set presumes some prior notion of "collection" (the elements) and "relation" (the equality) that can be put together.  These collections are sometimes called [[presets]], and can be formalized in various ways.  In particular, presets generally lack operations such as [[quotients]] and even [[subsets]].

One of the most common approaches is to use [[type theory]], where the collections are simply types.  Note that this is a different approach to the use of type theory in foundations of mathematics than that of, for instance, [[homotopy type theory]] --- in the latter, type theory is enriched with operations on types such as quotients, enabling them to be the basic set-like objects out of which mathematics is built; while in the Bishop-set approach one defines "sets" as types equipped with extra structure, so that the sets have quotient-type operations even though the types do not.  There is an analogy to the construction of the [[exact completion]] of a category, which has quotients even if the original category does not.

Frequently, the type theories used for this purpose do not even have a separate notion of "relation" or "proposition", and thus the untruncated [[propositions as types]] interpretation is used for the equivalence relations in a Bishop set.  That is, one has a type $X:Type$ of elements and a type family $R:X\to X \to Type$ with witnesses that it is "reflexive, symmetric, and transitive", but nothing prevents $R(x,y)$ from having more than one element.  (If the type theory has [[identity types]], one could demand that $R$ consist of [[h-propositions]], but at least historically this is not often done.)  This means that categorically, the Bishop sets are most like the [[ex/lex completion]] of the category of types --- although the morphisms in the ex/lex completion are defined as a *quotient* in the ambient set theory, whereas the morphisms between Bishop sets simply form another Bishop set.

For example, see ([Palmgren05](#Palmgren05)) for an exposition and ([Coquand-Spiwack, section 3](#CoquandSpiwack)) for a brief list of the axioms.

In the context of type theory a Bishop set is sometimes called a __[[setoid]]__.


## Properties

### The predicative topos of Bishop sets

In much of [[set theory]] the [[category]] [[Set]] of all sets is a [[Topos]]. For Bishop sets formalized in [[type theory]] this is not quite the case. Instead:

+-- {: .num_theorem }
###### Theorem

The category of Bishop sets in [[Martin-Löf dependent type theory]] is a [[strong predicative topos]].

=--

This is ([van den Berg, theorem 6.2](#vdBerg)), based on ([Moerdijk-Palmgren, section 7](#MoerdijkPalmgren)).


## Related concepts

* [[ETCS]]

[[!include types and logic - table]]



## References

The original publication is 

* [[Errett Bishop]], _Foundations of Constructive Analysis_. New York: McGraw-Hill (1967)
 {#Bishop}

in the context of [[constructive analysis]]. A detailed discussion is in 

* M. Hofmann, _Extensional constructs in Intensional Type theory_, Springer (1997)

Reviews include

* [[Erik Palmgren]],  _Bishop's set theory_ (2005) ([pdf](http://www.cse.chalmers.se/research/group/logic/TypesSS05/Extra/palmgren.pdf))
 {#Palmgren05}

* [[Erik Palmgren]], _Constructivist and Structuralist Foundations: Bishop's and Lawvere's Theories of Sets_ (2009) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.158.8166)) 


The formalization of Bishop set is reviewed for instance in section 3 of 

* [[Thierry Coquand]], [[Arnaud Spiwack]], _Towards constructive homological algebra in type theory_ ([pdf](https://hal.inria.fr/inria-00432525/document))
 {#CoquandSpiwack}

(there with an eye towards further formalization of [[homological algebra]]).

Some of the text above is taken from this section.

The [[predicative topos]] formed by Bishop sets in type theory is discussed in 

* [[Ieke Moerdijk]], [[Erik Palmgren]], _Wellfounded trees in categories. Ann. Pure Appl. Logic, 104(1-3):189&#8211;218, (2000)
 {#MoerdijkPalmgren}

* [[Benno van den Berg]], _Predicative toposes_  ([arXiv:1207.0959](http://arxiv.org/abs/1207.0959))
 {#vdBerg}

A formalization of constructive set theory in terms of setoids in [[intensional type theory|intensional]] [[type theory]] coded in [[Coq]] is discussed in 

* [[Erik Palmgren]], Olov Wilander, _Constructing categories of setoids in type theory_, ([pdf](http://www2.math.su.se/~palmgren/coq/czf_and_setoids/czf&setoids.pdf), [Coq](http://www2.math.su.se/~palmgren/coq/czf_and_setoids))
 {#PalmgrenWilander}

See also 

* [[UF-IAS-2012]], _On the setoid model of type theory_ ([video](http://video.ias.edu/univalent/palmgren))

* [[UF-IAS-2012]], _[Setoid model of type theory formalized](http://uf-ias-2012.wikispaces.com/Setoid+model+of+type+theory+formalized)_

* [Discussion](http://golem.ph.utexas.edu/category/2009/10/syntax_semantics_and_structura.html#c029271) on categorical aspects of the setoid construction. 


[[!redirects Bishop set]]
[[!redirects Bishop sets]]
