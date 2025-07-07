
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

> For more context on the following cf. at *[[classifying space]].*

For $n \in \mathbb{N}$, write $O(n)$ for the [[orthogonal group]] regarded as a [[topological group]] and  [[group action|acting]] canonically on $\mathbb{R}^n$. 

\begin{definition}\label{StiefelManifold}
For $n \leq N \in \mathbb{N}$, the $n$th **real Stiefel manifold** of $\mathbb{R}^N$ is the [[coset]] [[topological space]].

\[
  \label{CosetRealization}
  V_n\big(\mathbb{R}^N\big) 
    \;\coloneqq\; 
  O(N)/O(N-n)
  \,,
\]

where the [[action]] of $O(N-n)$ is via its evident [[subgroup]] inclusion $O(N-n)\hookrightarrow O(N)$.
\end{definition}

\begin{remark}
The canonical [[group action]] $O(N) \curvearrowright \mathbb{R}^n$ induces a [[transitive action]] on the set of $n$-dimensional [[linear subspaces]] $\mathbb{R}^n \subset \mathbb{R}^N$ equipped with an [[orthonormal basis]], and given any such, then its [[stabilizer subgroup]] inside $O(N)$ is isomorphic to $O(N-n)$. In this way the underlying set of $V_n(\mathbb{R}^N)$ is in [[natural bijection]] to the set of $n$-dimensional linear subspaces in $\mathbb{R}^N$ equipped with [[orthonormal bases]]. The realization of this set as a [[coset]] (eq:CosetRealization) serves to equip it naturally with the [[structure]] of a [[topological space]].
\end{remark}


\begin{definition}\label{EOn}

By def. \ref{StiefelManifold} there are canonical inclusions $V_n(\mathbb{R}^N) \hookrightarrow V_n(\mathbb{R}^{N+1})$ that are compatible with the $O(n)$-[[action]]. The [[colimit]] (in [[Top]], see [there](Top#UniversalConstructions)) over these inclusions is denoted

$$
  E O(n) 
   \;\coloneqq\; 
  \underset{\longrightarrow}{\lim}_N 
    V_n(\mathbb{R}^N)
  \,.
$$

\end{definition}

This is a model for the total space of the $O(n)$-[[universal principal bundle]].


## Properties

### Homotopy groups

\begin{proposition}\label{Connectedness}
The Stiefel manifold $V_n(\mathbb{R}^N)$ (Def. \ref{StiefelManifold}) is [[n-connected topological space|$(N-n-1)$-connected]].
\end{proposition}
\begin{proof}
Observe that 

1. the coset coprojection $O(N) \to O(N)/O(N-n)$ is a [[Serre fibration]] 

   (by [this prop.](orthogonal+group#OrthogonalGroupIsCompact) and [this corollary](coset#QuotientProjectionForCompactLieSubgroupIsPrincipal))

1. its [[fiber]] (hence: [[homotopy fiber]]) is $O(N-n)$

so that we have a [[homotopy fiber sequence]] of this form:

$$
  O(N-n)
    \longrightarrow
  O(N)
    \longrightarrow
  O(N)/O(N-n) 
    \;\equiv\; 
  V_n(\mathbb{R}^N)
$$

The corresponding [[long exact sequence of homotopy groups]] has, has the following structure in degrees bounded by $n$, 
by [this prop.](orthogonal+group#InclusionOfOnIntoOkIsnMinus1Equivalence):

$$
  \cdots
    \to
  \pi_{\bullet \leq n-1} O(N-n)
    \overset{epi}{\longrightarrow}
  \pi_{\bullet \leq n-1} O(N) 
    \overset{0}{\longrightarrow}
  \pi_{\bullet \leq n-1} V_n(N)
    \overset{0}{\longrightarrow}
  \pi_{\bullet-1 \lt n-1} O(N-n)
    \overset{\sim}{\longrightarrow}
  \pi_{\bullet-1 \lt n-1} O(N)
    \to
  \cdots
  \,.
$$

This implies the claim. (Exactness of the sequence says that every element in $\pi_{\bullet \leq n-1} V_n(\mathbb{R}^N) $ is in the kernel of zero, hence in the image of 0, hence is 0 itself.)
\end{proof}

\begin{corollary}
The colimiting space $E O(n) = \underset{\longleftarrow}{\lim}_N V_n(\mathbb{R}^N)$ from Def. \ref{EOn} is [[weakly contractible topological space|weakly contractible]].
\end{corollary}

\begin{proof}
This follows from Prop. \ref{Connectedness}, together with the fact that the sequence of maps $V_n(\mathbb{R}^N) \to V_n(\mathbb{R}^{N+1})$ are closed $T_1$-inclusions. See [[compact object#CompactObjectsInTop|this Prop.]] together with the accompanying commentary there.  
\end{proof}


### CW-complex structure

\begin{proposition}
The Stiefel manifold $V_n(\mathbb{R}^N)$ admits the [[structure]]] of a [[CW-complex]].
\end{proposition}

(e.g. [James 1959  p. 3](#James59), [James 1976  p. 5 with p. 21](#James76), [Hatcher 2002 p. 302](#Hatcher02), [Blaszczyk 2007](#Blaszczyk07))

{#CellularInclusionOfStiefelManifolds} And it should be true that with that cell structure the inclusions $V_n(\mathbb{R}^N) \hookrightarrow V_n(\mathbb{R}^{N+1})$ are subcomplex inclusions:

According to [Yokota 1956](#Yokota56), the inclusions $SU(n)\hookrightarrow SU(N)$ are cellular such that this is compatible with the group action (reviewed [here](http://web.stanford.edu/~kupers/liegroups.pdf) in 3.3 and 3.3.1). This implies that also the projection $SU(N) \to SU(N)/SU(N-n)$ is cellular (e.g. [Hatcher 2002 p. 302](#Hatcher02)).



### Relation to Grassmannians and universal bundles

Similarly, the _[[Grassmannian manifold]]_ is the [[coset]]

$$
  Gr_n(\mathbb{R}^N) 
    \;\coloneqq\; 
  O(N)/(O(n)\times O(N-n))
  \,.
$$

The [[quotient]] [[coprojection]]

$$
  V_{n}(\mathbb{R}^N)
    \longrightarrow 
  Gr_n(\mathbb{R}^N)
$$

is an $O(n)$-[[principal bundle]], with [[associated bundle]] $V_n(\mathbb{R}^N) \times_{O(n)} \mathbb{R}^N$ a [[vector bundle]] of [[rank of a vector bundle|rank]] $n$. In the limit ([[colimit]]) that $N \to \infty$ this gives a presentation of the $O(n)$-[[universal principal bundle]] and of the [[universal vector bundle]] of rank $n$, respectively. The base space $Gr_n(\infty)\simeq_{whe} B O(n)$ is the [[classifying space]] for $O(n)$-[[principal bundles]] and for rank $n$ vector bundles.



## Related concepts

* [[Grassmannian manifold]]

* [[classifying space]]

## References

Named after:

* {#Stiefel35} [[Eduard Stiefel]]: _Richtungsfelder und Fernparallelismus in $n$-dimensionalen Mannigfaltigkeiten_, Comment. Math. Helv. **8** (1935/6) 3-51

Further discussion:

* {#Saito55} Yoshihiro Saito: _On the homotopy groups of Stiefel manifolds_, J. Inst. Polytech. Osaka City Univ. Ser. A **6** 1 (1955) 39-45 &lbrack;[euclid:ojm/1353054734](http://projecteuclid.org/euclid.ojm/1353054734)&rbrack;

* {#Yokota56} I. Yokota, _On the cells of symplectic groups_, Proc. Japan Acad. **32** (1956) 399-400

* {#James59} [[Ioan Mackenzie James]]: _Spaces associated with Stiefel manifolds_, Proc. Lond. Math. Soc. (3) 9 (1959) &lbrack;[doi:10.1112/plms/s3-9.1.115](https://doi.org/10.1112/plms/s3-9.1.115), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/james4.pdf)&rbrack;

* [[Ioan Mackenzie James]]: _On the homotopy type of Stiefel manifolds_, Proceedings of the AMS, **29** 1 (1971)

* {#James76} [[Ioan Mackenzie James]]: _The topology of Stiefel manifolds_, Cambridge University Press (1976)

* {#Kochmann96} [[Stanley Kochmann]], section 1.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS (1996)

* {#Hatcher02} [[Allen Hatcher]]: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* {#Blaszczyk07} Zbigniew B&#322;aszczyk, _On cell decompositions of $SO(n)$_ (2007) &lbrack;[pdf](http://knm.mat.umk.pl/pliki/konferencje/zb_lsait3_2007.pdf)&rbrack;

See also:

* Wikipedia: _[Stiefel manifold](https://en.wikipedia.org/wiki/Stiefel_manifold)_

[[!redirects Stiefel manifolds]]

[[!redirects Stiefel space]]
[[!redirects Stiefl spaces]]

[[!redirects Stiefel variety]]
[[!redirects Stiefel varieties]]