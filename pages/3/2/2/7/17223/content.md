
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
For $k \leq N \in \mathbb{N}$, the $k$th **real Stiefel manifold** of $\mathbb{R}^N$ is the [[coset]] [[topological space]].

\[
  \label{CosetRealization}
  V_k\big(\mathbb{R}^N\big) 
    \;\coloneqq\; 
  O(N)/O(N-k)
  \,,
\]

where the [[action]] of $O(N-k)$ is via the standard [[subgroup]] inclusion $O(N-k)\hookrightarrow O(N)$ as an upper right block.
\end{definition}


\begin{remark}
The canonical [[group action]] $O(N) \curvearrowright \mathbb{R}^N$ induces a [[transitive action]] on the set of $k$-dimensional [[linear subspaces]] $\mathbb{R}^k \subset \mathbb{R}^N$ equipped with an [[orthonormal basis]], and given any such subspace $W$, then its [[stabilizer subgroup]] in $O(N)$ is isomorphic to $O(N-k)$, the symmetries of the orthogonal subspace $W^\perp$. In this way the underlying set of $V_k(\mathbb{R}^N)$ is in [[natural bijection]] to the set of $k$-dimensional linear subspaces in $\mathbb{R}^N$ equipped with [[orthonormal bases]]. The realization of this set as a [[coset]] (eq:CosetRealization) serves to equip it naturally with the [[structure]] of a [[topological space]].
\end{remark}

More generally, given any finite-dimensional [[inner product space]] $(V,\langle\ ,\ \rangle)$, there is a corresponding orthogonal group $O(V)$, and one can repeat the above definition more or less verbatim.

\begin{definition}\label{EOn}

By def. \ref{StiefelManifold} there are canonical inclusions $V_k(\mathbb{R}^N) \hookrightarrow V_k(\mathbb{R}^{N+1})$ that are compatible with the [[action]]s of the respective orthogonal groups. The [[colimit]] (in [[Top]], see [there](Top#UniversalConstructions)) over these inclusions is denoted

$$
  E O(k) 
   \;\coloneqq\; 
  \underset{\longrightarrow}{\lim}_N 
    V_k(\mathbb{R}^N)
  \,.
$$

\end{definition}

This is a model for the total space of the $O(k)$-[[universal principal bundle]].


## Properties

### Homotopy groups

\begin{proposition}\label{Connectedness}
The Stiefel manifold $V_k(\mathbb{R}^N)$ (Def. \ref{StiefelManifold}) is [[n-connected topological space|$(N-k-1)$-connected]].
\end{proposition}
\begin{proof}
Observe that 

1. the coset coprojection $O(N) \to O(N)/O(N-k)$ is a [[Serre fibration]] 

   (by [this prop.](orthogonal+group#OrthogonalGroupIsCompact) and [this corollary](coset#QuotientProjectionForCompactLieSubgroupIsPrincipal))

1. its [[fiber]] (hence: [[homotopy fiber]]) is $O(N-k)$

so that we have a [[homotopy fiber sequence]] of this form:

$$
  O(N-k)
    \longrightarrow
  O(N)
    \longrightarrow
  O(N)/O(N-k) 
    \;\equiv\; 
  V_k(\mathbb{R}^N)
$$

The corresponding [[long exact sequence of homotopy groups]] has, has the following structure in degrees strictly bounded above by $N-k$, 
by [this prop](orthogonal+group#InclusionOfOnIntoOkIsnMinus1Equivalence) (taking $n=N-k$ in the notation there):

$$
  \cdots
    \to
  \pi_{\bullet \lt N-k} O(N-k)
    \overset{epi}{\longrightarrow}
  \pi_{\bullet \lt N-k} O(N) 
    \overset{0}{\longrightarrow}
  \pi_{\bullet \lt N-k} V_k(N)
    \overset{0}{\longrightarrow}
  \pi_{\bullet-1 \lt N-k-1} O(N-k)
    \overset{\sim}{\longrightarrow}
  \pi_{\bullet-1 \lt N-k-1} O(N)
    \to
  \cdots
  \,.
$$

This implies the claim. (Exactness of the sequence says that every element in $\pi_{\bullet \lt N-k} V_k(\mathbb{R}^N) $ is in the kernel of zero, hence in the image of 0, hence is 0 itself.)
\end{proof}

\begin{corollary}
The colimiting space $E O(k) = \underset{\longleftarrow}{\lim}_N V_k(\mathbb{R}^N)$ from Def. \ref{EOn} is [[weakly contractible topological space|weakly contractible]].
\end{corollary}

\begin{proof}
This follows from Prop. \ref{Connectedness}, together with the fact that the sequence of maps $V_k(\mathbb{R}^N) \to V_k(\mathbb{R}^{N+1})$ are closed $T_1$-inclusions. See [[compact object#CompactObjectsInTop|this Prop.]] together with the accompanying commentary there.  
\end{proof}


### CW-complex structure

\begin{proposition}
The Stiefel manifold $V_k(\mathbb{R}^N)$ admits the [[structure]]] of a [[CW-complex]].
\end{proposition}

(e.g. [James 1959  p. 3](#James59), [James 1976  p. 5 with p. 21](#James76), [Hatcher 2002 p. 302](#Hatcher02), [Blaszczyk 2007](#Blaszczyk07))

{#CellularInclusionOfStiefelManifolds} And it should be true that with that cell structure the inclusions $V_k(\mathbb{R}^N) \hookrightarrow V_k(\mathbb{R}^{N+1})$ are subcomplex inclusions:

According to [Yokota 1956](#Yokota56), the inclusions $SU(k)\hookrightarrow SU(N)$ are cellular such that this is compatible with the group action (reviewed [here](http://web.stanford.edu/~kupers/liegroups.pdf) in 3.3 and 3.3.1). This implies that also the projection $SU(N) \to SU(N)/SU(N-k)$ is cellular (e.g. [Hatcher 2002 p. 302](#Hatcher02)).



### Relation to Grassmannians and universal bundles

Similarly, the _[[Grassmannian manifold]]_ is the [[coset]]

$$
  Gr_k(\mathbb{R}^N) 
    \;\coloneqq\; 
  O(N)/(O(k)\times O(N-k))
  \,.
$$

The [[quotient]] [[coprojection]]

$$
  V_k(\mathbb{R}^N)
    \longrightarrow 
  Gr_k(\mathbb{R}^N)
$$

is an $O(k)$-[[principal bundle]], with [[associated bundle]] $V_k(\mathbb{R}^N) \times_{O(k)} \mathbb{R}^k$ a [[vector bundle]] of [[rank of a vector bundle|rank]] $k$. In the limit ([[colimit]]) that $N \to \infty$ this gives a presentation of the $O(k)$-[[universal principal bundle]] and of the [[universal vector bundle]] of rank $k$, respectively. The base space $Gr_k(\infty)\simeq_{whe} B O(k)$ is the [[classifying space]] for $O(k)$-[[principal bundles]] and for rank $k$ vector bundles.



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