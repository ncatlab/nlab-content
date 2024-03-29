
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **germ** is an element of (a total space of) an [[etale space]] or equivalently an element in some [[stalk]] of a [[sheaf]] (all stalks together form the total space of the etale space of the sheaf). Exactly what this means depends on which sheaf one is considering.

This general description of what a germ of some sheaf at some point is can be extracted from [[stalk]], although that article is pretty abstract right now.


More generally, the notion of [[stalk]] makes sense in any [[topos]] that need not be a [[Grothendieck topos]] [[category of sheaves|of sheaves]] by way of the notion of [[point of a topos]]. Generally a germ is an element in the stalk of an object of a [[topos]] over some point of the topos.


## Examples 

Originally, the term came from geometry, where sheaves of (continuous, smooth, holomorphic etc.) functions or more generally, sections of a (say fibre) [[bundle]] $\xi:E\to B$ were considered; germs in geometrical intuition are always germs *of* something (of a [[section]] of the sheaf in some neighborhood of a point, but also elements of a [[colimit]] at a point of local sections of an original [[presheaf]] which is not always a sheaf; though the germs a posteriori make a sheaf, they can be considered or defined in relation to an original presheaf which is not necessarily a sheaf). __Germs of sections__ are defined as the elements of the colimit sets of the appropriate sets of sections $\Gamma_U \xi$ where the colimit is over all open sets containing $x\in B$ with inverse inclusion (inverse because a presheaf of sections of a bundle is a *contravariant* functor).

In other words, germs of sections at a point $x\in B$ are equivalence classes $[U,s]$ of pairs of the form $(U,s)$, where $U\ni x$ is an open set in the base $B$ and $s:U\to E$ is a section defined over $U$; two sections $(U,s)$, $(U',s')$ in $colim_{U\ni x} \Gamma_U \xi$ are equivalent if there is a smaller $W\subset U\cap U'$ and $s|_W=s'|_W$. This construction of germs of sections of a bundle over $B$ (object of the [[slice category]] $Top/B$) leads to an [[adjoint pair of functors]] between $Top/B$ and the category of *pre*sheaves of sets over $B$ which restricts to the [[equivalence of categories|equivalence]] of the category of [[etale spaces]] $Et_B$ and the category of sheaves over $B$.

For example, take the sheaf of continuous (say, real-valued) functions on some space $X$.  Then every [[partial function]] $f$ defined on a [[neighbourhood]] of any given point $a$ in $X$ defines a germ at $a$.  Furthermore, the germ of $f$ equals the germ of $g$ if and only if $f = g$ on some neighbourhood $U$ of $a$; note that $U$ must be contained in the intersection of the domains of $f$ and $g$, but it may be smaller yet.

For a modern example of this kind, with only $1$ stalk, consider the nonarchimedean [[field]] of germs of holomorphic functions at the origin of the field $\mathbb{C}$ of [[complex number]]s, which plays an important role in mirror symmetry as the [[base field]] for the geometry of families of [[Calabi-Yau manifold]]s in the large volume limit (cf. Kontsevich, Soibelman [doi:10.1007/0-8176-4467-9](http://dx.doi.org/10.1007/0-8176-4467-9), [arxiv:math/0406564v1](http://arxiv.org/abs/math/0406564v1)).  

## Related concepts

* [[synthetic differential topology]]

[[!include infinitesimal and local - table]]


## References

* R. Godement, Topologie algebrique et theorie de faisceaux, Paris 1958 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_, Grundlehren der Mathematischen Wissenschaften 332, Springer (2006)

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_, Springer 1992 


[[!redirects germs]]