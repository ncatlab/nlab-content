
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The archetypical example of a [[mechanical system]] is a [[particle]] propagating on a [[manifold]] $\Sigma$. The [[phase space]] of this particular system happens to be canonically identified with the [[cotangent bundle]] $X \coloneqq T^* \Sigma$ of $\Sigma$. Here the [[covector]] $(x,p)$ in $X$ over a point $x \in \Sigma$ is physically interpretd as describing a [[state]] of the system where the particle is at position $x \in \Sigma$ and has [[momentum]] (essentially: speed) as given by $p$. 

Therefore locally for [[coordinate patch]] $\phi : \mathbb{R}^{2n} \simeq \mathbb{R}^n \times \mathbb{R}^n \to T^* \Sigma$ the $2n$-canonical coordinates of the [[Cartesian space]] $\mathbb{R}^n$ are naturally thought of as decomposed into $n$ "canonical coordinates" on the first $n$ factors and a set of "canonical momenta", being the canonical coordinates on the second $\mathbb{R}^n$-factor.

Notice that "canonical" here refers (at best) to the canonical coordinates of the [[Cartesian space]] $\mathbb{R}^n$ _once $\phi$ has been chosen_. The choice of $\phi$ however is arbitrary. Hence, despite the (standard) term, there is nothing much canonical about these "canonical coordinates" and "canonical momenta".

In general, the [[phase space]] of a [[physical system]] is a [[symplectic manifold]] which need not be a [[cotangent bundle]] as for the [[particle]] [[sigma-model]]. 

But _locally_ over a [[coordinate patch]] every [[symplectic manifold]] looks like $\mathbb{R}^{2n} \simeq \mathbb{R}^n \times \mathbb{R}^n$ such that under this identification the [[symplectic form]] reads $\sum_{i = 1}^n d q_i \wedge d p^i$, for $\{q_i\}$ the canonical [[coordinates]] on one $\mathbb{R}^n$ and $\{p^i\}$ for the other. 

Therefore generally, in the context of [[mechanics]], with such a local  identification one calls _$p^i$_ the **canonical momentum** of the coordinate (or sometimes "canonical coordinate") $q_i$.

Globally the notion of canonical momenta may not exist at all. The notion that does exist globally is that of a [[polarization]] of a symplectic manifold. See there for more details.

## Properties

### On a symplectic vector space

Discussion of how there is a flat connection on the bundle of [[spaces of quantum states]] over the space of choices of [[polarizations]] of a [[symplectic vector space]] and how this reproduces the traditional relation between canonical coordinates and canonical momenta by [[Fourier transform]] is in ([Kirwin-Wu 04](#KirwinWu04)).

## Related concepts

* [[momentum]]

* [[canonical coordinates]], [[canonical transformation]]

* [[phase space]]

* [[Hamiltonian mechanics]]

* [[geometric quantization]]

## References

* [[Marc Henneaux]], [[Claudio Teitelboim]], §1.1.1 in: _[[Quantization of Gauge Systems]]_, Princeton University Press (1992) &lbrack;[ISBN:9780691037691](https://press.princeton.edu/books/paperback/9780691037691/quantization-of-gauge-systems), [jstor:j.ctv10crg0r](https://www.jstor.org/stable/j.ctv10crg0r)&rbrack;


* {#KirwinWu04} William Kirwin, Siye Wu, _Geometric Quantization, Parallel Transport and the Fourier Transform_,  	Comm. Math. Phys. 266 (2006), no. 3, pages 577 -- 594 ([arXiv:math/0409555](http://arxiv.org/abs/math/0409555))
 

[[!redirects canonical momenta]]
