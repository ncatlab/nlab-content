
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

_Differential characters_ &lbrack;[Cheeger & Simons 1985](#CheegerSimons85)&rbrack; are one geometric model for the [[differential cohomology]]-refinement of [[integral cohomology|integral]] [[ordinary cohomology]] -- i.e. of the [[cohomology theory]] [[Brown representability theorem|represented]] by the [[Eilenberg-MacLane spectrum]] $K(-,\mathbb{Z})$.

Accordingly, Cheeger-Simons differential characters model [[circle n-bundles with connection]] ($U(1)$-$(n-1)$-[[gerbes]]) and as such are equivalent to other models for these structures, notably to [[Deligne cohomology]]. For $n=1$ these are ordinary [[connection on a bundle|connections]] on ordinary [[circle group]]-[[principal bundles]].

The definition of CS-differential characters encodes rather directly the higher dimensional notion of [[parallel transport]] of such higher connections: a CS-character is a rule that assigns values in the [[circle group]] $U(1)$ (whence "[[character]]") to $n$-dimensional [[smooth manifolds]] $\Sigma_n \to X$ in a [[smooth manifold]] $X$, such that whenever $\Sigma_n = \partial \Sigma_{n+1}$ is the [[boundary of a manifold|boundary]] of a $\phi \colon \Sigma_{n+1} \to X$, this assignment coincides with the [[integration of differential forms|integral]] $\int_{\Sigma_{n+1}} \phi^* F$ of the [[pullback of differential forms|pullback]] of a [[curvature]] $(n+1)$-form $F \in \Omega^{n+1}_{cl}(X)$.


## As secondary characteristic classes

Since Cheeger-Simons characters enocde information beyond the [[curvature characteristic form]] which represents the underlying [[characteristic class]] in de Rham cohomology, they are frequently called *[[secondary characteristic classes]]*, in particular if the curvature characteristic form vanishes so that the corresponding [[Chern-Simons form]] becomes [[closed differential form|closed]].

## Related concepts

* [[ordinary differential cohomology]]

* [[Chern-Simons form]]

* [[circle n-bundle with connection]]

* [[Chern-Weil homomorphism]]

* [[secondary characteristic class]]

* [[Cheeger-Simons homomorphism]]


## References

The original article:

* {#CheegerSimons85} [[Jeff Cheeger]],  [[James Simons]]: _Differential characters and geometric invariants_,  in: _Geometry and Topology_, Lecture Notes in Mathematics, **1167** Springer (1985) 50-80 &lbrack;[pdf](http://numr.wdfiles.com/local--files/differential-cohomology/cheeger-simons.pdf), [doi:10.1007/BFb0075212](https://doi.org/10.1007/BFb0075212)&rbrack;
 
building on 

* [[Shiing-shen Chern]], [[James Simons]]: *[[Characteristic forms and geometric invariants]]*, The Annals of Mathematics, Second Series **99** 1 (1974) &lbrack;[jstor:1971013](http://www.jstor.org/stable/1971013)&rbrack;

Further developments:

* [[James Simons]], [[Dennis Sullivan]], _Axiomatic characterization of ordinary differential cohomology_,  J Topology **1** 1 (2008) 45-56 &lbrack;[arXiv:math/0701077](https://arxiv.org/abs/math/0701077), [doi:10.1112/jtopol/jtm006]( https://doi.org/10.1112/jtopol/jtm006) [web pdf](http://jtopol.oxfordjournals.org/content/1/1/45.full.pdf+html)&rbrack;

* Mark Brightwell, Paul Turner: _Relative differential characters_ &lbrack;[arXiv:math.AT/0408333](http://arxiv.org/abs/math.AT/0408333)&rbrack;

See also:

* [[Christian Bär]], [[Christian Becker]], *Differential Characters and Geometric Chains*, in: *Differential Characters*, Lecture Notes in Mathematics **2112**, Springer (2014)  &lbrack;[arXiv:1303.6457](https://arxiv.org/abs/1303.6457), [doi:10.1007/978-3-319-07034-6_1](https://doi.org/10.1007/978-3-319-07034-6_1)&rbrack;


For a review in the broader context of [[differential cohomology]] see also 

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_ (2005)

[[!redirects Cheeger-Simons differential characters]]

[[!redirects differential character]]
[[!redirects differential characters]]

[[!redirects Cheeger-Simons character]]
[[!redirects Cheeger-Simons characters]]



