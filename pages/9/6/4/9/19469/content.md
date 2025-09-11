
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

##Idea

For any [[2-category]] $K$, there are two 2-categories (each with several variants) that could be called "the 2-category of adjunctions in $K$".

* The 2-category which here we call $Adj(K)$ has the same objects as $K$, its morphisms are the [[adjunctions]] in $K$ (pointing in the direction of, say, the [[left adjoint]]), and its [[2-morphisms]] are [[mate]]-pairs of 2-morphisms between adjunctions in $K$.

* The 2-category $[Adj,K]$ is the [[functor 2-category]] from the [[walking adjunction]] $Adj$ to $K$.  Thus its *objects* are the adjunctions in $K$ --- or more precisely, triples $(x,y,(f,g,\eta,\epsilon))$ where $x,y$ are objects of $K$ and $(f,g,\eta,\epsilon)$ is an adjunction between $x$ and $y$.  Its morphisms are pairs of morphisms $x\to x'$ and $y\to y'$ such that certain squares commute (perhaps up to a transformation or isomorphism), and its 2-cells are similarly composed of cylinders.

Note that the *[[1-morphisms]]* of $Adj(K)$ are the *[[objects]]* of $[Adj,K]$.

## Properties

* The morphisms in $Adj\big(Adj(K)\big)$ are the [[adjoint triples]] in $K$.

* The inclusion of [[Mnd]], the free-standing monad, in [[Adj]] induces a [[2-functor]] from $[Adj,K]$ to $[Mnd,K]$, the [2-category of monads](monad#monad#TwoCategoryOfMonads) in $K$. The adjoints to this 2-functor are the [[Kleisli category|Kleisli]] and [[Eilenberg-Moore category|Eilenberg-Moore]] constructions on monads in $K$.

## Related concepts

* [[CatAdj|$Cat_{Adj}$]]

## References

* [[Claude Auderset]], _Adjonctions et monades au niveau des $2 $-catégories_, Cahiers de topologie et géométrie différentielle 15.1 (1974): 3-20. [Link](https://www.numdam.org/item/CTGDC_1974__15_1_3_0/)

* [[Stephen Schanuel]] and [[Ross Street]], *The free adjunction*, Cahiers de topologie et géométrie différentielle catégoriques, tome 27, no 1 (1986), p. 81-83 [Link](https://www.numdam.org/item/CTGDC_1986__27_1_81_0/)