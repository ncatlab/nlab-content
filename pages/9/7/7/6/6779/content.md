
> Not to be confused with the [[Hurwitz theorem]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The first nonzero [[homotopy group]] and [[ordinary homology|ordinary]]/[[singular homology]] [[homology group|group]] of a [[simply-connected topological space]] occur in the same dimension and are [[isomorphism|isomorphic]].


## Hurewicz homomorphism
 {#HurewiczHomomorphismSection}

### For topological spaces

+-- {: .num_defn #HurewiczHomomorphism}
###### Definition 
**(Hurewicz homomorphism)**

For $(X,x)$ a [[pointed object|pointed]] [[topological space]], the **Hurewicz homomorphism** is the [[function]]

$$
  \Phi : \pi_k(X,x) \to H_k(X)
$$

from the $k$th [[homotopy group]] of $(X,x)$ to the $k$th [[singular homology]] group defined by sending

$$
  \Phi : (f : S^k \to X)_{\sim} \mapsto f_*[S_k]
$$

a representative singular $k$-sphere $f$ in $X$ to the push-forward along $f$ of the [[fundamental class]] $[S_k] \in H_k(S^k) \simeq \mathbb{Z}$.


=--

+-- {: .num_remark}
###### Remark

The Hurewicz homomorphism is a [[natural transformation]] between

$$
  \Phi : \pi_k(-) \to H_k(-)
$$

between [[functors]] $Top^{*/} \to $ [[Ab]].

=--

### For spectra
 {#ForSpectra}

The above construction has an immediate analog in [[stable homotopy theory]]:

For $R$ a [[ring]], its [[Eilenberg-MacLane spectrum]] is an [[E-infinity ring]] and hence receives a canonical [[unit]] homomorphism $\mathbb{S} \longrightarrow H R$ from the [[sphere spectrum]].

Under [[smash product]] and passing to [[stable homotopy group]], this induces a [[natural transformation]] from [[stable homotopy groups]] of $X$ (its [[stable homotopy homology theory]]) to [[ordinary homology]] of $X$ with [[coefficients]] in $R$:

$$
  \pi^{st}_\bullet(X)
  \;\simeq\;
  \pi_\bullet( \mathbb{S} \wedge X_+ )
  \longrightarrow
  \pi_\bullet( H R \wedge X_+ )
  \simeq
  H_\bullet(X,R)
  \,.
$$

If here the [[Eilenberg-MacLane spectrum]] $H R$ is replaced by any other [[E-infinity ring spectrum]] the analogous construction is called the _[[Boardman homomorphism]]_.

## Hurewicz theorem

+-- {: .num_theorem}
###### Theorem

If a [[topological space]] (or [[infinity-groupoid]]) $X$ is [[n-connected object in an (infinity,1)-topos|(n-1)-connected]] for $n \geq 2$ then the [[Hurewicz homomorphism]], def. \ref{HurewiczHomomorphism} 

$$
  \Phi  
  \;\colon\; 
  \pi_n(X,x) 
    \longrightarrow 
  H_n(X)
$$

is an [[isomorphism]].

=--

A proof is spelled out for instance with theorem 2.1 in ([Hutchings](#Hutchings)).

+-- {: .num_remark}
###### Remark

With the [[universal coefficient theorem]] a corresponding statement follows for the [[cohomology group]] $H^n(X,A)$.

=--


## Related concepts

* [[Boardman homomorphism]]

* [[Hopf degree theorem]]

* The _[[Adams spectral sequence]]_ is a vast generalization of the computation of [[homotopy groups]] from [[cohomology groups]] via the Hurewicz theorem.


## References

Named after [[Witold Hurewicz]].

The basic statement is for instance in

* [[Allen Hatcher]], _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html))

Lecture notes:

* {#Hutchings} [[Michael Hutchings]], _Introduction to higher homotopy groups and obstruction theory_ (2011) ([pdf](http://math.berkeley.edu/~hutching/teach/215b-2011/homotopy.pdf))

* {#Kobin16} Andrew Kobin, Section 7.3 of: _Algebraic Topology_, 2016 ([[KobinAT2016.pdf:file]])

For discussion in [[stable homotopy theory]] modeled on [[symmetric spectra]] is in 

* {#Schwede12} [[Stefan Schwede]], part II, prop. 6.30 of _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

See also

* wikipedia, _[Hurewicz theorem](http://en.wikipedia.org/wiki/Hurewicz_theorem)_

In the generality of the [[Boardman homomorphism]]:

* [[Frank Adams]], Part II.6 of _[[Stable homotopy and generalised homology]]_, 1974

Discussion of the stable Hurewicz homomorphism includes

* [[Akhil Mathew]], _Torsion exponents in stable homotopy and the Hurewicz homomorphism_, Algebr. Geom. Topol. 16 (2016) 1025-1041 ([arXiv:1501.07561](https://arxiv.org/abs/1501.07561))

Proof of the [[Hurewicz theorem]] in [[homotopy type theory]], hence in general [[(∞,1)-toposes]]:

* [[Daniel Christensen]], [[Luis Scoccola]], _The Hurewicz theorem in Homotopy Type Theory_ ([arXiv:2007.05833](https://arxiv.org/abs/2007.05833))



[[!redirects Hurewicz theorem]]
[[!redirects Hurewicz Theorem]]
[[!redirects Hurewicz' theorem]]
[[!redirects Hurewicz' Theorem]]
[[!redirects Hurewicz’ theorem]]
[[!redirects Hurewicz’ Theorem]]
[[!redirects Hurewicz\' theorem]]
[[!redirects Hurewicz\' Theorem]]
[[!redirects Hurewicz's theorem]]
[[!redirects Hurewicz's Theorem]]
[[!redirects Hurewicz’s theorem]]
[[!redirects Hurewicz’s Theorem]]
[[!redirects Hurewicz\'s theorem]]
[[!redirects Hurewicz\'s Theorem]]

[[!redirects Hurewicz homomorphism]]
