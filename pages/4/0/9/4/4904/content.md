
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $T$ a [[Lawvere theory]] and $T Alg$ the [[category]] of [[algebra over a Lawvere theory]], there is a [[model category]] structure on the category $T Alg^{\Delta^{op}}$ of [[simplicial object|simplicial]] $T$-algebras which models the $\infty$-algebras for $T$ rregarded as an [[(∞,1)-algebraic theory]].

## Details

Recall that the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C^{op})$ itself is modeled by the [[model structure on simplicial presheaves]]

$$
  PSh_{(\infty,1)}(C^{op})
  \simeq
  [C, sSet]^\circ
  \,,
$$

where we regard $C$ as a [[Kan complex]]-[[enriched category]] and have on the right the [[sSet]]-[[enriched functor category]] with the projective or injective model structure, and $(-)^\circ$ denoting the full enriched subcategory on fibrant-cofibrant objects.

This says in particular that every weak $(\infty,1)$-functor $f : C \to \infty \mathrm{Grp}$ is equivalent to a _rectified_ one $F : C \to KanCplx$. And $f \in PSh_{(\infty,1)}(C^{op})$ belongs to $Alg_{(\infty,1)}(C)$ if $F$ preserves finite products _weakly_  in that for $\{c_i \in C\}$ a finite collection of objects, the canonical natural morphism

$$
  F(c_1 \times \cdots, \c_n)
  \to
  F(c_1) \times \cdots \times F(c_n)
$$ 

is a [[homotopy equivalence]] of [[Kan complex]]es.

We now look at model category structure on _strictly_ product preserving functors $C \to sSet$, which gives an equivalent model for $Alg_{(\infty,1)}(C)$. See [[model structure on homotopy T-algebras]].

+-- {: .un_prop}
###### Proposition
**(first model structure)**

Let $T$ be a [[category]] with finite [[product]]s, and let $T Alg^{\Delta^{op}} \subset Func(T,sSet)$ be the [[full subcategory]] of the [[functor category]] from $T$ to [[sSet]] on those functors that preserve these products.  

Then $T Alg^{\Delta^{op}}$ carries the structure of a [[model category]] $sAlg(C)_{proj}$ where the weak equivalences and the fibrations are objectwise those in the standard [[model structure on simplicial sets]]. 

=--

This is due to ([Quillen](#Quillen)).


The inclusion $i : sAlg(C) \hookrightarrow sPSh(C^{op})_{proj}$ into the projective [[model structure on simplicial presheaves]] evidently preserves fibrations and acylclic fibrations and gives a [[Quillen adjunction]]

$$
  sAlg(C)_{proj}
  \stackrel{\leftarrow}{\underset{i}{\hookrightarrow}}
  sPSh(C^{op})
  \,.
$$


+-- {: .un_prop}
###### Proposition

The total right [[derived functor]] 

$$
  \mathbb{R}i : Ho(sAlg(C)_{proj}) \to Ho(sPSh(C^{op})_{proj})
$$ 

is a [[full and faithful functor]] and an object $F \in sPSh(C^{op})$ belongs to the [[essential image]] of $\mathbb{R}i$ precisely if it preserves product up to [[weak homotopy equivalence]].

=--

This is due to ([Bergner](#Bergner)).

It follows that the natural $(\infty,1)$-functor

$$
  (sAlg(C)_{proj})^\circ \stackrel{}{\to}
  PSh_{(\infty,1)}(C^{op})
$$

is an [[equivalence of quasi-categories|equivalence]].

A comprehensive statement of these facts is in [[Higher Topos Theory|HTT, section 5.5.9]].

+-- {: .un_prop}
###### Proposition
**(second model structure)**

Let $T$ be the [[Lawvere theory]] for commutative [[associative algebra]]s over a ring $k$. Then $CAlg_k$ becomes a [[simplicial model category]] with

* weak equivalences the morphisms whose underlying morphusms of simplicial sets are weak equivalences;

* fibrations the morphisms $X \to Y$ such that $X \to \pi_0 X \times_{\pi_0 Y} Y$ is a degreewise surjection.

=--

This appears as ([GoerssSchemmerhorn, theorem 4.17](#GoerssSchemmerhorn)).


## Properties

+-- {: .un_theorem}
###### Theorem

There is a [[Quillen equivalence]] between the model structure on simplicial $T$-algebras and the model structure for [[homotopy T-algebra]]s. (See there).

=--

This is theorem 1.3 in ([Badzioch](#Badzioch)).

## Examples

* A [[simplicial ring]]s is a simplicial $T$-algebras for $T$ the Lawvere theory of rings. See there for more on the model category structure

## Related concepts

* [[model structure on monoids]]

* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

  * [[model structure on algebras over a monad]]

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / **model structure on simplicial T-algebras**

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]




## References

The classical reference for the transferred model structure on simplicial $T$-algebras is

* [[Dan Quillen]], _Homotopical Algebra_ Lectures Notes in Mathematics 43, SpringerVerlag, Berlin, (1967)

The simplicial model structure on ordinary simplicial algebras is in

* [[Paul Goerss]], [[Kirsten Schemmerhorn]], _Model categories and simplicial methods_ ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/ucnotes.pdf))

In 

* [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_ ([math/0003065](http://arxiv.org/abs/math/0003065)) ,
{#Rezk}

it is discussed that every model category of simplicial $T$-algebras is [[Quillen equivalence|Quillen equivalent]] to a left [[proper model category]].

The fact that the model structure on simplicial $T$-algebras serves to model $\infty$-algebras is in

* [[Julie Bergner]], _Rigidification of algebras over multi-sorted theories_ , Algebraic and Geometric Topoogy 7, 2007.
{#Bergner}.


The Quillen equivalence to the model structure on homotopy $T$-algebras is in 

* [[Bernard Badzioch]], _Algebraic theories in homotopy theory_ Annals of Mathematics, 155 (2002), 895-913 ([JSTOR](http://www.jstor.org/stable/3062135))
{#Badzioch}


[[!redirects model structure on simplicial T-algebras]]