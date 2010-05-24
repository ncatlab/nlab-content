
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **topological stack** is a [[geometric stack]] on the [[site]] [[Top]].


## Definition

Let [[Top]] be the category of [[compactly generated space]]s and continuous maps, equipped with a [[Grothendieck topology]] given by usual open covers of topological spaces. This topology is subcanonical. Consider the 2-category $\mathrm{TopStack}$ of 1-[[stack]]s of [[groupoid]]s on $\mathrm{Top}$; by [[Yoneda embedding|Yoneda]] $\mathrm{Top}$ is a full [[subcategory]]. 

By analogy with the case of [[algebraic stack]]s one says that a morphism of 1-stacks $f:X\to Y$ in $\mathrm{TopStack}$ is a **[[representable morphism of stacks]]** if for any morphism of 1-stacks $T\to Y$ from a (stack associated to a) topological space $T$ to $Y$ the pullback $T\times_Y X$ is (2-isomorphic to the stack associated to) a topological space. 

Let $P$ be a property of a map of topological spaces. $P$ is said to be __invariant under change of base__ if for all $f: Y \to X$ with property $P$, if $g:Z \to X$ is any continuous map, the induced map $Z \times_X Y \to Z$ also has property $P$. $P$ is said to be __invariant under restriction__ if this holds whenever $g$ is an embedding. A property $P$ which is invariant under restriction is said to be __local on the target__ if any $f: Y \to X$ for which there exists an open cover $\left(U_\alpha \to X\right)$ such that the induced map $\coprod_{\alpha}  {U_\alpha  }  \times_{X} Y \to \coprod_\alpha  {U_\alpha  } $ has property $P$, must also have property $P$.

Examples of such properties are being an open map, covering map, closed map, local homeomorphism etc.

A representable map $f:\X \to \Y$ of stacks is said to have property $P$ if for any map $T \to \Y$ from a topological space, the induced map $T \times_{\Y} \X \to T$ has property $P$



+-- {: .un_defn}
###### Definition

A 1-[[stack]] $X$ of [[groupoid]]s over $\mathrm{Top}$ having a representable epimorphism from a topological space $X_0 \to X$ is a __topological stack__. Such an representable epimorphism is called an atlas (or chart).

=--

This is what [[Behrang Noohi]] calls a __pretopological stack__  in Foundations I (see reference below). The terminology __topological stack__  is reserved for those stacks whose atlas can be chosen to belong to a class of "local fibrations"; there are axioms which the class of local fibrations have to satisfy; there are several natural choices of this class which modify the variant of topological stacks considered.

Any map from a topological space $S$ to a topological stack $X$ is representable (i.e. diagonal $X\to X\times X$ is always representable). For a topological stack $Y$, if $P$ is invariant under restriction and local on the target, a representable morphism $f : X \to Y$ of 1-stacks has this property if there exists an atlas $T\to Y$ such that the induced map $X\times_Y T\to T$ has property $P$. 

If $X_0 \to X$ is an atlas for a topological stack, then $X_0 \times_{X} X_0 \rightrightarrows X_0$ is a topological groupoid, $\mathbf{X}$. The stackification of the presheaf of groupoids $T \mapsto Hom((T^{id},\mathbf{X}))$ is (2-iso to) $X$ (where $T^{id}$ is $T$ considered as a topological groupoid with only identity arrows).

Conversely, given a topological groupoid $G$, we can consider the stackification of $Hom(blank,G):= \left[ G\right]$. By direct inspection, one sees that $\left[ G\right](T)$ is the groupoid of principal G-bundles over $T$, $Bun_G(T)$. The canonical map $(G_0)^id \to G$ yields a map $a:G_0 \to \left[ G\right]$. If $p:T \to \left[ G\right]$ is any map from a space, then $T \times_{\left[ G\right]} G_0$ is the total space of the principal $G$-bundle over $T$ which $p$ corresponds to via Yoneda. If under the correspondence between principal bundles and generalized homomorphims $p$ corresponds to a map $T^{id} \to G$, then $p$ factors through the map $a:G_0 \to \left[ G\right]$. If $p$ instead corresponds to a map $T_U \to G$ where $U \to T$ is a cover, then $p$ factors through $a$ locally, hence, $a$ is an epimorphism. Therefore an alternative definition of a topological stack is:

+-- {: .un_defn}
###### Definition

A 1-[[stack]] $X$ of [[groupoid]]s over $\mathrm{Top}$ is a __topological stack__ if it is (2-iso to) $Bun_G$ for some topological groupoid $G$.

=--

By Yoneda, $Hom(T,Bun_G) \cong Bun_G(T)$ for all $T$. Moreover, if $H$ is another topological groupoid, $Hom(Bun_H,Bun_G) \cong Bun_G(H)$, where $Bun_G(H)$ is the groupoid of principal $G$-bundles over $H$. In fact, one can use this to show that the 2-category of topological stacks is equivalent to the bicategory of topological groupoids and principal bundles. One may also show that topological stacks are equivalent to the bicategory of fractions of topological groupoids with respect to formally inverting Morita-equivalences.


## References

Articles by [[Behrang Noohi]] on this topic:

* Foundations of Topological Stacks I, [pdf] (http://arxiv.org/pdf/math.AG/0503247.pdf)
* [Homotopy types of topological stacks] (http://front.math.ucdavis.edu/0808.3799)
* [Mapping stacks of topological stacks](http://front.math.ucdavis.edu/0809.2373) 
* K. Behrend, G. Ginot, B. Noohi, P. Xu, [String topology for stacks](http://front.math.ucdavis.edu/0712.3857)

[[!redirects topological stacks]]