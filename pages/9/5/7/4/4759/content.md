
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

### Existence

+-- {: .num_prop #GeneratorsOfCohomologyOfBunChernClasses}
###### Proposition

The [[cohomology ring]] of the [[classifying space]] $B U(n)$ (for the [[unitary group]] $U(n)$) is the [[polynomial ring]] on generators $\{c_k\}_{k = 1}^{n}$ of degree 2, called the _Chern classes_

$$
  H^\bullet(B U(n), \mathbb{Z})
    \simeq
  \mathbb{Z}[c_1, \cdots, c_n]
  \,.
$$

Moreover, for $i \colon B U(n_1) \longrightarrow BU(n_2)$ the canonical inclusion for $n_1 \leq n_2 \in \mathbb{N}$, then the induced pullback map on cohomology 

$$
   i^\ast 
     \;\colon\;
   H^\bullet(B U(n_2))
     \longrightarrow
   H^\bullet(B U(n_1))
$$

is given by

$$
  i^\ast(c_k)
  \;=\;
  \left\{
    \array{
      c_k & for \; 1 \leq k \leq n_1
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

=--

(e.g. [Kochmann 96, theorem 2.3.1](#Kochmann96))

+-- {: .proof}
###### Proof

For $n = 1$, in which case $B U(1) \simeq \mathbb{C}P^\infty$ is the infinite [[complex projective space]], we have ([prop](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace))

$$
  H^\bullet(B U(1)) \simeq \mathbb{Z}[ c_1 ]
  \,,
$$

where $c_1$ is the [[first Chern class]]. From here we proceed by [[induction]]. So assume that the statement has been shown for $n-1$.

Observe that the canonical map $B U(n-1) \to B U(n)$ has as [[homotopy fiber]]  the [[n-sphere|(2n-1)sphere]] ([prop.](classifying+space#SphereFibrationOverInclusionOfClassifyingSpaces)) hence there is a [[homotopy fiber sequence]] of the form

$$
  S^{2n-1} \longrightarrow B U(n-1) \longrightarrow B U(n)
  \,.
$$

Consider the induced [[Thom-Gysin sequence]]. 

In odd degrees $2k+1 \lt 2n$ it gives the [[exact sequence]]

$$
  \cdots
   \to
  H^{2k}(B U(n-1))
   \longrightarrow
  \underset{\simeq 0}{\underbrace{H^{2k+1-2n}(B U(n))}}
   \longrightarrow
  H^{2k+1}(B U(n))
   \overset{i^\ast}{\longrightarrow}
  \underset{\simeq 0}{\underbrace{H^{2k+1}(B U(n-1))}}
  \to 
  \cdots
  \,,
$$

where the right term vanishes by induction assumption, and the middle term since [[ordinary cohomology]] vanishes in negative degrees. Hence

$$
  H^{2k+1}(B U(n)) \simeq 0 \;\;\; for \; 2k+1 \lt 2n
$$

Then for $2k+1 \gt 2n$ the Thom-Gysin sequence gives

$$
  \cdots
   \to
  H^{2k+1-2n}(B U(n))
   \longrightarrow
  H^{2k+1}(B U(n))
   \overset{i^\ast}{\longrightarrow}
  \underset{\simeq 0}{\underbrace{H^{2k+1}(B U(n-1))}}
  \to 
  \cdots
  \,,
$$

where again the right term vanishes by the induction assumption. Hence [[exact sequence|exactness]] now gives that 

$$
  H^{2k+1-2n}(B U(n))
   \overset{}{\longrightarrow}
  H^{2k+1}(B U(n))
$$

is an [[epimorphism]], and so with the previous statement it follows that 

$$
  H^{2k+1}(B U(n)) \simeq 0
$$

for all $k$.

Next consider the Thom Gysin sequence in degrees $2k$

$$
  \cdots
   \to
  \underset{\simeq 0}{\underbrace{H^{2k-1}(B U(n-1))}}
   \longrightarrow
  H^{2k-2n}(B U(n))
   \longrightarrow
  H^{2k}(B U(n))
   \overset{i^\ast}{\longrightarrow}
  H^{2k}(B U(n-1))
   \longrightarrow
  \underset{\simeq 0}{\underbrace{H^{2k +1 - 2n}(B U(n))}}
  \to 
  \cdots
  \,.
$$

Here the left term vanishes by the induction assumption, while the right term vanishes by the previous statement. Hence we have a [[short exact sequence]]

$$
  0   
   \to
  H^{2k-2n}(B U(n))
   \longrightarrow
  H^{2k}(B U(n))
   \overset{i^\ast}{\longrightarrow}
  H^{2k}(B U(n-1))
    \to
  0
$$

for all $k$. In degrees $\bullet\leq 2n$ this says

$$
  0   
   \to
  \mathbb{Z}
   \overset{c_n \cup (-)}{\longrightarrow}
  H^{\bullet \leq 2n}(B U(n))
   \overset{i^\ast}{\longrightarrow}
  (\mathbb{Z}[c_1, \cdots, c_{n-1}])_{\bullet \leq 2n}
    \to
  0
$$

for some [[Thom class]] $c_n \in H^{2n}(B U(n))$, which we identify with the next Chern class.

Since [[free abelian groups]] are [[projective objects]] in [[Ab]], their [[extensions]] are all split (the [[Ext]]-group out of them vanishes), hence the above gives a [[direct sum]] decomposition

$$
  \begin{aligned}
    H^{\bullet \leq 2n}(B U(n))
    & \simeq
    (\mathbb{Z}[c_1, \cdots, c_{n-1}])_{\bullet \leq 2n} \oplus \mathbb{Z}\langle 2n\rangle
    \\
    & \simeq
    (\mathbb{Z}[c_1, \cdots, c_{n}])_{\bullet \leq 2n}
  \end{aligned}
  \,.  
$$

Now by another induction over these short exact sequences, the claim follows. 

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

for the induced map of [[deloopings]]/[[classifying spaces]], then the $k$-universal Chern class $c_k \in H^{2k}(B U(n), \mathbb{Z})$ is uniquely characterized by the fact that its pullback to $B U(1)^n$ is the $k$th [[elementary symmetric polynomial]] $\sigma_k$ applied to these first Chern classes:

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

(e.g. [Kochmann 96, theorem 2.3.2](#Kochmann96))

+-- {: .proof}
###### Proof

The [[classifying space]] $B U(1)$ is equivalently the infinite [[complex projective space]] $\mathbb{C}P^\infty$. Its [[ordinary cohomology]] is the [[polynomial ring]] on a single generator $c_1$, the [[first Chern class]] ([prop.](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace))

$$
  H^\bullet(B U(1))
    \simeq
  \mathbb{Z}[ c_1 ]
  \,.
$$

Hence by the [[Künneth theorem]] for ordinary cohomology ([prop.](K%C3%BCnneth%20theorem#KunnethInOrdinaryCohomology)) the cohomology of the [[Cartesian product]] of $n$ copies of $B U(1)$ is the [[polynomial ring]] in $n$ generators

$$
  H^\bullet(B U(1)^n)
  \simeq
  \mathbb{Z}[(c_1)_1, \cdots, (c_1)_n]
  \,.
$$

Consider the canonical morphism 

$$
  \mu_n
   \;\colon\;
  B U(1)^n
   \longrightarrow
  B U(n)
$$

and the induced pullback operation in cohomology

$$
  \mu_n^\ast
    \;\colon\;
  H^\bullet( B U(n) )
    \longrightarrow
  H^\bullet( B U(1)^n)
  \,.
$$

By prop. \ref{GeneratorsOfCohomologyOfBunChernClasses} the domain is the [[polynomial ring]] in the Chern classes $\{c_i\}$, by the above the codomain is the polynomial ring on $n$ copies of the first Chern class

$$
  \mu_n^\ast
    \;\colon\;
   \mathbb{Z}[ c_1, \cdots, c_n ]
     \longrightarrow
   \mathbb{Z}[ (c_1)_1, \cdots, (c_1)_n ]
  \,.
$$

The hard part of the proof now is to show that: $\mu_n^\ast$ is a [[monomorphism]] (e.g. [Kochmann 96, p. 40](#Kochmann96)).


This allows to compute $\mu_n^\ast(c_k)$ by [[induction]].

First observe that for $n = 1$ then $\mu_1 = id$ is the identity and so $c_1 = (c_1)_1 = \sigma_1((c_1)_1)$, as it should be.

Hence consider $n \geq 2$ and assume that $\mu^\ast_{n-1}(c_k) = \sigma_k((c_1)_1, \cdots, (c_1)_{(n-1)})$. We need to show that then also $\mu_n^\ast(c_k) = \sigma_k((c_1)_1,\cdots, (c_1)_n)$.

Consider then the [[commuting diagram]]

$$
  \array{
    B U(1)^{n-1}
      &\overset{\mu'_{n-1}}{\longrightarrow}&
    B U(n-1)
    \\
    {}^{\mathllap{J'_t}}\downarrow
      &&
    \downarrow
    \\
    B U(1)^n
     &\underset{\mu_n}{\longrightarrow}&
    B U(n)
  }
$$

where the left vertical morphism is the inclusion that omits the $t$th factor of $U(1)$, and the top horizontal morphism is the composite of $J'_t$ with with the map $B U(1)^n \to B U(1)^{n-1} \overset{\mu_{n-1}}{\longrightarrow} B U(n-1)$, where the first map projects out the last copy of $U(1)$.

Since by induction assumption pullback along the right vertical morphism is an isomorphism on the classes $c_{k \leq n-1}$, the diagram gives for these that

$$
  \mu_n^\ast(c_{k \lt n})
   \simeq
   \sigma_{k\lt n}((c_1)_1, \cdots, \widehat{(c_n)_t}, \cdots, (c_1)_n)
   \;\;
   mod (c_1)_t
  \,.
$$

This implies the claim for $k \lt n$. 

For the case $k = n$ the commutativity of the diagram and the fact that the right map is zero on $c_n$ by prop. \ref{GeneratorsOfCohomologyOfBunChernClasses} shows that the element $(J'_t)^\ast \mu_n^\ast c_n = 0$ for all $1 \leq t \leq n$. But by injectivity of $\mu_n^\ast$, the element $\mu_n^\ast(c_n)$ itself is non-zero. Hence it must be proportional to all the $(c_1)_k$. By degree reasons this means that it has to be the product of all of them

$$
  \begin{aligned}
    \mu^{\ast}_n(c_n) 
     & = (c_1)_1 \otimes (c_1)_2 \otimes \cdots \otimes (c_1)_n
     \\
     & = \sigma_n( (c_1)_1, \cdots, (c_1)_n )
  \end{aligned}
  \,.
$$

This completes the induction step.

=--


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

[[!redirects universal Chern class]]
[[!redirects universal Chern classes]]

[[!redirects second Chern class]] 

[[!redirects Chern root]]
[[!redirects Chern roots]]
