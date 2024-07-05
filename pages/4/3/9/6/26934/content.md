## Idea

Whenever additive combinations of elements make sense in some object $M$ of a [[concrete category]] then for a family of subjects $(M_\lambda)_{\lambda\in L}$ embedded as subsets $M_\lambda\subset M$ one forms a subset $\sum_\lambda M_\lambda$ of all finite additive combinations of elements in $\cup_\lambda M_\lambda$. Set  $\sum_\lambda M_\lambda$ may be called the additive hull of the union. In good circumstances, for example in the case of $R$-modules where $R$ is a ring (and vector spaces over in particular), the additive hull of the union, $\sum_\lambda M_\lambda$, has a canonical structure of a subobject of $M$. In that case, we call it the internal sum of $(M_\lambda)_{\lambda\in L}$. 

Occasionally, one uses these concepts beyond concrete categories and beyond using additive combinations under the name of union of subobjects (see [[Francis Borceux]], Handbook of categorical algebra I.4.2). Namely, if the poset of [[subobject]]s considered as a category has coproducts, then the internal sum of subobjects may be defined as the coproduct of subobjects, that is the supremum in the poset of subobjects, when it exists. 

## Properties

In the case of $R$-modules, if $M_\lambda\cap M_\mu = 0$ for any pair $(\lambda,\mu)$ the internal sum is the [[internal direct sum]] (some take this as a definition).
 
In more abstract situation, the internal sum is direct if the object part (i.e. codomain) of the coproduct of subobjects is canonically isomorphic to the coproduct of the object parts of the subobjects. In other words, whenever in taking the coproduct one can forget that they are subobjects. 

category: algebra