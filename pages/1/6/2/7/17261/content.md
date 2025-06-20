
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[ordinary homology]]/[[ordinary cohomology]] represented as [[singular homology]]/[[singular cohomology]], _Kronecker pairing_ refers to the defining pairing of a [[chain]] with a [[cochain]]. 

More generally, in [[generalized (Eilenberg-Steenrod) cohomology]]/[[generalized homology]] represented by a [[ring spectrum]] $E$, then the _Kronecker pairing_ 
is a canonical pairing of the $E$-[[generalized cohomology]] [[cohomology group|groups]] $E^\bullet(X)$ with the $E$-[[generalized homology]] groups $E_\bullet(X)$ of suitable spaces ([[homotopy types]]/[[spectra]]) $X$

$$
  \langle-,-\rangle_X 
    \;\colon\; 
   E^{\bullet_1}(X) \otimes E_{\bullet_2}(X) \longrightarrow \pi_{\bullet_2-\bullet_1}(E)
  \,.
$$ 

The combination of the Kronecker pairing with a [[diagonal]] map yields the [[cap product]] pairing in generalized (co-)homology.


If $E_\bullet(X)$ is a [[projective module|projective]] [[graded module]] over the [[graded ring]] $\pi_\bullet(E)$ then the [[adjunct]] 

$$
  E^0(X) \longrightarrow Hom_{\pi_\bullet(E)}(E_\bullet(X), \pi_\bullet(E))
$$ 

of the Kronecker pairing is an [[isomorphism]] and hence exhibits $E$-[[generalized cohomology]] as the $\pi_\bullet(E)$-[[linear dual]] of the $E$-[[generalized homology]] of $X$; an instance of a [[universal coefficient theorem]] for generalized (co-)homology (prop. \ref{KroneckerPairingAdjunctIsIsomorphism} below).

On [[CW-complexes]] $X$ of [[finite number|finite]] [[dimension]], the Kronecker pairing induces a pairing of the corresponding [[Atiyah-Hirzebruch spectral sequences]] (prop. \ref{KroneckerPairingOnAHSS} below).


## Definition

Let $E$ be a [[ring spectrum]] with product denoted $\mu \colon E \wedge E \longrightarrow E$. Let $X,Y$ be any [[spectra]].

+-- {: .num_defn #KroneckerPairing}
###### Definition

Given $[f] \in E^k(X)$ with representative $f \colon X \longrightarrow \Sigma^k E$ and given $[w] \in E_{n+k}(X \wedge Y)$ with representative $w \colon S^{n+k} \longrightarrow E \wedge X \wedge Y$, then their _Kronecker pairing_ is the element

$$
  \langle f,w\rangle \in E_n(Y)
$$

represented by the composite

$$
  S^{k+n} 
    \stackrel{w}{\longrightarrow}
  E\wedge X \wedge Y
    \stackrel{id_E \wedge f \wedge id_Y}{\longrightarrow}
  E \wedge \Sigma^k E \wedge Y
   \stackrel{\Sigma^k \mu \wedge id_Y}{\longrightarrow}
  \Sigma^k E \wedge Y
  \,.
$$

This yields a homomorphism of [[graded abelian groups]]

$$
  \langle-,-\rangle
   \;\colon\;
  E^{\bullet_1}(X)
   \otimes
  E_{\bullet_2}(X \wedge Y)
   \longrightarrow
  E_{\bullet_2-\bullet_1}(Y)
  \,.
$$

(and similarly for $Y$ on the other side...)


For $Y = \mathbb{S}$ this is 

$$
  \langle-,-\rangle
   \;\colon\;
  E^{\bullet_1}(X)
   \otimes
  E_{\bullet_2}(X)
   \longrightarrow
  \pi_{\bullet_2-\bullet_1}(E)
  \,.
$$


=--

(e.g. [Kochman 96, (4.2.1)](#Kochman96), [Schwede 12, construction 6.13](#Schwede12))



## Properties


### Universal coefficient theorem
 {#UniversalCoefficientTheorem}

+-- {: .num_prop #KroneckerPairingAdjunctIsIsomorphism}
###### Proposition

If $E_\bullet(X)$ is a [[projective module|projective]] [[graded module]] over the [[graded ring]] $\pi_\bullet(E)$ then the [[adjunct]]

$$
  \pi_0[X, E \wedge Y]
  \longrightarrow
  Hom_{\pi_\bullet(E)}( E_\bullet(X), E_\bullet(Y) )
$$
$$
  f \mapsto \langle f,-\rangle
$$

of the Kronecker pairing, def. \ref{KroneckerPairing}, is an [[isomorphism]]. 

=--

(e.g. [Schwede 12, chapter II, prop.6.20](#Schwede12))

+-- {: .proof}
###### Proof idea

By the formula for [[adjuncts]], the morphism factors through the [[free-forgetful adjunction]] for $E$-[[module spectra]]

$$
  \pi_0[X, E \wedge Y]
    \stackrel{\simeq}{\longrightarrow}
  \pi_0[E\wedge X, E \wedge Y]_{E Mod}
    \stackrel{\pi_\bullet}{\longrightarrow}
  Hom_{\pi_\bullet}( E_\bullet(X), E_\bullet(Y) )
  \,.
$$

Hence one is reduced to showing that under the given conditions the second morphis is an iso. (...)

=--

This may be regarded as a [[universal coefficient theorem]] ([Adams 74, part III, around prop. 13.5](#Adams74)).

For $Y = \mathbb{S}$ prop. \ref{KroneckerPairingAdjunctIsIsomorphism} gives:

+-- {: .num_example}
###### Example

If $E_\bullet(X)$ is a [[projective module|projective]] [[graded module]] over the [[graded ring]] $\pi_\bullet(E)$ then the [[adjunct]]

$$
  E^0(X)
  \longrightarrow
  Hom_{\pi_\bullet(E)}( E_\bullet(X), \pi_\bullet(E) )
$$
$$
  f \mapsto \langle f,-\rangle
$$

of the Kronecker pairing, def. \ref{KroneckerPairing}, is an [[isomorphism]]. 

=--

### Pairing on Atiyah-Hirzebruch spectral sequences

+-- {: .num_prop #KroneckerPairingOnAHSS}
###### Proposition

For $E$ a [[ring spectrum]] and $X$ a [[CW complex]] of [[finite number|finite]] [[dimension]], then the Kronecker pairing $\langle -,-\rangle \colon E^\bullet(X)\otimes E_\bullet(X)\to \pi_\bullet(E)$ of def. \ref{KroneckerPairing} passes to a page-wise pairing of the corresponding [[Atiyah-Hirzebruch spectral sequences]] for $E$-cohomology/homology

$$
  \langle-,-\rangle_r
  \;\colon\;
  \mathcal{E}_r^{n,-s}
  \otimes
  \mathcal{E}^r_{n,t}
  \longrightarrow
  \pi_{s+t}(E)
$$

such that

1. on the $\mathcal{E}_2$-page this restricts to the Kronecker pairing for [[ordinary cohomology]]/[[ordinary homology]] with [[coefficients]] in $\pi_\bullet(E)$;

1. the [[differentials]] act as [[derivations]] 

   $$
     \langle d_r(-),-\rangle = \langle -, d^r(-)\rangle
     \,,
   $$

1. The pairing on the $\mathcal{E}_\infty$-page is compatible with the Kronecker pairing. 

=--

([Kochman 96, prop. 4.2.10](#Kochman96))


## References

Presumeably named after [[Leopold Kronecker]].

* {#Adams74} [[Frank Adams]], Part III, section 13 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Kochman96} [[Stanley Kochman]], (4.2.1) and prop. 4.2.10 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Schwede12} [[Stefan Schwede]], chapter II, section 6 (Construction 6.13) of _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))
