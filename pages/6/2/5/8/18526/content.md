

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Algbraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What are called _advanced_ and _retarded propagators_ $\Delta_{A/R}$ are the [[Green functions]] for the [[wave operator]]/[[Klein-Gordon operator]] (hence "[[propagators]]") on a [[globally hyperbolic spacetime]] $(X,e)$ characterized by the fact that their [[support of a distribution|support]] as [[distributions]]

$$
  \Delta_{A/R}
  \in \mathcal{D}'(X \times X)
$$

is such that 

1. $(x,y) \in supp(\Delta_R)$ precisely if $x$ is in the [[causal future]] of $y$;

1. $(x,y) \in supp(\Delta_A)$ precisely if $x$ is in the [[causal past]] of $y$.

Written as [[generalized functions]] these satisfy

$$
  \Delta_A(x,y) = \Delta_R(y,x)
  \,.
$$

This implies in particular that 

1. the _[[causal propagator]]_, which is the difference of the two

   $$
     \Delta_S \coloneqq \Delta_R - \Delta_A
   $$

   is skew-symmetric in its arguments (reflecting the fact that this is the [[integral kernel]] for the [[Peierls-Poisson bracket]] for the [[free field|free]] [[scalar field]] on the given spacetime);

1. the _[[Dirac propagator]]_, which is the sum of the two

   $$
     \Delta_D \coloneqq \Delta_R + \Delta_A
   $$

   is symmetric in its arguments, reflecting the fact that this is the integral kernel for [[time-ordered products]] away from the [[diagonal]].

## Related concepts

[[!include propagators - table]]


## References

* F. Friedlander, _The Wave Equation on a Curved Space-Time_, Cambridge: Cambridge University Press, 1975

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))


* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009 

Review in the context of [[perturbative algebraic quantum field theory]] includes

* [[Katarzyna Rejzner]], sections 4.1 and 6.2.3 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([pdf](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))




[[!redirects advanced propagators]]

[[!redirects retarded propagator]]
[[!redirects retarded propagators]]

[[!redirects advanced Green function]]
[[!redirects advanced Green functions]]

[[!redirects retarded Green function]]
[[!redirects retarded Green functions]]

[[!redirects retarded and advanced Green functions]]
[[!redirects advanced and retarded Green functions]]

[[!redirects advanced Green's function]]
[[!redirects advanced Green's functions]]

[[!redirects retarded Green's function]]
[[!redirects retarded Green's functions]]

[[!redirects retarded and advanced Green's functions]]
[[!redirects advanced and retarded Green's functions]]