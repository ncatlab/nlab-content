
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _hopfish algebra_ is a generalization of that of [[Hopf algebra]] designed to behave better with respect to [[Morita equivalence]] of algebras. It is defined to be a [[sesquialgebra]] (hence a 2-algebra/[[3-module]]) which is grouplike in a suitable sense.

The notion subsumes [[Hopf algebras]] and [[weak Hopf algebras]].

## Definition

Let $R$ be some [[commutative ring]] (or [[E-infinity ring]]).

+-- {: .num_defn}
###### Definition

A [[sesquiunital sesquialgebra]] over $R$ is an [[associative algebra]] $A$ over $R$ equipped with the structure of an [[algebra object]] internal to the [[2-category]] [[2Mod]] of [[associative algebras]], [[bimodules]] and [[bimodule intertwiners]].

This means that it is an $R$-algebra $A$ equipped with 

* a product $A \otimes_R A$-$A$-[[bimodule]] $\Delta$;

* a unit $R$-$A$-[[bimodule]] $\epsilon$

satisfying the evident [[associative law]] and [[unit law]].

=--

+-- {: .num_defn}
###### Definition

A **preantipode** for a [[sesquiunital sesquialgebra]] $A$ is a left $A \otimes A$-[[module]] $S$ equipped with an [[isomorphism]] of right $A \otimes A$-[[modules]]

$$
  S^* \simeq Hom_A(\epsilon, \Delta)
  \,.
$$

An preantipode is an **antipode** if it is a [[free module]] over $A$ of [[rank]] 1 when regarded as an $A$-$A^{op}$-[[bimodule]].

A sesquiunital sesquialgebra equipped with such an antipode is a **hopfish algebra**.

=--

This is ([TWZ, def. 3.1, def. 3.2](#TWZ)).

## Properties

### Module categories and Tannaka duality
 {#ModuleCategoriesAndTannakaDuality}

The notion of [[sesquialgebra]] generalizes that of [[bialgebra]] such that under [[Tannaka duality]] sesquialgebras corespondond to [[monoidal categories]] generally, while the strictness of bialgebras means that there their monoidal category of [[modules]] is equipped with a [[fiber functor]]. 

Since moreover [[Hopf algebras]] correspond to [[rigid monoidal categories]] with fiber functor under [[Tannaka duality]], the correct sesqui-algebra generalization of Hopf algebras should have exactly the rigid monoidal categories as module categories, up to equivalence, without necessarily a fiber functor. This is expressed by the following table

[[!include structure on algebras and their module categories - table]]
  

## References

The notion was introduced in

* Xiang Tang, [[Alan Weinstein]], [[Chenchang Zhu]], _Hopfish algebras_, Pacific J. Math. 231 (2007), no. 1, 193--216. ([arXiv:math/0510421](http://arxiv.org/abs/math/0510421))
 {#TWZ}


[[!redirects Hopfish algebra]]

[[!redirects hopfish algebras]]
[[!redirects Hopfish algebras]]


