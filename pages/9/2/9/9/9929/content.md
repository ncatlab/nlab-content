
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

## Definition
 {#Definition}

### In terms of generalized first Chern classes
 {#DefInTermsOfGeneralizedFirstChernClass}

Write $\mathbb{C}P^\infty \simeq B U(1) \simeq K(\mathbb{Z},2)$ for the inifinite [[complex projective space]], equivalently the [[classifying space]] for [[circle group]]-[[principal bundles]] (an [[Eilenberg-MacLane space]]); write $S^2$ for the [[2-sphere]] and write

$$
  i \;\colon\; S^2 \longrightarrow B U(1)
$$

for a representative of $1 \in \mathbb{Z} \simeq  \pi_2(B U(1))$. Regard both $S^2$ and $B U(1)$ as [[pointed homotopy types]] and take $i$ to be a pointed morphism.

Let $E^\bullet$ be a [[multiplicative cohomology theory]], i.e. a [[functor]] $X \mapsto \pi_\bullet[X,E]$ for $E$ a [[ring spectrum]]. Write $\tilde E^\bullet$ for the corresponding [[reduced cohomology]] on [[pointed topological spaces]], such that for any pointed space $X$ there is a canonical [[direct sum]] decomposition ([this prop.](generalized+%28Eilenberg-Steenrod%29+cohomology#UnreducedCohomologyIsReducedPlusPointValue))

$$
  E^\bullet(X) \simeq \tilde E^\bullet(X) \oplus E^\bullet(\ast)
  \,.
$$

By the [[suspension isomorphism]] there is an identification

$$
  \tilde E^2(S^2) \simeq \tilde E^0(S^0) \simeq E^0(\ast) \simeq \pi_0(E)
$$

with the [[commutative ring]] underlying $E$. Write $1 \in \pi_0(E)$ for the multiplicative identity element in this ring.


+-- {: .num_defn}
###### Definition

A [[multiplicative cohomology theory]] $E$ is _complex orientable_ if the the following equivalent conditions hold

1. The morphism

   $$
     i^\ast \;\colon\; E^2(B U(1)) \longrightarrow E^2(S^2)
   $$

   is [[surjection|surjective]].

1. The morphism

   $$
     \tilde i^\ast \;\colon\; \tilde E^2(B U(1)) \longrightarrow \tilde E^2(S^2)
     \simeq \pi_0(E)
   $$

   is [[surjection|surjective]].

1. The element $1 \in \pi_0(E)$ is in the [[image]] of the morphism $\tilde i^\ast$.

=--


+-- {: .num_defn #ComplexOrientation}
###### Definition

A **complex orientation** on a [[multiplicative cohomology theory]] $E^\bullet$ is an element 

$$
  c_1^E \in \tilde E^2(B U(1))
$$

(the "first [[generalized Chern class]]") such that 

$$
  i^\ast c^E_1 = 1 \in \pi_0(E)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Since $B U(1) \simeq K(\mathbb{Z},2)$ is the [[classifying space]] for [[complex line bundles]], it follows that a complex orientation on $E^\bullet$ induces an $E$-[[generalized Chern class|generalization]] of the [[first Chern class]] which to a [[complex line bundle]] $\mathcal{L}$ on $X$ classified by $\phi \colon X \to B U(1)$ assigns the class $c_1(\mathcal{L}) \coloneqq \phi^\ast c_1^E$. This construction extends to a general construction of $E$-[[Chern classes]]. 

=--


### In terms of genera and $E_\infty$ orientations 
 {#InTermsOfGenera}

Complex orientation in the [above](#Definition) sense is indeed universal [[MU]]-[[orientation in generalized cohomology]]:

+-- {: .num_prop #ComplexOrientationIsMUAlgebraStructure}
###### Proposition

For $E$ an [[E-∞ ring]] then there is a [[bijection]] between [[equivalence classes]] of complex orientations of $E$-cohomology and [[E-∞ ring]]-[[homomorphisms]] $MU \longrightarrow E$ out of [[MU]], hence equivalence classes of choices of $MU$-[[E-∞ algebra]] structures on $E$.

=--

([Hopkins 99, section 4](#Hopkins99), [Lurie, lecture 6, theorem 8](#LurieLecture))


+-- {: .num_remark}
###### Remark

In terms of [[E-∞ geometry]]/[[spectral geometry]], prop. \ref{ComplexOrientationIsMUAlgebraStructure} says that complex orientation on $E$ is equivalently a morphism

$$
  Spec(E)\longrightarrow Spec(MU)
$$

exhibiting the affine [[E-∞ scheme]] $Spec(E)$ as sitting over $Spec(MU)$. By [[Quillen's theorem on MU]], 

=--

## Examples

Examples of complex orientable cohomology theories:


+-- {: .num_example }
###### Example

For $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]], the ordinary [[first Chern class]]

$$
  c_1 \in H^2(B U(1), \mathbb{Z})
$$

defines a complex orientation of $H\mathbb{Z}$.
=--

+-- {: .num_example #ComplexCobordism}
###### Example

For $E = MU$ [[complex cobordism cohomology theory]], the canonical map

$$
  B U(1) \stackrel{\simeq}{\to} MU(1) \to MU
$$ 

defines a complex orientation. 

=--

+-- {: .num_example #BrownPeterson}
###### Example

[[Brown-Peterson cohomology]] $E = B P^\bullet$.

=--



## Properties

### Cohomology ring of $B U(1)$ and its formal group law
 {#CohomologyRingOfBU1}

+-- {: .num_prop #CohomologyRingOfBU1}
###### Proposition

Given a complex oriented cohomology theory $(E^\bullet, c^E_1)$
we have

1. $E^\bullet(B U(1)) \simeq E^\bullet(\ast)[ [ c_1^E] ]$;

1. $E^\bullet(B U(1) \times B U(1)) \simeq E^\bullet(\ast)[ [ c_1^E \otimes 1 , 1 \otimes c_1^E ] ]$.


=--

See at _[complex projective space -- Properties -- Cohomology](complex+projective+space#Cohomology)_.

+-- {: .num_prop}
###### Proposition

Given a complex oriented cohomology theory $(E^\bullet, c_1)$, there is a [[formal group law]] $\mathcal{G}_E$ that describes the $E$-[[first Chern class]] under [[tensor product]] of [[complex line bundles]]:

$$
  c_1^E(\mathcal{L}_1 \otimes \mathcal{L}_2)
  =
  c_1^E(\mathcal{L}_1) +_{\mathcal{G}_E} c_1^E(\mathcal{L}_2)
  \,.
$$

=--

Under different choices of orientation, one obtains isomorphic formal group laws. (...)


+-- {: .num_prop}
###### Proposition

The [[formal group law]] of [[complex cobordism cohomology theory]], example \ref{ComplexCobordism} is [[universal property|universal]] in that for every [[commutative ring]] $R$ there is a [[natural bijection]]

$$
  CRing(MU^\ast, A)
  \simeq
  FormalGroupLaws_{/R}
  \,.
$$

$MU^\ast$ is the _[[Lazard ring]]_.

=--

This is [[Quillen's theorem on MU]]

+-- {: .num_prop}
###### Proposition

The [[formal group law]] of [[Brown-Peterson cohomology theory]], example \ref{BrownPeterson} is [[universal property|universal]] for $p$-local cohomology theories in that $\mathbb{G}_{B P}$ is universal among $p$-local, [[p-typical formal group laws]].

(...)

=--

### Cohomology ring of $B U(n)$
 {#TheCohomologyRingOfBUn}

+-- {: .num_prop #CohomologyRingOfBUn}
###### Proposition

For $E$ a complex oriented cohomology theory and $n \in \mathbb{N}$, restriction along the canonical map

$$
  (B U(1))^n  \longrightarrow B U(n)
$$

induces an [[isomorphism]]

$$
  E^\bullet(B U(n))
    \stackrel{\simeq}{\longrightarrow}
  (\pi_\bullet E)[ [ c^E_1, \cdots, c^E_n ] ]
  \simeq
  E^\bullet((B U(1))^n)^{\Sigma_n}
  \hookrightarrow
  E^\bullet((B U(1))^n)
  \simeq
  (\pi_\bullet E)[ [(c_1^E)_1, \cdots (c_1^E)_n ] ]  
  \,,
$$

of $E^\bullet(B U(n))$ with the [[cyclic group]]-[[invariants]] in $E^\bullet((B U(1))^n)$, hence with the [[power series]] ring in the [[elementary symmetric polynomials]] $c_i^E$ (the [[generalized Chern classes]]) in the $c_1^E$-s (the generalized first Chern classes of prop. \ref{CohomologyRingOfBU1}).

=--

Use [this proposition](ordinary+homology+spectra+split#WhenGeneralizedHomologySpectraSplit) to reduce to the situation for ordinary [[Chern classes]]. (e.g. [Lurie 10, lecture 4](#LurieLecture))

### Canonical orientation on complex vector bundles

The follows says that complex oriented cohomology theories in the sense of def. \ref{ComplexOrientation}, indeed canonically have an [[orientation in generalized cohomology]] for the ([[spherical fibration]] of) any [[complex vector bundle]].

+-- {: .num_prop #ThomSpaceOfZetan}
###### Proposition

For $E$ any [[cohomology theory]] and $n \in \mathbb{N}$, $n \geq 1$, there is a canonical [[isomorphism]] of [[relative cohomology]]

$$
  E^\bullet(B U(n), B U(n-1))
  \simeq
  E^\bullet( B( \zeta_n), S( \zeta_n) )
  \,,
$$

where $\zeta_n \coloneqq E U(n) \underset{U(n)}{\times} \mathbb{R}^{2n}$ is the [[universal complex vector bundle]].

=--

+-- {: .proof}
###### Proof

Observe that the [[sphere bundle]] $S(\zeta_n) \to B U(n)$ of the [[universal complex vector bundle]] is equivalently the canonical map $B U(n-1) \to B U(n)$. 

This follows form the fact that $S^{2n-1} \simeq U(n)/U(n-1)$ and that hence the unit sphere bundle is equivalently the quotient of the $U(n)$-[[universal principal bundle]] by $U(n-1)$

$$
  \array{
    U(n) &\longrightarrow& \ast
    \\
    && \downarrow
    \\
    && B U(n)
  }
  \;\;\;\; \stackrel{}{\mapsto}\;\;\;\;
  \array{
     S^{2n-1} \simeq & U(n)/U(n-1) &\longrightarrow& B U(n-1) 
     \\
     & && \downarrow 
     \\
     & &&  B U(n)
  }
  \,.
$$

The unit ball bundle $B(\zeta_n)$ is weakly equivalent to $B U(n)$, and under this identification the map $S(\zeta_n) \to B(\zeta_n)$ is equivalent to $B U(n-1) \to B U(n)$.

=--

+-- {: .num_prop }
###### Proposition

For $E$ a complex oriented cohomology theory,
its $n$th [[generalized Chern class]] $c^E_n$, prop. \ref{CohomologyRingOfBUn}, identified as an element of 
$E^\bullet(B(\zeta_n), S(\zeta_n))$ via prop. \ref{ThomSpaceOfZetan},
is a [[Thom class]].

=--

(e.g. [Lurie 10, lecture 5, prop. 6](#LurieLecture))

## Related concepts

* [[real oriented cohomology theory]]

* [[generalized (Eilenberg-Steenrod) cohomology theory]]

* [[multiplicative cohomology theory]]

* [[orientation in generalized cohomology]]

* [[complex cobordism cohomology theory]]

* [[Landweber exact functor theorem]]

* [[chromatic homotopy theory]]

[[!include chromatic tower examples - table]]

## References

* [[Frank Adams]], part II, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Hopkins99} [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_, 1999 course notes ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))


* {#LurieLecture} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes ([web](http://www.math.harvard.edu/~lurie/252x.html))

  Lecture 4 _Complex-oriented cohomology theories_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf))

  Lecture 6 _MU and complex orientations_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture6.pdf))

 
See also the references at _[equivariant cohomology -- References -- Complex oriented cohomology](equivariant+cohomology#InComplexOrientedGeneralizedCohomologyTheory)_-.

[[!redirects complex oriented cohomology theories]]

[[!redirects complex oriented cohomology]]

[[!redirects complex-oriented cohomology theory]]
[[!redirects complex-oriented cohomology theories]]

[[!redirects complex orientable cohomology theory]]
[[!redirects complex orientable cohomology theories]]