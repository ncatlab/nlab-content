
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

Whenever additive combinations of elements make sense in some [[object]] $M$ of a [[concrete category]] then for a [[indexed set|family]] of [[subobjects]] $(M_\lambda)_{\lambda\in L}$ embedded as subsets $M_\lambda\subset M$ one forms a subset $\sum_\lambda M_\lambda$ of all finite additive combinations of elements in $\cup_\lambda M_\lambda$. The set  $\sum_\lambda M_\lambda$ may be called the *additive hull* of the union. In good circumstances, for example in the case of $R$-[[modules]] over a [[ring]] $R$ (and [[vector spaces]] in particular, when $R$ is a [[field]]), the additive hull of the union, $\sum_\lambda M_\lambda$, has a canonical structure of a subobject of $M$. In that case, we call it the *internal sum* of $(M_\lambda)_{\lambda\in L}$. 

Occasionally, one uses these concepts beyond concrete categories and beyond using additive combinations under the name of union of subobjects (cf. [Borceux 1994, I.4.2](#Borceux94)). Namely, if the poset of [[subobject]]s considered as a category has coproducts, then the internal sum of subobjects may be defined as the coproduct of subobjects, that is the supremum in the poset of subobjects, when it exists. 

## Properties

In the case of $R$-modules, if $M_\lambda\cap M_\mu = 0$ for any pair $(\lambda,\mu)$ the internal sum is the [[internal direct sum]] (some take this as a definition).
 
In more abstract situation, the internal sum is direct if the object part (i.e. codomain) of the coproduct of subobjects is canonically isomorphic to the coproduct of the object parts of the subobjects. In other words, whenever in taking the coproduct one can forget that they are subobjects. 

## References

* {#Borceux94} [[Francis Borceux]]: *[[Handbook of Categorical Algebra]]*, Vol. 1: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

category: algebra


