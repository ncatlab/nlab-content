# c-Reedy categories

* contents
{: toc}

## Idea

A *c-Reedy category* is a generalization of a [[Reedy category]], even more general than a [[generalized Reedy category]], in which the level morphisms need not even be invertible.

## Definition

A **c-Reedy category** is a category $C$ equipped with an ordinal-valued degree function on its objects, and subcategories $\overset{\leftrightarrow}{C}$, $\overset{\to}{C}$, and $\overset{\leftarrow}{C}$ containing all the objects, such that

* $\overset{\leftrightarrow}{C} \subseteq \overset{\to}{C}\cap \overset{\leftarrow}{C}$.
* Every morphism in $\overset{\leftrightarrow}{C}$ is level (i.e. its domain and codomain have the same degree).
* Every morphism in $\overset{\to}{C}\setminus\overset{\leftrightarrow}{C}$ strictly raises degree, and every morphism in $\overset{\leftarrow}{C}\setminus\overset{\leftrightarrow}{C}$ strictly lowers degree.
* Every morphism $f$ factors as $\overset{\to}{f} \overset{\leftarrow}{f}$, where $\overset{\to}{f} \in \overset{\to}{C}$ and $\overset{\leftarrow}{f}\in\overset{\leftarrow}{C}$, and the category of such factorizations with connecting maps in $\overset{\leftrightarrow}{C}$ is connected.
* For any $x$ and any degree $\delta\lt\deg(x)$, the functor $\overset{\leftarrow}{C}(x,-):\overset{\leftrightarrow}{C}_{=\delta} \to \Set$ is a coproduct of retracts of representables, where $\overset{\leftrightarrow}{C}_{=\delta}$ denotes the full subcategory of $\overset{\leftrightarrow}{C}$ on objects of degree $\delta$.

## References

* [[Mike Shulman]], *Reedy categories and their generalizations*, [blog](https://golem.ph.utexas.edu/category/2015/06/what_is_a_reedy_category.html), [arXiv](http://arxiv.org/abs/1507.01065)

[[!redirects c-Reedy categories]]
