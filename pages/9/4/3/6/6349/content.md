
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[Lorentzian manifold]] is called _globally hyperbolic_ if it admits a well-defined time evolution from initial data of [[field (physics)|physical fields]] on it.


## Definition

There are several equivalent definitions of global hyperbolicity. A simple one is:

+-- {: .num_defn}
###### Definition

A [[Lorentzian manifold]] (without [[boundary]]) is called **globally hyperbolic** if it contains a [[Cauchy surface]].

=--

In this form the characterization of global hyperbolicity appears for instance in the paragraph at the bottom of page 211 in ([HE](#LargeScale)).
The equivalence of this to more traditional definitions is ([HE, prop. 6.6.3](#LargeScale)) together with ([HE, prop. 6.6.8](#LargeScale)), due to ([Geroch1970](#Geroch)). The latter in fact implies the following stronger statement:

+-- {: .num_prop}
###### Proposition

A [[Lorentzian manifold]] (without [[boundary]]) is **globally hyperbolic** if it admits a [[foliation]] by [[Cauchy surfaces]].

=--

See also ([Baer-Ginoux-Pfaeffle 07, theorem 1.3.10](#BaerGinouxPfaeffle07)).

+-- {: .num_remark}
###### Remark

So in particular for a globally hyperbolic spacetime $X$ there is a [[homeomorphism]] 

$$
  \phi\colon \mathbb{R} \times \Sigma \to X
$$

from the [[product]] of the [[real line]] with a $(dim X - 1)$-[[dimension|dimensional]] [[smooth manifold]] $\Sigma$ and for each $t \in \mathbb{R}$ the image $\phi(t, \Sigma) \subset X$ is a [[Cauchy surface]] of $X$.

=--

A _time orientation_ of a globally hyperbolic Lorentzian spacetime is a choice of [[orientation]] of the factor $\mathbb{R}$ under the above homeomorphism.


## Related concepts

* [[AQFT on curved spacetimes]], [[locally covariant perturbative quantum field theory]]

* [[Cauchy problem]]

* [[Green hyperbolic partial differential equation]]

## References

Concise collection of definitions:

* {#MinguzziSánchez} E. Minguzzi, [[Miguel Sánchez]], §3.11 in: *The causal hierarchy of spacetimes*, in: *Recent Developments in Pseudo-Riemannian Geometry*, EMS ESI Lectures in Mathematics and Physics **4** (2008) 299-358 &lbrack;[arXiv:gr-qc/0609119](https://arxiv.org/abs/gr-qc/0609119), [ISBN:978-3-03719-051-7](https://bookstore.ams.org/view?ProductCode=EMSESILEC/4)&rbrack;

Survey:

* [[Miguel Sánchez]], *Globally hyperbolic spacetimes: slicings, boundaries and counterexamples*, Gen Relativ Gravit **54** 124 (2022) &lbrack;[arXiv:2110.13672](https://arxiv.org/abs/2110.13672), [doi:10.1007/s10714-022-03002-6](https://doi.org/10.1007/s10714-022-03002-6)&rbrack;


See also:

* {#LargeScale} Hawking, Ellis, section 6.6 of _The large-scale structure of Space-Time_ Cambridge (1973)

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))
  

The fact that a single Cauchy surface implies a foliation by Cauchy surfaces is due to:

* {#Geroch} [[Robert Geroch]], §5, Thm. 11 in: *Domain of Dependence*, J. Math. Phys. **11** (1970) 437–449 &lbrack;[doi:10.1063/1.1665157](https://doi.org/10.1063/1.1665157)&rbrack;
 
The refinement of this statement to a smooth splitting:

* [[Antonio N. Bernal]], [[Miguel Sánchez]], _On smooth Cauchy hypersurfaces and Geroch's splitting theorem_, Commun. Math. Phys. **243** (2003) 461-470 &lbrack;[arXiv:gr-qc/0306108v2](http://arxiv.org/abs/gr-qc/0306108), [doi:10.1007/s00220-003-0982-6](https://doi.org/10.1007/s00220-003-0982-6)&rbrack;

* [[Antonio N. Bernal]], [[Miguel Sánchez]], *Smoothness of time functions and the metric splitting of globally hyperbolic spacetimes*, Commun. Math. Phys. **257** (2005) 43-50 &lbrack;[arXiv:gr-qc/0401112](https://arxiv.org/abs/gr-qc/0401112), [doi:10.1007/s00220-005-1346-1](https://doi.org/10.1007/s00220-005-1346-1)&rbrack;

* [[Antonio N. Bernal]], [[Miguel Sánchez]], *Further results on the smoothability of Cauchy hypersurfaces and Cauchy time functions*, Lett. Math. Phys. **77** (2006) 183-197 &lbrack;[arXiv:gr-qc/0512095](https://arxiv.org/abs/gr-qc/0512095), [doi:10.1007/s11005-006-0091-5](https://doi.org/10.1007/s11005-006-0091-5)&rbrack;


[[!redirects globally hyperbolic Lorentzian manifolds]]

[[!redirects globally hyperbolic]]
[[!redirects globally hyperbolic Lorentzian manifold]]
[[!redirects globally hyperbolic pseudo-Riemannian manifold]]

[[!redirects globally hyperbolic spacetime]]
[[!redirects globally hyperbolic spacetimes]]


[[!redirects time orientation]]
[[!redirects time orientations]]



