
#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

A _[[Top|topological]] [[∞-groupoid]]_ is an [[internal ∞-groupoid]] in [[Top]]. As described there, a general interpretation of what that means is to say that this is an [[∞-stack]] on [[Top]].

## Homotopy invariance and topological spaces

A central result about [[∞-stack]]s on [[Top]] is that the sub-[[(∞,1)-topos]] of homotopy invariant objects is equivalent to [[Top]] itself. A nice discussion of this is in

* Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

In fact, this is true even for [[Lie ∞-groupoid]]s, i.e. [[∞-stack]]s on [[Diff]]: the homotopy invariant ones model plain [[topological space]]s.

This provides a useful resolutions of topological spaces that often helps to disentangle the twoo different roles played by a topological space: on the one hand as a model for an [[∞-groupoid]], in the other as a [[locale]].


Here are the details.

Let $SPSh(Diff)^{loc}$ be the local [[model structure on simplicial presheaves]] obtained by left [[Bousfield localization of model categories|Bousfield localization]] at the [[Cech nerve]]s of 
[[Cech cover]]s with respect to the standard [[Grothendieck topology]] on [[Diff]]. This is a [[models for ∞-stack (∞,1)-toposes|model for ∞-stacks]] on [[Diff]].

Let $SPSh(Diff)^{loc}_I$ be furthermore the left [[Bousfield localization of model categories|Bousfield localization]]
at the set of projection morphisms out of [[product]]s of the form $X \times \mathbb{R} \to X$ for all $X \in Diff$. The $\infty$-stacks that are [[local object]]s with respect
to these morphisms are the _homotopy invariant_ $\infty$-stacks, so this localization models the [[(∞,1)-topos]] of homotopy invariant
$\infty$-stacks on $Diff$.

There is a [[adjunction]]

$$
  L : SSet \stackrel{\leftarrow}{\to} SPSh(Diff) : R
$$

where $L$ sends a simplicial set to the simplicial presheaf constant on that simplicial
set, and where evaluates a simplicial presheaf on the manifold that is the [[point]]. 

**Theorem (Dugger)**

This adjunction $(L \dashv R)$ is a [[Quillen equivalence]] with respect to the  standard [[model structure on simplicial sets]] on the left and the above model structure $SPSh(Diff)^{loc}_I$ on the right.




[[!redirects topological ∞-groupoid]]