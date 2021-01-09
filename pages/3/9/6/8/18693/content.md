
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Historically, the theory of [[distributional densities]] (or just _[[distributions]]_, for short), conceived in [[functional analysis]], was phrased in terms of [[continuous linear functionals]] on [[topological vector spaces]] of [[smooth functions]]. However, since [[smooth functions]] on [[smooth manifolds]] are the subject of [[differential geometry]], and since spaces of [[smooth functions]] are naturally themselves [[generalized smooth spaces]], it makes sense to ask whether [[distribution]] theory is actually a native topic to [[differential geometry]].


In particular we may ask how distributions in the [[functional analysis|functional analytic]] sense relate to the _smooth linear functions_ on smooth spaces of smooth functions. Indeed, with respect to the natural formulation of differential geometry via [[functorial geometry]] ([[topos theory]]) in terms of [[diffeological spaces]], [[smooth sets]] etc. it turns out that distributional densities are equivalently the smooth linear functionals on smooth spaces of smooth functions.

This we discuss in the section 

* _[Statement](#Statement)_ 

below. To set the scene we briefly recall some concepts in

* _[Preliminaries](#Preliminaries)_.

Finally we discuss some 

* _[Applications](#Applications)_.

## Preliminaries
 {#Preliminaries}

+-- {: .num_defn #GeneralizedSmoothSpaces}
###### Definition
**([[generalized smooth spaces]])**


In the following we write $\mathbf{H}$ for the [[category]] of [[diffeological spaces]] rather for the [[toposes]] of [[smooth sets]] or [[formal smooth set]] or [[super formal smooth sets]] etc. These form a [[sequence]] of [[full subcategory]] inclusions

$$
  SmoothManifolds
    \hookrightarrow
  DiffeologicalSpaces
    \hookrightarrow
  SmoothSets
    \hookrightarrow
  FormalSmoothSets
    \hookrightarrow
  SuperFormalSmoothSets
  \,.
$$

=--

The smallest of these categories of [[generalized smooth spaces]] that is needed for accomodating the spaces of [[smooth functions]] that distributions are defined on are [[diffeological spaces]], and the reader may want to just focus on these. We mention these more general ambient categories mostly to amplify that the identificatin of distributions with smooth linear functionals remains true in these more general contexts.


+-- {: .num_example #SmoothMappingSpace}
###### Example
**(smooth [[mapping spaces]])**


For $X \in \mathbf{H}$ any object, we write $[X,\mathbb{R}]$ for the [[mapping space]] (the [[internal hom]]). The underlying set is $C^\infty(X)$. If $X$ itself has $\mathbb{R}$-linear structure, we write 

$$
  [X,\mathbb{R}]_{\mathbb{R}}
  \hookrightarrow
  [X,\mathbb{R}]
$$

for the [[subobject]] of $\mathbb{R}$-linear maps. 

Concretely, for $U$ a [[smooth manifold]] (or just a [[Cartesian space]]), then the [[sheaf]] $[X,\mathbb{R}]$ assigns (see at _[[closed monoidal structure on presheaves]]_ for details)

$$
  [X,\mathbb{R}](U) = C^\infty(U \times X)
$$

and $[X,\mathbb{R}](U) \subset C^\infty(U \times X)$ is the subset of those functions $\Phi_{(-)}(-)$ such that for all $u \in U$ the function $\Phi_u \colon X \to \mathbb{R}$ is $\mathbb{R}$-linear. The [[global elements]] $\Gamma(-)$ of the [[mapping space]] constitute the ordinary [[hom set]]

$$
  \Gamma [X,\mathbb{R}] \simeq \mathbf{H}(X,\mathbb{R})
  \,.
$$

If $X$ happens to be a [[compact topological space|compact]] [[smooth manifold]] then $C^\infty(X)$ carries the structure of a [[Fréchet manifold]] (see at _[[manifold structure of mapping spaces]]_). Under the [[full subcategory|full embdding]] of [[Fréchet manifolds]] into [[diffeological spaces]], this coincides with $[X,\mathbb{R}]$ (see [there](Fr&#233;chet+manifold#RelationBetweenDeffeologicalAndFrechetStructure)).

=--

## Statement
 {#Statement}

### Compactly supported distributions

+-- {: .num_prop #CompactlySupportedDistributionsAreTheSmoothLinearFunctionals}
###### Proposition
**([[compactly supported distributions are the smooth linear functionals]])**

For $n \in \mathbb{N}$, there is a [[natural bijection]] between the underlying sets of [[compactly supported distributions]] on $\mathbb{R}^n$ ([this def.](compactly+supported+distribution#CompactlySupportedDistributionsAsContinuousLinearDualsToBumpFunctions)) and the $\mathbb{R}$-linear [[mapping space]] formed in the [[category]] $\mathbf{H}$ of [[generalized smooth spaces]] from def. \ref{GeneralizedSmoothSpaces}:

$$
  \widetilde{(-)}
  \;\colon\;
  \mathcal{E}'(\mathbb{R}^n)
    \overset{\simeq}{\longrightarrow}
  \mathbf{H}([\mathbb{R}^n, \mathbb{R}], \mathbb{R})_{\mathbb{R}}
$$

given by sending $\mu \in \mathcal{E}'(\mathbb{R}^n)$ to the [[natural transformation]] which on a test space $U \in $ [[CartSp]] takes a smoothly $U$-parameterized function $\Phi_{(-)}(-) \colon U \times \mathbb{R}^n \to \mathbb{R}$ to its evaluation in $\mu$ pointwise in $U$:

$$
  \tilde \mu(\Phi_{(-)})(u)
  \;\coloneqq\;
  \langle \mu, \Phi_{u}\rangle
  \,.
$$

=--

([Moerdijk-Reyes 91, chapter II, prop. 3.6](#MoerdijkReyes91))


+-- {: .proof}
###### Proof

First consider this for the case that $\mathbf{H} = $ [[SmoothSet]] (which immediately subsumes the case that $\mathbf{H} =$ [[diffeological space|DiffelogicaSpace]]).

To see that $\widetilde{(-)}$ is well defined, we need to check that the function

$$
  \array{
     U 
     &\overset{
     \tilde \mu(\Phi_{(-)})}{\longrightarrow}&
     \mathbb{R}
     \\
     u &\mapsto& \langle \mu, \Phi_u\rangle
  }
$$

is [[smooth function|smooth]]. But this follows immediately since $\langle \mu,-\rangle$ by definition is [[linear function|linear]] and [[continuous function|continuous]].


To see that $\widetilde{(-)}$ is indeed a [[bijection]] for each $U$ it remains that every $\mathbb{R}$-linear smooth functional (morphisms of [[smooth sets]]) of the form

$$
  A \;\colon\; [\mathbb{R}^n,\mathbb{R}] \longrightarrow \mathbb{R}
$$

when restricted on [[global elements]] to a [[function]] of sets

$$
  A(\ast) \;\colon\; C^\infty(\mathbb{R}^n) \longrightarrow \mathbb{R}
$$

is [[continuous function|continuous]] with respect to the [[topological vector space]] structure from def. \ref{TVSOfCompactlySupportedFunctions} on the left.

Now by definition of the [[internal hom]] $A$ is actually "path-smooth" ([this def.](Frechet+space#PathSmoothFunction)) and hence the statement is implied by [this prop](Frechet+space#PathSmoothLinearFunctionsOnFrechetSpaceAreContinuous).

Finally to see that this argument generalizes to $\mathbf{H} = $ [[formal smooth set|FormalSmoothSet]] observe that the [[Weil algebra]] of every [[infinitesimally thickened point]] is a [[quotient ring]] of an algebra of smooth functions on some [[Cartesian space]] (by the [[Hadamard lemma]]). The previous argument now applies to representatives under this quotient coprojection and one checks that it is independent of the representative chosen.

=--

### General distributions

For general [[distributions]] in the sense of [[continuous linear functionals]] on the space $\mathcal{D}(\mathbb{R}^n)$ of [[compact support|compactly supported]] [[smooth functions]] ([[bump functions]]) their equivalence to smooth linear functionals is discussed in ([Kock-Reyes 04, section 2, esp. paragraph above theorem 2.3](#KockReyes04)).

(...)

## Applications
 {#Applications}

### In quantum field theory

This has some interesting consequences. For instance a major application of [[distribution]] theory is [[perturbative quantum field theory]], which, together with the rest of [[quantum physics]] is traditionally regarded to be a subject that makes heavy use of [[functional analysis]]. However, the development of [[algebraic quantum field theory]] with its emphasis of the abstract [[operator algebra]] [[algebra of observables|of observables]] and de-emphasis of [[Hilbert spaces]] [[space of quantum states|of quantum states]] (which is sometimes a convenient [[representation]] of the abstract [[operator algebra]] but more often just a distraction) combined with the development of [[perturbative quantum field theory]], where even these [[operator algebras]] are replaced by [[formal power series|formal]] [[star algebras]] of smooth functionals, has diminished the fundamental role of [[functional analysis]] in field theory. The theory of distributions survives as the tool of choice for understanding the singularity structure (or rather its absence) in the construction of the [[Wick algebra]] of [[quantum observables]] of the [[free fields]] and then in the process of [[renormalization]] via [[extension of distributions]] to the locus of coincident interaction points. But the [[quantum observables]] which are represented by these distributions are most naturally thought of as _smooth_ functions on the [[space of field histories]]. Therefore the fact that distributions in fact are the smooth linear functionals shows that their appearance in [[perturbative quantum field theory]] is a tool for studying smooth functionals, not a concept fundamental to the theory as such.

### Generalization to extensive quantities

The conception of distributions simply as elements of a double [[mapping space]] ([[internal hom]]) makes immediate that this concept exists in more generality than the traditional context. In [Lawvere 86](#Lawvere86) it was suggested that distribution theory should be considered more abstractly from such a point of general "[[extensive quantities]]". This is developed further in ([Kock 11](#Kock11)).

## References

Discussion of distributions in terms morphisms out of [[internal homs]] in the [[smooth topos]] over the site of [[smooth loci]] is in

* {#MoerdijkReyes91} [[Ieke Moerdijk]], [[Gonzalo Reyes]], around prop. 3.6 of _[[Models for Smooth Infinitesimal Analysis]]_, Springer 1991

Discussion for the [[Cahiers topos]] is in

* {#KockReyes03} [[Anders Kock]], [[Gonzalo Reyes]], _Some calculus with extensive quantities: wave equation_, Theory and Applications of Categories , Vol. 11, 2003, No. 14, pp 321-336 ([TAC](http://www.tac.mta.ca/tac/volumes/11/14/11-14abs.html))

* {#KockReyes04} [[Anders Kock]], [[Gonzalo Reyes]], _Categorical distribution theory; heat equation_ ([arXiv:math/0407242](https://arxiv.org/abs/math/0407242))

* {#Kock11} [[Anders Kock]], _Commutative monads as a theory of distributions_ ([arxiv/1108.5952](http://arxiv.org/abs/1108.5952)) 

using results of

* {#FroelicherKriegl88} [[Alfred Frölicher]], [[Andreas Kriegl]], section 5 of  _Linear spaces and differentiation theory_, Wiley 1988 ([pdf](http://www.fuw.edu.pl/~kostecki/scans/froelicherkriegl1988.pdf))

and following the general conception of "[[intensive and extensive]]" in 

* {#Lawvere86} [[William Lawvere]], Introduction to _[[Categories in Continuum Physics]], Lectures given at a Workshop held at SUNY, Buffalo 1982. Lecture Notes in Mathematics 1174. 1986

Similar [[sheaf theory|sheaf theoretic]] discussion of distributions as morphisms of [[smooth spaces]] is in 

* {#Paugam12} [[Frédéric Paugam]], section 3.2 of _Towards the mathematics of quantum field theory_, 2012 ([pdf](https://webusers.imj-prg.fr/~frederic.paugam/documents/enseignement/master-mathematical-physics.pdf)) 

[[!redirects compactly supported distributions are the smooth linear functionals]]
