
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

What is called _analytic torsion_ or _Ray-Singer torsion_ ([Ray-Singer 73](#RaySinger73)) is the invariant $T(X,g)$ of a [[Riemannian manifold]] $(X,g)$ given by a product of powers of the [[functional determinants]] $det_{reg} \Delta|_{\Omega^p}$ of the [[Laplace operators]] $\Delta|_{\Omega^p}$ of the manifold acting on the space of [[differential p-forms]]:

$$
  T(X,g)
  \coloneqq
  \underset{p}{\prod}
  \left(det_{reg} \Delta|_{\Omega^p}\right)^{-(-1)^p \frac{p}{2}}
  \,.
$$


This analytic torsion is an  [[analogy|analogue]] in [[analysis]] of the invariant of [[topological manifolds]] called _[[Reidemeister torsion]]_. The two agree for compact Riemannian manifolds ([Cheeger 77](#Cheeger77)).

## Properties

### Relation to Iwasawa theory

According to ([Morishita 09](arithmetic+topology#Morishita09)) the relation between Reidemeister torsion and analytic torsion is analogous to that between [[Iwasawa polynomials]] and [[zeta functions]] obtained by [[adelic integration]]. (...)

### Relation to Selberg and Ruelle zeta function
 {#RelationToSelbergZeta}

The [[special value of L-functions|special value]] of a [[Ruelle zeta function]] at $s= 0$ is expressed by [[Reidemeister torsion]]

([Fried 86](#Fried86))

### Relation to Chern-Simons theory

Analytic torsion appears as one factor in the [[perturbation theory|perturbative]] [[path integral]] [[quantization]] of [[Chern-Simons field theory]]. See there at _[Quantization -- Perturbative -- Path integral quantization](http://ncatlab.org/nlab/show/Chern-Simons+theory#PerturbativePathIntegralQuantization)_.

## References

* {#RaySinger73} D. Ray, [[Isadore Singer]], _Analytic torsion for complex manifolds_, Ann. Math. __98__, 1 (1973), 154--177.

* {#Cheeger77} [[Jeff Cheeger]], _Analytic torsion and Reidemeister torsion_, Proc. Natl. Acad. Sci. USA __74__, No. 7, pp. 2651-2654 (1977), [pdf](http://www.pnas.org/content/74/7/2651.full.pdf)

* Wikipedia, _[Analytic torsion](http://en.wikipedia.org/wiki/Analytic_torsion)_

* A.A. Bytsenko, A.E. Goncalves, W. da Cruz, _Analytic Torsion on Hyperbolic Manifolds and the Semiclassical Approximation for Chern-Simons Theory_ ([arXiv:hep-th/9805187](http://arxiv.org/abs/hep-th/9805187))

Review of the role played in the perturbative [[quantization of Chern-Simons theory]] includes

* {#Young} M. B. Young, section 2 of _Chern-Simons theory, knots and moduli spaces of connections_ ([pdf](http://www.math.sunysb.edu/~myoung/CS.pdf))

Discussion for [[hyperbolic manifolds]] in terms of the [[Selberg zeta function]]/[[Ruelle zeta function]] is due to 

* {#Fried86} [[David Fried]], _Analytic torsion and closed geodesics on hyperbolic manifolds_, Invent. math. 84, 523-540 (1986) ([pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN356556735_0084&divID=LOG_0026&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN356556735_0084%7C&targetFileName=PPN356556735_0084_LOG_0026.pdf&))

with further developments including

* {#BunkeOlbrich94a} [[Ulrich Bunke]], [[Martin Olbrich]], _Theta and zeta functions for odd-dimensional locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407012](http://arxiv.org/abs/dg-ga/9407012))

* {#Park09} Jinsung Park, _Analytic torsion and Ruelle zeta functions for hyperbolic manifolds with cusps_, Journal of Functional Analysis Volume 257, Issue 6, 15 September 2009, Pages 1713&#8211;1758


[[!redirects Ray-Singer torsion]]