#Definition#

Let $\mathrm{Top}$ be the category of [[compactly generated space]]s and continuous maps, equipped with a [[Grothendieck topology]] given by usual open covers of topological spaces. This topology is subcanonical. Consider the 2-category $\mathrm{TopStack}$ of 1-[[stack]]s of [[groupoid]]s on $\mathrm{Top}$; by [[Yoneda embedding|Yoneda]] $\mathrm{Top}$ is a full [[subcategory]]. 

By analogy with the case of [[algebraic stack]]s one says that a morphism of 1-stacks $f:X\to Y$ in $\mathrm{TopStack}$ is a **[[representable morphism of stacks]]** if for any morphism of 1-stacks $T\to Y$ from a (stack associated to a) topological space $T$ to $Y$ the pullback $T\times_Y X$ is isomorphic to (a stack associated to) a topological space. 

We say that a property $P$ of morphisms is *local on the target* if satisfaction of this property for a [[base change]] of a morphism $f$ along a surjective local homeomorphism implies the property for $f$. Given a property $P$ of morphisms of topological spaces stable under base change along embeddings and local on the target; a representable morphism $f : X \to Y$ of 1-stacks has this property if there exists a topological space $T$ and an [[epimorphism]] $T\to Y$ such that the inverse image $T\times_Y X\to X$ has property $P$. 



Following Noohi, we say that 

+-- {: .un_defn}
###### Definition

A 1-[[stack]] of [[groupoid]]s over $\mathrm{Top}$ having a representable epimorphism is a __pretopological stack__. Any map from a topological space $S$ to a pretopological stack $X$ is representable and the diagonal $X\to X\times X$ is representable as well. The pretopological stack is called __topological stack__ if the chart can be chosen to belong to a class of "local fibrations"; there are axioms which the class of local fibrations have to satisfy; there are several natural choices of this class which modify the variant of topological stacks considered. 
=--

#References#

Articles by Behrang Noohi on this topic:

* Foundations of Topological Stacks I, [pdf] (http://arxiv.org/pdf/math.AG/0503247.pdf)
* [Homotopy types of topological stacks] (http://front.math.ucdavis.edu/0808.3799)
* [Mapping stacks of topological stacks](http://front.math.ucdavis.edu/0809.2373) 
* K. Behrend, G. Ginot, B. Noohi, P. Xu, [String topology for stacks](http://front.math.ucdavis.edu/0712.3857)