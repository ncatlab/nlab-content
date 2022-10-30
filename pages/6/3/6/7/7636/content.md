
> under construction

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
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

To a large extent, [[type theory]] and [[category theory]] overlap or are equivalent, and more generally so are [[homotopy type theory]] and [[(∞,1)-category theory]]. One may view type theory as a formal [[syntax|syntactic]] language or _calculus_ for category theory, and conversely one may think of category theory as providing [[categorical semantics|semantics]] for type theory. 

## Overview
 {#Overview}

| flavor of type theory  | $\;$equivalent to$\;$ | flavor of category theory | |
|--|--|--|--|
|[[first-order logic]] |  | [[hyperdoctrine]] | ([Seely 1984a](#SeelyA)) |
|[[dependent type theory]]|  | [[locally cartesian closed category]] | ([Seely 1984b](#Seely)) |
|[[homotopy type theory]]|  | [[locally cartesian closed (∞,1)-category]] | (conjectural) |
|[[homotopy type theory]] with [[higher inductive types]] and [[univalence]] |  | [[elementary (∞,1)-topos]] | (conjectural) |


## Theorems

We discuss here formalizations and proofs of the relation/equivalence between various flavors of type theories and the corresponding flavors of categories.

* [First order logic and hyperdoctrines](#FirstOrderLogic)

* [Dependent type theory and locally cartesian closed categories](#DependentTypeTheory)

* [Homotopy type theory and locally cartesian closed (∞,1)-categories](#HomotopyTypeTheory)

* [Homotopy type theory with univalence and elementary (∞,1)-toposes](#HomotopyWithUnivalence)

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

+-- {: .num_theorem}
###### Theorem

There are [[2-functors]] 

* $Cont$, that forms a [[category of contexts]] of a [[dependent type theory]];

* $Lang$ that forms the [[internal language]] of a [[locally cartesian closed category]]

that constitute an [[equivalence of 2-categories]]

$$
  DependentTypeTheories
    \stackrel{\overset{Lang}{\leftarrow}}{\underset{Cont}{\to}}
  LocallyCartesianClosedCategories
  \,.
$$

=--

This was originally claimed as an [[equivalence of categories]] ([Seely, theorem 6.3](#Seely)). However, that argument did not properly treat a subtlety central to the whole subject: that [[substitution]] of [[terms]] for [[variables]] composes strictly, while its [[categorical semantics]] by [[pullback]] is by the [[universal construction|very nature]] of pullbacks only defined up to [[isomorphism]]. This problem was pointed out and a way to fix it was given in ([Curien](#Curien)) and ([Hofmann](#Hofmann)), which however lost sight of the equivalence of categories. Finally  ([Clairambault-Dybjer](#ClairambaultDybjer)) solved both problems by promoting the statement to an [[equivalence of 2-categories]].

We now indicate some of the details.

#### Type theories

For definiteness, self-containedness and for references below, we say what a [[dependent type theory]] is, following ([Seely, def. 1.1](#Seely)).

+-- {: .num_defn}
###### Definition

A **[[dependent type theory]]** or **[[Martin-Löf type theory]]** $T$ is a _[[theory]]_ with some [[signature (in logic)]] of function symbols with values in types and in terms (...) subject to the following rules

1. **type formation rules** 

   1. $1$ is a type (the [[unit type]]);
  
   1. if $a, b$ are terms of type $A$, then $(a = b)$ is a type (the [[equality type]]);

   1. if $A$ and $B[x]$ are types, $B$ depending on a [[free variable]] of type $A$, then the following symbols are types

      1. $\prod_{a : A} B[a]$ ([dependent product]), written also $(A \to B)$ if $B[x]$ in fact does not depend on $x$;

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

* a context $x_1 : X , x_2 : X, \cdots , x_n : X_n$ is a tower of morphisms

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

(...)

### Homotopy type theory with univalence and elementary $(\infty,1)$-toposes
 {#HomotopyWithUnivalence}

(...)

## References

The [[equivalence of categories]] between [[first order logic|first order theories]] and [[hyperdoctrines]] is discussed in

* [[R. A. G. Seely]], _Hyperdoctrines, natural deduction, and the Beck condition_, Zeitschrift f&#252;r Math. Logik und grundlagen der Math. (1984) ([pdf](http://www.math.mcgill.ca/rags/ZML/ZML.PDF))
 {#SeelyA}

A lecture reviewing aspects involved in this equivalence is (see the discussion building up to the theorem on  [slide 96](www.lama.univ-savoie.fr/~hirschowitz/talks/cours.pdf#page=96))

* [[Tom Hirschowitz]], _Introduction to categorical logic_ (2010) ([pdf](http://www.lama.univ-savoie.fr/~hirschowitz/talks/cours.pdf))

An [[adjunction]] between the category of [[type theories]] with [[product types]] and [[toposes]] is discussed in chapter II of

* [[Joachim Lambek]], P. Scott, _Introduction to higher order categorical logic_, Cambridge University Press (1986) .

The [[equivalence of categories]] between [[locally cartesian closed categories]] and [[dependent type theories]] was originally claimed in 

* [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))
  {#Seely}

following a statement earlier conjectured in 

* [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, In Logic Colloquium (1973), ed. H. E. Rose and J. C. Shepherdson (North-Holland, 1974), 73-118.

The problem with strict substitution compared to weak pullback in this argument was discussed and fixed in 

* [[Pierre-Louis Curien]], _Substitution up to isomorphism_, Fundamenta Informaticae, 19(1,2):51&#8211;86 (1993)
 {#Curien}

* [[Martin Hofmann]], _ On the interpretation of type theory in locally cartesian closed categories_, Proc. CSL '94, Kazimierz, Poland. Jerzy Tiuryn and Leszek Pacholski, eds. Springer LNCS, Vol. 933 ([CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.54.4410))
 {#Hofmann}

but in the process the equivalence of categories was lost. This was finally all rectified in 

* [[Pierre Clairambault]], [[Peter Dybjer]], _The Biequivalence of Locally Cartesian Closed Categories and Martin-L&#246;f Type Theories_ ([arXiv:1112.3456](http://arxiv.org/abs/1112.3456))
 {#ClairambaultDybjer}

The analogous statement relating [[homotopy type theory]] and [[locally cartesian closed (infinity,1)-categories]] was conjectured around

* [[André Joyal]], _Remarks on homotopical logic_, Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))
 {#Joyal}

The suggestion that with [[univalence]] this is refined to [[(∞,1)-topos theory]] appears around

* [[Steve Awodey]], _Type theory and homotopy_ ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/TTH.pdf))
 {#Awodey}

A precise definition of [[elementary (infinity,1)-topos]] inspired by giving a natural equivalence to [[homotopy type theory]] with [[univalence]] was then proposed in 

* [[Mike Shulman]], _Inductive and higher inductive types_ (2012) ([pdf](http://www.math.ucsd.edu/~mshulman/hottminicourse2012/04induction.pdf))

