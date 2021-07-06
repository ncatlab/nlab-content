
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

For $n \geq 1$ the _[[universal characteristic classes|universal]] Chern [[characteristic classes|classes]]_ 

$$
  c_i 
    \;\in\; 
  H^{2i}
  \big(
    B U(n), \mathbb{Z}
  \big)
$$ 

of the [[classifying space]] $B U(n)$ of the [[unitary group]] are the [[cohomology classes]] of $B U(n)$ in [[integral cohomology]] that are characterized as follows:

1. $c_0 = 1$ and $c_i = 0$ if $i \gt n$;

1. for $n = 1$, $c_1$ is the canonical generator of $H^2(B U(1), \mathbb{Z})\simeq \mathbb{Z}$;

1. under pullback along the inclusion $i : B U(n) \to B U(n+1)$ we have $i^* c_i^{(n+1)} = c_i^{(n)}$;

1. under the inclusion $B U(k) \times B U(l) \to B U(k+l)$ we have $i^* c_i = \sum_{j = 0}^i c_i \cup c_{j-i}$.

The corresponding _total Chern class_ is the formal sum

$$
  c 
  \;\coloneqq\;
  1 + c_1 + c_2 + \cdots
  \;\in\;
  \underset{k}{\prod} 
  H^{2k}
  \big(
    B U(n)
  \big)
$$

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

Moreover, for $B i \colon B U(n_1) \longrightarrow BU(n_2)$ the canonical inclusion for $n_1 \leq n_2 \in \mathbb{N}$, then the induced pullback map on cohomology 

$$
   (B i)^\ast 
     \;\colon\;
   H^\bullet(B U(n_2))
     \longrightarrow
   H^\bullet(B U(n_1))
$$

is given by

$$
  (B i)^\ast(c_k)
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

(e.g. [Kochman 96, theorem 2.3.1](#Kochman96))

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
   \overset{(B i)^\ast}{\longrightarrow}
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
   \overset{(B i)^\ast}{\longrightarrow}
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
   \overset{(B i)^\ast}{\longrightarrow}
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
   \overset{(B i)^\ast}{\longrightarrow}
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
   \overset{(B i)^\ast}{\longrightarrow}
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

### Top Chern class
 {#TopChernClass}

For $\mathcal{V}_X$ a [[complex vector bundle]] of complex [[rank]] $n$, the highest degree [[Chern class]] that may generally be non-vanishing is $c_n$. This is hence often called the _[[top Chern class]]_ of the vector bundle.

\begin{prop}
  The [[top Chern class]] of a [[complex vector bundle]] $\mathcal{V}_X$ equals the [[Euler class]] $e$ of the underlying [[real vector bundle]] $\mathcal{V}^{\mathbb{R}}_X$:

$$
  \mathcal{V}_X
  \;
  \text{has complex rank}\;n
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;   
  c_n
  \big(
    \mathcal{V}_X
  \big)
  \;\;
    =
  \;\;
  e
  \big(
    \mathcal{V}^{\mathbb{R}}_X
  \big)
  \;\;\;\;
  \in
  H^{2n}
  \big(
   X; 
   \,
   \mathbb{Z} 
  \big)
  \,.
$$
\end{prop}

(e.g. [Bott-Tu 82 (20.10.6)](#BottTu82))

\begin{prop}
  The [[top Chern class]] of a [[complex vector bundle]] $\mathcal{V}_X$ equals the [[pullback in cohomology|pullback]] of any [[Thom class]] 
$th \;\in\; H^{2n}\big( \mathcal{V}_X; \mathbb{Z} \big)$ on $\mathcal{V}_X$ along the [[zero-section]]:

$$
  \mathcal{V}_X
  \;
  \text{has complex rank}\;n
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;   
  c_n
  \big(
    \mathcal{V}_X
  \big)
  \;\;\;  
    =
  \;\;\;
  (0_X)^\ast
  (th)
  \;\;
  \in
  \;
  H^{2n}
  \big(
    X ;
    \,
    \mathbb{Z}
  \big)
$$
\end{prop}

(e.g. [Bott-Tu 82, Prop. 12.4](#BottTu82))


### Splitting principle and Chern roots
 {#SplittingPrinciple}


Under the [[splitting principle]] all Chern classes are determined by [[first Chern classes]]: 

Write $i \colon T \simeq U(1)^n \hookrightarrow U(n)$ for the [[maximal torus]] inside the [[unitary group]], which is the [[subgroup]] of [[diagonal matrix|diagonal]] unitary matrices. Then 

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

(e.g. [Kochman 96, theorem 2.3.2](#Kochman96), [tom Dieck 08, theorem 19.3.2](#tomDieck08))

+-- {: .num_lemma #FromBUnTOBU1nPullbackInCohomologyIsInjective}
###### Lemma

For $n \in \mathbb{N}$ let $B \iota_n \;\colon\; B (U(1)^n) \longrightarrow B U(n)$ be the canonical map. Then the induced pullback operation on [[ordinary cohomology]]

$$
  \left( 
    B \iota_n
  \right)
  \;\colon\;
   H^\bullet( B U(n); \mathbb{Z} )
   \longrightarrow
   H^\bullet( B U(1)^n; \mathbb{Z} )
$$

is a [[monomorphism]].

=--

A **[[proof]]** of lemma \ref{FromBUnTOBU1nPullbackInCohomologyIsInjective}, via analysis of the [[Serre spectral sequence]] of $U(n)/U(1)^n \to B U(1)^n \to B U(n)$ is indicated in ([Kochman 96, p. 40](#Kochman96)). A proof via [[Becker-Gottlieb transfer|transfer]] of the [[Euler class]] of $U(n)/U(1)^n$, following ([Dupont 78, (8.28)](#Dupont78)), is indicated at _[[splitting principle]]_ ([here](splitting+principle#InjectivityOfPullbackInCohomologyToBT)).

 

+-- {: .num_prop #SplittingPrincipleForChernClasses}
###### Proposition

For $k \leq n \in \mathbb{N}$ let $B \iota_n \;\colon\; B (U(1)^n) \longrightarrow B U(n)$ be the canonical map. Then the induced pullback operation on [[ordinary cohomology]] is of the form 

$$
  (B i_n)^\ast 
  \;\colon\;
  \mathbb{Z}[c_1, \cdots, c_k]
  \longrightarrow
  \mathbb{Z}[(c_1)_1,\cdots (c_1)_n]
$$

and sends the $k$th Chern class $c_k$ (def. \ref{GeneratorsOfCohomologyOfBunChernClasses}) to the $k$th [[elementary symmetric polynomial]] in the $n$ copies of the [[first Chern class]]:

$$
  (B i_n)^\ast 
    \;\colon\;
  c_k \mapsto \sigma_k( (c_1)_1, \cdots, (c_1)_n )
  \,.
$$

=--

+-- {: .proof}
###### Proof

First consider the case $n = 1$.

The [[classifying space]] $B U(1)$ is equivalently the infinite [[complex projective space]] $\mathbb{C}P^\infty$. Its [[ordinary cohomology]] is the [[polynomial ring]] on a single generator $c_1$, the [[first Chern class]] ([prop.](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace))

$$
  H^\bullet(B U(1))
    \simeq
  \mathbb{Z}[ c_1 ]
  \,.
$$

Moreover, $B i_1$ is the identity and the statement follows.

Now by the [[Künneth theorem]] for ordinary cohomology ([prop.](K%C3%BCnneth+theorem#KunnethInOrdinaryCohomology)) the cohomology of the [[Cartesian product]] of $n$ copies of $B U(1)$ is the [[polynomial ring]] in $n$ generators

$$
  H^\bullet(B U(1)^n)
   \simeq
  \mathbb{Z}[(c_1)_1, \cdots, (c_1)_n]
  \,.
$$

By prop. \ref{GeneratorsOfCohomologyOfBunChernClasses} the domain of $(B i_n)^\ast$ is the [[polynomial ring]] in the Chern classes $\{c_i\}$, and by the previous statement the codomain is the polynomial ring on $n$ copies of the first Chern class

$$
  (B i_n)^\ast
    \;\colon\;
   \mathbb{Z}[ c_1, \cdots, c_n ]
     \longrightarrow
   \mathbb{Z}[ (c_1)_1, \cdots, (c_1)_n ]
  \,.
$$

This allows to compute $(B i_n)^\ast(c_k)$ by [[induction]]:

Consider $n \geq 2$ and assume that $(B i_{n-1})^\ast_{n-1}(c_k) = \sigma_k((c_1)_1, \cdots, (c_1)_{(n-1)})$. We need to show that then also $(B i_n)^\ast(c_k) = \sigma_k((c_1)_1,\cdots, (c_1)_n)$.

Consider then the [[commuting diagram]]

$$
  \array{
    B U(1)^{n-1}
      &\overset{ B i_{n-1} }{\longrightarrow}&
    B U(n-1)
    \\
    {}^{\mathllap{B j_{\hat t}}}\downarrow
      &&
    \downarrow^{\mathrlap{B i_{\hat t}}}
    \\
    B U(1)^n
     &\underset{B i_n}{\longrightarrow}&
    B U(n)
  }
$$

where both vertical morphisms are induced from the inclusion

$$
  \mathbb{C}^{n-1} \hookrightarrow \mathbb{C}^n
$$

which omits the $t$th coordinate.

Since two embeddings $i_{\hat t_1}, i_{\hat t_2} \colon U(n-1) \hookrightarrow U(n)$ differ by [[conjugation]] with an element in $U(n)$, hence by an [[inner automorphism]], the maps $B i_{\hat t_1}$ and $B_{\hat i_{t_2}}$ are [[homotopy|homotopic]], and hence $(B i_{\hat t})^\ast = (B i_{\hat n})^\ast$, which is the morphism from prop. \ref{GeneratorsOfCohomologyOfBunChernClasses}.

By that proposition, $(B i_{\hat t})^\ast$ is the identity on $c_{k \lt n}$ and hence by induction assumption

$$
  \begin{aligned}
    (B i_{n-1})^\ast (B i_{\hat t})^\ast c_{k \lt n}
    &=
    (B i_{n-1})^\ast c_{k \lt n}
    \\
    = 
    \sigma_k( (c_1)_1, \cdots, \widehat{(c_1)_t}, \cdots, (c_1)_n )
  \end{aligned}
  \,.
$$

Since pullback along the left vertical morphism sends $(c_1)_t$ to zero and is the identity on the other generators, this shows that

$$
  (B i_n)^\ast(c_{k \lt n})
    \simeq
   \sigma_{k\lt n}((c_1)_1, \cdots, \widehat{(c_1)_t}, \cdots, (c_1)_n)
   \;\;
   mod (c_1)_t
  \,.
$$

This implies the claim for $k \lt n$. 

For the case $k = n$ the commutativity of the diagram and the fact that the right map is zero on $c_n$ by prop. \ref{GeneratorsOfCohomologyOfBunChernClasses} shows that the element $(B j_{\hat t})^\ast (B i_n)^\ast c_n = 0$ for all $1 \leq t \leq n$. But by lemma \ref{FromBUnTOBU1nPullbackInCohomologyIsInjective} the morphism $(B i_n)^\ast$, is injective, and hence $(B i_n)^\ast(c_n)$ is non-zero. Therefore for this to be annihilated by the morphisms that send $(c_1)_t$ to zero, for all $t$, the element must be proportional to all the $(c_1)_t$. By degree reasons this means that it has to be the product of all of them

$$
  \begin{aligned}
    (B i_n)^{\ast}(c_n) 
     & = (c_1)_1 \otimes (c_1)_2 \otimes \cdots \otimes (c_1)_n
     \\
     & = \sigma_n( (c_1)_1, \cdots, (c_1)_n )
  \end{aligned}
  \,.
$$

This completes the induction step.

=--

### Whitney sum formula
 {#WhitneySumFormula}

+-- {: .num_prop #WhitneySumChernClasses}
###### Proposition

For $k\leq n \in \mathbb{N}$, consider the canonical map

$$
  \mu_{k,n-k}
    \;\colon\;
  B U(k) \times B U(n-k)
    \longrightarrow
  B U(n)
$$

(which classifies the [[Whitney sum]] of [[complex vector bundles]] of [[rank]] $k$ with those of rank $n-k$). Under pullback along this map the universal [[Chern classes]] (prop. \ref{GeneratorsOfCohomologyOfBunChernClasses}) are given by

$$
  (\mu_{k,n-k})^\ast(c_t)
  \;=\;
  \underoverset{i = 0}{t}{\sum} c_i \otimes c_{t-i}
  \,,
$$

where we take $c_0 = 1$ and  $c_j = 0 \in H^\bullet(B U(r))$ if $j \gt r$.

So in particular

$$
  (\mu_{k,n-k})^\ast(c_n) \;=\; c_k \otimes c_{n-k}
  \,.
$$

=--

e.g. ([Kochman 96, corollary 2.3.4](#Kochman96)) 

+-- {: .proof}
###### Proof

Consider the [[commuting diagram]]

$$
  \array{
    H^\bullet( B U(n) )
      &\overset{\mu_{k,n-k}^\ast}{\longrightarrow}&
    H^\bullet( B U(k) ) \otimes H^\bullet( B U(n-k) )
    \\
    {}^{\mathllap{\mu_k^\ast}}\downarrow
      &&
    \downarrow^{\mathrlap{ \mu_{k}^\ast \otimes \mu_{n-k}^\ast }}
    \\
    H^\bullet( B U(1)^n )
     &\simeq&
    H^\bullet( B U(1)^k ) \otimes H^\bullet( B U(1)^{n-k} )
  }
  \,.
$$

This says that for all $t$ then

$$
  \begin{aligned}
    (\mu_k^\ast \otimes \mu_{n-k}^\ast) \mu_{k,n-k}^\ast(c_t)
    & =
    \mu^\ast_n(c_t)
    \\
    & = \sigma_t((c_1)_1, \cdots, (c_1)_n)
  \end{aligned}
  \,,
$$

where the last equation is by prop. \ref{SplittingPrincipleForChernClasses}. 

Now the [[elementary symmetric polynomial]] on the right decomposes as required by the left hand side of this equation as follows:

$$
  \sigma_t((c_1)_1, \cdots, (c_1)_n)
    \;=\; 
  \underoverset{r = 0}{t}{\sum}
  \sigma_r((c_1)_1, \cdots, (c_1)_{n-k})
  \cdot
  \sigma_{t-r}( (c_1)_{n-k+1}, \cdots, (c_1)_n )
  \,,
$$

where we agree with $\sigma_q((c_1)_1, \cdots, (c_1)_p) = 0$ if $q \gt p$. It follows that

$$
  (\mu_k^\ast \otimes \mu_{n-k}^\ast) \mu_{k,n-k}^\ast(c_t)
  = 
  (\mu_k^\ast \otimes \mu_{n-k}^\ast)
  \left(
    \underoverset{r=0}{t}{\sum} c_r \otimes c_{t-r}
  \right)
  \,.
$$

Since $(\mu_k^\ast \otimes \mu_{n-k}^\ast)$ is a monomorphism by lemma \ref{FromBUnTOBU1nPullbackInCohomologyIsInjective}, this implies the claim.

=--

## Examples

### Chern classes of linear representations
 {#ChernClassesOfLinearRepresentations}

Under the [[Atiyah-Segal completion]] map [[linear representations]] of a [[group]] $G$ induce K-theory classes on the [[classifying space]] $B G$. Their Chern classes are hence invariants of the [[linear representations]] themselves.

See at _[[characteristic class of a linear representation]]_ for more.

## Related concepts 

* [[Chern root]]

* [[Pontryagin class]]

* [[Stiefel-Whitney class]]

* [[Chern character]]

In [[Yang-Mills theory]] field configurations with non-vanishing [[second Chern class]] (and minimal energy) are called [[instantons]]. The second Chern class is the _[[instanton number]]_ . For more on this see at _[SU(2)-instantons from the correct maths to the traditional physics story](BPST-instanton#FromTheMathsToThePhysicsStory)_.

## References

Original articles:

* {#Hirzebruch56} [[Friedrich Hirzebruch]], Chapter 1, Section 4 of: _Neue topologische Methoden in der Algebraischen Geometrie_, Ergebnisse der Mathematik und Ihrer Grenzgebiete. 1. Folge, Springer 1956 ([doi:10.1007/978-3-662-41083-7](https://www.springer.com/de/book/9783662406052))

* [[A. Grothendieck]], _La th&#233;orie des classes de Chern_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __86__ (1958), p. 137--154, ([numdam:BSMF_1958__86__137_0](http://www.numdam.org/item?id=BSMF_1958__86__137_0))



Textbook accounts:

* {#KobayashiNomizu63} [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], Section  XII.3 in: _Foundations of Differential Geometry, Volume 1_, Wiley 1963 ([web](https://www.zuj.edu.jo/download/foundations-of-differential-geometry-vol-1-kobayashi-nomizu-pdf/), [ISBN:9780471157335](https://www.wiley.com/en-us/Foundations+of+Differential+Geometry%2C+Volume+1-p-9780471157335), [Wikipedia](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry))


* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], chapter IX of volume II of _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

* [[John Milnor]], [[Jim Stasheff|James D. Stasheff]], _Characteristic Classes_, Annals of Mathematics Studies 76, Princeton University Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

* {#Kochman96} [[Stanley Kochman]], section 2.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#tomDieck08} [[Tammo tom Dieck]], _Algebraic topology_, EMS 2008

With an eye towards [[mathematical physics]]:

* {#RudolhSchmidt} Gerd Rudolph, Matthias Schmidt, Def. 4.2.2 of _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))


A brief introduction is in chapter 23, section 7 

* [[Peter May]], _A concise course in algebraic topology_ ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

For [[Conner-Floyd Chern classes]] in [[complex oriented cohomology theory]]:

* {#Adams74} [[Frank Adams]], part II.2 and part III.10 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, 2010, lecture 4 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf)) and lecture 5 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))

See also 

* {#Dupont78} Dupont, _Curvature and characteristic classes_, Springer 1978

* Timothy Hosgood, _Chern classes of coherent analytic sheaves: a simplicial
approach_.  Université d’Aix-Marseille (AMU), 2020. [tel-02882140](https://tel.archives-ouvertes.fr/tel-02882140).

A [[MathOverflow]] question discussing references: <https://mathoverflow.net/questions/345437/canonical-reference-for-chern-characteristic-classes>

[[!redirects Chern classes]]

[[!redirects universal Chern class]]
[[!redirects universal Chern classes]]

[[!redirects second Chern class]] 

[[!redirects Chern root]]
[[!redirects Chern roots]]

[[!redirects total Chern class]]
[[!redirects total Chern classes]]

