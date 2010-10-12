
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _homotopy $T$-algebra_ over a [[Lawvere theory]] $T$ is a model for an $\infty$-algebra over $T$, when the latter is regarded as an [[(∞,1)-algebraic theory]].

As a model, homotopy $T$-algebras are equivalent to strict [[simplicial algebra]]s.


## Definition

For $T$ (the syntactic category of) a [[Lawvere theory]] with generating object $x$ an ordinary [[algebra over a Lawvere theory]]  [[functor]] $T \to Set$ that preserves products, in that for all $n \in \mathbb{N}$ the canonical morphism

$$
  \prod_{i = 1}^n A(p_i) :  A(x^n) \to (A(x))^n
$$ 

is an [[isomorphism]].

+-- {: .un_defn}
###### Definition

A **homotopy $T$-algebra** is a functor $A : T \to $ [[sSet]] with values in [[Kan complex]]es such that for all $n \in \mathbb{N}$ this canonical morphism is a [[weak homotopy equivalence]].

=--

For $n \in \mathbb{N}$ write $F_T(n)$ for the free simplicial $T$-algebra on $n$-generators, which is the image of $x^n$ under the [[Yoneda embedding]] $j : T^{op} \to [T,sSet]$. (See [[Lawvere theory]] for more on this.)

+-- {: .un_prop}
###### Proposition
A homotopy $T$-algebra is precisely 

* a fibrant object in the projective [[model structure on simplicial presheaves]];

* which is a [[local object]] with respect to the canonical morphisms

  $$
    \coprod F_T(1) \to F_T(n)
  $$

  for all $n \in \mathbb{N}$.

=--

+-- {: .proof}
###### Proof

The fibrant objects in $[T,sSet]_{proj}$ are precisely the [[Kan complex]]-valued co-presheaves. Because $F_T(n)$ is [[representable functor|representable]], it is cofibrant in $[T,sSet]_{proj}$ (as one easily checks). Therefore the [[derived hom-space]]s between $F_T(\cdots)$ and a degreewise Kan complex-valued $A$ may be computed simply as the [[sSet]]-[[hom-object]]s of the [[simplicial model category]] $[T,sSet]$ and so the degreewise fibrant $A$ being a [[local object]] means that all morphisms of [[sSet]]-[[hom-object]]s

$$
  [T,sSet](F_T(n),A) \to [T,sSet](\coprod_n F_T(1), A)
  \,.
$$

Due to the respect of the [[hom-functor]] for [[limit]]s the expression on the right is

$$
  \cdots = \prod_n [T,sSet](F_T(1), A)
  \,.
$$

Using the [[Yoneda lemma]] the morphism in question is indeed isomorphic to

$$
  A(x^n) \to A(x)^n
  \,.  
$$

=--

This observation motivated the following definition.

+-- {: .un_def}
###### Definition

The **[[model category]] structure for homotopy $T$-algebras** is the left [[Bousfield localization of model categories|Bousfield localization]] $[T,sSet]_{proj,loc}$ of the projective [[model structure on simplicial presheaves]] $[T,sSet]_{proj}$ at the set of morphisms $\{\coprod_n F_T(1) \to F_T(b)\}_{n \in \mathbb{N}}$.

=--


## Properties


+-- {: .un_prop}
###### Proposition

The model structure for homotopy $T$-algebra $[T,sSet]_{proj,loc}$ is a [[left proper model category|left proper]] [[simplicial model category]].

=--

+-- {: .proof}
###### Proof

Because the [[model structure on simplicial presheaves]] is and left [[Bousfield localization of model categories]] preserves these properties.

=--


+-- {: .un_theorem}
###### Theorem


Let $T Alg^{\Delta^{op}}_{proj}$ be the category of [[simplicial object|simplcial]] [[T-algebra]]s equipped with the standard [[model structure on simplicial algebras]] (with weak equivalences and fibrations the degreewise weak equivalences and fibrations in simplicial sets).

The adjunction (which is degreewise the corresponding adjunction described at [[T-algebra]])

$$
  T Alg^{\Delta^{op}} \stackrel{\leftarrow}{\hookrightarrow}
  [T,sSet] = [T,Set]^{\Delta^{op}}
$$

is a [[Quillen equivalence]]

$$
  T Alg^{\Delta^{op}}_{proj} \simeq
  [T,sSet]_{proj,loc}
  \,.
$$

=--

This is theorem 1.3 in ([Badzioch](#Badzioch))



## Examples

The model structure on homotopy $T$-algebras for $T = $ [[CartSp]] the Lawvere theory of [[smooth algebra]]s is considered in ([Spivak](#Spivak)) in the study of [[derived smooth manifold]]. (There is also a bit of disucssion of the relation to the model structure on simplicial algebras there.)

## References

In 

* [[Bernard Badzioch]], _Algebraic theories in homotopy theory_ Annals of Mathematics, 155 (2002), 895-913 ([JSTOR](http://www.jstor.org/stable/3062135))
{#Badzioch}

the model structure on homotopy $T$-algebras is discussed and its Quillen equivalence to simplcial $T$-algebras is proven.

A related dicussion showing that simplicial $T$ algebras model all $\infty$-$T$-algebras is in

* [[Julie Bergner]], _Rigidification of algebras over multi-sorted theories_ , Algebraic and Geometric Topoogy 7, 2007.
{#Bergner}

The model structure on homotopy $T$-algebras for $T = $ [[CartSp]] the Lawvere theory of [[smooth algebra]]s is considered in 

* [[David Spivak]], _Derived smooth manifolds_ ([arXiv:0810.5174](http://arxiv.org/abs/0810.5174))
{#Spivak}

[[!redirects homotopy T-algebras]]