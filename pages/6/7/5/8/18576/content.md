

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

What is called the _Dirac propagator_ is the [[Green functions]] for the [[wave operator]]/[[Klein-Gordon operator]] (hence "[[propagator]]") on a [[globally hyperbolic spacetime]] $(X,e)$ which is the sum of the [[advanced propagator]] $\Delta_A$ and the [[retarded propagator]] $\Delta_R$


$$
  \Delta_D \coloneqq \Delta_R + \Delta_A
$$

Since $\Delta_A(x,y) = \Delta_R(y,x)$, this is symmetric in its arguments, 
reflecting the fact that this is the integral kernel for [[time-ordered products]] away from the [[diagonal]]. 

## Related concepts

[[!include propagators - table]]


## References

What is now called the _Dirac propagator_ was first considered in

* [[Paul Dirac]], _Classical theory of radiating electrons_, Proc. Roy. Soc.  A 167 (1983) 148-169

An overview of the [[Green functions]] of the [[Klein-Gordon operator]], hence of the [[Feynman propagator]], [[advanced propagator]], [[retarded propagator]], [[causal propagator]] etc. is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])


Discussion for general [[globally hyperbolic spacetimes]] includes

* F. Friedlander, _The Wave Equation on a Curved Space-Time_, Cambridge: Cambridge University Press, 1975

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))


* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009 

Review in the context of [[perturbative algebraic quantum field theory]] includes

* [[Katarzyna Rejzner]], sections 4.1 and 6.2.3 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([pdf](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects Dirac propagators]]
