
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contemts#
* table of contents
{:toc}

## Idea

A _[[conformal transformation]]_ (conformal mapping) is a transformation of a space which preserves the angles between the curves. In other words, it preserves the angles infinitesimally. The __conformal group__ of a space which has well defined notion of angles between the curves is the group of space automorphisms which are also conformal transformations. 


## Examples

### Of euclidean space

In euclidean $n$-space for $n\gt 2$ a general conformal transformation is some composition of a translation, dilation, rotation and possibly an inversion with respect to a $n-1$-sphere.  

For $n=2$, i.e. in a complex plane, this still holds for (the group of) global conformal transformations but one also has nontrivial local automorphisms. One has in fact infinite-dimensional family of local conformal transformations, which can be described by an arbitrary holomorphic or an antiholomorphic automorphism (in fact one writes $z$ and $\bar{z}$ as independent coordinates in the complexification $\mathbb{C}^2$ and restricts to the real part $\mathbb{R}^2\cong \mathbb{C}$). This is important for CFT in 2d.  


### Of $\mathbb{R}^{d,t}$

For $d,t \in \mathbb{N}$ write $\mathbb{R}^{d,t}$ for the [[pseudo-Riemannian manifold]] which is the [[Cartesian space]] $\mathbb{R}^{d+t}$ equipped with the constant metric of [[signature of a quadratic form|signature]]  $(d,t)$. I.e. for $t = 0$ this is [[Euclidean space]] and for $t=1 $ this is [[Minkowski spacetime]]. 

If $d+t \gt 2$ then the conformal group of $\mathbb{R}^{d,t}$ is the [[orthogonal group]] $P(d+1, t+1)/\{\pm 1\}$. The [[connected component]] of the [[neutral element]] is the [[special orthogonal group]] $SO(d+1,t+1)$. (e.g [Schottenloher 08, chapter 2, theorem 2.9](#Schottenloher08)).

Notice that for $t= 1$ this is also the [[anti de Sitter group]], the [[isometry group]] of [[anti de Sitter spacetime]] of dimension $d+1+t$. This equivalence is the basis of the [[AdS-CFT correspondence]].


### Cosets

(...) [[Möbius space]] (...)

([Arutyunov-Sokatchev 02](#ArutyunovSokatchev02))

(...)

## Related concepts

* [[conformal invariance and scale invariance]]

* [[Möbius group]]

* [[conformal geometry]]

* [[conformal connection]]

* [[conformal field theory]]

* [[conformal symplectic group]]

[[!include table of orthogonal groups and related]]

[[!include local and global geometry - table]]

## References

Textbook accounts include

* {#Schottenloher08} [[Martin Schottenloher]], _The conformal group_, chapter 2 of _A mathematical introduction to conformal field theory_, 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/LNP-cft-pdf/02_978-3-540-68625-5_Ch02_23-08-08.pdf))

and (with an eye towards combination with [[spin geometry]])

* [[Pierre Anglès]], _Conformal Groups in Geometry and Spin Structures_, Progress in Mathematical Physics 2008

Details on the conformal Lie algebra of [[conformal Killing vectors]] acting on 3+1 dimensional [[Minkowski spacetime]] are spelled out for instance in

* [[Matthias Blau]], section 9.3 of _Lecture notes on general relativity_ ([web](http://www.blau.itp.unibe.ch/GRLecturenotes.html))

Discussion in [[conformal field theory]]

* {#ArutyunovSokatchev02} G. Arutyunov, E. Sokatchev, _Conformal fields in the pp-wave limit_, JHEP 0208 (2002) 014 ([arXiv:hep-th/0205270](https://arxiv.org/abs/hep-th/0205270))


See also

* Wikipedia, _[Conformal group](http://en.wikipedia.org/wiki/Conformal_group)_

[[!redirects conformal groups]]

[[!redirects conformal symmetry]]
