
#Contents#
* table of contents
{:toc}

## Idea

A [[zeta function]] naturally associated to a [[Riemann surface]].

([Minakshisundaram-Pleijel 49](#MinakshisundaramPleijel49)) considered the [[zeta function of an elliptic differential operator]] for the [[Laplace operator]] on a [[Riemann surface]].

Motivated by the resemblance of the [[Selberg trace formula]] to Weil's formula for the sum of zeros of the [[Riemann zeta function]], ([Selberg 56](#Selberg56)) defined for any compact hyperbolic [[Riemann surface]] a [[zeta function]]-like expression, the _Selberg zeta function of a Riemann surface_. (e.g. [Bump, below theorem 19](#Bump)).

> (Is it however on the nose the [[zeta function of an elliptic differential operator]] for the [[Laplace operator]]?)

## Examples

### For a complex torus / complex elliptic curve

For $\mathbb{C}/(\mathbb{Z}\oplus \tau \mathbb{Z})$
a [[complex torus]] (complex [[elliptic curve]]) equipped with its
standard flat [[Riemannian metric]], then the [[zeta function of an elliptic differential operator|zeta function]] of the corresponding [[Laplace operator]] $\Delta$ is

$$
  \zeta_{\Delta} = (2\pi)^{-2 s} E(s)
   \coloneqq
   (2\pi)^{-2 s} \underset{(k,l)\in \mathbb{Z}\times\mathbb{Z}-(0,0)}{\sum}
  \frac{1}{{\vert k +\tau l\vert}^{2s}}
  \,.
$$

The corresponding [[functional determinant]] is

$$
  \exp(
    E^\prime_{\Delta}(0)
  )
  = (Im \tau)^2 {\vert \eta(\tau)\vert}^4
  \,,
$$

where $\eta$ is the [[Dedekind eta function]]. 

(recalled e.g. in [Todorov 03, page 3](#Todorov03))


### Of Dirac operators twisted by a flat connection
 {#OfDiracOperatorTwistedByFlatConnection}

For $A$ a [[flat connection]] on a [[Riemannian manifold]], write $D_A$ for the [[Dirac operator]] twisted by this connection. 

On a suitable [[hyperbolic manifold]], the [[partition function]]/[[theta function]] for $D_A$ appears in ([Bunke-Olbrich 94a, def. 3.1](#BunkeOlbrich94a)) (there for the odd dimensional case). The corresponding Selberg zeta formula is ([Bunke-Olbrich 94a, def. 4.1](#BunkeOlbrich94a)). This has a form analogous to that of [[Artin L-functions]] with the flat connection replaced by a [[Galois representation]].

## Properties


### Function field analogy

[[!include function field analogy -- table]]

## Related concepts



[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

The original articles are
* {#MinakshisundaramPleijel49} S. Minakshisundaram, ; &#197; Pleijel, _Some properties of the eigenfunctions of the Laplace-operator on Riemannian manifolds_ (1949), Canadian Journal of Mathematics 1: 242&#8211;256, doi:10.4153/CJM-1949-021-5, ISSN 0008-414X, MR 0031145 ([web](http://cms.math.ca/10.4153/CJM-1949-021-5))


* {#Selberg56} [[Atle Selberg]], _Harmonic analysis and discontinuous groups in weakly symmetric Riemannian spaces with applications to Dirichlet series_, Journal of the Indian Mathematical Society 20 (1956) 47-87.


Review includes

* Wikipedia, _[Selberg zeta function](http://en.wikipedia.org/wiki/Selberg_zeta_function)_

* Wikipedia, _[Minakshisundaram&#8211;Pleijel zeta function](http://en.wikipedia.org/wiki/Minakshisundaram&#8211;Pleijel_zeta_function)_

* {#Watkins} [[Matthew Watkins]], citation collection on _[Selberg trace formula and zeta functions](http://empslocal.ex.ac.uk/people/staff/mrwatkin/zeta/physics4.htm)_

* {#Bump} Bump, below theorem 19 in _Spectral theory of $\Gamma \backslash SL(2,\mathbb{R})$_ ([[BumpSpectralTheory.pdf:file]])

Further developments include

* {#Friedman04} [[Joshua Friedman]], _The Selberg trace formula and Selberg zeta-function for cofinite Kleinian groups with finite-dimensional unitary representations_ ([arXiv:math/0410067](http://arxiv.org/abs/math/0410067))


Discussion in terms of [[theta functions]] of twisted [[Dirac operators]] is in 

* [[Ulrich Bunke]], [[Martin Olbrich]], Andreas Juhl, _The wave kernel for the Laplacian on the classical locally symmetric spaces of rank one, theta functions, trace formulas and the Selberg zeta function_, Annals of Global Analysis and Geometry February 1994, Volume 12, Issue 1, pp 357-405

* {#BunkeOlbrich94} [[Ulrich Bunke]], Martin Olbrich, _Theta and zeta functions for locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407013](http://arxiv.org/abs/dg-ga/9407013))

and for odd-dimensional spaces also in

* {#BunkeOlbrich94a} [[Ulrich Bunke]], [[Martin Olbrich]], _Theta and zeta functions for odd-dimensional locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407012](http://arxiv.org/abs/dg-ga/9407012))

* {#BunkeOlbrich94b} [[Ulrich Bunke]], [[Martin Olbrich]] _$\Gamma$-Cohomology and the Selbeg zeta function_ ([arXiv:dg-ga/9411004](http://arxiv.org/abs/dg-ga/9411004))

* [[Ulrich Bunke]], [[Martin Olbrich]], _Group cohomology and the singularities of the Selberg zeta function associated to a Kleinian group_ ([arXiv:dg-ga/9603003](http://arxiv.org/abs/dg-ga/9603003))

A survey is in 

* {#BunkeOlbrich95} [[Ulrich Bunke]], [[Martin Olbrich]], _Selberg zeta and theta functions: a differential operator approach_, Akademie Verlag 1995

See also

* {#Todorov03} [[Andrey Todorov]], _The analogue of the Dedekind eta function for CY threefolds_, 2003 [pdf](http://www.ma.huji.ac.il/conf/crelle.pdf)


[[!redirects Selberg zeta function]]


[[!redirects Selberg zeta function of a Riemann surface]]