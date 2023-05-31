
#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$, write $O(n)$ for the [[orthogonal group]] acting on $\mathbb{R}^n$. For the following we regard these groups as [[topological groups]] in the canonical way.

+-- {: .num_defn #StiefelManifold}
###### Definition

For $n, k \in \mathbb{N}$ and $n \leq k$, then the $n$th **real Stiefel manifold** of $\mathbb{R}^k$ is the [[coset]] [[topological space]].

$$
  V_n(\mathbb{R}^k) \coloneqq O(k)/O(k-n)
  \,,
$$

where the [[action]] of $O(k-n)$ is via its canonical embedding $O(k-n)\hookrightarrow O(k)$.

=--

+-- {: .num_remark}
###### Remark

The group $O(k)$ [[transitive action|acts transitively]] on the set of $n$-dimensional [[linear subspaces]] equipped with an [[orthonormal basis]], and given any such, then its [[stabilizer subgroup]] in $O(k)$ is isomorphic to $O(k-n)$. In this way the underlying set of $V_n(\mathbb{R}^k)$ is in [[natural bijection]] to the set of $n$-dimensional linear subspaces in $\mathbb{R}^k$ equipped with [[orthonormal basis]]. The realization as a [[coset]] as above serves to equip this set naturally with a [[topology|topological space]].

=--

+-- {: .num_defn #EOn}
###### Definition

By def. \ref{StiefelManifold} there are canonical inclusions $V_n(\mathbb{R}^k) \hookrightarrow V_n(\mathbb{R}^{k+1})$ that are compatible with the $O(n)$-[[action]]. The [[colimit]] (in [[Top]], see there) over these inclusions is denoted

$$
  E O(n) \coloneqq \underset{\longrightarrow}{\lim}_k V_n(\mathbb{R}^k)
  \,.
$$

=--

This is a model for the total space of the $O(n)$-[[universal principal bundle]].

## Properties

### Homotopy groups

+-- {: .num_prop}
###### Proposition

The Stiefel manifold $V_n(k)$ is [[n-connected topological space|(n-1)-connected]].

=--

+-- {: .proof}
###### Proof

Consider the [[coset]] [[quotient]] [[projection]]

$$
  O(n)
    \longrightarrow
  O(k)
    \longrightarrow
  O(k)/O(n) 
    = 
  V_n(\mathbb{R}^k)
  \,.
$$

By [this prop.](orthogonal+group#OrthogonalGroupIsCompact) and by [this corollary](coset#QuotientProjectionForCompactLieSubgroupIsPrincipal) the projection $O(k)\to O(k)/O(n)$ is a [[Serre fibration]]. Therefore there is the [[long exact sequence of homotopy groups]] of this [[fiber sequence]] and by [this prop.](orthogonal+group#InclusionOfOnIntoOkIsnMinus1Equivalence) it has the following structure in degrees bounded by $n$:

$$
  \cdots
    \to
  \pi_{\bullet \leq n-1}(O(k))
    \overset{epi}{\longrightarrow}
  \pi_{\bullet \leq n-1}(O(n))
    \overset{0}{\longrightarrow}
  \pi_{\bullet \leq n-1}(V_n(k))
    \overset{0}{\longrightarrow}
  \pi_{\bullet-1 \lt n-1}(O(k))
    \overset{\simeq}{\longrightarrow}
  \pi_{\bullet-1 \lt n-1}(O(n))
    \to
  \cdots
  \,.
$$

This implies the claim. (Exactness of the sequence says that every element in $\pi_{\bullet \leq n-1}(V_n(\mathbb{R}^k))$ is in the kernel of zero, hence in the image of 0, hence is 0 itself.)

=--

+-- {: .num_cor}
###### Corollary

The colimiting space $E O(n) = \underset{\longleftarrow}{\lim}_k V_n(\mathbb{R}^k)$ from def. \ref{EOn} is [[weakly contractible topological space|weakly contractible]].

=-- 

+-- {: .proof} 
###### Proof 
This follows from the proposition, together with the fact that the sequence of maps $V_n(\mathbb{R}^k) \to V_n(\mathbb{R}^{k+1})$ are closed $T_1$-inclusions. See the Proposition [[compact object#CompactObjectsInTop|here]] together with the accompanying commentary.  
=-- 

### CW-complex structure

+-- {: .num_prop}
###### Proposition

The Stiefel manifold $V_n(\mathbb{R}^k)$ admits the structure of a [[CW-complex]].

=--

e.g. ([James 59, p. 3](#James59), [James 76, p. 5 with p. 21](#James76), [Hatcher, p. 302](#Hatcher)[Blaszczyk 07](#Blaszczyk07))

{#CellularInclusionOfStiefelManifolds} And it should be true that with that cell structure the inclusions $V_n(\mathbb{R}^k) \hookrightarrow V_n(\mathbb{R}^{k+1})$ are subcomplex inclusions:

According to ([Yokota 56](#Yokota56)) the inclusions $SU(n)\hookrightarrow SU(k)$ are cellular and this is compatible with the group action (reviewed [here](http://web.stanford.edu/~kupers/liegroups.pdf) in 3.3 and 3.3.1). This implies that also the projection $SU(k) \to SU(k)/SU(k-n)$ is cellular (e.g. [Hatcher, p. 302](#Hatcher)).



### Relation to Grassmannians and universal bundles

Similarly, the _[[Grassmannian manifold]]_ is the [[coset]]

$$
  Gr_n(\mathbb{R}^k) \coloneqq O(k)/(O(n)\times O(k-n))
  \,.
$$

The [[quotient]] [[projection]]

$$
  V_{n}(\mathbb{R}^k)\longrightarrow Gr_n(\mathbb{R}^k)
$$

is an $O(n)$-[[principal bundle]], with [[associated bundle]] $V_n(\mathbb{R}^k)\times_{O(n)} \mathbb{R}^n$ a [[vector bundle]] of [[rank]] $n$. In the limit ([[colimit]]) that $k \to \infty$ is this gives a presentation of the $O(n)$-[[universal principal bundle]] and of the [[universal vector bundle]] of rank $n$, respectively.. The base space $Gr_n(\infty)\simeq_{whe} B O(n)$ is the [[classifying space]] for $O(n)$-[[principal bundles]] and rank $n$ vector bundles.



## Related concepts

* [[Grassmannian manifold]]

* [[classifying space]]

## References

* {#Stiefel35} [[Eduard Stiefel]], _Richtungsfelder und Fernparallelismus in
$n$-dimensionalen Mannigfaltigkeiten_, Comment. Math. Helv. , 8(1935/6),
3-51.

* {#Yokota56} I. Yokota, _On the cells of symplectic groups_, Proc. Japan Acad. 32 (1956), 399-400.


* {#James59} [[Ioan Mackenzie James]], _Spaces associated with Stiefel manifolds_, Proc. Lond. Math. Soc. (3) 9 (1959)

* [[Ioan Mackenzie James]], _On the homotopy type of Stiefel manifolds_, Proceedings of the AMS, vol. 29, Number 1, June 1971

* {#James76} [[Ioan Mackenzie James]], _The topology of Stiefel manifolds_, Cambridge University Press, 1976


* {#Kochmann96} [[Stanley Kochmann]], section 1.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Blaszczyk07} Zbigniew B&#322;aszczyk, _On cell decompositions of $SO(n)$_, 2007 ([pdf](http://knm.mat.umk.pl/pliki/konferencje/zb_lsait3_2007.pdf))

* {#Hatcher} Hatcher, _Algebraic topology_

* Wikipedia, _[Stiefel manifold](https://en.wikipedia.org/wiki/Stiefel_manifold)_

* {#Saito55} Yoshihiro Saito, _On the homotopy groups of Stiefel manifolds_, J. Inst. Polytech. Osaka City Univ. Ser. A Volume 6, Number 1 (1955), 39-45. [Project Euclid](http://projecteuclid.org/euclid.ojm/1353054734)

[[!redirects Stiefel manifolds]]

[[!redirects Stiefel space]]
[[!redirects Stiefl spaces]]

[[!redirects Stiefel variety]]
[[!redirects Stiefel varieties]]