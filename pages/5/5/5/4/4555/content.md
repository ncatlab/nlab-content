
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

_Differential characters_ &lbrack;[Cheeger & Simons 1985](#CheegerSimons85)&rbrack; are one geometric model for [[ordinary differential cohomology]], hence for the [[differential cohomology]]-refinement of [[integral cohomology|integral]] [[ordinary cohomology]] -- i.e. of the [[cohomology theory]] [[Brown representability theorem|represented]] by the [[Eilenberg-MacLane spectrum]] $K(-,\mathbb{Z})$.

Accordingly, Cheeger-Simons differential characters model [[circle n-bundles with connection]] ($U(1)$-$(n-1)$-[[bundle gerbes]]) and as such are equivalent to other models for these structures, notably to [[Deligne cohomology]]. For $n=1$ these are equivalently ordinary [[connection on a bundle|connections]] on ordinary [[circle group]]-[[principal bundles]].

The definition of CS-differential characters encodes rather directly the higher dimensional notion of [[parallel transport]] of such higher connections: a Cheeger-Simons-character is a rule that assigns values in the [[circle group]] $U(1)$ (whence "[[character]]") to $n$-dimensional [[smooth manifolds]] $\Sigma_n \to X$ in a [[smooth manifold]] $X$, such that whenever $\Sigma_n = \partial \Sigma_{n+1}$ is the [[boundary of a manifold|boundary]] of a $\phi \colon \Sigma_{n+1} \to X$, this assignment coincides with the [[integration of differential forms|integral]] $\int_{\Sigma_{n+1}} \phi^* F$ of the [[pullback of differential forms|pullback]] of a [[curvature]] $(n+1)$-form $F \in \Omega^{n+1}_{cl}(X)$.


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

* [[Shiing-shen Chern]], [[James Simons]]: *[[Characteristic forms and geometric invariants]]*, The Annals of Mathematics, Second Series **99** 1 (1974) 48-69 &lbrack;[doi:10.2307/1971013](ttps://doi.org/10.2307/1971013), [jstor:1971013](http://www.jstor.org/stable/1971013)&rbrack;


Monograph:

* [[Christian Bär]], [[Christian Becker]]: *Differential Chafacters*, Lecture Notes in Mathematics **2112** &lbrack;[doi:10.1007/978-3-319-07034-6](https://doi.org/10.1007/978-3-319-07034-6)&rbrack;

See in particular:

* [[Christian Bär]], [[Christian Becker]], *Differential Characters and Geometric Chains*, in: *Differential Characters*, Lecture Notes in Mathematics **2112**, Springer (2014)  &lbrack;[arXiv:1303.6457](https://arxiv.org/abs/1303.6457), [doi:10.1007/978-3-319-07034-6_1](https://doi.org/10.1007/978-3-319-07034-6_1)&rbrack;

Review in the broader context of [[differential cohomology]]:

* [[Mike Hopkins]], [[Isadore Singer]]: *Cheeger-Simons Cohomology*, section 3 in: _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_,  J. Differential Geom. **70** 3 (2005)  329-452 &lbrack;[arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216), [doi:10.4310/jdg/1143642908](https://doi.org/10.4310/jdg/1143642908), [euclid:1143642908](https://projecteuclid.org/euclid.jdg/1143642908)&rbrack;

Further discussion:

* Mark Brightwell, [[Paul Turner]]: _Relative differential characters_, Communications in Analysis and Geometry, **14** 2 (2006) 269-282 &lbrack;[doi:10.4310/CAG.2006.v14.n2.a3](https://dx.doi.org/10.4310/CAG.2006.v14.n2.a3), [arXiv:math.AT/0408333](http://arxiv.org/abs/math.AT/0408333)&rbrack;
  > ([[relative cohomology]])

* [[James Simons]], [[Dennis Sullivan]]: _Axiomatic characterization of ordinary differential cohomology_,  J Topology **1** 1 (2008) 45-56 &lbrack;[arXiv:math/0701077](https://arxiv.org/abs/math/0701077), [doi:10.1112/jtopol/jtm006]( https://doi.org/10.1112/jtopol/jtm006)m [web pdf](http://jtopol.oxfordjournals.org/content/1/1/45.full.pdf+html)&rbrack;
  > (the [[differential cohomology hexagon]])

* [[Christian Becker]], [[Marco Benini]], [[Alexander Schenkel]], [[Richard J. Szabo]]: *Cheeger-Simons differential characters with compact support and Pontryagin duality*, Communications in Analysis and Geometry **27** 7 (2019) 1473-1522 &lbrack;[arXiv:1511.00324](https://arxiv.org/abs/1511.00324), [doi:10.4310/CAG.2019.v27.n7.a2](https://doi.org/10.4310/CAG.2019.v27.n7.a2)&rbrack;
  > ([[Pontryagin duality]])




[[!redirects Cheeger-Simons differential characters]]

[[!redirects differential character]]
[[!redirects differential characters]]

[[!redirects Cheeger-Simons character]]
[[!redirects Cheeger-Simons characters]]



