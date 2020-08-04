
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

A _univalent foundations for mathematics_ refers to any [[foundations of mathematics|foundational system]] in which [[universes]] are [[object classifiers]], or, equivalently, satisfy the [[univalence axiom]].


### In higher topos theory 

See at _[[object classifier]]_ (in [[(∞,1)-toposes]]).

### In homotopy type theory

Voevodsky's univalent foundations ([UFIAS 12](#UFIAS12)) are an extension of [[Martin-Löf's dependent type theory]] obtained by adding:

* the [[univalence axiom]],

* [[propositional truncations]].

Notice that:

* [[function extensionality]] is implied by the [[univalence axiom]], so it is not necessary to assume separately;

* [[propositional resizing]] is sometimes also included as an axiom;

* the [[UniMath]] library also uses _type in type_, i.e., the [[axiom]] that the [[type universe]] contains itself. Strictly speaking, this makes the system [[inconsistency|inconsistent]], due to [[Girard's paradox]]. But the idea is that in practice the inconsistencies are readily avoided, so that the axiom serves as a convenient hack.

* The [[axiom of choice]] is consistent with the univalent foundations of mathematics and may be assumed separately.

## Overview of the basic concepts

A map $f:A\to B$ is an [[equivalence]] if it has a [[section]] and a [[retraction]]. The [[univalence axiom]] asserts that for any two types $A,B:\mathcal{U}$, the canonical map $(A=B)\to (A\simeq B)$ obtained via the induction principle of the [[identity type]], is an equivalence.

In the univalent foundations, one can distinguish between [[property]] and [[structure]]. Being an equivalence, for instance, should be a property. There is a hierarchy of [[homotopy level|homotopy levels]] that starts at the level of [[contractible type|contractible types]]. The next level consists of types of which each identity type is contractible. Such types are called [[propositions]]. The fact that being an equivalence is a property is proven by showing that $\mathsf{is{-}equiv}(f)$ is a proposition in the above sense. 

Types of which the identity types are propositions are called sets. Many familiar types, such as the types of [[natural numbers]], [[integers]], and [[real numbers]] are sets in this sense, and in many subjects of algebra, such as [[groups]], [[rings]], [[modules]], and so on, it is assumed that the underlying types are sets. The [[axiom of choice]] is also restricted to sets, because there are surjective maps between other types that provably do not split. For instance, the [[double cover]] of the [[circle]] has no section, while each of its fibers is inhabited by two points. We say that sets are of [[homotopy level]] 0. A type is said to be of homotopy level $n+1$ if its identity types are of homotopy level $n$. 

By the univalence axiom, we often have nice characterizations of "the type of a certain kind of thing". For instance, the type of n-dimensional [[vector spaces]] is simply the classifying space of the [[general linear group]] $GL(n)$. Similarly, the type of n-element sets is simply the classifying space of the [[symmetric group]] $\Sigma_n$. Such observations follow from the fact that the loop space of the type of objects of a certain kind is equivalent to the type of automorphisms of that kind.

## Related entries

* [[univalence axiom]]

* [[UniMath project]]

* [[modal homotopy type theory]]

## References

### In higher topos theory

* [[Jacob Lurie]], Section 6.1.6 of: _[[Higher Topos Theory]]_ (attributed there to [[Charles Rezk]])

### In type theory

* {#UFIAS12} [[UF-IAS-2012|Univalent Foundations Project]], _Homotopy Type Theory -- Univalent Foundations of Mathematics_ ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf), [[Planet Math|PM]] [wiki version](http://planetmath.org/node/87534))

* {#Corfield20} [[David Corfield]], _Modal homotopy type theory_, Oxford University Press 2020 ([ISBN: 9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404))

### Libraries with formalizations

* [UniMath](https://github.com/UniMath/UniMath)

* [Coq HoTT library](https://github.com/HoTT/HoTT)

* [Agda HoTT library](https://github.com/HoTT/HoTT-Agda)

* Martin Escardo, _Introduction to Univalent Foundations of Mathematics with Agda_. ([ArXiv](https://arxiv.org/abs/1911.00580), [web](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/index.html), [GitHub](https://github.com/martinescardo/HoTT-UF-Agda-Lecture-Notes))

* Egbert Rijke, [[Introduction to Homotopy Type Theory]] ([GitHub](https://github.com/HoTT-Intro/Agda))


[[!redirects Univalent Foundations for Mathematics]]

