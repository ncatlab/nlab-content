
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The classical _fracture theorem_ is a basic fact in [[number theory]]/[[arithmetic geometry]] and derived from this a fundamental result in  [[homotopy theory]], which says how working over the [[integers]] may be decomposed into working over the [[rational numbers]] and over the [[p-adic integers]], for all primes $p$.

### In number theory and arithmetic geometry
 {#ArithmeticFractureSquares}

The number theoretic statement is the following:

+-- {: .num_prop #ArithmeticFractureSquare}
###### Proposition

The [[integers]] $\mathbb{Z}$ are the [[fiber product]] of all the [[p-adic integers]] $\underset{p\;prime}{\prod} \mathbb{Z}_p$ with the [[rational numbers]] $\mathbb{Q}$ over the [[rationalization]] of the former, hence there is a [[pullback]] [[diagram]] in [[CRing]] of the form

$$
  \array{
     && \mathbb{Q}
     \\
     & \swarrow && \nwarrow
     \\
     \mathbb{Q}\otimes_{\mathbb{Z}}\underset{p\;prime}{\prod} \mathbb{Z}_p && && \mathbb{Z}
     \\
     & \nwarrow && \swarrow
     \\
     && \underset{p\;prime}{\prod} \mathbb{Z}_p
  }
  \,.
$$

Equivalently this is the [[fiber product]] of the rationals with the [[integral adeles]] $\mathbb{A}_{\mathbb{Z}}$ over the [[ring of adeles]] $\mathbb{A}_{\mathbb{Q}}$

$$
  \array{
     && \mathbb{Q}
     \\
     & \swarrow && \nwarrow
     \\
     \mathbb{A}_{\mathbb{Q}} && && \mathbb{Z}
     \\
     & \nwarrow && \swarrow
     \\
     && \mathbb{A}_{\mathbb{Z}}
  }
  \,,
$$

Since the [[ring of adeles]] is the [[rationalization]] of the integral adeles $\mathbb{A}_{\mathbb{Q}} = \mathbb{Q} \otimes_{\mathbb{Z}} \mathbb{A}_{\mathbb{Z}}$, this is also (by the discussion [here](category+of+monoids#PushoutOfCommutativeMonoids)) a [[pushout]] diagram in [[CRing]], and in fact in topological [[commutative rings]] (for $\mathbb{Q}$ with the [[discrete topology]] and $\mathbb{A}_{\mathbb{Z}}$ with its profinite/[[completion of a ring|completion]] topology).

=--

This is of course elementary in itself, but is conceptually important (see remark \ref{GeometricMeaning} below).
One place where the first pullback square above appears explicitly in relation to fracture theorems in homotopy theory (see [below](#InHomotopyTheory)) is in ([Riehl 14, lemma 14.4.2](#Riehl14)).

+-- {: .num_remark #GeometricMeaning}
###### Remark

Under the [[function field analogy]] we may think of 

* $Spec(\mathbb{Z})$ as an [[arithmetic curve]] over [[F1]];

* $\mathbb{A}_{\mathbb{Z}}$ as the [[ring of functions]] on the [[formal disks]] around all the points in this curve;

* $\mathbb{Q}$ as the ring of functions on the complement of a finite number of points in the curve;

* $\mathbb{A}_{\mathbb{Q}}$ is the ring of functions on punctured formal disks around all points, at most finitely many of which do not extend to the unpunctured disk.

Under this [[analogy]] the arithmetic fracture square of prop. \ref{ArithmeticFractureSquare} says that the curve $Spec(\mathbb{Z})$ has a [[cover]] whose patches are the complement of the curve by some points, and the formal disks around these points. 

This kind of cover plays a central role in [[number theory]], see for instance thr following discussions:

* _[Moduli stack of bundles over curves](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_;

* _[[geometric Langlands correspondence]]_;

* _[[Weil conjecture on Tamagawa numbers]]_.


=--

### In (stable) homotopy theory
 {#InHomotopyTheory}

In [[homotopy theory]] the corresponding statement is that [[homotopy types]] may be decomposed into that of [[rational homotopy types]] and [[p-complete homotopy types]] of [[p-local homotopy types]].

+-- {: .num_remark #FractureForSpectra}
###### Proposition

Let $p$ be a [[prime number]]. Let $X$ be a [[homotopy type]]/[[∞-groupoid]] satisfying at least one of the following sufficient conditions 

* $X$ is a [[connected]], [[nilpotent space]] with finitely generated [[homotopy groups]];

* $X$ is [[p-local homotopy type]];

Then $X$ is the [[homotopy fiber product]]

$$
  X \simeq X_{\mathbb{Q}} \underset{(X_p^\wedge)_{\mathbb{Q}}}{\times} X_p^\wedge
$$

of its [[rationalization]] $X_{\mathbb{Q}}$ with its [[p-completion]] $X_p^\wedge$ over the rationalization $(X_p^\wedge)_{\mathbb{Q}}$of the $p$-completions. 

=--

This originates around ([Bousfield-Kan 72, VI.8.1](#BousfieldKan72)). A detailed more modern account is in ([May-Ponto, theorem 13.1.4](#MayPonto)). A quick sruvey is in [Riehl 14, theorem 14.4.14](#Riehl14).

Similar statements hold in [[stable homotopy theory]] for [[spectra]], in which case the homotopy pullback squares here are also known as **arithmetic squares** ([Sullivan 05](#Sullivan05), for a review see [Bauer, section 2](#Bauer)).


+-- {: .num_remark }
###### Remark
**("one prime at a time")**

The impact of prop. \ref{FractureForSpectra} is that it decomposes the study of ([[stable homotopy theory|stable]]) [[homotopy theory]] into that of 

1. [[rational homotopy theory]]  and

1. [[p-adic homotopy theory]] for each prime $p$.

Both the [[rationalization]] $X_{\mathbb{Q}}$ and the [[p-completion]] $X_{p}^\\wedge$ are typically much easier to analyze than $p$ itself and so the fracture theorem gives a way to decompose the remaining hard part of study of [[homotopy types]] into that of $p$-local/$p$-complete spaces. 
This procedure is known in homotopy theory as working "one prime at a time".

=--

+-- {: .num_remark }
###### Remark

By the discussion at _[[Bousfield localization of spectra]]_ and at _[[localization of a space]]_, the [[rationalization]] and the [[p-completion]] maps on spectra are [[homotopy cofibers]] of $E$-acyclifications $G_E(X) \to X$, for $E = H\mathbb{Q}$ and $E = H \mathbb{F}_p$  the [[Eilenberg-MacLane spectra]] of $\mathbb{Q}$ and of the [[cyclic group]]/[[finite field]] $\mathbb{F}_p = \mathbb{Z}/(p)$, respectively (e.g. [Lurie 10, lecture 20](localization+of+a+space#Lurie)).

Including this into the statement of of prop. \ref{FractureForSpectra} says that for spectra $X$ satisfying sufficient conditions as above, then the canonical diagram

$$
  \array{
    && X_{\mathbb{Q}} && \longleftarrow && G_{H\mathbb{F}_p}(X)
    \\
    & \swarrow && \nwarrow && \swarrow
    \\
    (\prod_p X_p^\wedge)_{\mathbb{Q}} && && X
    \\
    & \nwarrow && \swarrow && \nwarrow
    \\
    && \prod_p X_p^\wedge && \longleftarrow && G_{H\mathbb{Q}}(X)
  }
$$

has the following exactness properties:

1. the square is a [[homotopy pullback]] and hence also a [[homotopy pushout]];

1. the diagonals are [[homotopy cofiber sequences]] and hence also [[homotopy fiber sequences]].


Notice that in view of remark \ref{GeometricMeaning} then $X_p^\wedge$ is like the restriction of $X$ from [[Spec(Z)]] to all [[formal disks]] around the points $(p)$, and hence $G_{H\mathbb{F}_p}$ is like the restriction to the "complement of all formal disks". Finally $X_{\mathbb{Q}}$ may be understood as the restriction to the [[Ran space]] of $Spec(\mathbb{Z})$ ([Gaitsgory 11](#Gaitsgory11)), roughly the colimit of the restriction of $X$ to the complement of finitely many points, as this set of points ranges through all points.


=--


### In cohesive (stable) homotopy theory

In an [[tangent cohesive (∞,1)-topos]] every [[stable homotopy type]] is canonically a cohesive/differential extension of its [[geometric realization of a cohesive homotopy type|geometric realization]] by way of a kind of fracture theorem involving the localizations induced by the [[shape modality]] and the [[flat modality]]: 

$$
  X \simeq \flat_{dR}\Sigma X   \underset{\Pi \flat_{dR}\Sigma X}{\times}  \Pi X
$$

See at _[tangent cohesion -- Cohesive and differential refinement](tangent+cohesive+%28?%2C1%29-topos#CohesiveAndDifferentialRefinement)_.

More generally, the statement of the
_[[differential cohomology hexagon]]_ is that for every stable cohesive homotopy type the canonical hexagon

$$
  \array{
    &&  \Pi_{dR} X && \stackrel{}{\longrightarrow} && \flat_{dR}X
    \\
    & \nearrow & & \searrow & & \nearrow_{} && \searrow
    \\
    \flat \Pi_{dR} X  && && X && && \Pi \flat_{dR}  X
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{}
    \\
    && \flat X  && \longrightarrow && \Pi X
  }
$$

is homotopy exact, in that both squares are both [[homotopy pullback]] as well as [[homotopy pushout]] squares and the two boundary sequences are long [[homotopy fiber sequences]]/[[homotopy cofiber sequences]].

Notice that for instance for [[synthetic differential infinity-groupoids]] regarded as cohesive over their [[formal moduli problems]], then the [[flat modality]] $\flat$ sends each space $X$ to the collection $\flat X$ of all its formal disks. Also notice that by the discussion [here](differential+cohomology+diagram#OrdinaryDifferentialCohomology) the [[cocycles]] on $\Pi_{dR} X$ are equivalently the rationalized (de Rham) cocycles on $X$.

Hence under [[Isbell duality|algebra/geometry duality]] and in view of the [[function field analogy]], then in this case the left square in the above behaves indeed as a geometric dual to the classical arithmetic fracture squares above.


## Examples

* [tmf -- Decomposition via arithmetic fracture squares](tmf#DecomopositionViaArithmeticSquares)

## Related concepts

* [[p-localization]]

* [[p-completion]]

## References

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, Vol 304, Springer 1972

* {#Sullivan05} [[Dennis Sullivan]], _Geometric topology: localization, periodicity and Galois symmetry_, volume 8 of K- Monographs in Mathematics. Springer, Dordrecht, 2005. The 1970 MIT notes, Edited and with a preface
by [[Andrew Ranicki]].

* {#Bauer} [[Tilman Bauer]], _Bousfield localization and the Hasse square_ ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))

* {#Riehl14} [[Emily Riehl]], _Categorical homotopy theory_, new mathematical monographs 24, Cambridge University Press 2014 (published version)


* {#MayPonto} [[Peter May]], [[Kate Ponto]], chapters 7 and 8 of _More concise algebraic topology: Localization, completion, and model categories_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/mayponto.pdf))

* [[Michael Shulman]], _The Propositional Fracture Theorem_, ([blog post](http://golem.ph.utexas.edu/category/2013/05/the_propositional_fracture_the.html))

Related MO-discussion:

* _[Fracture squares of Bousfield Localizations of Spectra](http://mathoverflow.net/a/91057/381)_

Discussion of rational functions as functions on the [[Ran space]] is in 

* {#Gaitsgory11} [[Dennis Gaitsgory]], _Contractibility of the space of rational maps_ ([arXiv:1108.1741](http://arxiv.org/abs/1108.1741))

[[!redirects fracture theorems]]

[[!redirects arithmetic square]]
[[!redirects arithmetic squares]]

[[!redirects fracture square]]
[[!redirects fracture squares]]