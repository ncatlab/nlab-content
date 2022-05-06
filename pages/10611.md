+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _modality_ in [[philosophy]] and formally in [[formal logic]]/[[type theory]] expresses a certain _mode_ (or "moment" as in [Hegel 12](#Hegel12)) of [[being]].

### In philosophy
 {#IdeaInPhilosophy}

According to ([Kant 1900](#Kant1900)) (see [WP](http://de.wikipedia.org/wiki/Kategorie_%28Philosophie%29)) the four "[[category (philosophy)|categories]]" are 

1. Quantity

1. Quality

1. Relation

1. Modality

and the modalities contain the three [[unity of opposites|pairs of opposites]]

* [[possibility]] - impossibility

* [[being]] - [[nothing]]

* [[necessity]] - Zuf&#228;lligkeit


### In formal logic
 {#InFormalLogic}

#### General

In [[formal logic]] and [[type theory]] modalities are formalized by
 _modal operator_ or _[[closure operator]]_ $\sharp$, that send [[propositions]]/[[types]] $X$ to new propositions/types $\sharp X$, satisfying some properties. 

Adding such modalities to [[propositional logic]] or similar produces what is called [[modal logic]]. Here operators that are meant to formalize [[necessity]] and [[possibility]] ([[S4 modal logic]]) are maybe most famous. Adding modalities more generally to [[type theory]] yields _[[modal type theory]]_. See there for more details.

The [[categorical semantics]] of these modalities is that $\sharp$ is interpreted an [[idempotent monad]]/[[comonad]] on the [[category of contexts]]. 

This has  a refinement to [[homotopy type theory]], where the [[categorical semantics]] of a _higher modality_ or _homotopy modality_ as an idempotent [[(infinity,1)-monad]] ([Shulman 12](#Shulman), [Rijke, Shulman, Spitters](#RSS) ).

#### In Homotopy Type Theory

There are a number of different but equivalent ways to define a modality in homotopy type theory [Rijke, Shulman, Spitters](#RSS).

* Higher modality: A modality consists of a modal operator $L : {Type} \to {Type}$ and for every type $X$ a modal unit $(-)^L : X \to LX$ together with 

1. an induction principle of type
$$\text{ind} : ((a : A) \to LB(a^L)) \to ((u : LA) \to LB(u))$$
for any type $A$ and type $B$ depending on $LA$

1. a computation rule
$$\text{com} : \text{ind}(f)(a^L) = f(a).$$

1. a witness that for any $x, y : LA$, the modal unit $(-)^L : (x = y) \to L(x = y)$ is an equivalence.

* Uniquely eliminating modality: A modality consists of a modal operator and modal unit such that operation 
$$f \mapsto f \circ (-)^L : ((u : LA) \to LB(u)) \to ((a : A) \to LB(a^L))$$
is an equivalence for all types $A$ and types $B$ depending on $LA$.

* $\Sigma$-closed reflective subuniverse (aka localization): A reflective subuniverse (a.k.a. localization) consists of a proposition $isLocal : {Type} \to {Prop}$ together with an operator $L : {Type} \to {Type}$ and a unit $(-)^L : X \to LX$ such that $LX$ is local for any type $X$ and for any local type $Z$, then function 
$$f \mapsto f \circ (-)^L : (LA \to Z) \to (A \to Z)$$
is an equivalence. A localization is $\Sigma$-closed if whenever $A$ is local and for all $a : A$, $B(a)$ is local, then the dependent sum $\Sigma_{a : A} B(a)$ is local. 

* Stable factorization systems: A modality consists of an orthogonal factorization system $(\mathcal{L}, \mathcal{R})$ in which the left class is stable under pullback. 

* A localization (reflective subuniverse) whose units $(-)^L : X \to LX$ are $L$-connected.

We say that a type $X$ is $L$-modal if the unit $(-)^L : X \to LX$ is an equivalence. We say a type $X$ $L$-connected if $LX$ is contractible. 

In terms of the other structure, the stable factorization system associated to a modality $L$ has

* left class the $L$-connected maps, whose fibers are $L$-connected.

* right class the $L$-modal maps, whose fibers are $L$-modal.

Conversely, given a stable factorization system, the modal operator and unit are given by factorizing the terminal map.

#### Notation
 {#Notation}

Typical notation (e.g. [SEP](#SEP), [Reyes 91](#Reyes91), but not [Hermida 10](#Hermida10)) is as follows: 

* a co-modality represented by an [[idempotent comonad]]  is typically denoted by $\Box$, following the traditional example of _[[necessity]]_ in [[modal logic]];

* a modality represented by an [[idempotent monad]] is typically denoted by $\lozenge$ or (less often) by $\bigcirc$, following the traditional example of _[[possibility]]_ in [[modal logic]].

When [[adjunctions]] between modalities matter ([[adjoint modalities]]), then some authors ([Reyes 91, p. 367](#Reyes91) [RRZ 04, p. 116](#ReyesEtAl), [Hermida 10, p.11](#Hermida10)) use $\lozenge$ for a [[left adjoint]] of a $\Box$. That leaves $\bigcirc$ as the natural choice of notation for a [[right adjoint]] (if any) of a $\Box$-modality.


This way for instance for [[cohesion]] with [[shape modality]] $\dashv$ [[flat modality|flat comodality]] $\dashv$ [[sharp modality]] the generic notation would be:

$$
  \array{
     monad && comonad && monad
     \\
     \lozenge &\dashv& \Box &\dashv& \bigcirc
     \\
     \\
     shape && flat && sharp
     \\
     &#643; &\dashv& \flat &\dashv& \sharp 
  }
$$



## Examples

* [[necessity]] $\dashv$ [[possibility]]

* [[local modality]], [[Lawvere-Tierney topology]]

* [[double negation modality]]

* [[n-truncation modality]]

* [[unit type]] modality, [[empty type]] co-modality ([[nothing]] $\dashv$ [[being]])

* [[exponential modality]]

* [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

* [[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]

* [[affine modality]]

* [[graded modality]]

## Related concepts

* [[graded modality]]

* [[de dicto and de re]]

* [[monad (in computer science)]]

* [[modal type]], [[anti-modal type]]

* [[adjoint modality]], [[adjoint logic]]

* [[Galois connection]]

## References
 {#References}

### In formal logic

Discussion in [[formal logic]] and [[homotopy type theory]] ([[modal type theory]]):

* [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]], October 2012  ([pdf](http://uf-ias-2012.wikispaces.com/file/view/modalitt.pdf))
 {#Shulman}

* [[Mike Shulman]], _[All modalities are Higher Inductive Types](http://homotopytypetheory.org/2012/11/19/all-modalities-are-hits/)_

* {#RSS} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], _Modalities in homotopy type theory_ [arXiv](https://arxiv.org/abs/1706.07526)

### In philosopy

* [[Georg Hegel]], _[[Science of Logic]]_, 1812
 {#Hegel12}

* [[Kant]], AA III, 93&#8211; KrV B 106
 {#Kant1900}

* German Wikipedia, _[Modalit&#228;t (Philosophie)](https://de.wikipedia.org/?curid=3382094)_

* {#SEP} Stanford Encyclopedia of Philosophy, _[Modal Logic](http://plato.stanford.edu/entries/logic-modal/)_

* {#Reyes91} [[Gonzalo Reyes]], _A topos-theoretic approach to reference and modality_, Notre Dame J. Formal Logic Volume 32, Number 3 (1991), 359-391 ([Euclid](http://projecteuclid.org/euclid.ndjfl/1093635834))

* {#ReyesEtAl} Reyes/Reyes/Zolfaghari, _Generic Figures and Their Glueings_ 2004, Polimetrica

* {#Hermida10} [[Claudio Hermida]], section 3.3. of _A categorical outlook on relational modalities and simulations_, 2010 ([pdf](http://maggie.cs.queensu.ca/chermida/papers/sat-sim-IandC.pdf))


[[!redirects modality]]
[[!redirects modalities]]
[[!redirects modal operator]]
[[!redirects modal operators]]

[[!redirects comodality]]
[[!redirects comodalities]]
[[!redirects comodal operator]]
[[!redirects comodal operators]]

[[!redirects co-modality]]
[[!redirects co-modalities]]
[[!redirects co-modal operator]]
[[!redirects co-modal operators]]

