
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
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

For $X$ a [[space]] equipped with a notion of [[dimension]] $dim X \in \mathbb{N}$ and a notion of [[Kähler differential forms]], 
a _$\Theta$-characteristic of $X$ is a choice of [[square root]] of the [[canonical characteristic class]] of $X$. See there for more details.

In [[complex analytic geometry]] and at least if the Theta characteristic is [[polarized variety|principally polarizing]] then its [[holomorphic sections]] are called [[theta functions]]. In particular for line bundles over the [[Jacobian variety]] of a [[Riemann surface]] they are called _[[Riemann theta functions]]_.

## Examples

### Over Riemann surfaces
 {#OverRiemannSurfaces}

+-- {: .num_prop }
###### Proposition

For $\Sigma$ a [[Riemann surface]], the choices of [[square roots]] of the [[canonical bundle]] correspond to the choice of [[spin structures]].

For $X$ of [[genus of a surface|genus]] $g$, there are $2^{2g}$ many choices of square roots of the canonical bundle. 

=--

([Atiyah, prop. 3.2](#Atiyah)). 

+-- {: .num_remark }
###### Remark

The first statement remains true in higher dimensions over [[Kähler manifolds]], see at  _[Spin structure -- On K&#228;hler manifolds](spin%20structure#OverAKahlerManifold)_.

=--


+-- {: .num_prop }
###### Proposition

The function that sends a square root line bundle to the [[dimension]] of its space of [[holomorphic sections]] $mod \;2$ is a [[quadratic refinement]] of the [[intersection pairing]] on $H^1(X, \mathbb{Z}_2)$. 

=--

This is due to ([Atiyah, theorem 2](#Atiyah)). A motivational survey in broader context of [[quadratic refinements]] of the [[intersection pairing]] in higher dimensions is in ([Hopkins-Singer 02, section 2.1](#HopkinsSinger02)).


### As metaplectic and Spin structure over (K&#228;hler-)polarized varieties
 {#AsMetaplecticCorretionOfK&#228;hlerPolarizations}

In the context of [[geometric quantization]] a [[metaplectic structure]] on a [[polarization]] is a [[square root]] of a certain line bundle. In the special case of [[Kähler polarization]] this is a square root precisely of the [[canonical line bundle]] of the underlying [[complex manifold]] and hence is a $\Theta$-characteristic. Also, equivalently this is a [[Spin structure]], see at _[spin structure -- Over a K&#228;hler manifold](http://ncatlab.org/nlab/show/spin%20structure#OverAKahlerManifold)_. For more on this see at _[geometric quantization -- Quantum states as index of Dolbeault-Dirac operator](geometric+quantization#IndexOfDolbeaultDiracOperator)_.

Notice that generalizing from [[complex analytic geometry]] to [[algebraic geometry]] over other bases, then the analog of a [[Kähler polarization]] is a _[[polarized variety]]_. Hence a choice of [[Theta characteristic]] on a [[polarized variety]] is the analog of a metaplectically corrected K&#228;hler manifold.

### Over intermediate Jacobians
 {#OverIntermediateJacobians}

A special square root of the canonical bundle on [[intermediate Jacobians]] in dimension $2k+1$ thought of as [[moduli spaces]] of (flat) [[circle n-bundles with connection|circle (2k+1)-bundles with connection]] has a unique [[section]] the [[partition function]] of abelian [[self-dual higher gauge theory]] (see there for details).  ([Witten 96](#Witten96), [Hopkins-Singer 02](#HopkinsSinger02)).

## Related concepts

[[!include square roots of line bundles - table]]

## References

The spaces of choices of $\Theta$-characteristics over [[Riemannian manifolds]] were originally discussed in

* {#Atiyah} [[Michael Atiyah]], _Riemann surfaces and spin structures_, Annales Scientifiques de l'&#201;cole Normale Sup&#233;rieure, (1971), Quatri&#232;me S&#233;rie 4: 47&#8211;62, ISSN 0012-9593, MR0286136
 

See also

* M. Bertola, _Riemann surfaces and Theta Functions_, August 2010 ([pdf](http://www.mathstat.concordia.ca/faculty/bertola/ThetaCourse/ThetaCourse.pdf))

* Gavril Farkas, _Theta characteristics and their moduli_ (2012) ([arXiv:1201.2557](http://arxiv.org/abs/1201.2557))


The relation of Theta characteristics on [[intermediate Jacobians]] to [[self-dual higher gauge theory]] was first recognized in 

* {#Witten96} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J.Geom.Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))

and the argument there was made rigorous in 

* {#HopkinsSinger02} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_

Related arguments revolving around [[characteristic element of a bilinear form|characteristic elements]] for the [[intersection pairing]] appear in 

* {#PoonenRains11} Bjorn Poonen, Eric Rains, _Self cup products and the theta characteristic torsor_ ([arXiv:1104.2105](http://arxiv.org/abs/1104.2105))

[[!redirects Θ characteristic]]
[[!redirects ∞-characteristic]]
[[!redirects Theta-characteristic]]

[[!redirects Θ characteristics]]
[[!redirects ∞-characteristics]]
[[!redirects Theta characteristics]]
[[!redirects Theta-characteristics]]

[[!redirects theta characteristic]]
[[!redirects theta characteristics]]
[[!redirects theta-characteristic]]
[[!redirects theta-characteristics]]