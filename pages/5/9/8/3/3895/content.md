
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

### General
 {#ReferencesGeneral}

The original articles:

* [[Daniel Burrill Ray]], [[Isadore Singer]]: *$R$-torsion and the Laplacian on Riemannian manifolds*, Adv. Math. **7** 2 (1971) 145-210 \[<a href="https://doi.org/10.1016/0001-8708(71)90045-4">doi:10.1016/0001-8708(71)90045-4</a>\]
  > (for [[Riemannian manifolds]])

* {#RaySinger73} [[Daniel Burrill Ray]], [[Isadore Singer]]: *Analytic torsion for complex manifolds*, Ann. Math. **98** 1 (1973) 154-177 \[<a href="https://doi.org/10.2307/1970909">doi:10.2307/1970909</a>, [jstor:1970909](https://www.jstor.org/stable/1970909)\]
  > (for [[complex manifolds]])

Proof of the Ray-Singer conjecture that on [[compact topological space|compact]] [[Riemannian manifolds]] the analytic torsion coincides with the [[Reidemeister torsion]]:

* {#Cheeger77} [[Jeff Cheeger]]: *Analytic torsion and Reidemeister torsion*, Proc. Natl. Acad. Sci. USA __74__ 7 (1977) 2651-2654 &lbrack;[doi:10.1073/pnas.74.7.2651](https://doi.org/10.1073/pnas.74.7.2651), [pdf](http://www.pnas.org/content/74/7/2651.full.pdf)&rbrack;

* Werner Müller: _Analytic torsion and R-torsion of Riemannian manifolds_, Adv. in Math. **28** 3 (1978) 233-305 \[<a href="https://doi.org/10.1016/0001-8708(78)90116-0">doi;10.1016/0001-8708(78)90116-0</a>\]


Review:

* [[John Lott]]: *The Ray-Singer torsion*, Bulletin of the AMS **62** 1 (2025) 17-34  &lbrack;[arXiv:2309.05688](https://arxiv.org/abs/2309.05688), [doi:10.1090/bull/1848](https://doi.org/10.1090/bull/1848), [pdf](https://www.ams.org/journals/bull/2025-62-01/S0273-0979-2024-01848-5/S0273-0979-2024-01848-5.pdf)&rbrack;

See also:

* Wikipedia, _[Analytic torsion](http://en.wikipedia.org/wiki/Analytic_torsion)_


### In Chern-Simons theory

Review of the role of analytic torsion played in the [[perturbative quantum field theory|perturbative]] [[quantization of Chern-Simons theory]]:

* A. A. Bytsenko, A. E. Goncalves, W. da Cruz, _Analytic Torsion on Hyperbolic Manifolds and the Semiclassical Approximation for Chern-Simons Theory_ ([arXiv:hep-th/9805187](http://arxiv.org/abs/hep-th/9805187))

* {#Young} M. B. Young, section 2 of _Chern-Simons theory, knots and moduli spaces of connections_ ([pdf](http://www.math.sunysb.edu/~myoung/CS.pdf))

Discussion for [[hyperbolic manifolds]] in terms of the [[Selberg zeta function]]/[[Ruelle zeta function]] is due to 

* {#Fried86} [[David Fried]], _Analytic torsion and closed geodesics on hyperbolic manifolds_, Invent. math. 84, 523-540 (1986) ([pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN356556735_0084&divID=LOG_0026&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN356556735_0084%7C&targetFileName=PPN356556735_0084_LOG_0026.pdf&))

with further developments including

* {#BunkeOlbrich94a} [[Ulrich Bunke]], [[Martin Olbrich]], _Theta and zeta functions for odd-dimensional locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407012](http://arxiv.org/abs/dg-ga/9407012))

* {#Park09} Jinsung Park, _Analytic torsion and Ruelle zeta functions for hyperbolic manifolds with cusps_, Journal of Functional Analysis Volume 257, Issue 6, 15 September 2009, Pages 1713&#8211;1758

In relation to the  [[topological string]] and [[black hole entropy]]:

* [[Cumrun Vafa]], *Ray-Singer Torsion, Topological Strings and Black Holes* &lbrack;[arXiv:2401.12816](https://arxiv.org/abs/2401.12816)&rbrack;

See also:

* [[Matthias Blau]], Mbambu Kakona, [[George Thompson]], *On the Evaluation of the Ray-Singer Torsion Path Integral* &lbrack;[arXiv:2402.14437](https://arxiv.org/abs/2402.14437)&rbrack;




[[!redirects Ray-Singer torsion]]