
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A basic fact in [[number theory]] is that the [[natural numbers]] may be decomposed into the [[rational numbers]] and the [[p-adic integers]] for all [[prime numbers]] $p$. Dually  in [[arithmetic geometry]] this says that [[Spec(Z)]] has a [[cover]] by all its [[formal disks]] and the complements of finitely many points, a fact that is crucial in the geometric interpretation of the [[function field analogy]] and which motivates for instance the [[geometric Langlands correspondence]]. (See [below](#ArithmeticFractureSquares).)

Lifting this statement to [[stable homotopy theory]] and "[[higher arithmetic geometry]]" the _arithmetic fracture theorem_ says that [[stable homotopy types]] (and suitably tame plain [[homotopy types]]) canonically decompose into their [[rationalization]] and their [[p-completion]] for all primes $p$, hence into their images in [[rational homotopy theory]] and [[p-adic homotopy theory]]. Since these images are typically simpler than the original homotopy type itself, this decomposition is a fundamental computational tool in stable homotopy theory, often known under the slogan of "working one prime at a time". (See [below](#TheArithmeticFractureSquare).)

One finds that this arithmetic fracturing in stable homotopy theory is really a statement about the [[Bousfield localization of spectra]] with respect to the [[Moore spectrum]] for $\mathbb{Q}$ and that of $\mathbb{Q}/\mathbb{Z}$. Viewed this way there is a a more general fracture theorem which says that for any suitable pair $E,F$ of [[spectra]]/[[homology theories]] the [[Bousfield localization of spectra|Bousfield localization]] at their [[coproduct]] decomposes into the separate Bousfield localizations. This generalized fracture theorem appears for instance in [[chromatic homotopy theory]] for localization at [[Morava K-theory]] and [[Morava E-theory]]. (See [below](#GeneralFractureSquares).)

In [[cohesive homotopy theory]] every [[stable homotopy type]] canonically sits in a fracture square formed from the localizaitons exhibited by the [[shape modality]] and the [[flat modality]]. For [[differential cohesion]] over [[infinitesimal cohesion]] this is a [[higher geometry|higher geometric]] analog of the classical artihmetic fracture. (See [below](#InCohesiveHomotopyTheory).)


## Statement
 {#Statement}

### In number theory and arithmetic geometry
 {#ArithmeticFractureSquares}

The  statement in [[number theory]]/[[arithmetic geometry]] is the following:

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

This kind of cover plays a central role in [[number theory]], see for instance the following discussions:

* _[Moduli stack of bundles over curves](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_;

* _[[geometric Langlands correspondence]]_;

* _[[Weil conjecture on Tamagawa numbers]]_.


=--

### In homotopy theory
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

This originates around ([Bousfield-Kan 72, VI.8.1](#BousfieldKan72)). A detailed more modern account is in ([May-Ponto, theorem 13.1.4](#MayPonto)). A quick survey is in ([Riehl 14, theorem 14.4.14](#Riehl14)).

### In stable homotopy theory
 {#InStableHomotopyTheory}

Similar statements hold in [[stable homotopy theory]] for [[spectra]]. There is a stable version of 

* [The arithmetic fracture square](#TheArithmeticFractureSquare)

but more generally there are fracture squares for the [[coproduct]] homology theory $E \vee F$ whenever $F$-localization is $E$-acyclic:

* [General fracture squares](#GeneralFractureSquares)

#### The arithmetic fracture square
 {#TheArithmeticFractureSquare}



For $p$ a [[prime number]] write

* $L_p$ for [[Bousfield localization of spectra]] at the [[Moore spectrum]] $S \mathbb{F}_p$, hence for [[p-completion]] $(-)_p^\wedge$;

* $L_{\mathbb{Q}}$ for the [[Bousfield localization of spectra]] at the [[Moore spectrum]]/[[Eilenberg-MacLane spectrum]] $S \mathbb{Q} \simeq H \mathbb{Q}$, hence for [[rationalization]].

+-- {: .num_prop #SullivanArithmeticFracture}
###### Proposition
**(Sullivan arithmetic square)**

For every [[spectrum]] $X$ the canonical square

$$
  \array{
    && L_{\mathbb{Q}}X
    \\
    & \swarrow && \nwarrow
    \\
    L_{\mathbb{Q}}
    \left(
      \prod_p L_p X
    \right)
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && \prod_p L_p X
  }
$$

=--

This is originally due to ([Sullivan 05](#Sullivan05), it is recalled for instance as ([Bauer 11, lemma 2.1](#Bauer11)).

+-- {: .num_remark }
###### Remark
**("one prime at a time")**

The impact of prop. \ref{FractureForSpectra} is that it decomposes the study of ([[stable homotopy theory|stable]]) [[homotopy theory]] into that of 

1. [[rational homotopy theory]]  and

1. [[p-adic homotopy theory]] for each prime $p$.

Both the [[rationalization]] $X_{\mathbb{Q}}$ and the [[p-completion]] $X_{p}^\wedge$ are typically much easier to analyze than $p$ itself and so the fracture theorem gives a way to decompose the remaining hard part of study of [[homotopy types]] into that of $p$-local/$p$-complete spaces. 
This procedure is known in homotopy theory as working "one prime at a time".

=--


More generally:

+-- {: .num_prop #ReformulationOfProdOverPComletionByLocalizationAtCoproduct}
###### Proposition

The product of all [[p-completions]] is equivalently the [[Bousfield localization of spectra]] at the [[coproduct]] $\vee_p S \mathbb{F}_p$ of all [[Moore spectra]]

$$
  \prod_p L_p X
  \simeq
   L_{\vee_p S \mathbb{F}_p} X
  \,.
$$

Moreover there is a  [[Bousfield equivalence]] 

$$
  S (\mathbb{Q}/\mathbb{Z}) \simeq_{Bousf} \vee_p S \mathbb{F}_p
  \,,
$$ 

and therefore also an equivalence

$$
  \prod_p L_p X
  \simeq
   L_{S (\mathbb{Q}/\mathbb{Z})} X
  \,.
$$


=--

The first statement appears for instance as ([Bauer 11, below prop. 2.2](#Bauer11)), the second is highlighted in ([Strickland 12, MO comment](http://mathoverflow.net/a/91057/381)).


+-- {: .num_remark }
###### Remark

By the discussion at _[[Bousfield localization of spectra]]_ and at _[[localization of a space]]_, the [[rationalization]] and the [[p-completion]] maps on spectra are [[homotopy cofibers]] of $E$-acyclifications $G_E(X) \to X$, for $E = S \mathbb{Q} \simeq H \mathbb{Q}$ and $E = S \mathbb{F}_p$  the [[Moore spectra]] of $\mathbb{Q}$ and of the [[cyclic group]]/[[finite field]] $\mathbb{F}_p = \mathbb{Z}/(p)$, respectively (e.g. [Lurie 10, lecture 20](localization+of+a+space#Lurie)).

Including this into the statement of prop. \ref{FractureForSpectra} says that for spectra $X$ satisfying sufficient conditions as above, then the canonical diagram

$$
  \array{
    && X_{\mathbb{Q}} && \longleftarrow && G_{S (\mathbb{Q}/\mathbb{Z})}(X)
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


Notice that in view of remark \ref{GeometricMeaning} then $X_p^\wedge$ is like the restriction of $X$ from [[Spec(Z)]] to all [[formal disks]] around the points $(p)$, and hence $G_{S\mathbb{F}_p}$ is like the restriction to the "complement of all formal disks". Finally $X_{\mathbb{Q}}$ may be understood as the restriction to the [[Ran space]] of $Spec(\mathbb{Z})$ ([Gaitsgory 11](#Gaitsgory11)), roughly the colimit of the restriction of $X$ to the complement of finitely many points, as this set of points ranges through all points.

=--

#### General fracture squares
 {#GeneralFractureSquares}


By prop. \ref{ReformulationOfProdOverPComletionByLocalizationAtCoproduct}
the arithmetic fracture square of prop. \ref{SullivanArithmeticFracture} is equivalently of the form

$$
  \array{
    && L_{H\mathbb{Q}}X
    \\
    & \swarrow && \nwarrow
    \\
    L_{H\mathbb{Q}}
    L_{S \mathbb{Q}/\mathbb{Z}} X
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && L_{S \mathbb{Q}/\mathbb{Z}} X
  }
  \,.
$$

In this form the statement holds much more generally:

+-- {: .num_prop #GeneralFractureSquare}
###### Proposition

Let $E, F, X$ be [[spectra]] such that the $F$-[[Bousfield localization of spectra|localization]] of $X$ is $E$-acyclic, i.e.  $E_\bullet(L_F X) \simeq 0$, then the canonical square [[diagram]]

$$
  \array{
    && L_F X
    \\
    & \swarrow && \nwarrow
    \\
    L_F
    L_E X
    &&  &&
    L_{E\vee F}
    \\
     & \nwarrow && \swarrow
    \\
    && L_E
  }
$$

is a [[homotopy pullback]] (and hence by stability also a [[homotopy pushout]]).


=--

e.g. ([Bauer 11, prop. 2.2](#Bauer11))

+-- {: .num_remark}
###### Remark

This general version is used frequently in [[chromatic homotopy theory]] for decomposition in [[Morava K-theory]] and [[Morava E-theory]]-localizations. In paticular it is used for instance in the construction of [[tmf]], see example \ref{ConstructionOfTmf} below.

=--


### In cohesive (stable) homotopy theory
 {#InCohesiveHomotopyTheory}

In [[cohesive homotopy theory]] every [[stable homotopy type]] $X$ sits in a fracture square of the form

$$
  \array{
    &&  \Pi_{dR} X &&  \longrightarrow && \flat_{dR} X
    \\
    & \nearrow & & \searrow  && \nearrow
    \\
    \flat \Pi_{dR} X  && && X 
    \\
    & \searrow &  & \nearrow && \searrow
    \\
    && \flat X   && \longrightarrow && \Pi X
  }
$$

where $\flat$ is the [[flat modality]] and $\Pi_{dR}$ the [[homotopy fiber]] of the [[unit of a monad|unit]] $X\to \Pi X$ of the [[shape modality]]. This is the left part of the [[differential cohomology hexagon]] for $X$, see there for details.

Here $\Pi_{dR} X$ is such that for any other stable cohesive homotopy type $\hat E$ then functions $\Pi_{dR} X \to \hat E$ are equivalent to functions $X \to \flat_{dR} \hat E$, where $\hat E \to \flat_{dR} \hat E$ is a generalized form of rationalization in the sense discussed at _[[differential cohomology hexagon]]_. In particular if $\hat E$ is a [Hopkins-Singer-type](differential%20cohomology%20diagram#HopkinsSingerCoefficients) [[differential cohomology]] refinement of a plain [[spectrum]] $E$, then $E\to \flat_{dR} E$ is its ordinary [[rationalization]] given by the [[Chern character]] and $\hat E \to \flat_{dR} \hat E$ is the corresponding map on Chern [[curvature forms]].

Moreover, if the ambient [[cohesion]] is [[differential cohesion]] over a base of [[infinitesimal cohesion]], then the [[flat modality]] $\flat$ takes any space $X$ to the union of all its [[formal disks]]. (See at _[[differential cohesion and idelic structure]]_.) Accordingly the collection of functions $\flat X \to \hat E$ in this case behave like the product of all [[formal power series]] of $\hat E$-valued functions around all global points of $X$, analogous to remark \ref{GeometricMeaning}.

An example of this are [[synthetic differential ∞-groupoids]] regarded as cohesive over their [[formal moduli problems]], as its its complex analytic incarnation by synthetic differential [[complex analytic ∞-groupoids]]. In this context if $X = \Sigma$ is a [[complex curve]] then $\flat \Sigma$ is precisely the analog of the [[integral adeles]] as it is predicted by the [[function field analogy]].


## Examples
 {#Examples}

+-- {: .num_example #ConstructionOfTmf}
###### Example

The construction of the [[tmf]]-spectrum -- the spectrum of [[global sections]] of the [[derived Deligne-Mumford stack]] of [[derived elliptic curves]] --  as described in ([Behrens 13](tmf#Behrens13)) proceeds by first applying the arithmetic fracture square of prop. \ref{#ArithmeticFractureSquare} to decompose the [[moduli stack of elliptic curves]] into rational and $p$-adic curves, and then in a second step in applying in turn the general fracture square of prop. \ref{GeneralFractureSquare} for [[Morava K-theory]] to the remaining $p$-adic pieces.

See at _[tmf -- Decomposition via arithmetic fracture squares](tmf#DecomopositionViaArithmeticSquares)_ for more on this.

=--

## Related concepts

* [[p-adic homotopy theory]], [[p-completion]]

* [[rational homotopy theory]], [[rationalization]]


## References

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, Vol 304, Springer 1972

* {#Sullivan05} [[Dennis Sullivan]], _Geometric topology: localization, periodicity and Galois symmetry_, volume 8 of K- Monographs in Mathematics. Springer, Dordrecht, 2005. The 1970 MIT notes, Edited and with a preface
by [[Andrew Ranicki]].

* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_, 2011 ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))

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