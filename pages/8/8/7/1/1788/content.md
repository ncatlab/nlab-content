> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak



***

### The Lagrangian density and the Level

Let's normalize [[connection]] [[differential forms|forms]] according to the common convention in theoretical physics, where the [[field strength]]/[[flux density]]  $F_A \coloneqq \mathrm{d}A$ it such that
\[
  \label{NormalizationPfFluxDensity}
  \tfrac{1}{2\pi} F_A
  \;\in\;
  \Omega^2_{int, cls}
\]
is an [[integral form]], in that it has [[integer]] [periods](period#InDifferentialGeometry) (cf. *[[Dirac charge quantization]]* and *[[ordinary differential cohomology]]*).


The [[Lagrangian density]] of abelian Chern-Simons theory is a multiple of the [[Chern-Simons form]]
$$
  L(A)
  \;\coloneqq\;
  \tfrac{K}{4\pi} A \wedge \mathrm{d} A
  \,
$$ 
for a numerical parameter $K$ to be fixed, so that the [[action functional]]
$$
  S(\Sigma^3, A)
  \;\coloneqq\;
  \tfrac{K}{4\pi}
  \textstyle{\int_{\Sigma^3}} 
  A \wedge \mathrm{d}A
$$
has [[gauge invariance|gauge-invariant]] [[exponential]]
$$
  \exp\Big(
    \mathrm{i} S(A)
  \Big)
  \;=\;
  \exp\Big( 
    \mathrm{i}
    \tfrac{K}{4\pi}
    \textstyle{\int_{\Sigma^3}} 
    A \wedge \mathrm{d}A
  \Big)
  \;\in\;
  \mathrm{U}(1)
  \,.
$$

A transparent way to understand this condition is to consider (in the style of the definition of [[Cheeger-Simons differential characters]]) a [[compact topological space|compact]] [[4-manifold]] $\Sigma^4$ [[manifold with boundary|with boundary]] $\Sigma^3 = \partial \Sigma^4$ and an extension of the $\mathrm{U}(1)$-connection to $\Sigma^4$, where we will denote its [[curvature]]/[[field strength]]/[[flux density]] still by $F$. 

Then the [[Stokes theorem]] gives
$$
  \exp\Big(
    \mathrm{i} S(A)
  \Big)
  \;=\;
  \exp\Big(
    \mathrm{i}
    \tfrac{K}{4\pi}
    \textstyle{\int_{\Sigma^4}}
    F \wedge F
  \Big)
  \;=\;
  \exp\Big(
    K \pi \mathrm{i}
    \textstyle{\int_{\Sigma^4}}
    \frac{F}{2\pi} \wedge \frac{F}{2\pi}
  \Big)
  \,.
$$
For this to be well-defined --- in that it takes the same value for any other choice of $\Sigma^4$, we need that for *[[closed manifold|closed]]* $\widehat{\Sigma}^4$ we have
$$
  \tfrac{1}{2\pi \mathrm{i}}
  K \pi \mathrm{i}
  \underset{
    c_1^2(\Sigma^4)
  }{
    \underbrace{
      \textstyle{\int_{\widehat{\Sigma}^4}}
      \frac{F}{2\pi} \wedge \frac{F}{2\pi}
    }
  }
  \;\in\;
  \mathbb{Z}
  \,.
$$

If there is no further condition on $\Sigma^3$ and hence on $\widehat{\Sigma}^4$, then by (eq:NormalizationPfFluxDensity), $c_1^2(\Sigma^4) \in \mathbb{Z}$ and the condition is that 
$$
  k 
    \;\coloneqq\; 
  \tfrac{K}{2}
    \;\in\;
  \mathbb{Z}
$$ 
must be an [[integer]]. This is the *[[Chern-Simons level]]*.

However, if we restrict evaluation to [[spin manifolds]] then ([Dijkgraaf & Witten 1990 §5](#DijkgraafWitten90)):

from the observation that the [[cobordism ring]] for spin 3-manifolds with complex line bundles is trivial, and that 
$$
  \widehat{\Sigma}^4 
  \;
  \text{spin manifold}
  \;\;
  \Rightarrow
  \;\;
  \int_{\widehat{\Sigma}^4}
  \frac{F}{2\pi} \wedge \frac{F}{2\pi}
  \;\in\;
  2\mathbb{Z}
$$
it follows that for *[[spin Chern-Simons theory]]* one may allow
$$ 
  k 
    \;\in\;
  \tfrac{1}{2}\mathbb{Z} 
  \;\;\;\;\;\;
  \text{equivalently}
  \;\;\;\;\;\;
  K \coloneqq 2k 
  \;\in\;
  \mathbb{Z}
  \,.
$$

(...)
