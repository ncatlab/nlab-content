
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The ordinary _Chern classes_ are the [[integral cohomology|integral]] [[characteristic classes]] 

$$
  c_i : B U \to B^{2 i} \mathbb{Z}
$$

of the [[classifying space]] $B U$ of the [[unitary group]].

Accordingly these are characteristic classes in [[ordinary cohomology]] of [[unitary group|U]]-[[principal bundles]] and hence of [[complex vector bundle]]

The first Chern class is the unique characteristic class of [[circle group]]-principal bundles.

The analogous classes for the [[orthogonal group]] are the [[Pontryagin classes]].

More generally, there are _[[generalized Chern classes]]_ for any [[complex oriented cohomology theory]] ([Adams 74](#Adams74), [Lurie 10](#Lurie10)).

## Definition

+-- {: .num_defn}
###### Definition

For $n \geq 1$ the Chern universal [[characteristic classes]] $c_i \in H^{2i}(B U(n), \mathbb{Z})$ of the [[classifying space]] $B U(n)$ of the [[unitary group]] are characterized as follows:

1. $c_0 = 1$ and $c_i = 0$ if $i \gt n$;

1. for $n = 1$, $c_1$ is the canonical generator of $H^2(B U(1), \mathbb{Z})\simeq \mathbb{Z}$;

1. under pullback along the inclusion $i : B U(n) \to B U(n+1)$ we have $i^* c_i^{(n+1)} = c_i^{(n)}$;

1. under the inclusion $B U(k) \times B U(l) \to B U(k+l)$ we have $i^* c_i = \sum_{j = 0}^i c_i \cup c_{j-i}$.

=--


## Properties

### General 

+-- {: .num_prop}
###### Proposition

The [[cohomology ring]] of $B U(n)$ is the [[polynomial]] algebra on the Chern classes:

$$
  H^\bullet(B U(n), \mathbb{Z})
  \simeq
  \mathbb{Z}(c_1, \cdots, c_n)
  \,.
$$

=--


### First Chern class

* The [[first Chern class]] of a bundle $P$ is the class of its [[determinant line bundle]] $det P$

  $$
    c_1(P) = [det P]
    \,.
  $$

  See [[determinant line bundle]] for more.

### Splitting principle and Chern roots
 {#SplittingPrinciple}


Under the [[splitting principle]] all Chern classes are determnined by [[first Chern classes]]: 

Write $i \colon T \simeq U(1)^n \hookrightarrow U(n)$ for the [[maximal torus]] inside the [[unitary group]], which is the [[subgroup]] of diagonal unitary matrices. Then 

$$
  H^\bullet(B T, \mathbb{Z}) \simeq H^\bullet(B U(1)^n, \mathbb{Z})
$$

is the [[polynomial ring]] in $n$ [[generators]] (to be thought of as the universal [[first Chern classes]] $c_i$ of each copy of $B U(1)$; equivalently as the [weights](group+character#RelationToChernRootsAndSplittingPrinciple) of the [[group characters]] of $U(n)$) which are traditionally written $x_i$:

$$
  H^\bullet(B U(1)^n, \mathbb{Z})  \simeq \mathbb{Z}[x_1, \cdots, x_n]
  \,.
$$

Write 

$$
  B i \;\colon\; B U(1)^n \to B U(n)
$$

for the induced map of [[deloopings]]/[[classifying spaces]], then the $k$-universal Chern class $c_k \in H^{2k}(B U(n), \mathbb{Z})$ is uniquely characterized by the fact that its pullbacl to $B U(1)^n$ is the $k$th [[elementary symmetric polynomial]] $\sigma_k$ applied to these first Chern classes:

$$
 (B i)^\ast (c_k) = \sigma_k(x_1, \cdots, x_n)
  \,.
$$

Equivalently, for $c = \sum_{i = 1}^n c_k$ the formal sum of all the Chern classes, and using the fact that the [[elementary symmetric polynomials]] $\sigma_k(x_1, \cdots, k_n)$ are the degree-$k$ piece in $(1+x_1) \cdots (1+x_n)$, this means that

$$
 (B i)^\ast (c) = (1+x_1) (1+ x_2) \cdots (1+ x_n)
  \,.
$$

Since here on the right the first Chern classes $x_i$ appear as the [[roots]] of the Chern polynomial, they are also called **Chern roots**.

See also at _[splitting principle -- Examples -- Complex vector bundles and their Chern roots](splitting+principle#ComplexVectorBundleAndTheirChernRoots)_.


## Related concepts 

* [[Chern root]]

* [[Pontryagin class]]

* [[Stiefel-Whitney class]]

* [[Chern character]]

In [[Yang-Mills theory]] field configurations with non-vanishing second Chern-class (and minimal energy) are called [[instanton]]s. The second Chern class is the _instanton number_ .

## References

Original articles include

* [[A. Grothendieck]], _La th&#233;orie des classes de Chern_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __86__ (1958), p. 137--154, [numdam](http://www.numdam.org/item?id=BSMF_1958__86__137_0)


Textbook accounts include

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], chapter IX of volume II of _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

* [[John Milnor]], [[Jim Stasheff|James D. Stasheff]], _Characteristic Classes_, Annals of Mathematics Studies 76, Princeton University Press (1974). 

* {#Kochmann96} [[Stanley Kochmann]], section 2.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


A brief introduction is in chapter 23, section 7 

* [[Peter May]], _A concise course in algebraic topology_ ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

For [[Conner-Floyd Chern classes]] in [[complex oriented cohomology theory]]:

* {#Adams74} [[Frank Adams]], part II.2 and part III.10 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, 2010, lecture 4 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf)) and lecture 5 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))



[[!redirects Chern classes]]

[[!redirects second Chern class]] 

[[!redirects Chern root]]
[[!redirects Chern roots]]