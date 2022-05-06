
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For a [[natural number]] $n \in \mathbb{N}$, the **unitary group** $U(n)$ is the [[group]] of [[isometry|isometries]] of the $n$-dimensional complex [[Hilbert space]] $\mathbb{C}^n$.   This is canonically identified with the group of $n \times n$ [[unitary matrices]].


More generally, for a Hilbert space $\mathcal{H}$, $U(\mathcal{H})$ is the group of [[unitary operator]]s on that Hilbert space. For the purposes of studying unitary representations of Lie groups, the topology is chosen to be the [[operator topology|strong operator topology]], although other topologies on $U(\mathcal{H})$ are frequently considered for other purposes. 

## Properties

The unitary groups are naturally [[topological group]]s and [[Lie groups]] (infinite dimensional if $\mathcal{H}$ is infinite dimensional).

+-- {: .num_prop #UnitaryGroupIsCompact}
###### Proposition

The unitary group $U(n)$ is [[compact topological space]], hence in particular a [[compact Lie group]].
 
=--


### Homotopy groups
 {#HomotopyGroups}

+-- {: .num_prop #InclusionOfUnitaryGroupnIntoUnitaryGroupnPlusIneIsnMinus1Equivalence}
###### Proposition

For $n,N \in \mathbb{N}$, $n \leq N$, then the canonical inclusion of unitary groups

$$
  U(n) \hookrightarrow U(N)
$$

is a [[n-equivalence|2n-equivalence]], hence induces an [[isomorphism]] on [[homotopy groups]] in degrees $\lt 2n$ and a [[surjection]] in degree $2n$.

=--

+-- {: .proof}
###### Proof

Consider the [[coset]] [[quotient]] [[projection]]

$$
  U(n)
  \longrightarrow
  U(n+1)
  \longrightarrow
  U(n+1)/U(n)
  \,.
$$

By prop. \ref{UnitaryGroupIsCompact} and by [this corollary](coset#QuotientProjectionForCompactLieSubgroupIsPrincipal), the projection $U(n+1)\to U(n+1)/U(n)$ is a [[Serre fibration]]. Furthermore, example \ref{nSphereAsUnitaryCosetSpace} identifies the [[coset]] with the [[n-sphere|(2n+1)-sphere]] 

$$
  S^{2n+1}\simeq U(n+1)/U(n)
  \,.
$$

Therefore the [[long exact sequence of homotopy groups]] of the [[fiber sequence]] $U(n)\to U(n+1) \to S^{2n+1}$ is of the form

$$
  \cdots
    \to
  \pi_{\bullet+1}(S^{2n+1})
    \longrightarrow
  \pi_\bullet(U(n))
    \longrightarrow
  \pi_\bullet(U(n+1))
    \longrightarrow
  \pi_\bullet(S^{2n+1})
   \to
  \cdots
$$

Since $\pi_{\leq 2n}(S^{2n+1}) = 0$, this implies that 

$$
  \pi_{\lt 2n}(U(n))
    \overset{\simeq}{\longrightarrow}
  \pi_{\lt 2n}(U(n+1))
$$

is an isomorphism and that

$$
  \pi_{2n}(U(n))
    \longrightarrow
  \pi_{2n}(U(n+1))
$$

is surjective. Hence now the statement follows by induction over $N-n$.


=--

It follows that the [[homotopy groups]] $\pi_k(U(n))$ are independent of $n$ for $n \gt \frac{k}{2}$ (the "stable range"). So if $U = \underset{\longrightarrow}{\lim}_n U(n)$, then $\pi_k(U(n)) = \pi_k(U)$. By [[Bott periodicity]] we have

$$
\array{
\pi_{2k+0}(U) &= 0\\
\pi_{2k+1}(U) &= \mathbb{Z}.
}
$$

In the unstable range for low $n$ they instead start out as follows 

| $G$ | $\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ | $\pi_13$ | $\pi_14$ | $\pi_15$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $U(1)$ | $\mathbb{Z}$ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| $U(2)$ | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_{12}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_3$ | $\mathbb{Z}_{15}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2^{\oplus 2}$ | $\mathbb{Z}_3\oplus\mathbb{Z}_{12}$ | $\mathbb{Z}_2^{\oplus 2}\oplus\mathbb{Z}_{84}$ | $\mathbb{Z}_2\oplus\mathbb{Z}_2$ |
| $U(3)$ | " | " | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_6$ | 0 | $\mathbb{Z}_{12}$ | $\mathbb{Z}_3$ | $\mathbb{Z}_{30}$ | $\mathbb{Z}_4$ | $\mathbb{Z}_{60}$ | $\mathbb{Z}_6$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{84}$ | $\mathbb{Z}_{36}$ |
| $U(4)$ | " | " | " | " | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{24}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{120}$ | $\mathbb{Z}_4$ | $\mathbb{Z}_{60}$ | $\mathbb{Z}_4$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{1680}$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{72}$ |
| $U(5)$ | " | " | " | " | " | " | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{120}$ | 0 | $\mathbb{Z}_{360}$ | $\mathbb{Z}_4$ | $\mathbb{Z}_{1680}$ | $\mathbb{Z}_6$ |
| $U(6)$ | " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{720}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{5040}$ | $\mathbb{Z}_6$ |
| $U(7)$ | " | " | " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{5040}$ | 0 |
| $U(8)$ | " | " | " | " | " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}$ |

Due to the [[unitary group#SUn | relation to the special unitary group]], the higher homotopy groups of $U(n)$ and $SU(n)$ agree. The $U(2)$ row can be found using the fact that $SU(2)$ is diffeomorphic to $S^3$. The $U(3)$ row can be found using [Mimura-Toda 63](#MimuraToda63). Otherwise the table is given in columns $\pi_k$, $k= 6,\ldots, 15$, and in rows $U(n)$, $n=4,\ldots,8$, by the [[Encyclopedic Dictionary of Mathematics]], Table 6.VII in Appendix A.

### In infinite dimension

A good discussion about the various topologies one might place on $U(\mathcal{H})$ and how they all agree and make $U(\mathcal{H})$ a [[Polish space|Polish]] group is in ([Espinoza-Uribe](#EspinozaUribe)).

+-- {: .num_prop}
###### Proposition

For $\mathcal{H}$ a [[Hilbert space]], which can be either finite or infinite dimensional, the unitary group $U(\mathcal{H})$ and the [[general linear group]] $GL(\mathcal{H})$, regarded as [[topological group]]s, have the same [[homotopy type]]. 

Additionally, $U(\mathcal{H})$ is a [[maximal compact subgroup]] of $GL(\mathcal{H})$ for finite-dimensional $\mathcal{H}$.

=--

+-- {: .proof}
###### Proof

By the [[Gram-Schmidt process]].

=--


+-- {: .num_theorem}
###### Theorem
**(Kuiper's theorem)**

For a separable infinite-dimensional complex [[Hilbert space]] $\mathcal{H}$, the unitary group $U(\mathcal{H})$ is [[contractible]] in the [[norm topology]].

=--

See also [[Kuiper's theorem]]. Note that $U(\mathcal{H})$ is also contractible in the [[strong operator topology]] (due to Dixmier and Douady).

+-- {: .num_remark}
###### Remark

This in contrast to the finite dimensional situation. For $n \in \mathbb{N}$ ($n \ge 1$), $U(n)$ is not contractible.

=--


Write $B U(n)$ for the [[classifying space]] of the [[topological group]] $U(n)$. Inclusion of matrices into larger matrices gives a canonical sequence of inclusions

$$
  \cdots \to B U(n) \hookrightarrow B U(n+1) \hookrightarrow B U(n+2) \to \cdots
  \,.
$$

The [[homotopy limit|homotopy]] [[direct limit]] over this is written

$$
  B U := {\lim_\to}_n B U(n)
$$

or sometimes $B U(\infty)$. Notice that this is very different from $B U(\mathcal{H})$ for $\mathcal{H}$ an infinite-dimensional Hilbert space. See [[topological K-theory]] for more on this.

### Relation to special unitary group {#SUn}

+-- {: .num_prop}
###### Proposition

For all $n \in \mathbb{N}$, the [[unitary group]] $U(n)$ is a [[split exact sequence|split]] [[group extension]] of the [[circle group]] $U(1)$ by the [[special unitary group]] $SU(n)$

$$
  SU(n) \to U(n) \to U(1)
  \,.
$$

Hence it is a [[semidirect product group]]

$$
  U(n) \simeq SU(n) \rtimes U(1)
  \,.
$$

=--

### Relation to orthogonal, symplectic and general linear group
 {#RelationToOrthogonalSymplecticAndGeneralLinearGroup}

The unitary group $U(n)$ is equivalently the [[intersection]]
of the [[orthogonal group]] $O(2n)$, the [[symplectic group]] $Sp(2n,\mathbb{R})$ and the complex [[general linear group]] $GL(n,\mathbb{C})$ inside the real [[general linear group]] $GL(2n,\mathbb{R})$.

Actually it is already the intersection of any two of these three, 
a fact also known as the "2 out of 3-property" of the unitary group.

This intersection property makes a [[G-structure]] for $G = U(n)$ (an [[almost Hermitian structure]]) precisely a joint [[orthogonal structure]], [[almost symplectic structure]] and [[almost complex structure]]. In the [[integrability of G-structure|first-order integrable case]] this is precisely a joint [[orthogonal structure]] ([[Riemannian manifold]] structure), [[symplectic structure]] and [[complex structure]].

## Examples

$U(1)$ is the [[circle group]].

### Coset spaces

+-- {: .num_example #nSphereAsUnitaryCosetSpace}
###### Example

The [[n-spheres|(2n+1)-spheres]] are [[coset spaces]] of unitary groups

$$
  S^{2n+1} \simeq U(n+1)/U(n)
  \,.
$$

=--



+-- {: .num_example #ComplexStiefelManifold}
###### Example

For $n \leq k$, the [[coset]]

$$
   V_n(\mathbb{C}^k) \coloneqq U(k)/U(k-n)
$$

is called the $n$th _complex [[Stiefel manifold]]_ of $\mathbb{C}^k$.

=--



+-- {: .num_prop }
###### Proposition

The complex [[Stiefel manifold]] $V_n(\mathbb{C}^k)$ (example \ref{ComplexStiefelManifold}) is [[n-connected topological space|2(k-n)-connected]].

=--

+-- {: .proof}
###### Proof

Consider the [[coset]] [[quotient]] [[projection]]

$$
  U(k-n)
    \longrightarrow
  U(k)
    \longrightarrow
  U(k)/U(k-n) 
    = 
  V_n(\mathbb{C}^k)
  \,.
$$

By prop. \ref{UnitaryGroupIsCompact} and by [this corollary](QuotientProjectionForCompactLieSubgroupIsPrincipal) the projection $U(k)\to U(k)/U(k-n)$ is a [[Serre fibration]]. Therefore there is induced the [[long exact sequence of homotopy groups]] of this [[fiber sequence]], and by prop. \ref{InclusionOfUnitaryGroupnIntoUnitaryGroupnPlusIneIsnMinus1Equivalence} it has the following form in degrees bounded by $n$:

$$
  \cdots
    \to
  \pi_{\bullet \leq 2(k-n)}(U(k-n))
    \overset{epi}{\longrightarrow}
  \pi_{\bullet \leq 2(k-n)}(U(k))
    \overset{0}{\longrightarrow}
  \pi_{\bullet \leq 2(k-n)}(V_n(\mathbb{C}^k))
    \overset{0}{\longrightarrow}
  \pi_{\bullet-1 \lt 2(k-n)}(U(k))
    \overset{\simeq}{\longrightarrow}
  \pi_{\bullet-1 \lt 2(k-n)}(U(k-n))
    \to
  \cdots
  \,.
$$

This implies the claim. 


=--



## Related concepts

* [[stable unitary group]]

* The subgroup of unitary matrices with [[determinant]] equal to 1 is the [[special unitary group]]. The [[quotient]] by the [[center]] is the [[projective unitary group]].  The space of equivalence classes of unitary matrices under conjugation is the [[symmetric product of circles]].

* The analog of the unitary group for real metric spaces is the [[orthogonal group]].

* similarly: [[quaternionic unitary group]]

* The [[Lie algebra]] is the [[unitary Lie algebra]].

* [[unitary representation]]

* [[unitary operator]]


## References


* {#MimuraToda63} M. Mimura and H. Toda, _Homotopy Groups of $SU(3)$, $SU(4)$ and $Sp(2)$_, J. Math. Kyoto Univ. Volume 3, Number 2 (1963), 217-250. ([Euclid](http://projecteuclid.org/euclid.kjm/1250524818))

* {#EspinozaUribe} Jesus Espinoza, [[Bernardo Uribe]], _Topological properties of the unitary group_, JP Journal of Geometry and Topology
**16** (2014) Issue 1, pp 45-55 ([arXiv:1407.1869](https://arxiv.org/abs/1407.1869), [doi:10.18257/raccefyn.317](http://dx.doi.org/10.18257/raccefyn.317))

[[!redirects unitary group]]
[[!redirects unitary groups]]

[[!redirects infinite unitary group]]
[[!redirects infinite unitary groups]]

[[!redirects U(n)]]


