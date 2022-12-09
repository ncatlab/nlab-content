
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _differential character_ as introduced by [CheegerSimons](#CheegerSimons) is one geometric model for the [[differential cohomology]]-refinement of ordinary integral cohomology -- i.e. of the [[cohomology theory]] represented by the [[Eilenberg-MacLane spectrum]] $K(-,\mathbb{Z})$.

Accordingly, Cheeger-Simons differential characters model [[connection on a bundle|connection]]s on <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle n-group</a>-[[principal ∞-bundle]]s ( $U(1)$-$(n-1)$-[[gerbe]]s)  and as such are equivalent to other models for these structures, such as [[Deligne cohomology]]. For $n=1$ these are ordinary [[connection on a bundle|connections]] on ordinary [[circle group]]-[[principal bundle]]s.

The definition of CS-differential characters encodes rather directly the higher dimensional notion of [[parallel transport]] of such higher connections: a CS-character is a rule that assigns values in the [[circle group]] $U(1)$ (whence "[[character]]") to $n$-dimensional  surfaces $\Sigma_n \to X$ in a manifold $X$, such that whenever $\Sigma_n = \partial \Sigma_{n+1}$ is the boundary of a $\phi : \Sigma_{n+1} \to X$, this assignment coincides with the integral $\int_{\Sigma_{n+1}} \phi^* F$ of a smooth [[curvature]] $(n+1)$-form $F \in \Omega^{n+1}_{cl}(X)$.


## As secondary characteristic classes

Since Cheeger-Simons characters enocde information beyond the [[curvature characteristic form]] which represents the underlying [[characteristic class]] in de Rham cohomology, they are frequently called [[secondary characteristic class]]es, in particular if the curvature characteristic form vanishes so that the corresponding [[Chern-Simons form]] becomes exact.

## Related concepts

* [[ordinary differential cohomology]]

* [[Chern-Simons form]]

* [[circle n-bundle with connection]]

* [[Chern-Weil homomorphism]]

* [[secondary characteristic class]]

* [[Cheeger-Simons homomorphism]]

## References

The original article is

* {#CheegerSimons} [[Jeff Cheeger]],  [[James Simons]], _Differential characters and geometric invariants_, pages 50&#8211;80 in: _Geometry and Topology_, Lecture Notes in Mathematics, vol 1167. Springer (1985)  ([pdf](http://numr.wdfiles.com/local--files/differential-cohomology/cheeger-simons.pdf), [doi:10.1007/BFb0075212](https://doi.org/10.1007/BFb0075212))
 
building on 

* [[Shiing-shen Chern]], [[James Simons]], _[[Characteristic forms and geometric invariants]]_, The Annals of Mathematics, Second Series, Vol. 99, No. 1 (1974) ([jstor](http://www.jstor.org/stable/1971013)).

Further developments are in 

* [[James Simons]], [[Dennis Sullivan]], _Axiomatic characterization of ordinary differential cohomology_,  J Topology (2008) 1 (1): 45-56 ([arXiv:math/0701077](https://arxiv.org/abs/math/0701077), [doi:10.1112/jtopol/jtm006]( https://doi.org/10.1112/jtopol/jtm006) [web pdf](http://jtopol.oxfordjournals.org/content/1/1/45.full.pdf+html))

* Mark Brightwell, Paul Turner, _Relative differential characters_ ([arXiv:math.AT/0408333](http://arxiv.org/abs/math.AT/0408333))

See also:

* [[Christian Bär]], [[Christian Becker]], *Differential Characters and Geometric Chains*, in: *Differential Characters*, Lecture Notes in Mathematics **2112**, Springer (2014)  &lbrack;[arXiv:1303.6457](https://arxiv.org/abs/1303.6457), [doi:10.1007/978-3-319-07034-6_1](https://doi.org/10.1007/978-3-319-07034-6_1)&rbrack;


For a review in the broader context of [[differential cohomology]] see also 

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_ (2005)

[[!redirects differential character]]
[[!redirects differential characters]]
[[!redirects Cheeger-Simons differential characters]]
