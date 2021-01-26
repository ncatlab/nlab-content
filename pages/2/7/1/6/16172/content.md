
> For other, related, concepts of a similar name see at _[[cone]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In ([[pseudo-Riemannian geometry|pseudo-]])[[Riemannian geometry]], a _cone_ is a part of a  (pseudo-)[[Riemannian manifold]] where the [[metric tensor]] is locally of the form $d s^2 = d r^2 + r^2 d s^2_1$. The point that would correspond to $r = 0$ is the "conical singularity". 

## Examples

### Spherical cones
 {#SphericalCones}

The metric cone on the [[round sphere]] is simply [[Euclidean space]]

$$
  C(S^n) \simeq \mathbb{R}^{n+1} \setminus \{0\}
$$

and hence may in fact be continued non-singularly also at the cone tip.

For $G$ a [[finite group]] with a [[free action|free]] [[action]] on the [[round sphere]] $S^n$, the [[quotient space]] $S^n/G$ exists as a [[Riemannian manifold]]. The metric cone $C(S^n/G)$ on this is singular at the origin as soon as $G$ is not the [[trivial group]]. 

If here $G = \mathbb{Z}_n$ is a [[cyclic group]] one says that this cone is obtained from flat [[Euclidean space]] by introducing a "deficit angle".

<center>
<img src="https://ncatlab.org/nlab/files/ConicalSingularity.jpg" width="300">
</center>

If one passes beyond [[smooth manifolds]] to [[orbifolds]], then the cone tip in $C(S^n/G)$ may be included. The result is the [[orbifold]] $\mathbb{R}^{n+1}\sslash G$ which is the [[homotopy quotient]] of [[Euclidean space]] by the linear $G$-[[action]] ($G$-[[representation]]).

Such conical singularities appear for instance in the [[far-horizon geometry]] of [[BPS state|BPS]] [[black branes]]. Special cases are [[ADE-singularities]].


### $G_2$-manifolds
 {#ExamplesG2Manifolds}

* Three examples of cones admitted by [[simply-connected]] [[G2-manifolds]] seem to be known: cones on $\mathbb{C}P^3$, $SU(3)/U(1)\times U(1)$ and $S^3 \times S^3$. ([Atiyah-Witten 01](#AtiyahWitten01))

* The [[metric cone over complex projective 3-space]] carries the [[mathematical structure|structure]] of  a [[G2-manifold]] whose [[Riemannian metric]] is [[invariant]] under the canonical [[Sp(2)]] [[action]] by left-[[matrix multiplication]] on homomogeneous coordinates in $\mathbb{H}^2 \simeq_{\mathbb{R}} \mathbb{C}^4 \to \mathbb{C}P^3$ ([Byant-Salamon 89](metric+cone+over+complex+projective+3-space#BryantSalamon89), see also [Acharya-Bryant-Salamon 20](metric+cone+over+complex+projective+3-space#AcharyaBryantSalamon20)).

## Related concepts

* [[conifold]]

* [[piecewise flat spacetime]]

* [[Sasakian manifold]]

* [[conical space]]

* [[M-theory on G2-manifolds]]


## References

### General

Discussion in the context of [[3-manifolds]] and [[orbifolds]]:

* Daryl Cooper, Craig Hodgson, Steve Kerckhoff, _Three-dimensional Orbifolds and Cone-Manifolds_,  MSJ Memoirs Volume 5, 2000 ([pdf](https://web.math.ucsb.edu/~cooper/37.pdf), [euclid:1389985812](https://projecteuclid.org/euclid.msjm/1389985812))


### Black brane conical singularities

Discussion of [[supergravity]] [[black brane]]-solutions at conical singularities ([[cone branes]]) includes the following (see also at _[[far-horizon geometry]]_)

* [[Bobby Acharya]], [[Jose Figueroa-O'Farrill]], [[Chris Hull]], B. Spence, _Branes at conical singularities and holography_, Adv. Theor.Math. Phys.2:1249-1286, 1999 ([arXiv:hep-th/9808014](https://arxiv.org/abs/hep-th/9808014))

* {#FigOFar98} [[Jose Figueroa-O'Farrill]], _Near-horizon geometries of supersymmetric branes_, talk at [SUSY 98](http://inspirehep.net/record/971430/) ([arXiv:hep-th/9807149](https://arxiv.org/abs/hep-th/9807149), [talk slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/SUSY98.pdf))


* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]], _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

A suggestion that there is an analogue of [[AdS-CFT duality]] for conical bulk spacetimes and their conical singularities:

* Rong-Xin Miao, _Codimension-$n$ Holography for the Cones_ ([arXiv:2101.10031](https://arxiv.org/abs/2101.10031))




[[!include G2-conifolds -- references]]


[[!redirects conical singularity]] 
[[!redirects conical singularities]] 

[[!redirects conifold singularity]]

[[!redirects metric cone]]
[[!redirects metric cones]]
