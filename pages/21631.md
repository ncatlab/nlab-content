
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

Specifically, this applies to [[mathematical foundations]] in 
(a) [[dependent type theory]], or in (b) [[topos theory]], 
respectively, which -- apart from exactly such fine-print on the existence and nature of [[universes]] -- correspond to each other under the [[syntax-semantics duality|syntax/semantics]]-[[relation between type theory and category theory]].

Here, _univalent foundations_ is in contrast to other (earlier) approaches of laying foundations in [[type theories]] or [[toposes]], that have (only) a [[universe of propositions]] or (only) a [[subobject classifier]], respectively, hence where only a truncated sub-class of all [[types]]/[[objects]] is reflected in the [[universe]].

The basic idea of univalent foundations is, simply, to allow for universes that reflect _all_ [[types]]/[[objects]]. Or rather -- to avoid the notorious [[inconsistencies]] of the form of [[Russell's paradox]]/[[Girard's paradox]] -- universes that reflect all those [[types]]/[[objects]] that are "small" compared to the universe. It is this technical subtlety -- due to which a [[type]]/[[object]] may not be reflected in a given universe (namely if it is too large) but if it is, then it is so essentially _uni_quely -- which motivates the term "_uni_valent".

The term "univalent foundations" as such was coined by [Voevodsky 11](#Voevodsky11), much popularized with the textbook [UFIAS 12](#UFIAS12), and is usually taken to refer to [[mathematical foundations]] based on [[Martin-Löf dependent type theory]], or similar, with the [[univalence axiom]] imposed on the [[type universe]]. But the existence of (the [[categorical semantics]] of) such "univalent type universes" in higher analogues of [[toposes]] ("[[(∞,1)-toposes|∞-toposes]]") was observed (and published) earlier in [Lurie 09, Sec. 6.1.6](#Lurie09), there called _[[object classifiers]]_ and attributed to yet earlier private conversation with [[Charles Rezk]]. 

That both concepts, 

1. [[univalence axiom|univalent]]$\,$[[type universes|universes]] in [[Martin-Löf dependent type theory|type theory]] 

1. [[object classifiers]] in ([[elementary (∞,1)-topos|elementary]]) [[(∞,1)-toposes|∞-toposes]] 

do indeed correspond to each other was understood from the beginning (see [Shulman 12a](#Shulman12a), [lecture 3, slide 3](http://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=3), for the statement); based on proofs in special cases ([Shulman 12b](#Shulman12b)). Full proof appeared in [Shulman 19](#Shulman19).

Concretely, what makes univalent foundations univalent is the condition, respectively,

1. that there exists a [[type universe]] $Type$ (also often denoted $\mathcal{U}$) which _reflects types and their equivalences_, in that for any two types $A,B$ _in_ that universe, them being [[equivalence in homotopy type theory|equivalent as types]] is equivalent to them being equivalent ("[[identity type|equal]]") as [[terms]] of type $Type$;

   the usual formal [[syntax]] for this statement of the [[univalence axiom]] is the famous expression

   $$
     \underset{ 
       \color{blue}
       \text{equivalence as types}
     }{
       (A \simeq B)
     } 
     \underset{
       \color{blue}
       \;\;\text{univalence}\;\;
     }{
       \simeq 
     }
     \underset{
       \color{blue}
       \text{equivalence as terms}
       \atop \color{blue}
       \text{in the type universe}
     }{
       (A = B)
     }
   $$


1. that there exists an [[object classifier]] $Object$ which _reflects objects and their equivalences_, in that for any two objects $A,B$ them being [[equivalence in an (infinity,1)-category|equivalent as objects]]
is equivalent to their [[classifying maps]] to $Object$ being equivalent ([[homotopy|homotopic]]).


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
 {#OverviewOfTheBasicConcepts}

A map $f:A\to B$ is an [[equivalence]] if it has a [[section]] and a [[retraction]]. The [[univalence axiom]] asserts that for any two types $A,B:\mathcal{U}$, the canonical map $(A=B)\to (A\simeq B)$ obtained via the induction principle of the [[identity type]], is an equivalence.

In the univalent foundations, one can distinguish between [[property]] and [[structure]] (in general, [[higher structure]]). Being an equivalence, for instance, should be a property. There is a hierarchy of [[homotopy level|homotopy levels]] that starts at the level of [[contractible type|contractible types]]. The next level consists of types of which each identity type is contractible. Such types are called [[propositions]]. The fact that being an equivalence is a property is proven by showing that $\mathsf{is{-}equiv}(f)$ is a proposition in the above sense. 

Types of which the identity types are propositions are called sets. Many familiar types, such as the types of [[natural numbers]], [[integers]], and [[real numbers]] are sets in this sense, and in many subjects of algebra, such as [[groups]], [[rings]], [[modules]], and so on, it is assumed that the underlying types are sets. The [[axiom of choice]] is also restricted to sets, because there are surjective maps between other types that provably do not split. For instance, the [[double cover]] of the [[circle]] has no section, while each of its fibers is inhabited by two points. We say that sets are of [[homotopy level]] $0$. A type is said to be of homotopy level $n+1$ if its identity types are of homotopy level $n$. 

By the univalence axiom, we often have nice characterizations of "the type of a certain kind of thing". For instance, the type of $n$-dimensional [[vector spaces]] (over a [[discrete topology|discrete]] [[field]]) is the [[classifying space]] of the [[general linear group]] $GL(n)$. Similarly, the type of $n$-element sets is the classifying space of the [[symmetric group]] $\Sigma_n$, and the type of [[cyclic order|cyclically ordered]] $n$-element sets is the classifying space of the [[cyclic group]] $\mathrm{C}_n$. Such observations follow from the fact that the loop space of the type of objects of a certain kind is equivalent to the type of automorphisms of that kind.

## Related entries

* [[univalence axiom]]

* [[UniMath project]]

* [[modal homotopy type theory]]

* [[higher structures]]

## References

### In higher topos theory

* {#Lurie09} [[Jacob Lurie]], Section 6.1.6 of: _[[Higher Topos Theory]]_ (attributed there to [[Charles Rezk]])

### In type theory

#### Texts

* _[Univalent foundations webpage](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations.html)_

* {#Voevodsky11} [[Vladimir Voevodsky]],  _Univalent foundations_, talk at IAS 2011 ([pdf](https://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/2011_UPenn.pdf))

* {#UFIAS12} [[UF-IAS-2012|Univalent Foundations Project]], _Homotopy Type Theory -- Univalent Foundations of Mathematics_ ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf), [[Planet Math|PM]] [wiki version](http://planetmath.org/node/87534))

* {#Corfield20} [[David Corfield]], _Modal homotopy type theory_, Oxford University Press 2020 ([ISBN: 9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404)) doi:[10.1093/oso/9780198853404.001.0001](https://doi.org/10.1093/oso/9780198853404.001.0001)

#### Formalization libraries

* [UniMath](https://github.com/UniMath/UniMath)

* [Coq HoTT library](https://github.com/HoTT/HoTT)

* [Agda HoTT library](https://github.com/HoTT/HoTT-Agda)

* [[Martin Escardo]], _Introduction to Univalent Foundations of Mathematics with Agda_. ([ArXiv](https://arxiv.org/abs/1911.00580), [web](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/index.html), [GitHub](https://github.com/martinescardo/HoTT-UF-Agda-Lecture-Notes))

* [[Egbert Rijke]], [[Introduction to Homotopy Type Theory]] ([GitHub](https://github.com/HoTT-Intro/Agda))

### Relation between higher topos theory and univalent type theory

* {#Shulman12a} [[Michael Shulman]], _Minicourse on Homotopy Type Theory_ 2012 ([webpage](http://home.sandiego.edu/~shulman/hottminicourse2012/))

* {#Shulman12b} [[Michael Shulman]], _The univalence axiom for inverse diagrams_ ([arXiv:1203.3253](http://arxiv.org/abs/1203.3253)).

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004)).


[[!redirects univalent foundations]]
[[!redirects Univalent Foundations]]

[[!redirects Univalent Foundations for Mathematics]]

[[!redirects univalent mathematics]]


