
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


\tableofcontents

## Statement


+-- {: .num_theorem}
###### Theorem
**(Poincar&#233; conjecture)**

Every [[simply connected]] [[compact space|compact]] [[topological manifold|topological]] [[3-manifold]] without boundary is [[homeomorphism|homeomorphic]] to the 3-sphere.

=--

+-- {: .proof}
###### Proof strategy


A proof strategy was given by [[Richard Hamilton]]: imagine the manifold is equipped with a [[metric]]. Follow the [[Ricci flow]] of that metric through the space of metrics. As the flow proceeds along parameter time, it will from time to time pass through metrics that describe singular geometries where the compact metric manifold pinches off into separate manifolds. Follow the flow through these singularities and then continue the flow on each of the resulting components. If this process terminates in finite parameter time with the metric on each component stabilizing to that of the round 3-sphere, then the original manifold was a 3-sphere.

The hard technical part of this program is to show that the passage through the  singularities can be controlled. This was finally shown in ([Perelman 02](Perelman02)).

=--

See at _[[Ricci flow]]_ for more.

## Related entries

* [[geometrization conjecture]]

[[!include four-dimensional geometry and topology -- table]]

## References

### In dimension 3

The proof of the Poincaré conjecture is attributed to these unpublished articles:

* {#Perelman02} [[Grigori Perelman]]: _The entropy formula for the Ricci flow and its geometric applications_ &lbrack;[arXiv:math/0211159](http://arxiv.org/abs/math/0211159)&rbrack;

* {#Perelman03a} [[Grigori Perelman]]: *Ricci flow with surgery on three-manifolds* &lbrack;[arXiv:0303109](https://arxiv.org/abs/math/0303109)&rbrack;

* {#Perelman03b} [[Grigori Perelman]]: *Finite extinction time for the solutions to the Ricci flow on certain three-manifolds* &lbrack;[arXiv:math/0307245](https://arxiv.org/abs/math/0307245)&rbrack;

Further discussion:

* {#BessiersEtAl} Laurent Bessieres, Gerard Besson, Michel Boileau, Sylvain Maillot, Joan Porti, _Geometrisation of 3-manifolds_ ([pdf](http://www-fourier.ujf-grenoble.fr/~besson/book.pdf))

* [[John W. Morgan]], [[Gang Tian]]: _Ricci Flow and the Poincaré Conjecture_, Clay Mathematics Monographs __3__ (2007) &lbrack;[arXiv:math/0607607](https://arxiv.org/abs/math/0607607), [webpage](https://www.claymath.org/resource/ricci-flow-and-the-poincare-conjecture/), [pdf](https://www.claymath.org/wp-content/uploads/2022/03/Ricci-pdf.pdf)&rbrack;


Notes from a survey talk: 

* [Huisken on Uniformization I](http://golem.ph.utexas.edu/category/2007/02/huisken_on_uniformization.html)

* [Huisken on Uniformization II](http://golem.ph.utexas.edu/category/2007/02/huisken_on_uniformization_ii.html)

See also

* {#Martelli16} Bruno Martelli, _An Introduction to Geometric Topology_ ([arXiv:1610.02592](https://arxiv.org/abs/1610.02592))

### In higher dimesnions

On the analog of the Poincaré conjecture in higher dimensions:


* {#Newman66} [[M. H. A. Newman]], Theorem 7 in: *The Engulfing Theorem for Topological Manifolds*, Annals of Mathematics Second Series, *84** 3 (1966) 555-571  ([jstor:1970460](https://www.jstor.org/stable/1970460))

* {#Siebenmann82} [[Laurent Siebenmann]]: *La conjecture de Poincaré topologique en dimension 4*, Séminaire Bourbaki volume 1981/82, exposés 579-596, Astérisque, no. 92-93 (1982), Talk no. 588 &lbrack;[numdam:SB_1981-1982__24__219_0](https://www.numdam.org/item/?id=SB_1981-1982__24__219_0)&rbrack;

* [[Laurent Siebenmann]] (translation by M. H. Kim & M. Powell): _Topological Poincaré conjecture in dimension 4 (the work of M. H. Freedman)_, Celebratio Mathematica &lbrack;[celebratio:752](https://celebratio.org/Freedman_MH/article/752)&rbrack;


[[!redirects Poincare conjecture]]