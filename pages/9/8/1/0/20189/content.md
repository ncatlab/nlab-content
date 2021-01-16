
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

There is an [[exceptional isomorphism]]

$$
  Spin(5) 
  \;\simeq\;
  Sp(2)
$$

between [[Spin(5)]] and the [[quaternionic unitary group]] $Sp(2) = U(2,\mathbb{H})$.

=--

This is an indirect consequence of [[triality]], see e.g. [Čadek-Vanžura 97](#CadekVanzura97).  Alternatively, it can be shown as follows.

Let $V$ be a 4-dimensional complex vector space with an inner product and a compatible complex volume form.    As explained [here](https://ncatlab.org/nlab/show/Spin%286%29#ExceptionalIsomorphism), this structure can be used to define a conjugate-linear Hodge star operator on $\Lambda^2 V$ whose $+1$ and $-1$ eigenspaces, say $\Lambda_{\pm}^2 V$, are each 6-dimensional *real* inner product spaces.  Thus, the group $\mathrm{SU}(V)$ acts as linear transformations of $\Lambda_{\pm}^2 V$ that preserve the inner product, giving a homomorphism $\rho: \mathrm{SU}(V) \to \mathrm{O}(\Lambda_{\pm}^2 V)$.  In fact $\rho$ maps $\mathrm{SU}(V)$ in a 2-1 and onto way to $\mathrm{SO}(\Lambda_{\pm}^2 V)$.  Taking $V = \mathbb{C}^4$ this shows $\mathrm{SU}(4) \cong \mathrm{Spin}(6)$. 

Now suppose $V$ is additionally equipped with an complex symplectic structure, i.e. a nondegenerate skew-symmetric complex-bilinear form 
$J \in \Lambda^2 V$. The subgroup $\mathrm{Sp}(V)$ of $\mathrm{SU}(V)$ preserving this extra structure is isomorphic to the [[compact symplectic group]] $\mathrm{Sp}(2)$, which is also the [[quaternionic unitary group]].   This subgroup $\mathrm{Sp}(V)$ acts on $\Lambda_+^2 V$ and $\Lambda_-^2 V$ 
preserving $J \in \Lambda^2 V = \Lambda_+^2 V \oplus \Lambda_-^2 V$.  Since $\mathrm{Sp}(V)$ is compact, every invariant subspace has an invariant complement, so one or both of the 6-dimensional subspaces $\Lambda_+^2 V$ and $\Lambda_-^2 V$ must have a 5-dimensional subspace invariant under the action of $\mathrm{Sp}(V)$.  This shows that the double cover $\rho: \mathrm{SU}(4) \to \mathrm{SO}(6)$ restricts to a 2-1 homomorphism $\sigma : \mathrm{Sp}(2) \to \mathrm{SO}(5)$.   Since
$$   \dim(\mathrm{Sp}(2)) = 10 = \dim(\mathrm{SO}(5)) $$
the differential $d\sigma$, being injective, must also be surjective.  Thus $\sigma : \mathrm{Sp}(2) \to \mathrm{SO}(5)$ is actually a double cover.  Since $\mathrm{Sp}(2)$ is connected this implies $\mathrm{Sp}(2) \cong \mathrm{Spin}(5)$.

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

This is a special case of the general statement in [Pittie 91](#Pittie91), see e.g. [Kalkkinen 06, Section 3](#Kalkkinen06)).

\linebreak

+-- {: .num_prop  #FiberIntegrationOfCupPowersOfChiOver4Sphere}
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


### Coset spaces

[[!include coset space structure on n-spheres -- table]]



### $G$-Structure and exceptional geometry


[[!include Spin(8)-subgroups and reductions -- table]]


\linebreak

## Related concepts

* [[Spin(5,1)]]

[[!include low dimensional rotation groups -- table]]

linebreak

## References

* {#Porteous95} [[Ian Porteous]], _Clifford Algebras and the Classical Groups_, Cambridge Studies in Advanced Mathematics, Cambridge University Press (1995)

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

* {#BottCattaneo98} [[Raoul Bott]], [[Alberto Cattaneo]], _Integral Invariants of 3-Manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

* {#Pittie91} [[Harsh Pittie]], _The integral homology and cohomology rings of SO(n) and Spin(n)_, Journal of Pure and Applied Algebra Volume 73, Issue 2, 19 August 1991, Pages 105&#8211;153 (<a href="https://doi.org/10.1016/0022-4049(91)90108-E">doi:10.1016/0022-4049(91)90108-E</a>)

* {#Kalkkinen06} [[Jussi Kalkkinen]], _Global Spinors and Orientable Five-Branes_, JHEP 0609: 028, 2006 ([arXiv:hep-th/0604081](https://arxiv.org/abs/hep-th/0604081))

[[!redirects Sp(2)]]

[[!redirects Spin5]]