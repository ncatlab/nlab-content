
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The structure of an _algebraic model category_ is a refinement of that of a [[model category]].

Where a bare [[model category]] structure is a [[category with weak equivalences]] refined by two [[weak factorization systems]] ($(cofibrations, acyclic fibrations)$ and $(acyclic cofibrations, fibrations)$) in an algebraic model structure these are refined further to [[algebraic weak factorization systems]] plus a bit more. 

This extra structure supplies more control over constructions in the model category. For instance its choice induces a [[weak factorization system]] also in every [[diagram]] [[category]] of the given model category.

## Definition

An _algebraic model structure_ on a [[homotopical category]] $(M,W)$ consists of a pair of algebraic weak factorization systems $(C_t, F)$, $(C,F_t)$ together with a _morphism of algebraic weak factorization systems_

$$(C_t,F) \to (C,F_t)$$

such that the underlying weak factorization systems form a model structure on $M$ with weak equivalences $W$.

A _morphism of algebraic weak factorization systems_ consists of a natural transformation
  $$\array{  &  \text{dom} f &  \\  {}^{C_{t}f}\swarrow & & \searrow {}^{{C}{f}}  \\ Rf & \stackrel{\xi_f}{\to}  & Qf \\  {}_{{F}{f}}\searrow & & \swarrow {}_{F_{t}f}  \\  & \text{cod} f &  }$$
comparing the two functorial factorizations of a map $f$ that defines a [[monad|colax comonad morphism]] $C_t \to C$ and a lax monad morphism $F_t \to F$.

## Properties

Every [[cofibrantly generated model category]] structure can be lifted to that of an algebraic model category.  It is not clear whether or not this is true for any [[accessible model category]].

Any algebraic model category has a fibrant replacement monad $R$ and a cofibrant replacement comonad $Q$. There is also a canonical [[distributive law]] $RQ \to QR$ comparing the two canonical bifibrant replacement functors.

## Related pages

* [[algebraic weak factorization system]]
* [[accessible model category]]

[[!include algebraic model structures - table]]

## References

The notion was introduced in 

* [[Emily Riehl]], _Algebraic model structures_, New York J. Math. 17 (2011) 173-231 ([journa](http://nyjm.albany.edu/j/2011/17-10.html), [arXiv](http://arxiv.org/abs/0910.2733))

The algebraic analog of [[monoidal model categories]] is discussed in 

* [[Emily Riehl]], _Monoidal algebraic model structures_ ([arXiv:1109.2883](http://arxiv.org/abs/1109.2883))

[[!redirects algebraic model categories]]

[[!redirects algebraic model structure]]
[[!redirects algebraic model structures]]