
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

Formally, the *Ricci curvature* $Ric$ of a [[Riemannian manifold]] is a symmetric [[tensor|rank-2 tensor]] obtained by [[tensor contraction|contraction]] from the [[Riemann curvature]]. Geometrically one may think $Ric(v, w)$ as the first order approximation of the infinitesimal behavior of the [[surface]] spanned by [[vectors]] $v$ and $w$. This is made explicit by the following formula for the volume element around some point
$$
 d\mu _{g}
  \;=\;
  \left[1-{\tfrac {1}{6}}Ric_{jk}x^{j}x^{k}+O\left(|x|^{3}\right)\right]d\mu _{Euclidean}
$$

(where we are using the [[Einstein summation convention]]). 

A [[spacetime]] with vanishing Ricci curvature is also called _Ricci flat_.


## Properties

### Harmonic coordinate representation and regularity
 {#Regularity}

By a trick of [Lanczos 1922](#Lanczos22), rediscovered by [DeTurck & Kazdan 1981](#DeTurckKazdan81), in harmonic coordinates the Ricci tensor can be expressed as
$$
  Ric_{lm} 
  \;=\; 
  -\frac{1}{2} 
  \sum_{j,k} g^{j k} \partial_j \partial_k g_{lm} 
  + Q_{lm}(g, \nabla g)
  \,,
$$
where $g^{j k}$ denotes the inverse of the [[metric tensor]] and $Q_{lm}$ is a [[quadratic form]] in $\nabla g$ with [[coefficients]] that are [[rational function|rational expressions]] in which [[numerators]] are [[polynomials]] $g$ and the [[denominator]] depends only on $\sqrt{\det g}$. 

Note that this formula describes the metric tensor as a quasilinear [[elliptic differential operator|elliptic]] [[PDE]]. This is especially useful in two ways: 

1. There are theorems that give bounds on the regularity of the metric tensor in harmonic coordinates under geometric assumptions ([Anderson 1990](#Anderson90), [Anderson & Cheeger 1992](#AndersonCheeger92), [Cheeger & Naber 2013](#CheegerNaber13)). 

2. As this expression is a quasilinear elliptic PDE, one can conclude on regularity bounds for the metric tensor from regularity estimates for the Ricci tensor. 

This argument allows for a regularity bootstrap in case of [[Einstein manifold|Einstein manifolds]]: given a rough Einstein metric with $k$ derivatives, the regularity theory for quasilinear PDEs gives $k+2$-regularity of the metric tensor. But the Einstein property $g = \lambda Ric$ implies the same regularity for the Ricci tensor. Hence one can apply the argument again and add infinitum.



### Cheeger-Gromoll theorem

See at *[[Cheeger-Gromoll theorem]]*.



## Examples
 {#Examples}

\begin{example}\label{RicciTensorOfRoundNSphere}
  For $n \in \mathbb{N}_{\gt 0}$ and $r \in \mathbb{R}_{\gt 0}$, the Ricci tensor of the [[round sphere|round]] [[n-sphere|$n$-sphere]] $S^n$ of [[radius]] $r$ satisfies
$$
  Ric(v,v) \;=\; \frac{n-1}{r^2}
$$
for all unit-length [[tangent vectors]] $v \in T S^n$, ${\vert v \vert} = 1$.

Accordingly, the [[scalar curvature]] of the [[round sphere|round]] [[n-sphere|$n$-sphere]] of [[radius]] $r$ is the [[constant function]] with value
$$
  \mathrm{R} \;=\; \frac{n(n-1)}{r^2}
  \,.
$$
\end{example}
(e.g. [Lee 2018, Cor. 11.20](#Lee18))



## Related concepts


[[!include curvature in Riemannian geometry -- table]] 


* [[Einstein-Hilbert action]]

* [[Einstein equations of motion]]

* [[Einstein manifold]]




## References

See most references listed at *[[Riemannian geometry]]*, for instance:

* {#Lee97} [[John M. Lee]], _Riemannian manifolds. An introduction to curvature_, Graduate Texts in Mathematics **176** Springer (1997) &lbrack;ISBN: 0-387-98271-X&rbrack;

  second edition (retitled):

  {#Lee18} [[John M. Lee]], *Introduction to Riemannian Manifolds*, Springer (2018) &lbrack;ISBN:978-3-319-91754-2, [doi:10.1007/978-3-319-91755-9](https://doi.org/10.1007/978-3-319-91755-9)&rbrack;

See also:

* Wikipedia, _[Ricci curvature](http://en.wikipedia.org/wiki/Ricci_curvature)_

On Lanczos's trick:

* {#Lanczos22} Lanczos, *Ein vereinfachendes Koordinatensystem für die Einsteinschen Gravitationsgleichungen*, Phys. Z. **23**  (1922) 537-539

* {#DeTurckKazdan81} Dennis DeTurck, Jerry Kazdan, *Some regularity theorems in Riemannian geometry*, Annales scientifiques de l'École Normale Supérieure, Serie 4, Volume 14 (1981) no. 3, pp. 249-260 &lbrack;[numdam:ASENS_1981_4_14_3_249_0](http://www.numdam.org/item/?id=ASENS_1981_4_14_3_249_0)&rbrack;


On regularity results:

* {#Anderson90} [[Michael T. Anderson]], *Convergence  and rigidity of manifolds under Ricci curvature bounds*, Invent. Math. **102** (1990) 429-445 &lbrack;[doi:10.1007/BF01233434](https://doi.org/10.1007/BF01233434), [pdf](https://link.springer.com/content/pdf/10.1007/BF01233434.pdf)&rbrack;

* {#CheegerNaber13} [[Jeff Cheeger]], [[Aaron Naber]]: *Lower bounds on Ricci curvature and quantitative behavior of singular sets*,  Invent. Math. **191** (2013) 321–339 &lbrack;[arXiv:1103.1819](https://arxiv.org/abs/1103.1819), [doi:10.1007/s00222-012-0394-3](https://doi.org/10.1007/s00222-012-0394-3)&rbrack;

For weaker but more general regularity results see also:

* {#AndersonCheeger92} [[Michael T. Anderson]], [[Jeff Cheeger]], _$C^\alpha$-compactness for manifolds with Ricci curvature and injectivity radius bounded below_ J. Diff. Geo. **35** 2 (1992) 265-281 &lbrack;[doi:10.4310/jdg/1214448075](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-35/issue-2/Calpha-compactness-for-manifolds-with-Ricci-curvature-and-injectivity-radius/10.4310/jdg/1214448075.full)&rbrack;

A conjecture that all [[compact topological space|compact]] Ricci flat manifolds either have [[special holonomy]] or else are "unstable":

* {#Acharya19} [[Bobby Acharya]], *Supersymmetry, Ricci Flat Manifolds and the String Landscape*, High Energ. Phys. **2020** 128 (2020) &lbrack;[arXiv:1906.06886](https://arxiv.org/abs/1906.06886), <a href="https://doi.org/10.1007/JHEP08(2020)128">doi:10.1007/JHEP08(2020)128</a>&rbrack;

[[!redirects Ricci curvatures]]

[[!redirects Ricci tensor]]
[[!redirects Ricci tensors]]

[[!redirects Ricci flat]]
[[!redirects Ricci flatness]]


[[!redirects Ricci flat manifold]]
[[!redirects Ricci flat manifolds]]
