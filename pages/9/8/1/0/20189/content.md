
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
 {#ExceptionalIsomorphism}

\begin{proposition}

There is an [[exceptional isomorphism]]

\[
  Spin(5) 
  \;\simeq\;
  Sp(2)
\]

between [[Spin(5)]] and the [[quaternionic unitary group]] $Sp(2) = U(2,\mathbb{H})$.

\end{proposition}
\begin{proof}

This is an indirect consequence of [[triality]], see e.g. [Čadek-Vanžura 97](#CadekVanzura97).  Alternatively, it can be shown as follows.

Let $V$ be a 4-dimensional complex vector space with an inner product and a compatible complex volume form.    As explained [here](https://ncatlab.org/nlab/show/Spin%286%29#ExceptionalIsomorphism), this structure can be used to define a conjugate-linear Hodge star operator on $\Lambda^2 V$ whose $+1$ and $-1$ eigenspaces, say $\Lambda_{\pm}^2 V$, are each 6-dimensional *real* inner product spaces.  Thus, the group $\mathrm{SU}(V)$ acts as linear transformations of $\Lambda_{\pm}^2 V$ that preserve the inner product, giving a homomorphism $\rho: \mathrm{SU}(V) \to \mathrm{O}(\Lambda_{\pm}^2 V)$.  In fact $\rho$ maps $\mathrm{SU}(V)$ in a 2-1 and onto way to $\mathrm{SO}(\Lambda_{\pm}^2 V)$.  Taking $V = \mathbb{C}^4$ this shows $\mathrm{SU}(4) \cong \mathrm{Spin}(6)$. 

Now suppose $V$ is additionally equipped with an complex symplectic structure, i.e. a nondegenerate skew-symmetric complex-bilinear form 
$J \in \Lambda^2 V$. The subgroup $\mathrm{Sp}(V)$ of $\mathrm{SU}(V)$ preserving this extra structure is isomorphic to the [[compact symplectic group]] $\mathrm{Sp}(2)$, which is also the [[quaternionic unitary group]].   This subgroup $\mathrm{Sp}(V)$ acts on $\Lambda_+^2 V$ and $\Lambda_-^2 V$ 
preserving $J \in \Lambda^2 V = \Lambda_+^2 V \oplus \Lambda_-^2 V$.  Since $\mathrm{Sp}(V)$ is compact, every invariant subspace has an invariant complement, so one or both of the 6-dimensional subspaces $\Lambda_+^2 V$ and $\Lambda_-^2 V$ must have a 5-dimensional subspace invariant under the action of $\mathrm{Sp}(V)$.  This shows that the double cover $\rho: \mathrm{SU}(4) \to \mathrm{SO}(6)$ restricts to a 2-1 homomorphism $\sigma : \mathrm{Sp}(2) \to \mathrm{SO}(5)$.   Since
$$   \dim(\mathrm{Sp}(2)) = 10 = \dim(\mathrm{SO}(5)) $$
the differential $d\sigma$, being injective, must also be surjective.  Thus $\sigma : \mathrm{Sp}(2) \to \mathrm{SO}(5)$ is actually a double cover.  Since $\mathrm{Sp}(2)$ is connected this implies $\mathrm{Sp}(2) \cong \mathrm{Spin}(5)$.
\end{proof}

\begin{remark}\label{SubgroupOfSL2H}
  There is hence a canonical [[subgroup]] inclusion into [[SL(2,H)]], equivalent to the subgroup inclusion into the [[Lorentz group|Lorentz]] [[spin group]] [[Spin(1,5)]]:

\begin{tikzcd}
  \mathrm{Spin}(5) 
    \ar[r, hook] 
    \ar[d, "\sim"{sloped}]
  & 
  \mathrm{Spin}(1,5)
    \ar[d, "\sim"{sloped}]
  \\
  \mathrm{U}(2,\mathbb{H}) 
    \ar[r, hook] 
  & 
  \mathrm{SL}(2,\mathbb{H})
\end{tikzcd}

See at *[[SL(2,H)]]*, the sections *[Unitary subgroup](SL2H#UnitarySubgroup)* and *[Relation to Spin(1,5)](SL2H#RelationToSpin51)*.
\end{remark}


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

### Homotopy groups

$\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ | $\pi_13$ | $\pi_14$ | $\pi_15$ | $\pi_16$ | $\pi_17$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
$\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $0$ | $\mathbb{Z}$ | $0$ | $0$ | $\mathbb{Z}_120$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_4\oplus\mathbb{Z}_2$ | $\mathbb{Z}_1680$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_40$

$\pi_18$ | $\pi_19$ | $\pi_20$ | $\pi_21$ | $\pi_22$ | $\pi_23$ |
|--|--|--|--|--|--|
$\mathbb{Z}_2520\oplus\mathbb{Z}_2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_2^3$ | $\mathbb{Z}_32\oplus\mathbb{Z}_2$ | $\mathbb{Z}_5280\oplus\mathbb{Z}_2^2$ | $\mathbb{Z}_2^3$

([Mimura & Toda 63](#MimuraToda63))

## Related concepts

* [[principal Sp(2)-bundle]]
* [[Spin(5,1)]]

[[!include low dimensional rotation groups -- table]]

linebreak

## References

* {#MimuraToda63} [[Mamoru Mimura]] and [[Hiroshi Toda]], _Homotopy Groups of SU(3), SU(4) and Sp(2)_ (1963), Journal of Mathematics of Kyoto University **3** (2), p. 217–250, [doi:10.1215/kjm/1250524818](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-3/issue-2/Homotopy-Groups-of-SU3-SU4-and-Sp2/10.1215/kjm/1250524818.full)

* {#Porteous95} [[Ian Porteous]], _Clifford Algebras and the Classical Groups_, Cambridge Studies in Advanced Mathematics, Cambridge University Press (1995)

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

* {#BottCattaneo98} [[Raoul Bott]], [[Alberto Cattaneo]], _Integral Invariants of 3-Manifolds_, J. Diff. Geom. **48** (1998) 91-133 &lbrack;[arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001), [doi:10.4310/jdg/1214460608](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-48/issue-1/Integral-invariants-of-3-manifolds/10.4310/jdg/1214460608.full)&rbrack;

* {#Pittie91} [[Harsh Pittie]], _The integral homology and cohomology rings of SO(n) and Spin(n)_, Journal of Pure and Applied Algebra Volume 73, Issue 2, 19 August 1991, Pages 105&#8211;153 (<a href="https://doi.org/10.1016/0022-4049(91)90108-E">doi:10.1016/0022-4049(91)90108-E</a>)

* {#Kalkkinen06} [[Jussi Kalkkinen]], _Global Spinors and Orientable Five-Branes_, JHEP 0609: 028, 2006 ([arXiv:hep-th/0604081](https://arxiv.org/abs/hep-th/0604081))


[[!redirects Sp(2)]]

[[!redirects Spin5]]