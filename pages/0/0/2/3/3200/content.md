
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given a linear [[differential operator]] (ordinary or partial) $P$ on a [[domain]] $M\subset\mathbb{R}^n$ or a [[manifold]] $M$, one can consider both the homogeneous [[differential equation]] $P f = 0$ and the nonhomogeneous equation of the form $P f = g$ where $g$ is a given nonhomogeneous term. If $g$ is a [[delta distribution]] and the boundary conditions are given, then the [[generalized solution of a PDE|generalized solution]] of the nonhomogenous equation

$$
  P f = \delta
$$

is called the **fundamental solution** for $P$; alternative names like __Green function__ and __function of influence__ are also used. A particular solution of the nonhomogeneous equation for some other $g$ can be obtained by calculating the [[convolution]] with the fundamental solution. (Compare the fact that the delta distribution is the [[identity element]] for convolution.)

As a first step one may also considers searching for $f$ such that $P f - \delta$ is a smooth function, the solution to the latter problem is called a [[parametrix]].

## Examples

### Propagators for free fields

The Green functions for the [[wave operator]]/[[Klein-Gordon operator]] are known as the _[[propagators]]_ for [[free fields]] in [[field theory]]:

[[!include propagators - table]]

## Properties and results

(Malgrange-Ehrenpreis theorem) If $D$ is a differential operator with constant coefficients in $n$-dimensional real space $\mathbf{R}^n$ then the fundamental solution exists in the Schwarz space $\mathcal{S}'(\mathbf{R}^n)$. The proof is using Fourier transform which sends the equation for the fundamental solution into an algebraic equation for the Fourier transform of the solution seeked; the algebraic equation requires inversion and one checks that the conditions for finding the inverse in the Schwarz space are satisfied. 

## Related concepts

* [[Feynman propagator]]

* [[Dirac propagator]]

* [[parametrix]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 3.3 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


* [[Sergiu Klainerman]], chapter 4 of _Lecture notes in analysis_, 2011 ([pdf](https://web.math.princeton.edu/~seri/homepage/courses/Analysis2011.pdf))


* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], section 2 and 3 of _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))


* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009 

* {#Khavkine14} [[Igor Khavkine]], section 2 of _Covariant phase space, constraints, gauge and the Peierls formula_, Int. J. Mod. Phys. A, 29, 1430009 (2014) ([arXiv.1402.1282](https://arxiv.org/abs/1402.1282))


* Wikipedia, _[Fundamental solution](http://en.wikipedia.org/wiki/Fundamental_solution)_

* Wikipedia, _[Green's functions](http://en.wikipedia.org/wiki/Green%27s_function)_

[[!redirects fundamental solutions]]

[[!redirects Green function]]
[[!redirects Green functions]]

[[!redirects Green's function]]
[[!redirects Green's functions]]


[[!redirects function of influence]]
[[!redirects functions of influence]]

[[!redirects Green operator]]
[[!redirects Green operators]]
