
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Definition

For $n \in \mathbb{N}$ the **orthogonal group** is the group of [[isometry|isometries]] of a real $n$-dimensional [[Hilbert space]]. This is naturally a [[Lie group]].
This is canonically isomorphic to the group of $n \times n$ orthogonal [[matrices]].

More generally there is a notion of _[[orthogonal group of an inner product space]]_.

The analog for complex Hilbert spaces is the [[unitary group]].


## Properties

### Compactness

+-- {: .num_prop #OrthogonalGroupIsCompact}
###### Proposition

The orthogonal group $O(n)$ is [[compact topological space]], hence in particular a [[compact Lie group]].
 
=--

### Homotopy groups
 {#HomotopyGroups}

+-- {: .num_prop #InclusionOfOnIntoOkIsnMinus1Equivalence}
###### Proposition

For $n, N \in \mathbb{N}$, $n \leq N$, then the canonical inclusion of orthogonal groups

$$
  O(n) \hookrightarrow O(N)
$$

is an [[n-equivalence|(n-1)-equivalence]], hence induces an [[isomorphism]] on [[homotopy groups]] in degrees $\lt n-1$ and a [[surjection]] in degree $n-1$.

=--

+-- {: .proof}
###### Proof

Consider the [[coset]] [[quotient]] [[projection]]

$$
  O(n)
    \longrightarrow
  O(n+1)
    \longrightarrow
  O(n+1)/O(n)
  \,.
$$

By prop. \ref{OrthogonalGroupIsCompact} and by [this corollary](coset#QuotientProjectionForCompactLieSubgroupIsPrincipal), the projection $O(n+1)\to O(n+1)/O(n)$ is a [[Serre fibration]]. Furthermore, example \ref{nSphereAsCosetSpace} identifies the [[coset]] with the [[n-sphere]] 

$$
  S^{n}\simeq O(n+1)/O(n)
  \,.
$$

Therefore the [[long exact sequence of homotopy groups]] of the [[fiber sequence]] $O(n)\to O(n+1)\to S^n$ looks like

$$
  \cdots
    \to
  \pi_{\bullet+1}(S^n)
    \longrightarrow
  \pi_\bullet(O(n))
    \longrightarrow
  \pi_\bullet(O(n+1))
    \longrightarrow
  \pi_\bullet(S^n)
   \to
  \cdots
$$

Since $\pi_{\lt n}(S^n) = 0$, this implies that 

$$
  \pi_{\lt n-1}(O(n))
    \overset{\simeq}{\longrightarrow}
  \pi_{\lt n-1}(O(n+1))
$$

is an isomorphism and that

$$
  \pi_{n-1}(O(n))
    \longrightarrow
  \pi_{n-1}(O(n+1))
$$

is surjective. Hence now the statement follows by induction over $N-n$.

=--

It follows that the [[homotopy groups]] $\pi_k(O(n))$ are independent of $n$ for $n \gt k + 1$ (the "stable range"). So if $O = \underset{\longrightarrow}{\lim}_n O(n)$, then $\pi_k(O(n)) = \pi_k(O)$. By [[Bott periodicity]] we have

$$
\array{
\pi_{8k+0}(O) & = \mathbb{Z}_2
\\
\pi_{8k+1}(O) & = \mathbb{Z}_2
\\
\pi_{8k+2}(O) & = 0
\\
\pi_{8k+3}(O) & = \mathbb{Z}
\\
\pi_{8k+4}(O) & = 0
\\
\pi_{8k+5}(O) & = 0
\\
\pi_{8k+6}(O) & = 0
\\
\pi_{8k+7}(O) & = \mathbb{Z}.
}
$$

In the unstable range for [[low-dimensional topology|low degrees]] they instead start out as follows 

| $G$ | $\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ | $\pi_13$ | $\pi_14$ | $\pi_15$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $SO(2)$ | $\mathbb{Z}$ |  0 | 0 |0 |0 |0 |0 |0 |0 |0 |0 |0 | 0 | 0 | 0 |
| $SO(3)$ | $\mathbb{Z}_2$ | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_{12}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{3}$ | $\mathbb{Z}_{15}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{12}$ | $\mathbb{Z}_2^{\oplus 2}\oplus\mathbb{Z}_{84}$ | $\mathbb{Z}_2^{\oplus 2}$ |
| $SO(4)$ | " | 0 | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{12}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{3}^{\oplus 2}$ | $\mathbb{Z}_{15}^{\oplus 2}$|$\mathbb{Z}_{2}^{\oplus 2}$ |$\mathbb{Z}_{2}^{\oplus 4}$  | $\mathbb{Z}_2^{\oplus 2}\oplus\mathbb{Z}_{12}^{\oplus 2}$ | $\mathbb{Z}_2^{\oplus 4}\oplus\mathbb{Z}_{84}^{\oplus 2}$ | $\mathbb{Z}_2^{\oplus 4}$ | 
| $SO(5)$ | " | " | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | 0 | $\mathbb{Z}$ | 0 | 0 |$\mathbb{Z}_{120}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{2}^{\oplus 2}$| $\mathbb{Z}_2\oplus\mathbb{Z}_4$ | $\mathbb{Z}_{1680}$ | $\mathbb{Z}_2$ |
| $SO(6)$ | " | " | " | 0 | $\mathbb{Z}$ | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{24}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{120}$| $\mathbb{Z}_{4}$| $\mathbb{Z}_{60}$| $\mathbb{Z}_4$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{1680}$ | $\mathbb{Z}_2\oplus\mathbb{Z}_{72}$ |
| $SO(7)$ | " | " | " | " | 0 | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{8}$| $\mathbb{Z}_2\oplus\mathbb{Z}$| 0 | $\mathbb{Z}_2$ | $\mathbb{Z}_2\oplus\mathbb{Z}_8\oplus\mathbb{Z}_{2520}$ | $\mathbb{Z}_2^{\oplus 4}$ |
| $SO(8)$ | " | " | " | " | " | 0 | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 3}$ | $\mathbb{Z}_{2}^{\oplus 3}$ | $\mathbb{Z}_{8} \oplus \mathbb{Z}_{24}$ | $\mathbb{Z}_2 \oplus \mathbb{Z}$ | 0 | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_2\oplus\mathbb{Z}_8\oplus\mathbb{Z}_{120}\oplus\mathbb{Z}_{2520}$ | $\mathbb{Z}_2^{\oplus 7}$ |
| $SO(9)$ | " | " | " | " | " | " | $\mathbb{Z}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ |$\mathbb{Z}_{8}$ | $\mathbb{Z}_2\oplus \mathbb{Z}$ | 0 | $\mathbb{Z}_2$ | $\mathbb{Z}_2\oplus\mathbb{Z}_8$ | $\mathbb{Z}_2^{\oplus 3}\oplus\mathbb{Z}$ |
|$SO(10)$| " | " | " | " | " | " | " | $\mathbb{Z}_{2}$ | $\mathbb{Z}_2\oplus \mathbb{Z}$ | $\mathbb{Z}_{4}$| $\mathbb{Z}$ | $\mathbb{Z}_{12}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_8$ | $\mathbb{Z}_2^{\oplus 2}\oplus\mathbb{Z}$ |
|$SO(11)$| " | " | " | " | " | " | " | " |$\mathbb{Z}_{2}$ |$\mathbb{Z}_{2}$ | $\mathbb{Z}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_2^{\oplus 2}$ | $\mathbb{Z}_8$ | $\mathbb{Z}_2\oplus\mathbb{Z}$ |
|$SO(12)$| " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_2^{\oplus 2}$ | $\mathbb{Z}_4\oplus\mathbb{Z}_{24}$ | $\mathbb{Z}_2\oplus\mathbb{Z}$ |
|$SO(13)$| " | " | " | " | " | " | " | " | " | " | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_8$ | $\mathbb{Z}_2\oplus\mathbb{Z}$ |
|$SO(14)$| " | " | " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}$ | $\mathbb{Z}_4$ | $\mathbb{Z}$ |
|$SO(15)$| " | " | " | " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}_2$ | $\mathbb{Z}$ |
|$SO(16)$| " | " | " | " | " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z}^{\oplus 2}$ |
|$SO(17)$| " | " | " | " | " | " | " | " | " | " | " | " | " | " | $\mathbb{Z}$ |

The $SO(6)$ row can be found using [Mimura-Toda 63](#MimuraToda63), using $Spin(6) = SU(4)$, and that $Spin(6)$ is a $\mathbb{Z}_2$-[[covering space]] of $SO(6)$. The $SO(7)$ row can be derived from the homotopy groups of $Spin(7)$ as found in [Mimura 67](#Mimura67). Otherwise the table is given in columns $\pi_k$, $k=10,\ldots, 15$, and in rows $SO(n)$, $n=8,\ldots,17$, by the [[Encyclopedic Dictionary of Mathematics]], Table 6.VII in Appendix A.

Note that the maps
$$
  \array{
    \pi_3(SO(3)) \longrightarrow \pi_3(SO(4)) \longrightarrow \pi_3(SO(5))
    \\
     \mathbb{Z}\longrightarrow \mathbb{Z}\oplus \mathbb{Z} \longrightarrow\mathbb{Z}
  }
$$
are inclusion of the first summand followed by the map sending $(1,0)\mapsto 2$ and $(0,1)\mapsto 1$, so that stabilization from $SO(3)$ to $SO(5)$ induces multiplication by $2$ on $\pi_3$ (e.g. equations (2.1) and (2.2) in ([Tamura 57](#Tamura57)) and surrounding discussion). The same is also true for $\pi_7(SO(7)) \to \pi_7(SO(8)) \to \pi_7(SO(9))$.

### Homology and cohomology 

[[ordinary cohomology]] of the [[classifying spaces]] $B O(n)$ and $B SO(n)$:

([Brown 82](#Brown82), [Feshbach 83](#Feshbach83), [Pittie 91](#Pittie91), [Rudolph-Schmidt 17, Theorem 4.2.23](#RudolphSchmidt17))

### Whitehead tower and higher orientation structures

The [[Whitehead tower]] of the orthogonal group plays an important role in applications related to [[quantum physics]]. 

The first steps are

$$
  \cdots \to Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to \mathrm{O}(n)
  \,.
$$

[[Fivebrane group]] to [[String group]] to [[Spin group]] to [[special orthogonal group]] to **orthogonal group**.


Given a [[manifold]] $X$, lifts of the structure map $X \to \mathcal{B}O(n)$ of the $O(n)$-[[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] through this tower define, respectively

* [[orientation]]

* [[Spin structure]]

* [[String structure]]

* [[Fivebrane structure]]

on $X$.

### Coset spaces
 {#CosetSpaces}

+-- {: .num_example #nSphereAsCosetSpace}
###### Example

The [[n-spheres]] are [[coset spaces]] of orthogonal groups

$$
  S^n \simeq O(n+1)/O(n)
  \,.
$$

For fix a unit vector in $\mathbb{R}^{n+1}$. Then its [[orbit]] under the defining $O(n+1)$-[[action]] on $\mathbb{R}^{n+1}$ is clearly the canonical embedding $S^n \hookrightarrow \mathbb{R}^{n+1}$. But precisely the subgroup of $O(n+1)$ that consists of rotations around the axis formed by that unit vector [[stabilizer group|stabilizes]] it, and that subgroup is isomorphic to $O(n)$, hence $S^n \simeq O(n+1)/O(n)$.

=--

+-- {: .num_example #StiefelManifold}
###### Example

For $n \leq k$, the [[coset]]

$$
   V_n(\mathbb{R}^k) \coloneqq O(k)/O(k-n)
$$

is called the $n$th _real [[Stiefel manifold]]_ of $\mathbb{R}^k$.

=--

+-- {: .num_prop }
###### Proposition

The [[Stiefel manifold]] $V_n(\mathbb{R}^k)$ (example \ref{StiefelManifold}) is [[n-connected topological space|(k-n-1)-connected]].

=--

+-- {: .proof}
###### Proof

Consider the [[coset]] [[quotient]] [[projection]]

$$
  O(k-n)
    \longrightarrow
  O(k)
    \longrightarrow
  O(k)/O(k-n) 
    = 
  V_n(\mathbb{R}^k)
  \,.
$$

By prop. \ref{OrthogonalGroupIsCompact} and by [this corollary](QuotientProjectionForCompactLieSubgroupIsPrincipal) the projection $O(k)\to O(k)/O(k-n)$ is a [[Serre fibration]]. Therefore there is induced the [[long exact sequence of homotopy groups]] of this [[fiber sequence]], and by prop. \ref{InclusionOfOnIntoOkIsnMinus1Equivalence} it has the following form in degrees bounded by $n$:

$$
  \cdots
    \to
  \pi_{\bullet \leq k-n-1}(O(k-n))
    \overset{epi}{\longrightarrow}
  \pi_{\bullet \leq k-n-1}(O(k))
    \overset{0}{\longrightarrow}
  \pi_{\bullet \leq k-n-1}(V_n(\mathbb{R}^k))
    \overset{0}{\longrightarrow}
  \pi_{\bullet-1 \lt k-n-1}(O(k))
    \overset{\simeq}{\longrightarrow}
  \pi_{\bullet-1 \lt k-n-1}(O(k-n))
    \to
  \cdots
  \,.
$$

This implies the claim. (Exactness of the sequence says that every element in $\pi_{\bullet \leq n-1}(V_n(\mathbb{R}^k))$ is in the kernel of zero, hence in the image of 0, hence is 0 itself.)


=--

## Related concepts

* [[orthogonal calculus]]

* [[Stiefel manifold]], [[Grassmannian]]

* [[stable orthogonal group]]

 $\cdots\to$ [[fivebrane group]] $\to$ [[string group]] $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ **orthogonal group**

[[!include table of orthogonal groups and related]]

## Examples

\linebreak

[[!include low dimensional rotation groups -- table]]

\linebreak


## References

Examples of sporadic (exceptional) [[isogenies]] from [[spin groups]] onto orthogonal groups are discussed in

* [[Paul Garrett]], _Sporadic isogenies to orthogonal groups_, July 2013 ([pdf](http://www.math.umn.edu/~garrett/m/v/sporadic_isogenies.pdf))

The [[homotopy groups]] of $O(n)$ are listed for instance in 

* {#Abanov09} Alexander Abanov, Homotopy groups of Lie groups 2009 ([pdf](http://felix.physics.sunysb.edu/~abanov/Teaching/Spring2009/Notes/abanov-cpA1-upload.pdf))
  
* {#MimuraToda63} M. Mimura and H. Toda, _Homotopy Groups of $SU(3)$, $SU(4)$ and $Sp(2)$_, J. Math. Kyoto Univ. Volume 3, Number 2 (1963), 217-250. ([Euclid](http://projecteuclid.org/euclid.kjm/1250524818))

* {#Mimura67} M. Mimura, _The Homotopy groups of Lie groups of low rank_, Math. Kyoto Univ. Volume 6, Number 2 (1967), 131-176. ([Euclid](http://projecteuclid.org/euclid.kjm/1250524375))

The [[ordinary cohomology]] and [[ordinary homology]] of the manifolds $SO(n)$ is discussed in 

* {#Brown82} [[Edgar H. Brown]], _The Cohomology of $B SO_n$ and $BO_n$ with Integer Coefficients_, Proceedings of the American Mathematical Society Vol. 85, No. 2 (Jun., 1982), pp. 283-288 ([jstor:2044298](https://www.jstor.org/stable/2044298))

* {#Feshbach83} Mark Feshbach, _The Integral Cohomology Rings of the Classifying Spaces of $\mathrm{O}(n)$ and $\mathrm{SO}(n)$,_ Indiana Univ. Math. J.  32 (1983), 511-516 ([doi:10.1512/iumj.1983.32.32036](https://doi.org/10.1512/iumj.1983.32.32036))

* {#Pittie91} Harsh V. Pittie, _The integral homology and cohomology rings of SO(n) and Spin(n)_, Journal of Pure and Applied Algebra Volume 73, Issue 2, 19 August 1991, Pages 105&#8211;153 (<a href="https://doi.org/10.1016/0022-4049(91)90108-E">doi:10.1016/0022-4049(91)90108-E</a>))

* {#RudolphSchmidt17} Gerd Rudolph, Matthias Schmidt, around Theorem 4.2.23 of _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))


See also

* {#Tamura57} Itiro Tamura, _On Pontrjagin classes of homotopy types of manifolds_, Journal of the mathematical society of Japan, Vol. 9 No. 2 , 1957 [pdf](http://www.maths.ed.ac.uk/~aar/papers/tamura3.pdf)

[[!redirects orthogonal groups]]

[[!redirects O(n)]]

[[!redirects O(2)]]
