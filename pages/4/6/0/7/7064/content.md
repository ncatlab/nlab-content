
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Homotopy groups of spheres
* table of contents
{: toc}

***

> With all due respect to anyone interested in them, the stable homotopy groups of spheres are a mess. ([[Stable homotopy and generalised homology|J. F. Adams 74, p 204]])

> My initial inclination was to call this book _[[The Music of the Spheres]]_, but I was dissuaded from doing so by my diligent publisher, who is ever mindful of the sensibilities of librarians. ([D. Ravenel 86, preface](#Ravenel86))

***

## Idea

The [[homotopy groups]] of [[spheres]] $\pi_{n+k}(S^n)$ are the [[homotopy classes]] of maps $S^{n+k} \longrightarrow S^n$

$$
  \pi_{n+k}(S^n) \coloneqq [S^k, S^n]
  \,.
$$

For fixed $k$, the [[colimit]] over $n$ with respect to the [[suspension]] homomorphism

$$
  \pi_{n+k}(S^n) \longrightarrow \pi_{n+k+1}(S^{n+1})
$$

over all $\pi_{n+k}(S^n)$ (called the $k$-[[stem]]) is called the _[[stable homotopy groups]] of spheres_ (also: the "stable $k$-[[stem]]")

$$
  \pi_k^S = \coloneqq \underset{\longrightarrow}{\lim}_n \pi_{n+k}(S^n)  
 \,.
$$

In fact, by the [[Freudenthal suspension theorem]], the value of the $\pi_{n+k}(S^n)$ stabilizes for $n \gt k+1$ (depend only on $k$ in this range), whence the name.

The [[stable homotopy groups]] of sphere are equivalently the [[homotopy groups of a spectrum]] for the [[sphere spectrum]] $\mathbb{S}$

$$
  \pi_k^S = \pi_k(\mathbb{S})
  \,.
$$

The stable homotopy groups of spheres are notorious for their immense computational richness. Many of the tools of [[algebraic topology]] and [[stable homotopy theory]] were devised to compute more and more of the stable stems. This notably include the [[Adams spectral sequence]], the [[Adams-Novikov spectral sequence]].

## Tables
 {#Tables}

The first stable homotopy groups of the [[sphere spectrum]] $\mathbb{S}$ are

| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | $\cdots$ | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S}) = $ | $\mathbb{Z}$  | $\mathbb{Z}_2$  |  $\mathbb{Z}_2$ |  $\mathbb{Z}_{24}$ |  $0$ |  $0$ | $\mathbb{Z}_2$ |   $\mathbb{Z}_{240}$ | $(\mathbb{Z}_2)^2$ |  $(\mathbb{Z}_2)^3$ | $\mathbb{Z}_6$ | $\mathbb{Z}_{504}$ | $0$ | $\mathbb{Z}_3$ | $(\mathbb{Z}_2)^2$ | $\mathbb{Z}_{480} \oplus \mathbb{Z}_2$ | $\cdots$ |

The following tables show the [[p-primary group|p-primary decomposition]] of these and the following stable homotopy groups.

The horizontal index is the degree $n$ of the stable homotopy group $\pi_n$. The appearance of a string of $k$ connected dots vertically above index $n$ means that there is a [[direct sum|direct summand]] [[primary group]] of [[order of a group|order]] $p^k$. The bottom rows in each case are given by the [[image of the J-homomorphism]].

See at _[fundamental theorem of finitely generated abelian grouops -- Graphical representation](fundamental+theorem+of+finitely+generated+abelian+groups#GraphicalRepresentation)_ for details on the notation used in these table, and  see example \ref{InterpretTable} below for illustration.

(the following graphics are taken from [Hatcher's website](http://www.math.cornell.edu/~hatcher/), based on  ([Ravenel 86](#Ravenel86))


**$p = 2$-primary component**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D2pic.gif" alt="stable homotopy groups of spheres at 2" width="800" />


**$p = 3$-primary component**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D3pic.gif" alt="stable homotopy groups of spheres at 3" width="800" />


**$p = 5$-primary component**

<img src="http://www.math.cornell.edu/~hatcher/stemfigs/p%3D5pic.gif" alt="stable homotopy groups of spheres at 5" width="800" />


+-- {: .num_example #InterpretTable}
###### Example


The [[finite abelian group]] $\pi_3(\mathbb{S}) \simeq \mathbb{Z}_{24}$ decomposes into [[primary groups]] as $\simeq \mathbb{Z}_8 \oplus \mathbb{Z}_3$. Here $8 = 2^3$ corresponds to the three dots above $n = 3$ in the first table, and $3 = 3^1$ to the single dot over $n = 3$ in the second.

The [[finite abelian group]] $\pi_7(\mathbb{S}) \simeq \mathbb{Z}_{24}$ decomposes into [[primary groups]] as $\simeq \mathbb{Z}_{16} \oplus \mathbb{Z}_3 \oplus \mathbb{Z}_5$. Here $16 = 2^4$ corresponds to the four dots above $n = 7$ in the first table, and $3 = 3^1$ to the single dot over $n = 7$ in the second and $5 = 5^1$ to the single dot over $n = 7$ in the third table.


=--



## Properties

### Serre finiteness theorem

+-- {: .num_theorem }
###### Theorem
**([[Serre finiteness theorem]])**

The [[homotopy group]] $\pi_{n+k}(S^k)$ is a [[finite group]] except

1. for $n = 0$ in which case $\pi_k(S^k) = \mathbb{Z}$;

1. $k = 2m$ and $n = 2m -1$ in which case

   $$
     \pi_{4m - 1}(S^{2m}) \simeq \mathbb{Z} \oplus F_m
   $$

   for $F_m$ a [[finite group]].

=--

([Serre 53](#Serre53))

### Nishida nilpotence theorem

The [[Nishida nilpotence theorem]]...

### Relation to the framed bordism ring
 {#RelationToFramedBordismRing}

By [[Thom's theorem]], for any [[(B,f)-structure]] $\mathcal{B}$, there is an [[isomorphism]] (of [[commutative rings]])

$$
  \Omega^{\mathcal{B}}_\bullet
  \overset{\simeq}{\longrightarrow}
  \pi_\bullet(M\mathcal{B})
$$

from the [[cobordism ring]] of manifolds with stable normal $\mathcal{B}$-structure to the [[homotopy groups of a spectrum|homotopy groups]] of the universal $\mathcal{B}$-[[Thom spectrum]]. 

Now for $\mathcal{B} = Fr$ [[framing]] structure, then 

$$
  M Fr \simeq \mathbb{S}
$$

is equivalently the [[sphere spectrum]]. Hence in this case [[Thom's theorem]] states that there is an isomorphism

$$
  \Omega^{fr}_\bullet
  \overset{\simeq}{\longrightarrow}
  \pi_\bullet(\mathbb{S})
$$

between the framed cobordism ring and the stable homotopy groups of spheres.

For discussion of computation of $\pi_\bullet(\mathbb{S})$ this way, see for instance ([Wang-Xu 10, section 2](#WangXu10)) and ([Putnam](#Putnam)).

For instance 

* $\Omega^{fr}_0 = \mathbb{Z}$ because there are two $k$-framings on a single point, corresponding to $\pi_0(O(k)) \simeq \mathbb{Z}_2$, the negative of a point with one framing is the point with the other framing, and so under disjoint union, the framed points form the group of integers;

* $\Omega^{fr}_1 = \mathbb{Z}_2$ because the only compact connected 1-manifold is the circle, there are two framings on the circle, corresponding to $\pi_1(O(k)) \simeq \mathbb{Z}_2$ and they are their own negatives.


### J-homomorphism and Adams e-invariant

The following characterizes the [[image]] of the [[J-homomorphism]] 

$$
  J \;\colon\; \pi_\bullet(O) \longrightarrow \pi_\bullet(\mathbb{S})
$$

from the [[homotopy groups]] of the [[stable orthogonal group]] to the stable homotopy groups of spheres. This was first conjectured in ([Adams 66](#Adams66)) (since called the _Adams conjecture_) and then proven in ([Quillen 71](#Quillen71)).

+-- {: .num_remark}
###### Remark

By the discussion at _[orthogonal group -- homotopy groups](orthogonal%20group#HomotopyGroups)_ we have that the [[homotopy groups]] of the [[stable orthogonal group]] are 

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| $\pi_n(O)$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ |0 | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ |

Because all groups appearing here and in the following are [[cyclic groups]], we instead write down the [[order of a group|order]]

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| ${\vert\pi_n(O)\vert}$ | 2 | 2 | 1 | $\infty$ | 1 | 1 | 1 | $\infty$ |

=--

+-- {: .num_theorem}
###### Theorem

The [[stable homotopy groups of spheres]] $\pi_n(\mathbb{S})$ are the [[direct sum]] of the ([[cyclic group|cyclic]]) [[image]] of the 
[[J-homomorphism]], and the [[kernel]] of the [[Adams e-invariant]].

Moreover,

* for $n = 0 \;mod \;$ and $n = 1 \;mod \; 8$ and $n$ positive the J-homomorphism is [[injection|injective]], hence its image is $\mathbb{Z}_2$, 

* for $n = 3\; mod\; 8$ and $n = 7 \; mod \; 8$ hence for $n = 4 k -1$, the [[order of a group|order]] of the image is equal to the [[denominator]] of $B_{2k}/4k$, where $B_{2k}$ is the [[Bernoulli number]]

* for all other cases the image is necessarily zero.

=--

[[!include image of J -- table]]


## Related concepts

* [[EHP spectral sequence]]

* [[Adams–Novikov spectral sequence]]

* [[The Music of the Spheres]]

## References

### General

Introductions and surveys include

* Alex Writght, _Homotopy groups of spheres: A very basic introduction_ ([pdf](http://web.stanford.edu/~amwright/HomotopyGroupsOfSoheres.pdf))

* {#WangXu10} [[Guozhen Wang]], Zhouli Xu _A survey of computations of homotopy groups of Spheres and Cobordisms_, 2010 ([pdf](http://math.mit.edu/~guozhen/homotopy%20groups.pdf))

* {#Putnam} [[Andrew Putman]], _Homotopy groups of spheres and low-dimensional topology_ ([pdf](http://www.math.rice.edu/~andyp/notes/HomotopySpheresLowDimTop.pdf))

* {#Hatcher} [[Alan Hatcher]], _Stable homotopy groups of spheres_ ([html](http://www.math.cornell.edu/~hatcher/stemfigs/stems.html))

* [[Mark Mahowald]], [[Doug Ravenel]], _Towards  a Global Understanding of the Homotopy Groups of Spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/global.pdf))

* [[Haynes Miller]], [[Doug Ravenel]], _Mark Mahowald's work on the homotopy groups of spheres_ ([pdf](http://www-math.mit.edu/~hrm/ksem/miller-ravenel.pdf))


* [[eom]], _[Spheres, homotopy groups of the](http://www.encyclopediaofmath.org/index.php/Spheres,_homotopy_groups_of_the)_

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, since 1986 ([web](http://www.math.rochester.edu/people/faculty/doug/mu.html))
 
* [[Stanley Kochmann]], _Stable Homotopy Groups of Spheres -- A Computer-Assisted Approach_, Lecture Notes in Mathematics, 1990

* {#Kochmann96} [[Stanley Kochmann]], section 5 of  of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

A tabulation of stable homotopy groups of spheres is in 

* [[Doug Ravenel]], Appendix 3 of _[[Complex cobordism and stable homotopy groups of spheres]]_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA3.pdf))

Original articles on basic properties include

* {#Serre53} [[Jean-Pierre Serre]] _Groupes d'homotopie et classes de groupes abelien_, Ann. of Math. 58 (1953), 258&#8211;294.
 


See also

* Wikipedia, _[Homotopy groups of spheres](http://en.wikipedia.org/wiki/Homotopy_groups_of_spheres)_

* MO, _[Computational complexity of computing homotopy groups of spheres](http://mathoverflow.net/questions/31004/computational-complexity-of-computing-homotopy-groups-of-spheres)_


### Image of the J-homomorphism

Discussion of the [[image]] of the [[J-homomorphism]] is due to

* {#Adams66} [[John Adams]], _On the groups $J(X)$ IV_, Topology 5: 21,(1966)  _Correction_, Topology 7 (3): 331 (1968)
 

* {#Quillen71} [[Daniel Quillen]], _The Adams conjecture_, Topology. an International Journal of Mathematics 10: 67&#8211;80 (1971)
 


### Formalization in homotopy type theory

For formalization in [[homotopy type theory]] see at

* [[UF-IAS-2012]], _[HomotopyGroupsOfSpheres](http://uf-ias-2012.wikispaces.com/HomotopyGroupsOfSpheres)_

* {#Brunerie16} [[Guillaume Brunerie]], _On the homotopy groups of spheres in homotopy type theory_ ([arXiv:1606.05916](http://arxiv.org/abs/1606.05916))






[[!redirects homotopy group of a sphere]]
[[!redirects homotopy groups of a sphere]]
[[!redirects homotopy groups of spheres]]
[[!redirects stable homotopy groups of spheres]]