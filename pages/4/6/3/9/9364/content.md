
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

A **polynomial monad** is a [[monad]] whose underlying [[endofunctor]] is a [[polynomial functor]]. This is of course equivalent to being a monad in the [[bicategory]] of polynomial functors.

## Examples

A basic example is the free-monoid monad ([Gambino-Kock 09, Example 1.9](#GambinoKock09)). This is exhibited by the polynomial $1\leftarrow \mathbb{N}^\prime\rightarrow  \mathbb{N}\rightarrow 1$ where the middle arrow is such that for all $n\in \mathbb{N}$ its fiber over $n$ has cardinality $n$.

One can construct the free monad on a polynomial endofunctor, and it is a polynomial monad.

## Cartesian polynomial monads

Since all polynomial functors preserve [[pullbacks]], a polynomial monad is a [[cartesian monad]] just when its unit and multiplication are [[cartesian natural transformations]].  But cartesian transformations between polynomial functors also have an explicit description: they are given by diagrams
$$ \array{
  & & X & \to & Y\\
  & \swarrow & & & & \searrow \\
  W && \downarrow && \downarrow && Z \\
  & \nwarrow & & & & \nearrow \\
  & & X' & \to & Y'
  }$$
in which the middle square is a pullback.  Thus, cartesian polynomials monad can be described very concretely.  This gives a convenient way to produce cartesian monads, and indeed very many cartesian monads arising in practice are in fact polynomial.

Cartesian polynomial monads are also, in some sense, the most natural base monads for the theory of [[clubs]].  Although the club construction can be performed over any cartesian monad, if this monad is polynomial, then all clubs over it are also polynomial, since polynomial functors are a [[sieve]] with respect to cartesian transformations.  Moreover, the club monoidal structure can be seen as just an instance of the explicit construction of composition for polynomials (see 1.11 of ([Gambino-Kock](#GambinoKock09))).

Cartesian polynomial monads also have a natural interpretation in terms of [[object classifiers]].  Specifically, given any polynomial $1 \leftarrow B \xrightarrow{g} A \to 1$, generating a polynomial functor $P_{1,g,1}$, we can consider the class $S_g$ of all pullbacks of $g$.  A cartesian unit $Id \to P_{1,g,1}$ says that $id_1 : 1\to 1$ is a pullback of $g$, and therefore so are all identities.  Similarly, the composite $P_{1,g,1} \circ P_{1,g,1}$ involves the classifying object for a pair of composable $S_g$-morphisms, and so a cartesian multiplication $P_{1,g,1} \circ P_{1,g,1} \to P_{1,g,1}$ tells us that $S_g$ is closed under composition.

Thus, a cartesian polynomial monad (on $C \cong C/1$) can be regarded as a morphism $g$ together with a coherent way to make $S_g$ into a category.  More precisely, consider the slice category $Cart(C)/g$, where $Cart(C)$ is the category whose objects are morphisms of $C$ and whose morphisms are pullback squares.  This comes with source and target functors $Cart(C)/g \rightrightarrows C$.  To make $P_{1,g,1}$ into a cartesian polynomial monad is then equivalent to giving unit and composition functors enhancing $Cart(C)/g \rightrightarrows C$ to a [[double category]] such that the forgetful map $Cart(C)/g \to Cart(C)$ is a double functor.

+--{: .standout}
This claim could stand some independent verification.
=--

For example, consider the free monoid monad above determined by $g:\mathbb{N}\prime \to \mathbb{N}$.  To exhibit a function as a pullback of this $g$ is to say that its fibers are finite and have been equipped with bijections to canonical finite sets, which we may as well think of as giving them linear orders.  To give the monad structure on this functor is equivalent to noting that every identity map has ordered finite fibers, and the composite of functions with ordered finite fibers again has ordered finite fibers, in a way that is associative, unital, and stable under pullback.

Other interesting examples include:

* The monad for symmetric strict monoidal categories on $Cat$: its $S_g$ consists of discrete (op)fibrations with ordered finite fibers in which all reindexing functions are bijections.
* The monad for cartesian strict monoidal categories on $Cat$: its $S_g$ consists of discrete fibrations with ordered finite fibers.
* The monad for cocartesian strict monoidal categories on $Cat$: its $S_g$ consists of discrete opfibrations with ordered finite fibers.

The class of discrete [[Conduche functors]] with ordered finite fibers is *almost* an example; it wants to be classified by the bicategory $FinSpan$ of spans between finite sets, but that is not an object of $Cat$.  Thus, a cartesian polynomial monad in $Cat$ determined by a discrete Conduche functor with ordered finite fibers is a reasonable substitute for the nonexistent notion of "$FinSpan$-club".

Identifying the classes of morphisms corresponding to standard cartesian polynomial monads like these also tells us how to identify when a polynomial monad is a [[club]] over them: when the $g$ for that monad belongs to the appropriate class, compatibly.  For instance, if $S$ is the monad for cartesian strict monoidal categories, then a cartesian polynomial monad is an $S$-club just when the morphism $g$ in its defining polynomial is a discrete fibration with ordered finite fibers, and its composition and unit respect that structure.


## References

A fairly comprehensive discussion of the notion is due to

* [[Nicola Gambino]], [[Joachim Kock]], _Polynomial functors and polynomial monads_, (2009);  ([arXiv:0906.4931](http://arxiv.org/abs/0906.4931))
 {#GambinoKock09}

The [[homotopy theory]] of [[algebra over a monad|algebras]] over polynomial monads is in 

* [[Michael Batanin]], [[Clemens Berger]], _Homotopy theory for algebras over polynomial monads_ ([arXiv:1305.0086](http://arxiv.org/abs/1305.0086))
 {#BataninBerger13}

An application to the theory of [[opetopes]] in discussed in

* [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]] (2010); Polynomial functors and opetopes; Advances in Mathematics, vol 224, pages 2690--2737, [arXiv:0706.1033](http://arxiv.org/abs/0706.1033)
{#KJBM}, &#167;4.3-4.6 where the main result is that the polynomial monad of stable opetopes is a least fixpoint of the Baez-Dolan construction for polynomial monads.

[[!redirects polynomial monads]]