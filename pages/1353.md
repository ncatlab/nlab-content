#Idea#

Weak complicial sets are [[simplicial set]]s with [[stuff, structure, property|extra structure]] that are thought of as being [[nerve]]s of weak [[omega-category|omega-categories]]. Therefore they are also called [[simplicial weak omega-category|simplicial weak omega-categories]].

Weak complicial sets are a joint generalization of

* [[strict omega-category|strict omega-categories]];

* [[Kan complex]]es;

* [[quasi-category|quasi-categories]].

#Definition#

An **elementary anodyne extension** in $Strat$, the category [[stratified simplicial set]]s is 

* a **complicial horn extension** $\Lambda^k[n] \stackrel{\subset_r}{\hookrightarrow} \Delta^k[n]$ 

or

* a **complicial thinness extension** $\Lambda^k[n]' \stackrel{\subset_e}{\hookrightarrow} \Delta^k[n]''$ 

for $n = 1,2, \cdots$ and $k \in [n]$.

(See reference below for more details.)


A [[stratified simplicial set]] is a **weak complicial set** if it has the right lifting property with respect to all elementary anodyne extensions.

#Examples#

* For $C$ a [[strict omega-category]] and $N(C)$ its [[oriental|omega-nerve]], the _Roberts stratification_ which regards each identity morphism as a thin cell makes $N(C)$ a strict [[complicial set]]. However, there is also the [[stratified simplicial set|stratification]] which regards each $\omega$-equivalence morphism as a thin cell. $N(C)$ with this stratification is a weak complicial set. (example 17 of [Ver06](http://arxiv.org/abs/math/0604414))


#References#

The definition of weak complicial sets is definition 14, page 9 of 

* Dominic Verity, _Weak complicial sets Part I: Basic homotopy theory_ ([arXiv](http://arxiv.org/abs/math/0604414))

Further developments are in 

* Dominic Verity, _Weak complicial sets Part II: Nerves of complicial Gray-categories_ ([arXiv](http://arxiv.org/abs/math/0604416))


