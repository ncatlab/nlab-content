
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

### Homotopy groups
 {#HomotopyGroups}

The [[homotopy groups]] of $O = O(n)$ are for $k \in \mathbb{N}$ and for $n\gt k+1$ (the "stable range") are

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
     \pi_{8k+7}(O) & = \mathbb{Z}
  }
  \,.
$$

In the unstable range for low $n$ they instead start out as follows 

| $G$ | $\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $SO(2)$ | $\mathbb{Z}$ |  0 | 0 |0 |0 |0 |0 |0 |0 |0 |0 |0 |
| $SO(3)$ | $\mathbb{Z}_2$ | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_{12}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{3}$ | $\mathbb{Z}_{15}$|$\mathbb{Z}_{2}$ |$\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}$ |
| $SO(4)$ | " | 0 | $\mathbb{Z} \oplus \mathbb{Z}$ | $\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}$ | $\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}$ | $\mathbb{Z}_{12} \oplus \mathbb{Z}_{12}$ | $\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}$ | $\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}$ | $\mathbb{Z}_{3} \oplus \mathbb{Z}_{3}$ | $\mathbb{Z}_{15}\oplus \mathbb{Z}_{15}$|$\mathbb{Z}_{2}\oplus \mathbb{Z}_{2}$ |$\mathbb{Z}_{2}^{\oplus 4}$ |
| $SO(5)$ | " | " | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | 0 | $\mathbb{Z}$ | 0 | 0 |$\mathbb{Z}_{120}$ | $\mathbb{Z}_{2}$ | $\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}$|
| $SO(6)$ | " | " | " | 0 | $\mathbb{Z}$ | 0 | $\mathbb{Z}$ | $\mathbb{Z}_{24}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_{120}\oplus\mathbb{Z}_2$| $\mathbb{Z}_{4}$| $\mathbb{Z}_{60}$|
| $SO(7)$ | " | " | " | " | 0 | 0 | $\mathbb{Z}$ | 0 | 0 | $\mathbb{Z}_{8}$| $\mathbb{Z}\oplus\mathbb{Z}_{12}$| 0|
| $SO(8)$ | " | " | " | " | " | 0 | $\mathbb{Z} \oplus \mathbb{Z}$ | $\mathbb{Z}_{2}^{\oplus 3}$ | $\mathbb{Z}_{2}^{\oplus 3}$ | $\mathbb{Z}_{24} \oplus \mathbb{Z}_{8}$ | $\mathbb{Z} \oplus \mathbb{Z}_{2}$ | 0 |
| $SO(9)$ | " | " | " | " | " | " | $\mathbb{Z}$ | $\mathbb{Z}_{2}\oplus \mathbb{Z}_{2}$ | $\mathbb{Z}_{2}\oplus \mathbb{Z}_{2}$ |$\mathbb{Z}_{8}$ | $\mathbb{Z}\oplus \mathbb{Z}_{2}$ | 0 |
|$SO(10)$| " | " | " | " | " | " | " | $\mathbb{Z}_{2}$ | $\mathbb{Z}\oplus \mathbb{Z}_{2}$ | $\mathbb{Z}_{4}$| $\mathbb{Z}$ | $\mathbb{Z}_{12}$ |
|$SO(11)$| " | " | " | " | " | " | " | " |$\mathbb{Z}_{2}$ |$\mathbb{Z}_{2}$ | $\mathbb{Z}$ | $\mathbb{Z}_{2}$ |
|$SO(12)$| " | " | " | " | " | " | " | " | " | 0 | $\mathbb{Z} \oplus \mathbb{Z}$ | $\mathbb{Z}\oplus \mathbb{Z}_{2}$ |

The $SO(6)$ row can be found using [Mimura-Toda 63](#MimuraToda63), using $Spin(6) = SU(4)$, and that $Spin(6)$ is a $\mathbb{Z}_2$-[[covering space]] of $SO(6)$. The $SO(7)$ row can be derived from the homotopy groups of $Spin(7)$ as found in [Mimura 67](#Mimura67). Otherwise the table is given in columns $\pi_i$, $i=10,11,12$, and in rows $SO(n)$, $n=8,\ldots,12$, by the [[Encyclopedic Dictionary of Mathematics]], Table 6.VII in Appendix A.

### Homology and cohomology 

([Pittie 91](#Pittie91))

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

## Related concepts

* [[stable orthogonal group]]

 $\cdots\to$ [[fivebrane group]] $\to$ [[string group]] $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ **orthogonal group**

[[!include table of orthogonal groups and related]]

## References

Examples of sporadic (exceptional) [[isogenies]] from [[spin groups]] onto orthogonal groups are discussed in

* [[Paul Garrett]], _Sporadic isogenies to orthogonal groups_, July 2013 ([pdf](http://www.math.umn.edu/~garrett/m/v/sporadic_isogenies.pdf))

The [[homotopy groups]] of $O(n)$ are listed for instance in 

* {#Abanov09} Alexander Abanov, Homotopy groups of Lie groups 2009 ([pdf](http://felix.physics.sunysb.edu/~abanov/Teaching/Spring2009/Notes/abanov-cpA1-upload.pdf))
  
* {#MimuraToda63} M. Mimura and H. Toda, _Homotopy Groups of $SU(3)$, $SU(4)$ and $Sp(2)$_, J. Math. Kyoto Univ. Volume 3, Number 2 (1963), 217-250. ([Euclid](http://projecteuclid.org/euclid.kjm/1250524818))

* {#Mimura67} M. Mimura, _The Homotopy groups of Lie groups of low rank_, Math. Kyoto Univ. Volume 6, Number 2 (1967), 131-176. ([Euclid](http://projecteuclid.org/euclid.kjm/1250524375))

The [[ordinary cohomology]] and [[ordinary homotopy]] of the manifolds $SO(n)$ is discussed in 

* {#Pittie91} Harsh V. Pittie, _The integral homology and cohomology rings of SO(n) and Spin(n)_, Journal of Pure and Applied Algebra Volume 73, Issue 2, 19 August 1991, Pages 105&#8211;153 ([web](http://www.sciencedirect.com/science/article/pii/002240499190108E))



[[!redirects orthogonal groups]]