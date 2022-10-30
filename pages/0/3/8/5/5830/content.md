
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Homotopy type theory_ is [[intensional type theory|intensional]] ([[Martin-Löf type theory|Martin-Löf]]-)[[dependent type theory]]  equipped with the [[univalence axiom]]. 

Its [[semantics]] interprets [[types]] not as [[sets]] but as [[homotopy types]]/[[∞-groupoids]].
Where [[extensional type theory]] is the [[internal language]] of [[locally cartesian closed categories]], [[intensional type theory]] with the [[identity types]] that it provides and supplemented by univalence behaves like the [[internal language of an (∞,1)-topos]]. 

Some details are still being worked out, but the impression is that homotopy type theory thus should serve as a [[foundation]] for [[mathematics]] that is natively about [[homotopy theory]]/[[(∞,1)-category theory]].

## Properties

### Models

It is well known that [[extensional type theory|extensional]] [[dependent type theory]] is essentially the [[internal logic]] of [[locally cartesian closed categories]]. The step from extensional to [[intensional type theory]] and the [[identity types]] that this brings with it makes intensional dependent type theors have models in certain [[(∞,1)-categories]]. The conjecture is ([Joyal, 2011](#Joyal)) that intensional dependent type theory with the [[univalence axiom]], hence homotopy type theory, is the internal language of [[locally cartesian closed (∞,1)-categories]].

## Machine implementation

An important aspect of HoTT is the fact that [[intensional type theory|intensional]] [[Martin-Löf type theory]] has a computational implementation in proof assistants like [[Coq]] and [[Agda]].

This forms the basis of  the _Univalent Foundations_ program ([Voevodsky](#Voevodsky)), which uses Coq to generate and verify proofs with [[homotopy theory|homotopical]] content.

See the [code page](http://homotopytypetheory.org/coq/) at the [HoTT site](#HoTTSite) for more.

## Dictionary HoTT-Coq / $(\infty,1)$-Category theory
 {#DictionaryToCoq}

The following list displays some keywords defined in the [[Coq]]-implementation of homotopy type theory together with their meaning in the [[homotopy theory]]/[[(∞,1)-category theory]] that they describe.

Let $C$ be a given ambient [[(∞,1)-category]] which

* is [[locally cartesian closed (∞,1)-category|locally cartesian closed]];


* in addition has [[(∞,1)-colimits]]. 

For instance $C$ could be an [[(∞,1)-topos]] (in which case the homotopy type theory would be the [[internal language of an (∞,1)-topos]]).
 
While Coq-HoTT is supposed to be the internal language for such $C$, the _strict [[models]]_ for it are actually [[homotopical category|homotopical]] [[1-categories]] equipped with extra structure that make them serve as [[presentable (infinity,1)-categories|presentations]] for $C$. These strict models take place in [[categories of fibrant objects]].

We then have the following dictionary.

The [[type]] [[Type]] of types

    Type

denotes an [[object classifier]] in $C$ for a certain size of [[universe]]. The [[Coq]] system automatically performs [[universe enlargement]] as necessary.

A [[term]] of [[type]] Type

    X : Type

denotes an [[object]] in the $(\infty,1)$-category $C$; equivalently an [[(∞,1)-functor]] $X : * \to C$.

The [[unit type]]

    unit : Type

is the [[terminal object in an (∞,1)-category|terminal object]].

For $X, Y \in C$ two objects, the [[function type]]

    X -> Y : Type

denotes the [[internal hom]] $[X,Y] \in C$ (a formal proof of that fact is [here](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/AdjunctionProdHom.v)).

A [[dependent type]]

    P (x : X) : Type

denotes a [[bundle]] $P \to X$ in $C$, called. In a [[presentable (∞,1)-category|presentation]] of $C$ by a [[category of fibrant objects]] it denotes a [[fibration]] $P \to X$.

    P : X -> Type

denotes the corresponding classifying map, via an internal [[(∞,1)-Grothendieck construction]].

The total space object $P$ of this bundle -- the _[[dependent sum type]]_ -- is the type equivalently coded as

    { x : X  & P x} : Type

or

    total (fun (x : X) => P x) : Type.

It should also equivalently be called

    exists x : X, P x

(see [[existential quantifier]]) but in the current [[Coq]] implementation that keyword is reserved for [[(-1)-truncated]] $P_x$ ([[proposition]]s).

The code

    forall x : X, P x

for the [[universal quantifier]], denotes the object of [[homotopy]] [[section]]s of this bundle (the _[[dependent product]]_ of the bundle, see the section _[relation to spaces of sections](http://ncatlab.org/nlab/show/dependent+product#RelationToSpacesOfSections)_ there).

    f : forall x : X, P x

denotes therefore a particular [[section]] of this bundle

$$
  \array{
     && P
     \\  
     & {}^{\mathllap{f}}\nearrow& \downarrow
     \\ 
     X &= & X
  }
  \,.
$$

The [[identity type]]

    paths X : X -> X -> Type

or

    Id (x y : X) : Type

corresponds in a [[presentable (infinity,1)-category|presentation]] of $C$ by a [[category of fibrant objects]] to the [[path space object]] $X^I$. The fact that there is a [[weak equivalence]] $X \stackrel{\simeq}{\to} X^I$ given by the inclusion of [[identity]] [[morphisms]] is reflected in the [[inductive type]]-definition of <code>paths</code>, which says that any proposition about terms in the path type is already fixed by its value on all identity paths.

Then for <code>x y : X</code> two [[terms]], the type (also called the [[identity type]]) denoted

    paths X x y : Type

or

    x ~~> y : Type

or
  
    x == y : Type

denotes the [[homotopy pullback]] of the form

$$
  \array{
    x \times_X y &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{x}}
    \\
    {*} &\stackrel{y}{\to}&  X
  }
$$

which in a presentation by a [[category of fibrant objects]] is given (see [[factorization lemma]]) by the ordinary pullback

$$
  \array{
    P_{x,y} X &\to& &\to& {*}
    \\
    \downarrow && && \downarrow^{\mathrlap{x}}
    \\
    \downarrow && X^{\Delta[1]} &\to& X
    \\  
    \downarrow && \downarrow
    \\
    {*} &\stackrel{y}{\to}& X
  }
  \,.
$$

Beware that the [[identity type|path induction rule]] applies to <code>paths X</code> not to <code>paths X x y</code>. Where for the former a proposition is fixed by what it does on identity paths, for the latter this is not the case anymore.

More generally, we can define arbitrary pullbacks. If `f : A -> C` and `g : B -> C`, the [[homotopy pullback]] of `f` and `g` is defined by

    {a : A & {b : B & f a ~~> g b}}

together with the obvious projections to `A` and `B` and the homotopy between the composites.
(a proof can be found [here](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/Pullbacks.v))

Using [[higher inductive types]], we can also define [[homotopy pushouts]]. if `g : C -> A` and `f : C -> B`, the [[homotopy pushout]] of `f` and `g` is defined by

    Inductive hopushout :=
      | inl : A -> hopushout
      | inr : B -> hopushout
      | glue : forall x : C, inl (g x) ~~> inr (f x).

together with the map `inl`, `inr` and the homotopy `glue`.
(see [here](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/Pushout.v) for the proof)


## References
 {#References}

### Introductions

Introductions to the idea of homotopy type theory include

* [[Steve Awodey]], _Type theory and homotopy_ ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/TTH.pdf))
 {#Awodey}

* [[Michael Shulman]], _Homotopy type theory_ [I](http://golem.ph.utexas.edu/category/2011/03/homotopy_type_theory_i.html), [II](http://golem.ph.utexas.edu/category/2011/03/homotopy_type_theory_ii.html), [III](http://golem.ph.utexas.edu/category/2011/03/homotopy_type_theory_iii.html), [IV](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_iv.html), [V](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_v.html), [VI](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html)

* [[Vladimir Voevodsky]], _[Univalent foundations](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations.html)_
  {#Voevodsky}

A guided walk through the formal proof in [[Coq]] that the [[univalence axiom]] implies [[functional extensionality]] is at

* [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_


### General

A blog serving as a base for the HoTT community is at

* _Homotopy Type Theory_ [website](http://homotopytypetheory.org/)
 {#HoTTSite}

Reports from a workshop on homotopy type theory are in 

* _Homotopy type theory_ , Oberwolfach Reports 11-2011, ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf)).


### Models

The first [[model]] for [[intensional type theory|intensional]] [[Martin-Löf type theory]] on [[groupoid]]s (instead of [[sets]] = [[0-groupoids]]) was

* [[Martin Hofmann]], [[Thomas Streicher]]  _The groupoid interpretation of type theory_. in Sambin, Giovanni (ed.) et al., _Twenty-five years of constructive type theory_ . Proceedings of a congress, Venice, Italy, October 19&#8212;21, 1995. Oxford: Clarendon Press. Oxf. Logic Guides. 36, 83-111 (1998).  ([ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz))

The fact that every [[simplicial model category]] in which the cofibrations are [[monomorphisms]] provides a sound [[model]] for [[intensional type theory|intensional]] [[Martin-Löf type theory]] is discussed in 

* [[Steve Awodey]], [[Michael Warren]], _Homotopy theoretic models of identity type_,  Mathematical Proceedings of the Cambridge Philosophical Society vol 146, no. 1 (2009) ([arXiv:0709.0248](http://arxiv.org/abs/0709.0248))
 {#AwodeyWarren}

and with more details in 

* [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, PhD thesis (2008) ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))

* [[Richard Garner]],  [[Benno van den Berg]], _Topological and simplicial models of identity types_. , ACM Transactions on Computational Logic ([pdf](http://www.mathematik.tu-darmstadt.de/~berg/papers/main.pdf))

What is not yet shown is that these models also validate the [[univalence axiom]]. This is currently only known to be the case for the standard [[model structure on simplicial sets]], hence for the archetypical [[(∞,1)-topos]] [[∞Grpd]] of [[discrete ∞-groupoids]].

In

* [[André Joyal]], _Remarks on homotopical logic_ Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))

is explicitly stated the conjecture that the models of HoTT are [[locally cartesian closed (∞,1)-categories]].

### Syntax

* [[Nicola Gambino]], [[Richard Garner]], _The identity type weak factorisation system_ , Theoretical Computer Science 409 (2008), no. 3, pages 94&#8211;109. 

* [[Richard Garner]], [[Benno van den Berg]],  _Types are weak &#969;-groupoids_ , 

* [[Peter LeFanu Lumsdaine]], _Weak &#969;-Categories from Intensional Type Theory_ , TLCA 2009, Bras&#237;lia, Logical Methods in Computer Science, Vol. 6, issue 23, paper 24. 

* [[Peter LeFanu Lumsdaine]], _Higher Categories from Type Theories_ , PhD Thesis: Carnegie Mellon University, 2010. [PDF]
    
* Michael Hedberg, _A coherence theorem for Martin-L&#246;f's type theory_ , Journal of Functional Programming 8 (4): 413&#8211;436, July 1998.
 

### Code
 {#Code}

The basic [[Coq]]-code libraries that set up [[identity types]] and the resulting homotopy type theory are at

* [https://github.com/HoTT/HoTT/tree/master/Coq](https://github.com/HoTT/HoTT/tree/master/Coq)

A slightly more human readable version is collected as a single pdf in

* _HoTT-Coq code_ ([[HoTT-Coq-code.pdf:file]]) .

A collection of all this code equipped with html-functionality that does display also the proofs (which otherwise only display when the code is loaded into a Coq-system) is at 

* _[Proviola/HoTT](http://mws.cs.ru.nl/proviola/HoTT/)_ .


More is in the repositories of various authors:

* [[Andrej Bauer]], ([GitHub](https://github.com/andrejbauer/Homotopy))

* [[Peter LeFanu Lumsdaine]], ([GitHub](https://github.com/peterlefanulumsdaine/Oberwolfach-explorations))

* [[Mike Shulman]], _Higher inductive types_ ([GitHub](https://github.com/HoTT/HoTT/tree/master/Coq/HIT))

* [[Vladimir Voevodsky]], _Foundations_ ([GitHub](https://github.com/vladimirias/Foundations/))


[[!redirects homotopy type theory]]
[[!redirects (∞,1)-type theory]]
[[!redirects (infinity,1)-type theory]]
[[!redirects univalent foundations]]

[[!redirects HoTT]]
[[!redirects internal language of an (∞,1)-topos]]