
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **polynomial monad** is a [[monad]] on a [[category]] $C$ whose underlying [[endofunctor]] is a [[polynomial functor]] and whose unit and multiplication are [[cartesian natural transformations]].  This is of course equivalent to being a monad in the [[bicategory]] of polynomial functors and cartesian transformations.

## Examples

A basic example is the free-monoid monad ([Gambino-Kock 09, Example 1.9](#GambinoKock09)). This is exhibited by the polynomial $1\leftarrow \mathbb{N}^\prime\rightarrow  \mathbb{N}\rightarrow 1$ where the middle arrow is such that for all $n\in \mathbb{N}$ its fiber over $n$ has cardinality $n$.

One can construct the free monad on a polynomial endofunctor, and it is a polynomial monad.

## Properties

### Parametric right adjointness

Every polynomial monad is a [[p.r.a. monad]].

### Cartesianness

Since all polynomial functors preserve [[pullbacks]], a polynomial monad is necessarily a [[cartesian monad]].  Note that cartesian transformations between polynomial functors also have an explicit description: they are given by diagrams
$$ \array{
  & & X & \to & Y\\
  & \swarrow & & & & \searrow \\
  W && \downarrow && \downarrow && Z \\
  & \nwarrow & & & & \nearrow \\
  & & X' & \to & Y'
  }$$
in which the middle square is a pullback.  Thus, all the data of a polynomial monad can be described very concretely.  This gives a convenient way to produce cartesian monads, and indeed very many cartesian monads arising in practice are in fact polynomial.  Polynomial monads have close relations with a number of other notions.

### Relation to clubs

Polynomial monads (on $C$ rather than a slice of it) are, in some sense, the most natural base monads for the theory of [[clubs]].  Although the club construction can be performed over any cartesian monad, if this monad is polynomial, then all clubs over it are also polynomial, since polynomial functors are a [[sieve]] with respect to cartesian transformations.  Moreover, the club monoidal structure can be seen as just an instance of the explicit construction of composition for polynomials (see 1.11 of ([Gambino-Kock](#GambinoKock09))).

### Relation to generalized multicategories

The bicategory of polynomial functors and cartesian transformations is in fact the horizontal bicategory of a [[double category]] $\underline{Poly}$, whose vertical arrows are the morphisms of $C$ and whose cells are diagrams like
$$ \array{
  W & \leftarrow & X & \to & Y & \to & Z \\
  \downarrow && \downarrow && \downarrow &&\downarrow\\
  W' & \leftarrow & X' & \to & Y' & \to & Z'
}$$
in which the *middle* square (only) is a pullback.  Suppose $W'=Z'=1$, so the bottom polynomial is determined by a single morphism $g':X'\to Y'$, and that $W=Z$.  Then to give the rest of the diagram is to give an object $Y$, a morphism $Y\to Z$, and a morphism $X' \times_{Y'} Y \to Z$.  By adjointness, the latter is equivalent to giving a morphism $Y\to \Pi_{g'}(Z\times X')$; but this codomain is just $T Z$, where $T$ is the polynomial functor determined by $g'$.

Thus, a polynomial equipped with a cartesian transformation to $1 \leftarrow X' \to Y' \to 1$ is exactly a "$T$-span" such as arises in the theory of [[generalized multicategories]].  A similar argument shows that if $T$ is a polynomial monad, then the slice double category of $\underline{Poly}$ over $g'$ is equivalent to the double category of $T$-spans (a.k.a. the "horizontal Kleisli" double category).  Therefore, polynomial monads cartesianly-over $T$, being the horizontal monads in this double category, are precisely $T$-multicategories.  (Such polynomial monads on $C$ itself, rather than any slice, are the $T$-clubs mentioned above; in general a $T$-multicategory $T X_0 \leftarrow X_1 \to X_0$ is identified with the monad it induces on $C/X_0$.)


### Relation to object classifiers

Polynomial monads have a natural interpretation in terms of [[object classifiers]].  Specifically, given any polynomial $1 \leftarrow B \xrightarrow{g} A \to 1$, generating a polynomial functor $P_{1,g,1}$, we can consider the class $S_g$ of all pullbacks of $g$.  A cartesian unit $Id \to P_{1,g,1}$ says that $id_1 : 1\to 1$ is a pullback of $g$, and therefore so are all identities.  Similarly, the composite $P_{1,g,1} \circ P_{1,g,1}$ involves the classifying object for a pair of composable $S_g$-morphisms, and so a cartesian multiplication $P_{1,g,1} \circ P_{1,g,1} \to P_{1,g,1}$ tells us that $S_g$ is closed under composition.

Thus, a polynomial monad (on $C \cong C/1$) can be regarded as a morphism $g$ together with a coherent way to make $S_g$ into a category.  More precisely, consider the slice category $Cart(C)/g$, where $Cart(C)$ is the category whose objects are morphisms of $C$ and whose morphisms are pullback squares.  This comes with source and target functors $Cart(C)/g \rightrightarrows C$.  To make $P_{1,g,1}$ into a polynomial monad is then equivalent to giving unit and composition functors enhancing $Cart(C)/g \rightrightarrows C$ to a [[double category]] such that the forgetful map $Cart(C)/g \to Cart(C)$ is a double functor.

+--{: .standout}
This claim could stand some independent verification.
=--

For example, consider the free monoid monad above determined by $g:\mathbb{N}\prime \to \mathbb{N}$.  To exhibit a function as a pullback of this $g$ is to say that its fibers are finite and have been equipped with bijections to canonical finite sets, which we may as well think of as giving them linear orders.  To give the monad structure on this functor is equivalent to noting that every identity map has ordered finite fibers, and the composite of functions with ordered finite fibers again has ordered finite fibers, in a way that is associative, unital, and stable under pullback.

Other interesting examples include:

* The monad for symmetric strict monoidal categories on $Cat$: its $S_g$ consists of discrete (op)fibrations with ordered finite fibers in which all reindexing functions are bijections.
* The monad for cartesian strict monoidal categories on $Cat$: its $S_g$ consists of discrete fibrations with ordered finite fibers.
* The monad for cocartesian strict monoidal categories on $Cat$: its $S_g$ consists of discrete opfibrations with ordered finite fibers.

The class of discrete [[Conduche functors]] with ordered finite fibers is *almost* an example; it wants to be classified by the bicategory $FinSpan$ of spans between finite sets, but that is not an object of $Cat$.  Thus, a polynomial monad in $Cat$ determined by a discrete Conduche functor with ordered finite fibers is a reasonable substitute for the nonexistent notion of "$FinSpan$-club".

Identifying the classes of morphisms corresponding to standard polynomial monads like these also tells us how to identify when a polynomial monad is induced by a [[club]] (or more generally a [[generalized multicategory]]) over them: when the $g$ for that monad belongs to the appropriate class, compatibly.  For instance, if $S$ is the monad for cartesian strict monoidal categories, then a polynomial monad on $Cat$ is an $S$-club just when the morphism $g$ in its defining polynomial is a discrete fibration with ordered finite fibers, and its composition and unit respect that structure.


## References

A fairly comprehensive discussion of the notion is due to

* [[Nicola Gambino]], [[Joachim Kock]], _Polynomial functors and polynomial monads_, (2009);  ([arXiv:0906.4931](http://arxiv.org/abs/0906.4931))
 {#GambinoKock09}

The [[homotopy theory]] of [[algebra over a monad|algebras]] over polynomial monads is in 

* [[Michael Batanin]], [[Clemens Berger]], _Homotopy theory for algebras over polynomial monads_ ([arXiv:1305.0086](http://arxiv.org/abs/1305.0086))
 {#BataninBerger13}

An application to the theory of [[opetopes]] in discussed in

* [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]] (2010); Polynomial functors and opetopes; Advances in Mathematics, vol 224, pages 2690--2737, [arXiv:0706.1033](http://arxiv.org/abs/0706.1033)
{#KJBM}, &#167;4.3-4.6, where the main result is that the polynomial monad of stable opetopes is a least fixpoint of the Baez-Dolan construction for polynomial monads.

An extension of type theory with a universe of associative and unital polynomial monads to define [[opetopic type theory| opetopic types]] in order to encode fully coherent algebraic structures is in

* {#AlliouxFinsterSozeau20} [[Antoine Allioux]], [[Eric Finster]], [[Matthieu Sozeau]], _Types are internal infinity-groupoids_ ([PDF](https://hal.inria.fr/hal-03133144/document))

Polynomial monads as a "generalization of small categories" for homotopy theory are studied in

* [[Michael Batanin]], Florian De Leger; _Grothendieck's homotopy theory, polynomial monads and delooping of spaces of long knots_, 2017: [arxiv](https://arxiv.org/abs/1712.00904)


[[!redirects polynomial monads]]
