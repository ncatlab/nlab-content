
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For [[sequential spectra]] and for [[highly structured spectra]] such as [[symmetric spectra]] and [[orthogonal spectra]], the [[functor]] $(-)_n$ which picks their $n$th component space, for any $n \in \mathbb{N}$, has a [[left adjoint]] $F_n$. 

A structured spectrum in the image of this [[free functor]] is called a _free symmetric spectrum_ or _free orthogonal spectrum_, respectively ([Hovey-Shipley-Smith 00, def. 2.2.5](HoveyShipleySmith00), [Mandell-May-Schwede-Shipley 01, section 8](#MandellMaySchwedeShipley01), [Schwede 12, example 3.20](#Schwede12)). 

For a general abstract account see at _[[Model categories of diagram spectra]]_ the section _[Free spectra](Model+categories+of+diagram+spectra#FreeSpectra)_.


+-- {: .num_prop #ExplicitFormOfFreeSpectra}
###### Proposition

Explicitly, these free spectra look as follows:

For [[sequential spectra]]: $(F_n K)_q = K \wedge S^{q-n}$;

for [[orthogonal spectra]]: $(F_n K)_q = O(q)_+ \wedge_{O(q-n)} K \wedge S^{q-n}$;

for [[symmetric spectra]]: $(F_n K)_q = \Sigma(q)_+ \wedge_{\Sigma(q-n)} K \wedge S^{q-n}$.

=--


## Properties

For $n = 0$ the free construction is [[isomorphism|isomorphic]] to the corresponding structured [[suspension spectrum]] construction: $F_0 \simeq \Sigma^\infty$. Generally, the [[stable homotopy type]] of $F_n K$ is that of $\Omega^n (\Sigma^\infty K)$ ([Schwede 12, example 4.35](#Schwede12)).




## References

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))


* {#MandellMaySchwedeShipley01} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))

* {#Schwede12} [[Stefan Schwede]], section I.3 of _[[Symmetric spectra]]_ (2012)

[[!redirects free spectra]]

[[!redirects free structured spectrum]]
[[!redirects free structured spectra]]

[[!redirects free symmetric spectrum]]
[[!redirects free symmetric spectra]]

[[!redirects free orthogonal spectrum]]
[[!redirects free orthogonal spectra]]

