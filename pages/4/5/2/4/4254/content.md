
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

_Floer homology_ is a common name for several similar frameworks of infinite-dimensional analogues of [[Morse homology]], related to certain [[elliptic operator]]s. Some of these are related to [[symplectic geometry]] or [[contact geometry]] and another group is related to aspects of the geometry of 3-[[manifolds]]. One of these uses the [[Chern-Simons theory]] [[action functional]] as a [[Morse function]] on the space of [[connection on a bundle|connection]]s on $G$-[[principal bundle]]s over the given 3-manifold.

The most important flavours are the **Floer-Oh homology for [[action functional]]s** which is important in the study of [[symplectic manifold]]s, its version for Lagrangean intersection theory and the instanton Floer homology studied by Andreas Floer and important in the study of 3-manifolds and the mathematics of [[gauge theories]]. 

Floer homology for the [[action functional]] is a more systematic approach to the phenomena which were discovered several years before Floer in a historical article of [[Mikhail Gromov]] on J-holomorphic curves. 

## Examples and Variants

### Instanton Floer homology

For $\Sigma$ a 3-[[dimension]]al [[compact space|compact]] [[smooth manifold]] and $G$ a [[simply connected]] [[compact space|compact]] [[Lie group]] let $[\Sigma,\mathbf{B}G_{conn}]$ be the [[space]] of $G$-[[connection on a bundle|connections]] on $\Sigma$, which is equivalently the [[groupoid of Lie algebra valued forms]] on $\Sigma$ in this case.

The _instanton Floer homology_ groups of $\Sigma$ are something like the "mid-dimensional" [[singular homology]] groups of the [[configuration space]] $[\Sigma,\mathbf{B}G_{conn}]$.

More precisely, there is canonically the [[Chern-Simons action functional]]

$$
  S_{CS} : [\Sigma,\mathbf{B}G_{conn}] \to U(1)
$$

on this space of connections, and one can form the corresponding [[Morse homology]].

The [[critical locus]] of $S_{CS}$ is the space of flat $G$-connections (vanishing [[curvature]]), whereas the [[flow line]]s of $S_{CS}$ correspond to the [[Yang-Mills instanton]]s on $\Sigma \times [0,1]$.

For more see

* [[instanton Floer homology]].

## References

The original articles are

* [[Andreas Floer]], 

  * _The unregularized gradient flow of the symplectic action_ , Comm. Pure Appl. Math. 41 (1988), 775&#8211;813.

  * _An instanton-invariant for 3-manifolds_ , Comm. Math. Phys. 118 (1988), no. 2, 215&#8211;240. 

  * _Morse theory for Lagrangian intersections- , J. Differential Geom. 28 (1988), no. 3, 513&#8211;547.

  * _Cuplength estimates on Lagrangian intersections_ , Comm. Pure Appl. Math. 42 (1989), no. 4, 335&#8211;356.

  * _Symplectic fixed points and holomorphic spheres_ , Comm. Math. Phys. 120, no. 4 (1989), 575&#8211;611.

  * _Witten's complex and infinite dimensional Morse Theory_ , J. Diff. Geom. 30 (1989), p. 202&#8211;221.

Surveys are in

* [[Yong-Geun Oh]], _Symplectic Topology and Floer Homology_ ([pdf](http://www.math.wisc.edu/~oh/all.pdf))
 {#Oh}

* D Milinkovic, _Floer Homology in Classical Mechanics and Quantum Field Theory_ ([ps](http://www.mphys5.phy.bg.ac.rs/proceedings3/Milinkovic.ps))

* [[Simon Donaldson]], _Floer homology groups in Yang-Mills theory_ Cambridge University Press (2002) ([pdf](http://catdir.loc.gov/catdir/samples/cam031/2001035888.pdf))


See also

* [wikipedia](http://en.wikipedia.org/wiki/Floer_homology)