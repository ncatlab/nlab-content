<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


#Idea#

Weak complicial sets are [[simplicial sets]] with [[stuff, structure, property|extra structure]] that are closely related to the [[nerves]] of weak $\omega$-[[omega-category|categories]].

The goal of characterizing such nerves, without an *a priori* definition of "weak $\omega$-category" to start from, is called  [[simplicial weak ∞-category]] theory.  It is expected that the (nerves of) weak $\omega$-categories will be weak complicial sets satisfying an extra "saturation" condition ensuring that "every [[equivalence]] is [[thin element|thin]]."  General weak complicial sets can be regarded as "presentations" of weak $\omega$-categories.

Weak complicial sets are a joint generalization of

* [[strict omega-category|strict ∞-categories]];

* [[Kan complexes]];

* [[quasi-category|quasi-categories]].

#Definition#

An **elementary anodyne extension** in $Strat$, the category [[stratified simplicial sets]] is 

* a **complicial horn extension** $\Lambda^k[n] \stackrel{\subset_r}{\hookrightarrow} \Delta^k[n]$ 

or

* a **complicial thinness extension** $\Lambda^k[n]' \stackrel{\subset_e}{\hookrightarrow} \Delta^k[n]''$ 

for $n = 1,2, \cdots$ and $k \in [n]$.

(See reference below for more details.)

A [[stratified simplicial set]] is a **weak complicial set** if it has the right lifting property with respect to all elementary anodyne extensions.  A [[complicial set]] is a weak complicial set in which such liftings are unique.

#Examples#

* For $C$ a [[strict ∞-category]] and $N(C)$ its [[oriental|∞-nerve]], the _Roberts stratification_ which regards each identity morphism as a thin cell makes $N(C)$ a strict [[complicial set]], hence a weak complicial set.  This example is not "saturated."

* There is also the [[stratified simplicial set|stratification]] of $N(C)$ which regards each $\omega$-equivalence morphism as a thin cell.  $N(C)$ with this stratification is a weak complicial set (example 17 of [Ver06](http://arxiv.org/abs/math/0604414)).  This should be the "saturation" of the previous example, and exhibits the inclusion of strict $\omega$-categories into weak ones.

* A simplicial set is a weak complicial set when equipped with its maximal [[stratified simplicial set|stratification]] (every simplex of dimension $\gt 0$ is thin) if and only if it is a [[Kan complex]].  This example is, of course, saturated, and is viewed as embedding $\omega$-groupoids into  $\omega$-categories.

* A simplicial set is a [[quasi-category]] if and only if it is a  weak complicial set when equipped with the stratification in which every simplex of dimension $\gt 1$ is thin, and only degenerate 1-simplices are thin.  This example is not saturated; in its saturation the thin 1-simplices are the internal equivalences in a quasi-category (equivalently, those that become isomorphisms in its [[homotopy category]]).  It presents the embedding of $(\infty,1)$-[[(infinity,1)-category|categories]] into weak $\omega$-categories.

  Note that 1-simplex equivalences in a quasi-category are automatically preserved by simplicial maps between quasi-categories; this is why $QCat$ can "correctly" be regarded as a full subcategory of $sSet$.  This is not true at higher levels; for instance not every simplicial map between nerves of strict $\omega$-categories necessarily preserves $\omega$-equivalence morphisms.


#References#

The definition of weak complicial sets is definition 14, page 9 of 

* Dominic Verity, _Weak complicial sets Part I: Basic homotopy theory_ ([arXiv](http://arxiv.org/abs/math/0604414))

Further developments are in 

* Dominic Verity, _Weak complicial sets Part II: Nerves of complicial Gray-categories_ ([arXiv](http://arxiv.org/abs/math/0604416))

[[!redirects weak complicial sets]]