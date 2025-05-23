
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

[[type theory|Type theory]] and certain kinds of [[category theory]] are closely related.  By a [[syntax-semantics duality]] one may view type theory as a formal [[syntax|syntactic]] language or _calculus_ for category theory, and conversely one may think of category theory as providing [[categorical semantics|semantics]] for type theory.  The flavor of category theory used depends on the flavor of type theory; this also extends to [[homotopy type theory]] and certain kinds of [[(∞,1)-category theory]].
 


## Overview
 {#Overview}

| internal logic/type theory (syntax) | $\;$equivalent to$\;$ | category of contexts (semantics) | |
|--|--|--|--|
| [[propositional logic]] | | [[Lindenbaum-Tarski algebra]] | |
| [[intuitionistic logic|intuitionistic]] [[propositional logic]] | | [[Heyting algebra]] | |
| [[classical logic|classical]] [[propositional logic]] | | [[Boolean algebra]] | |
| [[dual intuitionistic logic|dual intuitionistic]] [[propositional logic]] | | [[co-Heyting algebra]] | |
| [[first-order logic]] |  | [[hyperdoctrine]] | [Seely 1984a](#SeelyA) |
| [[regular logic]] |  | [[regular hyperdoctrine]]/[[regular category]] | |
| [[coherent logic]] |  | [[coherent hyperdoctrine]]/[[coherent category]] | |
| [[intuitionistic logic|intuitionistic]] [[predicate logic]] |  | [[first-order hyperdoctrine]]/[[Heyting category]] | |
| [[classical logic|classical]] [[predicate logic]] |  | [[Boolean hyperdoctrine]]/[[Boolean category]] | |
| [[modal logic]] |  | [[modal hyperdoctrine]] | |
| [[linear logic]] |  | [[linear hyperdoctrine]] | |
| [[simply-typed lambda calculus]] | | [[cartesian closed category]] | [Lambek & Scott 1986, Part I](#LambekScott86) |
| extensional [[dependent type theory]]|  | [[locally cartesian closed category]] | [Seely 1984b](#Seely84b) |
| [[bunched logic]] | | [[doubly closed monoidal category]] |  [O'Hearn & Pym 1999](bunched+logic#O'HearnPym99) |
| [[homotopy type theory]] without [[univalence]] (intensional M-L dependent type theory) |  | [[locally cartesian closed (∞,1)-category]] | [Cisinski 2012](locally+cartesian+closed+%28infinity%2C1%29-category#Presentations) & [Shulman 2012](#Shulman12) |
| [[homotopy type theory]] with [[higher inductive types]] and [[univalence]] |  | [[elementary (∞,1)-topos]] | see [[homotopytypetheory:model of type theory in an (infinity,1)-topos|here]] |
| [[multiplicative intuitionistic linear logic]] | | [[symmetric monoidal category|symmetric]] [[closed monoidal category]] | [various authors since ~68](linear%20type%20theory#HistoryCategoricalSemantics) | 
| [[classical linear logic]] | | [[star-autonomous category ]] | [Seely 1989](#Seely89) |
| [[dependent linear type theory]] |   | [[indexed monoidal category]] (with comprehension)  | [Riley 2022](#Riley22Thesis) |  

[[!include types and logic - table]]

## Theorems
 {#Theorems}

We discuss here formalizations and proofs of the relation/equivalence between various flavors of type theories and the corresponding flavors of categories.

* [First order logic and hyperdoctrines](#FirstOrderLogic)

* [Dependent type theory and locally cartesian closed categories](#DependentTypeTheory)

* [Homotopy type theory and locally cartesian closed (∞,1)-categories](#HomotopyTypeTheory)

* [Univalent homotopy type theory and elementary (∞,1)-toposes](#HomotopyWithUnivalence)


### First-order logic and hyperdoctrines
 {#FirstOrderLogic}

+-- {: .num_theorem}
###### Theorem

The [[functors]] 

* $Cont$, that form a [[category of contexts]] of a [[first-order logic|first-order theory]];

* $Lang$, that forms the [[internal language]] of a [[hyperdoctrine]]

constitute an [[equivalence of categories]]

$$
  FirstOrderTheories
    \stackrel{\overset{Lang}{\leftarrow}}{\underset{Cont}{\to}}
  Hyperdoctrines
  \,.
$$

=--


([Seely, 1984a](#SeelyA))


### Dependent type theory and locally cartesian closed categories
 {#DependentTypeTheory}

We discuss here how [[dependent type theory]] is the syntax of which [[locally cartesian closed categories]] provide the [[semantics]]. For a dedicated discussion of this (and the subtle [[coherence]] issues involved) see also at _[[categorical model of dependent types]]_.

+-- {: .num_theorem #SeelyEquivalence}
###### Theorem

There are [[2-functors]] 

* $Cont$, that forms a [[category of contexts]] of a [[Martin-Löf dependent type theory]];

* $Lang$ that forms the [[internal language]] of a [[locally cartesian closed category]]

that constitute an [[equivalence of 2-categories]]

$$
  MLDependentTypeTheories
    \underoverset
     {\underset{Cont}{\longrightarrow}}
     {\overset{Lang}{\longleftarrow}}
     {\simeq}
  LocallyCartesianClosedCategories
  \,.
$$

=--

This was originally claimed as an [[equivalence of categories]] [Seely 1974 theorem 6.3](#Seely84b). However, that argument did not properly treat a subtlety central to the whole subject: that [[substitution]] of [[terms]] for [[variables]] composes strictly, while its [[categorical semantics]] by [[pullback]] is by the [[universal construction|very nature]] of pullbacks only defined up to [[isomorphism]]. This problem was pointed out and ways to fix it were given by [Curien](#Curien) and [Hofmann](#Hofmann); see _[[categorical model of dependent types]]_ for the latter.  However, the full equivalence of categories was not recovered until [Clairambault & Dybjer](#ClairambaultDybjer) solved both problems by promoting the statement to an [[equivalence of 2-categories]], see also [Curien, Garner & Hofmann](#CurienGarnerHofmann). Another approach to this which also works with [[intensional identity types]] and hence with [[homotopy type theory]] is in [Lumsdaine & Warren 2013](#LumsdaineWarren13).

We now indicate some of the details.



#### Type theories
 {#TypeTheories}

For definiteness, self-containedness and for references below, we say what a [[dependent type theory]] is, following ([Seely, def. 1.1](#Seely)).

+-- {: .num_defn}
###### Definition

A **Martin-L&#246;f [[dependent type theory]]** $T$ is a _[[theory]]_ with some [[signature (in logic)|signature]] of dependent function symbols with values in types and in terms (...) subject to the following rules

1. **type formation rules** 

   1. $1$ is a type (the [[unit type]]);
  
   1. if $a, b$ are terms of type $A$, then $(a = b)$ is a type (the [[equality type]]);

   1. if $A$ and $B[x]$ are types, $B$ depending on a [[free variable]] of type $A$, then the following symbols are types

      1. $\prod_{a : A} B[a]$ ([[dependent product]]), written also $(A \to B)$ if $B[x]$ in fact does not depend on $x$;

      1. $\sum_{a : A} B[a]$ ([[dependent sum]]), written also $A \times B$ if $B[x]$ in fact does not depend on $x$;

1. **term formation rules**

   1. $* \in 1$ is a term of the [[unit type]];

   1. (...)

1. **equality rules**

   1. (...)


=--


#### Category of contexts

+-- {: .num_defn}
###### Definition

Given a [[dependent type theory]] $T$, its **[[category of contexts]]** $Con(T)$ is the category whose

* [[objects]] are the [[types]] of $T$;

* [[morphisms]] $f : A \to B$ are the [[terms]] $f$ of [[function type]] $A \to B$.

Composition is given in the evident way.
 
=--

+-- {: .num_prop}
###### Proposition

$Con(T)$ has [[finite limits]] and is a [[cartesian closed category]].

=--

([Seely, prop. 3.1](#Seely))

+-- {: .proof}
###### Proof

Constructions are straightforward. We indicated some of them. 

Notice that all [[finite limits]] (as discussed there) are induced as soon as there are all [[pullbacks]] and [[equalizers]]. A [[pullback]] in $Con(T)$

$$
  \array{
    P &\to& A
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    B &\stackrel{g}{\to}& C
  }
$$

is given by 

$$
  P \simeq \sum_{a : A} \sum_{b \in B} (f(a) = g(b))
  \,.
$$

The [[equalizer]]

$$
  P \to A \stackrel{\overset{f}{\to}}{\underset{g}{\to}} B
$$

is given by

$$
  P = \sum_{a : A} (f(a) = g(a))
  \,.
$$

Next, the [[internal hom]]/[[exponential object]] is given by [[function type]]

$$
  [A,B] \simeq (A \to B)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

$Con(T)$ is a [[locally cartesian closed category]].

=--

([Seely, theorem 3.2](#Seely))

+-- {: .proof}
###### Proof

Define the $Con(T)$-[[indexed category|indexed]] [[hyperdoctrine]] $P(T)$
by taking for $A \in Con(T)$ the category $P(T)(A)$ to have as objects the $A$-[[dependent types]] and as morphisms $(a : A \vdash X(a) : type) \to (a : A \vdash Y(a) : type)$ the terms of dependent function type $(a : A \vdash t : (X(a) \to Y(a)))$.

This is cartesian closed by the same kind of argument as in the previous proof. It is now sufficient to exhibit a compatible [[equivalence of categories]] with the [[slice category]] $Con(T)_{/A}$.

$$
  Con(T)_{/A}
   \simeq
  P(T)(A)
  \,.
$$

In one direction, send a morphism $f : X \to A$ to the dependent type 

$$
  a : A \vdash f^{-1}(a) \coloneqq \sum_{x : X} (a = f(x))
  \,.
$$

Conversely, for $a : A \vdash X(a)$ a dependent type, send it to the projection
$\sum_{a : A} X(a) \to A$.

One shows that this indeed gives an equivalence of categories which is compatible with base change ([Seely, prop. 3.2.4](#Seely)).

=--

+-- {: .num_defn}
###### Definition

For $T$ a dependent type theory and $C$ a locally cartesian closed category, an **[[categorical semantics|interpretation]]** of $T$ in $C$ is a morphism of locally cartesian closed categories

$$
  Con(T) \to C
  \,.
$$

An interpretation of $T$ in another dependent type theory $T'$ is a morphism of locally cartesian closed categories

$$
  Con(T) \to Con(T')
  \,.
$$

=--


#### Internal language

+-- {: .num_prop}
###### Proposition

Given a [[locally cartesian closed category]] $C$, define the corresponding [[dependent type theory]] $Lang(C)$ as follows

* the non-dependent types of $Lang(C)$ are the [[objects]] of $C$;

* the $A$-dependent types are the morphisms $B \to A$;

* a context $x_1 : X_1 , x_2 : X_2, \cdots , x_n : X_n$ is a tower of morphisms

  $$
    \array{
      X_n
      \\
      \downarrow
      \\
      \cdots
      \\
      \downarrow
      \\
      X_2
      \\
      \downarrow
      \\
      X_1
    }
  $$

* the terms $t[x_A] : B[x_A]$ are the [[sections]] $A \to B$ in $C_{/A}$

* the [[equality type]] $(x_A = y_A)$ is the [[diagonal]] $A \to A \times A$

* ...

=--


### Homotopy type theory and locally cartesian closed $(\infty,1)$-categories
 {#HomotopyTypeTheory}

All of the above has an analog in [[(∞,1)-category theory]] and [[homotopy type theory]].

+-- {: .num_prop }
###### Proposition

Every [[presentable (∞,1)-category|presentable]] and [[locally cartesian closed (∞,1)-category]] has a presentation by a [[type-theoretic model category]]. This provides the [[categorical semantics]] for [[homotopy type theory]] (without, possibly, the [[univalence]] [[axiom]]).

This includes in particular all ([[∞-stack]]-) [[(∞,1)-toposes]] (which should in addition satisfy [[univalence]]). See also at _[[internal logic of an (∞,1)-topos]]_.

=--

Some form of this statement was originally formally conjectured in ([Joyal 11](#Joyal11)), following ([Awodey 10](#Awodey10)). For more details see at _[locally cartesian closed (∞,1)-category](locally+cartesian+closed+%28infinity%2C1%29-category#InternalLogic)_.



### Univalent homotopy type theory and elementary $(\infty,1)$-toposes
 {#HomotopyWithUnivalence}

> For more details see *[[model of type theory in an (infinity,1)-topos]]*.

A ([[locally presentable (∞,1)-category|locally presentable]]) [[locally Cartesian closed (∞,1)-category]] (as [above](#HomotopyTypeTheory)) which in addition has a system of [[object classifiers]] is an ([[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]]-)[[(∞,1)-topos]].

It has been conjectured in ([Awodey 10](#Awodey10)) that this [[object classifier]] is the categorical semantics of a [[univalence|univalent]] [[type universe]] ([[type of types]]), hence that [[homotopy type theory]] with [[univalence]] has categorical semantics in [[(∞,1)-toposes]].  This statement was proven for the canonical $(\infty,1)$-topos [[∞Grpd]] in ([Kapulkin-Lumsdaine-Voevodsky 12](#KapulkinLumsdaineVoevodsky12)), and more generally for [[(∞,1)-presheaf]] $(\infty,1)$-toposes over [[elegant Reedy categories]] in ([Shulman 13](#Shulman13)). The general case is proven in [Shulman 19](#Shulman19).

In these proofs the [[type-theoretic model categories]] which interpret the homotopy type theory syntax are required to provide type universes that behave strictly under pullback.  This matches the usual syntactically convenient universes in type theory (either a la Russell or a la Tarski), but more difficult to implement in the categorical semantics.  More flexibly, one may consider syntactic [type universes weakly &#224; la Tarski](type+of+types#TarskiStyle) ([Luo 12](Luo12), [Gallozzi 14](#Gallozzi14)).  These are more complicated to work with syntactically, but should have interpretations in a ([[type-theoretic model categories]] presenting) any [[(∞,1)-topos]].  Discussion of [[univalence]] in this general flexible sense is in ([Gepner-Kock 12](#GepnerKock12)). For the general syntactic issue see at 

* [[homotopytypetheory:model of type theory in an (infinity,1)-topos]]

While [[(∞,1)-sheaf]] [[(∞,1)-toposes]] are those currently understood, the basic type theory with univalent universes does not see or care about their [[locally presentable (∞,1)-category|local presentability]] as such (although it is used in other places, such as the construction of [[higher inductive types]]).  It is to be expected that there is a decent concept of [[elementary (∞,1)-topos]] such that [[homotopy type theory]] with [[univalence|univalent]] [[type universes]] and some supply of [[higher inductive types]] has categorical semantics precisely in [[elementary (∞,1)-toposes]] (as conjectured in [Awodey 10](#Awodey10)). But the fine-tuning of this statement is currently still under investigation.

Notice that this statement, once realized, makes (or would make) Univalent HoTT+HITs a sort of [[homotopy theory|homotopy theoretic]] refinement of [[foundations of mathematics]] in [[topos theory]] as proposed by [[William Lawvere]].  It could be compared to his [[elementary theory of the category of sets]], although being a type theory rather than a theory in first-order logic, it is more analogous to the internal type theory of an elementary topos.






## Related concepts

* [[initiality conjecture]]

* [[categorical model of dependent types]]

* [[syntax-semantics duality]]

* [[computational trinitarianism]]

* [[Awodey's conjecture]]


## References
 {#References}


An elementary exposition of in terms of the [[Haskell]] [[programming language]] is in

* WikiBooks, _[Haskell/The Curry&#8211;Howard isomorphism](https://en.wikibooks.org/wiki/Haskell/The_Curry%E2%80%93Howard_isomorphism)_


The [[equivalence of categories]] between [[first order logic|first order theories]] and [[hyperdoctrines]] is discussed in

* {#SeelyA} [[R. A. G. Seely]], _Hyperdoctrines, natural deduction, and the Beck condition_, Zeitschrift f&#252;r Math. Logik und Grundlagen der Math. (1984) ([pdf](http://www.math.mcgill.ca/rags/ZML/ZML.PDF))
 
The [[categorical model of dependent types]] and initiality is discussed in

* Simon Castellan, _Dependent type theory as the initial category with families_, 2014 ([pdf](http://iso.mor.phis.me/archives/2011-2012/stage-2012-goteburg/report.pdf))

which was formalized inside type theory with set quotients of [[higher inductive types]] in:

* {#AltKap2015} [[Thorsten Altenkirch]], Ambrus Kaposi, _Type Theory in Type Theory using Quotient Inductive Types_, (2015) ([pdf](http://www.cs.nott.ac.uk/~txa/publ/tt-in-tt.pdf)), ([formalisation in Agda](https://bitbucket.org/akaposi/tt-in-tt)).

Surveys inclue 

* [[Tom Hirschowitz]], _Introduction to categorical logic_ (2010) ([pdf](http://www.lama.univ-savoie.fr/~hirschowitz/talks/cours.pdf)) 

  (see the discussion building up to the theorem on  [slide 96](http://www.lama.univ-savoie.fr/~hirschowitz/talks/cours.pdf#page=96))

* Roy Crole, _Deriving category theory from type theory_, Theory and Formal Methods 1993 Workshops in Computing 1993, pp 15-26

* {#Maietti05} [[Maria Maietti]], _Modular correspondence between dependent type theories and categories including pretopoi and topoi_, Mathematical Structures in Computer Science archive Volume 15 Issue 6, December 2005  Pages 1089 - 1149 ([pdf](https://www.math.unipd.it/~maietti/papers/tumscs.pdf))


The [[categorical semantics]] of [[linear logic]] in [[star-autonomous categories]] is due to

* {#Seely89} [[R. A. G. Seely]],  *Linear logic, $\ast$-autonomous categories and cofree coalgebras*, in *Categories in Computer Science and Logic*, Contemporary Mathematics **92** (1989)  &lbrack;[[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz), [ISBN:978-0-8218-5100-5](https://bookstore.ams.org/conm-92)&rbrack;

and reviews/further developments are in 

* G. M. Bierman, _What is a Categorical Model of Intuitionistic Linear Logic?_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.31.8687))

* Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))


* [[Paul-André Melliès]] , _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))


For [[dependent linear type theory]] see:


* {#Vakar14} [[Matthijs Vákár]], _Syntax and Semantics of Linear Dependent Types_ &lbrack;[arXiv:1405.0033](http://arxiv.org/abs/1405.0033)&rbrack;

* {#RileyFinsterLicata21} [[Mitchell Riley]], [[Eric Finster]], [[Daniel Licata]], *Synthetic Spectra via a Monadic and Comonadic Modality* &lbrack;[arXiv:2102.04099](https://arxiv.org/abs/2102.04099)&rbrack;

* [[Mitchell Riley]], *Extending Homotopy Type Theory with Linear Type Formers*, talk at *The ForML Lab* (2021)  &lbrack;[web](https://the-au-forml-lab.github.io/colloquium_talks/Riley.html), [video](https://www.youtube.com/watch?v=sPxtdCtjSDc)&rbrack;

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269), [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;

  > (using ideas from [[bunched logic]])

* {#Riley22} [[Mitchell Riley]], *Linear Homotopy Type Theory*, talk at: [HoTTEST Event for Junior Researchers 2022](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest_junior_2022.html)  (Jan 2022) &lbrack;slides: [pdf](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Riley-2022-01-20-HoTTEST.pdf), video: [YT](https://www.youtube.com/watch?v=o2oWhHabjdM)&rbrack;


The relation between [[typed lambda-calculus]] and [[cartesian closed categories]] is discussed in part I, and the [[adjunction]] between the category of [[type theory|type theories]] with [[product types]] and [[toposes]] is discussed in chapter II of:

* {#LambekScott86} [[Joachim Lambek]], [[Philip J. Scott]], *Introduction to higher order categorical logic*, Cambridge Studies in Advanced Mathematics **7** (1986) &lbrack;[ISBN: 0-521-24665-2](https://www.cambridge.org/ae/academic/subjects/mathematics/logic-categories-and-sets/introduction-higher-order-categorical-logic?format=PB&isbn=9780521356534), [pdf](https://raw.githubusercontent.com/Mzk-Levi/texts/master/Lambek%20J.%2C%20Scott%20P.J.%20Introduction%20to%20Higher%20Order%20Categorical%20Logic.pdf)&rbrack;

The [[equivalence of categories]] between [[locally cartesian closed categories]] and [[dependent type theories]] was originally claimed in 

* {#Seely84b} [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. **95** (1984) 33-48  &lbrack;[doi:10.1017/S0305004100061284](https://doi.org/10.1017/S0305004100061284), [pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf)&rbrack;


following a statement earlier conjectured in 

* [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, In Logic Colloquium (1973), ed. H. E. Rose and J. C. Shepherdson (North-Holland, 1974), 73-118. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))

The problem with strict substitution compared to weak pullback in this argument was discussed and fixed in 

* {#Curien} [[Pierre-Louis Curien]], *Substitution up to isomorphism*, Fundamenta Informaticae, **19** 1-2 (1993) 51-86 &lbrack;[doi:10.5555/175469.175471](https://dl.acm.org/doi/10.5555/175469.175471)&rbrack; and: Diagrammes **23** (1990) 43-66 &lbrack;[numdam:DIA_1990__23__43_0](http://www.numdam.org/item/DIA_1990__23__43_0)&rbrack;
 

* {#Hofmann} [[Martin Hofmann]], *On the interpretation of type theory in locally cartesian closed categories*, in *Computer Science Logic. CSL 1994*, Lecture Notes in Computer Science **933** (1994) 427–441 &lbrack;[doi:10.1007/BFb0022273](https://doi.org/10.1007/BFb0022273)&rbrack;

but in the process the equivalence of categories was lost. This was finally all rectified in 

* {#ClairambaultDybjer} [[Pierre Clairambault]], [[Peter Dybjer]], *The Biequivalence of Locally Cartesian Closed Categories and Martin-L&#246;f Type Theories*, in *Typed lambda calculi and applications*, Lecture Notes in Comput. Sci. **6690** Springer (2011) &lbrack;[arXiv:1112.3456](http://arxiv.org/abs/1112.3456), [doi:10.1007/978-3-642-21691-6_10](https://doi.org/10.1007/978-3-642-21691-6_10)&rbrack;
 
and

* {#CurienGarnerHofmann} [[Pierre-Louis Curien]], [[Richard Garner]], [[Martin Hofmann]], *Revisiting the categorical interpretation of dependent type theory*, Theoretical Computer Science **546** 21 (2014) 99-119 &lbrack;[doi:10.1016/j.tcs.2014.03.003](https://doi.org/10.1016/j.tcs.2014.03.003), [[CurienGarnerHofmann.pdf:file]]&rbrack;

Another version of this which also applies to [[intensional identity types]] and hence to [[homotopy type theory]] is in

* {#LumsdaineWarren13} [[Peter LeFanu Lumsdaine]], [[Michael Warren]], _An overlooked coherence construction for dependent type theory_, CT2013 ([[LumsdaineWarren2013.pdf:file]])

* [[Peter LeFanu Lumsdaine]], [[Michael Warren]], _The local universes model: an overlooked coherence construction for dependent type theories_ ([arXiv:1411.1736](http://arxiv.org/abs/1411.1736))

The analogous statement relating [[homotopy type theory]] and [[locally cartesian closed (infinity,1)-categories]] was formally conjectured around

* {#Joyal} [[André Joyal]], _Remarks on homotopical logic_, Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))
 
following earlier suggestions by [[Steve Awodey]]. Explicitly, the suggestion that with the [[univalence]] axiom added this is refined to [[(∞,1)-topos theory]] appears around

* {#Awodey} [[Steve Awodey]], _Type theory and homotopy_ ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/TTH.pdf))
 

Details on this higher categorical semantics of [[homotopy type theory]] are in 

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_ (*From type theory and homotopy theory to Univalent Foundations of Mathematics*), Mathematical Structures in Computer Science **25** 5  (2015) &lbrack;[arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565)&rbrack;

with lecture notes in 

* [[Mike Shulman]], _Categorical models of homotopy type theory_, April 13, 2012 ([pdf](https://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf))

* {#Joyal11} [[André Joyal]], _Remarks on homotopical logic_, Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))

* {#Joyal14} [[André Joyal]], _Categorical homotopy type theory_, March 17, 2014 ([pdf](http://ncatlab.org/homotopytypetheory/files/Joyal.pdf))

See also

* {#Kapulkin14} [[Chris Kapulkin]], _Type theory and locally cartesian closed quasicategories_, Oxford 2014 ([video](https://www.youtube.com/watch?v=g87bZJ2bvYk))

* [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], _The homotopy theory of type theories_, Advances in Mathematics **337** (2018) 1-38 ([arXiv:1610.00037](https://arxiv.org/abs/1610.00037), [doi:10.1016/j.aim.2018.08.003](https://doi.org/10.1016/j.aim.2018.08.003))

* {#KapulkinSzumilo17} [[Chris Kapulkin]], [[Karol Szumilo]], _Internal Language of Finitely Complete $(\infty,1)$-categories_ ([arXiv:1709.09519](https://arxiv.org/abs/1709.09519))

* {#Isaev16} [[Valery Isaev]], _Algebraic Presentations of Dependent Type Theories_ ([arXiv:1602.08504](https://arxiv.org/abs/1602.08504))

* {#Isaev18} [[Valery Isaev]], _Morita equivalences between algebraic dependent type theories_ ([arXiv:1804.05045](https://arxiv.org/abs/1804.05045))

Models specifically in ([[constructive set theory|constructive]]) [[cubical sets]] are discussed in

* {#BezemCoquandHuber13} Marc Bezem, [[Thierry Coquand]], Simon Huber, _A model of type theory in cubical sets_, 2013  ([web](http://drops.dagstuhl.de/opus/volltexte/2014/4628/), [pdf](http://drops.dagstuhl.de/opus/volltexte/2014/4628/pdf/7.pdf))

* {#KaposiAltenkirch14} Ambrus Kaposi, [[Thorsten Altenkirch]], _A syntax for cubical type theory_ ([pdf](http://mazzo.li/dump/aim-kaposi-pres.pdf))

* {#Docherty14} Simon Docherty, _A model of type theory in cubical sets with connection_, 2014 ([pdf](http://www.illc.uva.nl/Research/Publications/Reports/MoL-2014-12.text.pdf))


A precise definition of [[elementary (infinity,1)-topos]] inspired by giving a natural equivalence to [[homotopy type theory]] with [[univalence]] was then proposed in 

* [[Mike Shulman]], _Inductive and higher inductive types_ (2012) ([pdf](http://www.sandiego.edu/~shulman/hottminicourse2012/04induction.pdf))

Categorical semantics of [[univalence|univalent]] [[type universes]] is discussed in 

* {#Awodey10} [[Steve Awodey]], _Type theory and homotopy_ (2010) ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/TTH.pdf))

* {#KapulkinLumsdaineVoevodsky12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], _The Simplicial Model of Univalent Foundations_ ([arXiv:1211.2851](http://arxiv.org/abs/1211.2851))

* {#Shulman13} [[Michael Shulman]], _The univalence axiom for elegant Reedy presheaves_ ([arXiv:1307.6248](http://arxiv.org/abs/1307.6248))

* {#GepnerKock12} [[David Gepner]], [[Joachim Kock]], _Univalence in locally cartesian closed ∞-categories_ ([arXiv:1208.1749](http://arxiv.org/abs/1208.1749))

* {#Cisinski14} [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_ ([arXiv:1406.0058](http://arxiv.org/abs/1406.0058))

Proof of [[Awodey's conjecture]], that all [[∞-stack]] [[(∞,1)-topos]] have [[presentable (∞,1)-category|presentations]] by [[model categories]] which interpret (provide [[categorical semantics]]) for [[homotopy type theory]] with [[univalence|univalent]] [[type universes]]:

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004)).

Introduction and review in: 

* {#Riehl22} [[Emily Riehl]], *On the $\infty$-topos semantics of homotopy type theory*, lecture at *[Logic and higher structures](https://conferences.cirm-math.fr/2689.html)* CIRM (Feb. 2022) &lbrack;[pdf](https://emilyriehl.github.io/files/semantics.pdf), [[Riehl-InfinityToposSemantics.pdf:file]]&rbrack;

Discussion of weak Tarskian homotopy type universes is in 

* {#Luo12} [[Zhaohui Luo]], _Notes on Universes in Type Theory_, 2012 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/universes.pdf))


* {#Gallozzi14} [[Cesare Gallozzi]], _Constructive Set Theory from a Weak Tarski Universe_, MSc thesis (2014) ([[GalloziCSTTarski.pdf:file]])


A discussion of the correspondence between type theories and categories of various sorts, from lex categories to toposes is in

* Maria Emilia Maietti, _Modular correspondence between dependent type
theories and categories including pretopoi and topoi_, Math. Struct. in Comp. Science (2005), vol. 15, pp. 1089&#8211;1149 ([gzipped ps](http://www.math.unipd.it/~maietti/papers/tumscs.ps.gz)) ([doi](http://dx.doi.org/10.1017/S0960129505004962))


[[!redirects relation between category theory and type theory]]
[[!redirects the relation between type theory and category theory]]
[[!redirects the relation between category theory and type theory]]