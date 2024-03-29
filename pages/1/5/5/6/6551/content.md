
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Instanton Floer homology_ is a variant of [[Floer homology]] which applies to 3-dimensional [[manifold]]s. It is effectively the [[Morse homology]] of the [[Chern-Simons theory]] [[action functional]].

For $\Sigma$ a 3-[[dimension]]al [[compact space|compact]] [[smooth manifold]] and $G$ a [[simply connected]] [[compact space|compact]] [[Lie group]] let $[\Sigma,\mathbf{B}G_{conn}]$ be the [[space]] of $G$-[[connection on a bundle|connections]] on $\Sigma$, which is equivalently the [[groupoid of Lie algebra valued forms]] on $\Sigma$ in this case.

The _instanton Floer homology_ groups of $\Sigma$ are something like the "mid-dimensional" [[singular homology]] groups of the [[configuration space]] $[\Sigma,\mathbf{B}G_{conn}]$.

More precisely, there is canonically the [[Chern-Simons action functional]]

$$
  S_{CS} : [\Sigma,\mathbf{B}G_{conn}] \to U(1)
$$

on this space of connections, and one can form the corresponding [[Morse homology]].

The [[critical locus]] of $S_{CS}$ is the space of flat $G$-connections (those with vanishing [[curvature]]), whereas the [[flow line]]s of $S_{CS}$ correspond to the [[Yang-Mills instanton]]s on $\Sigma \times [0,1]$.

## References

The original reference is

* [[Andreas Floer]], _An instanton-invariant for 3-manifolds_ , Comm. Math. Phys. __118__ (1988), no. 2, 215&#8211;240, [euclid](http://projecteuclid.org/euclid.cmp/1104161987)

Reviews:

* [[Simon Donaldson]], _Floer homology groups in Yang-Mills theory_ Cambridge Tracts in Mathematics __147__ (2002), [pdf](http://catdir.loc.gov/catdir/samples/cam031/2001035888.pdf)

* Tomasz S. Mrowka, _Introduction to Instanton Floer Homology_ at _Introductory Workshop: Homology Theories of Knots and Links_ , MSRI ([video](http://www.msri.org/web/msri/online-videos/-/video/showVideo/4015))

Generalizations to 3-manifolds with [[boundary]] are discussed in 

* Dietmar Salamon, Katrin Wehrheim, _Instanton Floer homology with Lagrangian boundary conditions_ ([arXiv:0607318](http://arxiv.org/abs/math/0607318))

[[!redirects instanton Floer homology]]

[[!redirects instanton homology]]