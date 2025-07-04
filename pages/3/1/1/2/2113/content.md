
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A __[[flag]]__ in a [[vector space]] or a [[projective space]] is a nested system of linear/projective subspaces, one of each [[dimension]]
from $0$ to $n-1$. 

Given a [[field]] $k$, the space of all flags in an $n$-dimensional $k$-vector space has the structure of a [[projective variety]] over $k$, this is the __flag variety__. 

If $k$ is the field of real or complex numbers, then it has a structure of a smooth [[manifold]]. It can be considered as the [[homogeneous space]] $SL(n,k)/B$ where $B$ is the subgroup of lower (or upper if you like) triangular matrices. By the [Gram--Schmidt orthogonalization procedure](http://en.wikipedia.org/wiki/Gram%E2%80%93Schmidt_process), one shows the isomorphism as real manifolds $SL(n,\mathbb{C})/B\cong SU(n)/T$ where $T$ is the subgroup of the diagonal $n\times n$-matrices. 

More generally, the __generalized flag variety__ is the complex projective variety obtained as the [[coset space]] $G/T\cong G^{\mathbb{C}}/B$ where $G$ is a [[compact Lie group]], $T$ its [[maximal torus]], $G^{\mathbb{C}}$ the [[complexification]] of $G$, which is a complex semisimple group, and $B\subset G^{\mathbb{C}}$ is the [[Borel subgroup]]. It has a structure of a compact [[Kähler manifold]]. It is a special case of the larger family of coset spaces of semisimple groups modulo [[parabolic subgroup|parabolics]] which includes, for example, [[Grassmannians]]. There are quantum, noncommutative and infinite-dimensional generalizations. Flag varieties have rich combinatorial and geometric structure and play an important role in [[representation theory]] and [[integrable systems]]. 

## Related concepts

* [[Grassmannian]]

* [[coset space]]

* [[coadjoint orbit]]

* [[building]]

* [[Schubert variety]]

* [[Schubert calculus]]

* [[character sheaf]], [[horocycle correspondence]], [[Harish Chandra transform]]


[[!include local and global geometry - table]]


## References

### General

* D. Monk, _The geometry of flag manifolds_, Proceedings of the London Mathematical Society 1959 s3-9(2):253--286; [doi:10.1112/plms/s3-9.2.253](http://dx.doi.org/10.1112/plms/s3-9.2.253)

* Wikipedia, _[Generalized flag variety](http://en.wikipedia.org/wiki/Generalized_flag_variety)_

* M. Brion, _Lectures on the geometry of flag varieties_, [pdf](http://www-fourier.ujf-grenoble.fr/~mbrion/lecturesrev.pdf)

* [[Armand Borel]], _Linear algebraic groups_, Springer

* [[Neil Strickland]], section 5 of: *A Bestiary of Topological Objects* \[<a href="https://strickland1.org/courses/bestiary/bestiary.pdf">pdf</a>, [[Strickland-BestiaryTopological.pdf:file]]\]


On flag varieties of [[loop groups]]:

* {#Kumar02} [[Shrawan Kumar]], _Kac-Moody Groups, their Flag Varieties and Representation Theory_, Birkh&#228;user 2002

On [[flag manifold sigma-models]]:

* [[Ian Affleck]], [[Dmitri Bykov]], [[Kyle Wamer]], *Flag manifold sigma models: spin chains and integrable theories*,  Phys. Rept. **953** (2022) 1-93 &lbrack;[arXiv:2101.11638](https://arxiv.org/abs/2101.11638), [doi:10.1016/j.physrep.2021.09.004](https://doi.org/10.1016/j.physrep.2021.09.004)&rbrack;



[[!include unstable classification of topological phases -- references]]



[[!redirects flag varieties]]
[[!redirects flag manifold]]
[[!redirects flag manifolds]]
[[!redirects generalized flag variety]]
[[!redirects generalized flag varieties]]

[[!redirects partial flag variety]]
[[!redirects partial flag varieties]]

[[!redirects flag space]]
[[!redirects flag spaces]]