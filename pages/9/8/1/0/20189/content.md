
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The [[spin group]] in [[dimension]] 5.

## Properties

### Exceptional isomorphism

+-- {: .num_prop #ExceptionalIsoToSp2}
###### Proposition

There is an exceptional [[isomorphism]]

$$
  Spin(5) 
  \;\simeq\;
  Sp(2)
$$

between [[Spin(5)]] and the [[quaternionic unitary group]] $Sp(2) = U(2,\mathbb{H})$.

=--

This is an indirect consequence of [[triality]], see e.g. [Čadek-Vanžura 97](#CadekVanzura97))

### Action on quaternionic Hopf fibration


+-- {: .num_prop #Spin5EquivarianceOfQuaternionicHopfFibration}
###### Proposition
**([[Spin(5)]]-[[action|equivariance]] of [[quaternionic Hopf fibration]])**

Consider 

1. the [[Spin(5)]]-[[action]] on the [[4-sphere]] $S^4$ which is induced by the defining action on $\mathbb{R}^5$ under the identification $S^4 \simeq S(\mathbb{R}^5)$;

1. the [[Spin(5)]]-action on the [[7-sphere]] $S^7$ which is induced under the exceptional isomorphism $Spin(5) \simeq Sp(2) = U(2,\mathbb{H})$ (from Prop. \ref{ExceptionalIsoToSp2}) by the canonical left action of $U(2,\mathbb{H})$ on $\mathbb{H}^2$ via $S^7 \simeq S(\mathbb{H}^2)$.

Then the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$ is [[equivariant]] with respect to these [[actions]].

=--

This is almost explicit in [Porteous 95, p. 263](#Porteous95)


\begin{center}
\begin{imagefromfile}
  "file_name": "Spin5OnHopfH.jpg",
  "width": 280
\end{imagefromfile}
\end{center}

### Cohomology

+-- {: .num_prop}
###### Proposition

The [[integral cohomology|integral]] [[cohomology ring]] of the [[classifying space]] $B Spin(5)$ is spanned by two generators

1. the [[first fractional Pontryagin class]] $\tfrac{1}{2}p_1$

1. the [[linear combination]] $\tfrac{1}{2}p_2 - \tfrac{1}{2}(p_1)^2$ of the half the [[second Pontryagin class]] with half the [[cup product]]-square of the [[first Pontryagin class]]:

$$
  H^\bullet
  \big(
    B Spin(5), \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}
  \left[
    \tfrac{1}{2}p_1,
    \;
    \tfrac{1}{2}p_2 - \tfrac{1}{2}(p_1)^2 
  \right]
$$

=--

(e.g. [Kalkkinen 06, Section 3](#Kalkkinen06))

+-- {: .num_prop }
###### Proposition


Let 

$$
  \array{
    S^4
    &\longrightarrow& 
    B Spin(4)
    \\
    &&
    \big\downarrow^{\mathrlap{\pi}}
    \\
    && 
    B Spin(5)
  }
$$

be the [[spherical fibration]] of [[classifying spaces]] induced from the canonical inclusion of [[Spin(4)]] into [[Spin(5)]] and using that the [[4-sphere]] is equivalently the [[coset space]] $S^4 \simeq Spin(5)/Spin(4)$ ([this Prop.](sphere#nSphereAsCosetSpace)).

Then the [[fiber integration]] of the odd [[cup product|cup powers]] $\chi^{2k+1}$ of the [[Euler class]] $\chi \in H^4\big( B Spin(4), \mathbb{Z}\big)$ (see [this Prop](Spin4#IntegralCohomologyOfClassifyingSpace))  are proportional to [[cup product|cup powers]] of the [[second Pontryagin class]] 

$$
  \pi_\ast
  \left(
    \chi^{2k+1}
  \right)
  \;=\;
  2 \big( p_2 \big)^k 
  \;\;\in\;\;
  H^4\big( B Spin(5), \mathbb{Z} \big) 
  \,,
$$

for instance

$$
  \begin{aligned}
    \pi_\ast
    \big(
      \chi
    \big)
    & = 
    2 
    \\
    \pi_\ast
    \left(
      \chi^3
    \right)
    & = 
    2 p_2 
    \\
    \pi_\ast
    \left(
      \chi^5
    \right)
    & = 
    2 (p_2)^2 
  \end{aligned}
    \;\;\in\;\;
    H^4\big( B Spin(5), \mathbb{Z} \big) 
  \,;
$$

while the [[fiber integration]] of the even [[cup product|cup powers]] $\chi^{2k}$ vanishes

$$
  \pi_\ast
  \left(
    \chi^{2k}
  \right)
  \;=\;
  0
  \;\;\in\;\;
  H^4\big( B Spin(5), \mathbb{Z} \big) 
  \,.
$$

 
=--

([Bott-Cattaneo 98, Lemma 2.1](#BottCattaneo98))

\linebreak

## Related concepts

[[!include low dimensional rotation groups -- table]]

linebreak

## References

* {#Porteous95} [[Ian Porteous]], _Clifford Algebras and the Classical Groups_, Cambridge Studies in Advanced Mathematics, Cambridge University Press (1995)

* {#CadekVanzura97} [[Martin Čadek]], Jiří Vanžura, _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

* {#BottCattaneo98} [[Raoul Bott]], [[Alberto Cattaneo]], _Integral Invariants of 3-Manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

* {#Kalkkinen06} Jussi Kalkkinen, _Global Spinors and Orientable Five-Branes_, JHEP0609:028, 2006 ([arXiv:hep-th/0604081](https://arxiv.org/abs/hep-th/0604081))

[[!redirects Sp(2)]]

[[!redirects Spin5]]