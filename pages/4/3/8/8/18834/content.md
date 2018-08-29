
## Renormalization
 {#Renormalization}



In this chapter we discuss the following topics:

* _[Epstein-Glaser normalization](#EpsteinGlaserRenormalization)_

* _[Stückelberg-Petermann re-normalization](#SPRenormalizationGroup)_

* _[UV-Regularization via Counterterms](#UVRegularizationViaZ)_

* _[Wilson-Polchinski effective QFT flow](#EffectiveQFTFlowWislonian)_

* _[Renormalization group flow](#RGFlowGeneral)_

* _[Gell-Mann & Low RG Flow](#ScalingTransformatinRGFlow)_

$\,$

In the [previous chapter](#InteractingQuantumFields) we have seen that the construction of [[interacting quantum field theory|interacting]] [[perturbative quantum field theories]] is given by perturbative [[S-matrix schemes]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}), equivalently by [[time-ordered products]] (def. \ref{TimeOrderedProduct}) or equivalently by  [[Feynman amplitudes]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}). These are uniquely fixed away from coinciding interaction points (prop. \ref{TimeOrderedProductAwayFromDiagonal}) by the given [[local observable|local]] [[interaction]] (prop. \ref{TimeOrderedProductAwayFromDiagonal}), but involve further choices of interactions whenever interaction vertices coincide (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}). This choice is called the choice of [[renormalization|("re"-)normalization]] (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}) in [[perturbative QFT]].

In this rigorous discussion no "infinite divergent quantities" (as in the original informal discussion due to [[Schwinger-Tomonaga-Feynman-Dyson]]) that need to be "re-normalized" to finite well-defined quantities are ever considered,
instead finite well-defined quantities are considered right away, and the available space of choices is determined.
Therefore making such choices is rather a _normalization_ of the [[time-ordered products]]/[[Feynman amplitudes]]
(as prominently highlighted in [Scharf 95, see title, introduction, and section 4.3](causal+perturbation+theoryscatt#Scharf95)).
Actual re-normalization is the the change of such normalizations.


The construction of [[perturbative QFTs]] may be explicitly described by an [[induction|inductive]] [[extension of distributions]]
of [[time-ordered products]]/[[Feynman amplitudes]] to coinciding interaction points. This is called

* _[Epstein-Glaser renormalization](#EpsteinGlaserRenormalization)_.

This inductive construction has the advantage that it gives accurate control over the space
of available choices of ("re"-)normalizations (theorem \ref{ExistenceRenormalization} below) but it
leaves the nature of the "new interactions" that are to be chosen at coinciding interaction points somwewhat implicit.

Alternatively, one may [[vertex redefinition|re-define the interactions]] explicitly (by adding "[[counterterms]]", remark \ref{TermCounter} below),
depending on a chosen [[UV cutoff]]-scale (def. \ref{CutoffsUVForPerturbativeQFT} below), and construct the [[limit of a sequence|limit]] as the "cutoff is removed" (prop. \ref{UVRegularization} below). This is called ("re"-)normalization by

* _[UV-Regularization via Counterterms](#UVRegularizationViaZ)_.

This still leaves open the question how to choose the [[counterterms]]. For that it serves to understand
the _[[relative effective action]]_ induced by the choice of [[UV cutoff]] at any given cutoff scale (def. \ref{EffectiveActionRelative} below). This is the perspective of _[[effective quantum field theory]]_ (remark \ref{pQFTEffective} below).

The [[infinitesimal]] change of these [[relative effective actions]] follows a universal [[differential equation]], known as 
_[[Polchinski's flow equation]]_ (prop. \ref{FlowEquationPolchinski} below). This makes the problem of ("re"-)normalization
be that of solving this [[differential equation]] subject to chosen initial data. This is the perspective on
("re"-)normalization called

* _[Wilson-Polchinski effective QFT flow](#EffectiveQFTFlowWislonian)_.

The [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem} below) states that different [[S-matrix schemes]] are precisely related by [[vertex redefinitions]]. This yields the

* _[Stückelberg-Petermann renormalization group](#SPRenormalizationGroup)_.

If a sub-collection of [[renormalization schemes]] is parameterized by some [[group]] $RG$,
then the [[main theorem of perturbative renormalization|main theorem]] implies [[vertex redefinitions]]
depending on pairs of elements of $RG$ (prop. \ref{FlowRenormalizationGroup} below). This is known as

* _[Renormalization group flow](#RGFlowGeneral)_

Specifically [[scaling transformations]] on [[Minkowski spacetime]] yield such a collection of [[renormalization schemes]] (prop. \ref{RGFlowScalingTransformations} below);
the corresponding [[renormalization group flow]] is known as

* _[Gell-Mann & Low RG flow](#ScalingTransformatinRGFlow)_.

The [[infinitesimal]] behaviour of this flow is known as the _[[beta function]]_, describing the _[[running of the coupling constants]]_ with scale (def. \ref{CouplingRunning} below).

$\,$


**[[Epstein-Glaser renormalization|Epstein-Glaser normalization]]**
 {#EpsteinGlaserRenormalization}

The construction of [[perturbative quantum field theories]] around a given [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free field]] [[vacuum]]
is equivalently, by prop. \ref{InteractingFieldAlgebraOfObservablesIsFormalDeformationQuantization}, the construction of [[S-matrices]] $\mathcal{S}(g S_{int} + j A)$ in the sense of [[causal perturbation theory]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) for the given [[local observable|local]] [[interaction]]
$g S_{int} + j A$. By prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal} the construction of these
[[S-matrices]] is [[induction|inductively]] in $k \in \mathbb{N}$ a choice of [[extension of distributions]] (remark \ref{TimeOrderedProductOfFixedInteraction} and def. \ref{ExtensionOfDistributions} below) of the corresponding $k$-ary [[time-ordered products]] of the [[interaction]] to the locus of coinciding interaction points. An inductive construction of the
[[S-matrix]] this way is called _[[Epstein-Glaser renormalization|Epstein-Glaser-("re"-)normalization]]_ (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}).

By paying attention to the [[scaling degree of distributions|scaling degree]] (def. \ref{ScalingDegree} below)
one may precisely characterize the space of choices in the [[extension of distributions]] (prop. \ref{SpaceOfPointExtensions} below):
For a given [[local observable|local]] [[interaction]] $g S_{int} + j A$ it is inductively in $k \in \mathbb{N}$ a
[[finite dimensional vector space|finite-dimensional]] [[affine space]]. This conclusion is theorem \ref{ExistenceRenormalization} below.

$\,$

+-- {: .num_prop #RenormalizationIsInductivelyExtensionToDiagonal}
###### Proposition
**([[renormalization|("re"-)normalization]] is [[induction|inductive]] [[extension of distributions|extension]] of [[time-ordered products]] to [[diagonal]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[gauge fixing|gauge-fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}).

Assume that for $n \in \mathbb{N}$, [[time-ordered products]]
$\{T_{k}\}_{k \leq n}$ of arity $k \leq n$ have been constructed
in the sense of def. \ref{TimeOrderedProduct}.
Then the time-ordered product $T_{n+1}$ of arity $n+1$ is uniquely fixed on the [[complement]]

$$
  \Sigma^{n+1} \setminus diag(n)
  \;=\;
  \left\{
     (x_i \in \Sigma)_{i = 1}^n
     \;\vert\;
     \underset{i,j}{\exists} (x_i \neq x_j)
  \right\}
$$

of the [[image]] of the [[diagonal]] inclusion $\Sigma \overset{diag}{\longrightarrow} \Sigma^{n}$
(where we regarded $T_{n+1}$ as a [[generalized function]] on $\Sigma^{n+1}$ according to remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}).

=--

This statement appears in ([Popineau-Stora 82](renormalization#PopineauStora82)), with (unpublished) details in ([Stora 93](renormalization#Stora93)), following personal communication by [[Henri Epstein]] (according to [Dütsch 18, footnote 57](renormalization#Duetsch18)). Following this, statement and detailed proof appeared in ([Brunetti-Fredenhagen 99](renormalization#BrunettiFredenhagen99)).


+-- {: .proof}
###### Proof

We will construct an [[open cover]] of $\Sigma^{n+1} \setminus \Sigma$ by subsets $\mathcal{C}_I \subset \Sigma^{n+1}$ which are [[disjoint unions]]
of [[inhabited set|non-empty]] sets that are in [[causal order]], so that by [[causal factorization]] the
time-ordered products $T_{n+1}$ on these subsets are uniquely given by $T_{k}(-) \star_H T_{n-k}(-)$.
Then we show that these unique products on these special subsets do coincide on [[intersections]].
This yields the claim by a [[partition of unity]].

We now say this in detail:

For $I \subset \{1, \cdots, n+1\}$  write $\overline{I} \coloneqq \{1, \cdots, n+1\} \setminus I$.
For $I, \overline{I} \neq \emptyset$, define the subset

$$
  \mathcal{C}_I
  \;\coloneqq\;
  \left\{
    (x_i)_{i \in \{1, \cdots, n+1\}} \in \Sigma^{n+1}
    \;\vert\;
    \{x_i\}_{i \in I} {\vee\!\!\!\wedge} \{x_j\}_{j \in \{1, \cdots, n+1\} \setminus I}
  \right\}
  \;\subset\;
  \Sigma^{n+1}
  \,.
$$

Since the [[causal order]]-relation involves the [[closed future cones]]/[[closed past cones]], respectively, it is clear that these are [[open subsets]]. Moreover it is immediate that they form an [[open cover]] of the [[complement]] of the [[diagonal]]:

$$
  \underset{ { I \subset \{1, \cdots, n+1\} \atop { I, \overline{I} \neq \emptyset } }   }{\cup}
  \mathcal{C}_I
  \;=\;
  \Sigma^{n+1} \setminus diag(\Sigma)
  \,.
$$

(Because any two distinct points in the [[globally hyperbolic spacetime]] $\Sigma$ may be causally separated by a [[Cauchy surface]],
and any such may be deformed a little such as not to intersect any of a given finite set of points. )

Hence the condition of [[causal factorization]] on $T_{n+1}$ implies that
[[restriction of distributions|restricted]] to any $\mathcal{C}_{I}$ these have to be given (in the condensed [[generalized function]]-notation from remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}) on
any unordered tuple $\mathbf{X} = \{x_1, \cdots, x_{n+1}\} \in \mathcal{C}_I$ with corresponding induced tuples
$\mathbf{I} \coloneqq \{x_i\}_{i \in I}$ and $\overline{\mathbf{I}} \coloneqq \{x_i\}_{i \in \overline{I}}$ by

$$
  \label{InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal}
  T_{n+1}( \mathbf{X} )
  \;=\;
  T(\mathbf{I}) T(\overline{\mathbf{I}})
  \phantom{AA}
  \text{for}
  \phantom{A}
  \mathcal{X} \in \mathcal{C}_I
  \,.
$$

This shows that $T_{n+1}$ is unique on $\Sigma^{n+1} \setminus diag(\Sigma)$ if it exists at all,
hence if these local identifications glue to a global definition of $T_{n+1}$. To see that this is the case,
we have to consider any two such subsets

$$
  I_1, I_2
  \subset
  \{1, \cdots, n+1\}
  \,,
  \phantom{AA}
  I_1, I_2, \overline{I_1}, \overline{I_2} \neq \emptyset
  \,.
$$

By definition this implies that for

$$
  \mathbf{X} \in \mathcal{C}_{I_1} \cap \mathcal{C}_{I_2}
$$

a tuple of spacetime points which decomposes into causal order with respect to both these subsets,
the corresponding mixed intersections of tuples  are spacelike separated:

$$
  \mathbf{I}_1 \cap \overline{\mathbf{I}_2}
    \;
    {\gt\!\!\!\!\lt}
    \;
  \overline{\mathbf{I}_1} \cap \mathbf{I}_2
  \,.
$$

By the assumption that the $\{T_k\}_{k \neq n}$ satisfy causal factorization, this implies that the corresponding
time-ordered products commute:

$$
  \label{TimeOrderedProductsOfMixedIntersectionsCommute}
  T(\mathbf{I}_1 \cap \overline{\mathbf{I}_2})
  \,
  T(\overline{\mathbf{I}_1} \cap \mathbf{I}_2)
  \;=\;
  T(\overline{\mathbf{I}_1} \cap \mathbf{I}_2)
  \,
  T(\mathbf{I}_1 \cap \overline{\mathbf{I}_2})
  \,.
$$

Using this we find that the identifications of $T_{n+1}$
on $\mathcal{C}_{I_1}$ and on $\mathcal{C}_{I_2}$, accrding to (eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal),
agree on the intersection: in that for $  \mathbf{X}  \in \mathcal{C}_{I_1} \cap \mathcal{C}_{I_2}$ we have

$$
  \begin{aligned}
    T( \mathbf{I}_1 ) T( \overline{\mathbf{I}_1} )
    & =
    T( \mathbf{I}_1 \cap \mathbf{I}_2 )
    T( \mathbf{I}_1 \cap \overline{\mathbf{I}_2} )
    \,
    T( \overline{\mathbf{I}_1} \cap \mathbf{I}_2 )
    T( \overline{\mathbf{I}_1} \cap \overline{\mathbf{I}_2} )
    \\
    & =
    T( \mathbf{I}_1 \cap \mathbf{I}_2 )
    \underbrace{
    T( \overline{\mathbf{I}_1} \cap \mathbf{I}_2 )
    T( \mathbf{I}_1 \cap \overline{\mathbf{I}_2} )
    }
    T( \overline{\mathbf{I}_1} \cap \overline{\mathbf{I}_2} )
    \\
    & =
    T( \mathbf{I}_2 )
    T( \overline{\mathbf{I}_2} )
  \end{aligned}
$$

Here in the first step we expanded out the two factors using (eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal) for $I_2$,
then under the brace we used (eq:TimeOrderedProductsOfMixedIntersectionsCommute) and in the last step we used again
(eq:InductiveIdentificationOfTimeOrderedProductAwayFromDiagonal), but now for $I_1$.

To conclude, let

$$
  \label{PartitionCausalOfUnityForComplementOfDiagonal}
  \left(
    \chi_I
    \in
    C^\infty_{cp}(\Sigma^{n+1}),
    \,
    supp(\chi_I) \subset \mathcal{C}_i
  \right)_{ { I \subset \{1, \cdots, n+1\} } \atop { I, \overline{I} \neq \emptyset } }
$$

be a [[partition of unity]] subordinate to the [[open cover]] formed by the $\mathcal{C}_I$:


Then the above implies that
setting for any $\mathbf{X} \in \Sigma^{n+1} \setminus diag(\Sigma)$

$$
  \label{TimeOrderedProductsAwayFromDiagonalByInduction}
  T_{n+1}(\mathbf{X})
  \;\coloneqq\;
  \underset{
    { I \in \{1, \cdots, n+1\} }
    \atop
    { I, \overline{I} \neq \emptyset }
  }{\sum}
  \chi_i(\mathbf{X}) T( \mathbf{I} ) T( \overline{\mathbf{I}} )
$$

is well defined and satisfies causal factorization.

=--

+-- {: .num_remark #TimeOrderedProductOfFixedInteraction}
###### Remark
**([[time-ordered products]] of fixed [[interaction]] as [[distributions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[gauge fixing|gauge-fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and assume that the [[field bundle]] is a
[[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle})

and let

$$
  g S_{int} + j A
  \;\in\;
  LoObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle
$$

be a polynomial [[local observable]] as in def. \ref{FormalParameters}, to be regarded as a [[adiabatic switching|adiabatically switched]]
[[interaction]] [[action functional]]. This means that there is a [[finite set]]

$$
  \left\{
    \mathbf{L}_{int,i}, \mathbf{\alpha}_{i'} \in \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})
  \right\}_{i,i'}
$$

of [[Lagrangian densities]] which are monomials in the field and jet coordinates,
and a corresponding finite set

$$
  \left\{
    g_{sw,i} \in C^\infty_{cp}(\Sigma)\langle g \rangle
    \,,\,
    j_{sw,i'} \in C^\infty_{cp}(\Sigma)\langle j \rangle
  \right\}
$$

of [[adiabatic switchings]], such that

$$
  g S_{int} + j A
  \;=\;
  \tau_{\Sigma}
  \left(
    \underset{i}{\sum}
    g_{sw,i} \mathbf{L}_{int,i}
    \;+\;
    \underset{i'}{\sum}
    j_{sw,i'} \mathbf{\alpha}_{i'}
  \right)
$$

is the [[transgression of variational differential forms]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
of the sum of the products of these [[adiabatic switching]] with these [[Lagrangian densities]].

In order to discuss the [[S-matrix]] $\mathcal{S}(g S_{int} + j A)$ and hence the
[[time-ordered products]] of the special form $T_k\left(  \underset{k \, \text{factors}}{\underbrace{g S_{int} + j A, \cdots, g S_{int} + j A }} \right)$ it is sufficient to restrict attention to the [[restriction]] of each $T_k$ to the subspace of
[[local observables]] induced by the finite set of [[Lagrangian densities]] $\{\mathbf{L}_{int,i}, \mathbf{\alpha}_{i'}\}_{i,i'}$.

This restriction is a [[continuous linear functional]] on the corresponding space of [[bump functions]] $\{g_{sw,i}, j_{sw,i'}\}$,
hence a [[distribution|dstributional]] [[section]] of a corresponding [[trivial vector bundle]].

In terms of this, prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal} says that the
choice of [[time-ordered products]] $T_k$ is [[induction|inductively]] in $k$ a choice of [[extension of distributions]] to the [[diagonal]].

If $\Sigma = \mathbb{R}^{p,1}$ is [[Minkowski spacetime]] and we impose the [[renormalization condition]] "translation invariance" (def. \ref{RenormalizationConditions}) then each $T_k$ is a distribution on $\Sigma^{k-1} = \mathbb{R}^{(p+1)(k-1)}$ and the [[extension of distributions]] is from the complement of the origina $0 \in \mathbb{R}^{(p+1)(k-1)}$.

=--

Therefore we now discuss [[extension of distributions]] (def. \ref{ExtensionOfDistributions} below) on [[Cartesian spaces]] from the complement of the origin to the origin. Since the space of choices of such extensions turns out to depend on the _[[scaling degree of distributions]]_,
we first discuss that (def. \ref{ScalingDegree} below).

+-- {: .num_defn #RescaledDistribution}
###### Definition
**([[scaling degree of distributions|rescaled distribution]])**

Let $n \in \mathbb{N}$. For $\lambda \in (0,\infty) \subset \mathbb{R}$ a [[positive number|positive]] [[real number]] write

$$
  \array{
    \mathbb{R}^n
      &\overset{s_\lambda}{\longrightarrow}&
    \mathbb{R}^n
    \\
    x &\mapsto& \lambda x
  }
$$

for the [[diffeomorphism]] given by multiplication with $\lambda$, using the canonical [[real vector space]]-structure of $\mathbb{R}^n$.

Then for $u \in \mathcal{D}'(\mathbb{R}^n)$ a [[distribution]] on the [[Cartesian space]] $\mathbb{R}^n$ the _rescaled distribution_ is the [[pullback of a distribution|pullback]] of $u$ along $m_\lambda$

$$
  u_\lambda
  \coloneqq
   s_\lambda^\ast u
  \;\in\;
  \mathcal{D}'(\mathbb{R}^n)
  \,.
$$

Explicitly, this is given by

$$
  \array{
     \mathcal{D}(\mathbb{R}^n)
       &\overset{ \langle  u_\lambda, - \rangle}{\longrightarrow}&
     \mathbb{R}
     \\
     b &\mapsto& \lambda^{-n} \langle u , b(\lambda^{-1}\cdot (-))\rangle
  }
  \,.
$$

Similarly for $X \subset \mathbb{R}^n$ an [[open subset]] which is invariant under $s_\lambda$, the rescaling of a distribution $u \in \mathcal{D}'(X)$ is is $u_\lambda \coloneqq s_\lambda^\ast u$.

=--

+-- {: .num_defn #ScalingDegree}
###### Definition
**([[scaling degree of a distribution]])**

Let $n \in \mathbb{N}$ and let $X \subset \mathbb{R}^n$ be an [[open subset]] of [[Cartesian space]] which is invariant under [[rescaling]] $s_\lambda$ (def. \ref{RescaledDistribution}) for all $\lambda \in (0,\infty)$, and let $u \in \mathcal{D}'(X)$ be a [[distribution]] on this subset. Then

1. The _[[scaling degree of a distribution|scaling degree]]_ of $u$ is the [[infimum]]

   $$
     sd(u)
     \;\coloneqq\;
     inf
     \left\{
       \omega \in \mathbb{R}
        \;\vert\;
       \underset{\lambda \to 0}{\lim}
        \lambda^\omega u_\lambda
        = 0
     \right\}
   $$

   of the set of [[real numbers]] $\omega$ such that the [[limit of a sequence|limit]] of the rescaled distribution $\lambda^\omega u_\lambda$ (def. \ref{RescaledDistribution}) vanishes. If there is no such $\omega$ one sets $sd(u) \coloneqq \infty$.

1. The _[[degree of divergence of a distribution|degree of divergence]]_ of $u$ is the difference of the scaling degree by the [[dimension]] of the underlying space:

  $$
    deg(u) \coloneqq sd(u) - n
     \,.
  $$

=--

+-- {: .num_example #NonSingularDistributionsScalingDegree}
###### Example
**([[scaling degree of distributions|scaling degree]] of [[non-singular distributions]])**

If $u = u_f$ is a [[non-singular distribution]] given by [[bump function]] $f \in C^\infty(X) \subset \mathcal{D}'(X)$, then its [[scaling degree of a distribution|scaling degree]] (def. \ref{ScalingDegree}) is non-[[positive number|positive]]

$$
  sd(u_f) \leq 0
  \,.
$$

Specifically if the first non-vanishing [[partial derivative]] $\partial_\alpha f(0)$ of $f$ at 0 occurs at order ${\vert \alpha\vert} \in \mathbb{N}$, then the scaling degree of $u_f$ is $-{\vert \alpha\vert}$.

=--

+-- {: .proof}
###### Proof

By definition we have for $b \in C^\infty_{cp}(\mathbb{R}^n)$ any [[bump function]] that

$$
  \begin{aligned}
    \left\langle
      \lambda^{\omega}
      (u_f)_\lambda,
      n
    \right\rangle
    & =
    \lambda^{\omega-n}
    \underset{\mathbb{R}^n}{\int}
       f(x) g(\lambda^{-1} x)
    d^n x
    \\
    & =
    \lambda^{\omega}
    \underset{\mathbb{R}^n}{\int}
       f(\lambda x) g(x)
    d^n x
  \end{aligned}
  \,,
$$

where in last line we applied [[change of integration variables]].

The limit of this expression is clearly zero for all  $\omega \gt 0$, which shows the first claim.

If moreover the first non-vanishing [[partial derivative]] of $f$ occurs at order ${\vert \alpha \vert} = k$, then [[Hadamard's lemma]] says that $f$ is of the form

$$
  f(x)
    \;=\;
  \left( \underset{i}{\prod} \alpha_i ! \right)^{-1}
  (\partial_\alpha f(0))
  \underset{i}{\prod} (x^i)^{\alpha_i}
  +
  \underset{ {\beta \in \mathbb{N}^n} \atop { {\vert \beta\vert} = {\vert \alpha \vert} + 1 }  }{\sum}
  \underset{i}{\prod} (x^i)^{\beta_i}
  h_{\beta}(x)
$$

where the $h_{\beta}$ are [[smooth functions]]. Hence in this case

$$
  \begin{aligned}
    \left\langle
      \lambda^{\omega}
      (u_f)_\lambda,
      n
    \right\rangle
    & =
    \lambda^{\omega + {\vert \alpha\vert }}
    \underset{\mathbb{R}^n}{\int}
      \left( \underset{i}{\prod} \alpha_i ! \right)^{-1}
     (\partial_\alpha f(0))
     \underset{i}{\prod} (x^i)^{\alpha_i}
     b(x)
    d^n x
    \\
    & \phantom{=}
    +
    \lambda^{\omega + {\vert \alpha\vert} + 1}
    \underset{\mathbb{R}^n}{\int}
      \underset{i}{\prod} (x^i)^{\beta_i}
      h_{\beta}(x)
      b(x)
    d^n x
  \end{aligned}
  \,.
$$

This makes manifest that the expression goes to zero with $\lambda \to 0$ precisely for $\omega \gt - {\vert \alpha \vert}$, which means that

$$
  sd(u_f) = -{\vert \alpha \vert}
$$

in this case.






=--

+-- {: .num_example #DerivativesOfDeltaDistributionScalingDegree}
###### Example
**([[scaling degree of a distribution|scaling degree]] of [[derivative of a distribution|derivatives]] of [[delta-distributions]])**

Let $\alpha \in \mathbb{N}^n$ be a multi-index and $\partial_\alpha \delta \in \mathcal{D}'(X)$ the corresponding [[partial derivative|partial]] [[derivative of distributions|derivatives]] of the [[delta distribution]] $\delta_0 \in \mathcal{D}'(\mathbb{R}^n)$ [[support of a distribution|supported]] at $0$. Then the [[degree of divergence of a distribution|degree of divergence]] (def. \ref{ScalingDegree}) of $\partial_\alpha \delta_0$ is the total order the derivatives

$$
  deg\left(
    {\, \atop \,} \partial_\alpha\delta_0{\, \atop \,}
  \right)
  \;=\;
  {\vert \alpha \vert}
$$

where ${\vert \alpha\vert} \coloneqq \underset{i}{\sum} \alpha_i$.

=--

+-- {: .proof}
###### Proof

By definition we have for $b \in C^\infty_{cp}(\mathbb{R}^n)$ any [[bump function]] that

$$
  \begin{aligned}
    \left\langle
      \lambda^\omega (\partial_\alpha \delta_0)_\lambda,
      b
    \right\rangle
    & =
    (-1)^{{\vert \alpha \vert}}
    \lambda^{\omega-n}
    \left(
      \frac{
        \partial^{{\vert \alpha \vert}}
      }{
       \partial^{\alpha_1} x^1  \cdots \partial^{\alpha_n}x^n
      }
      b(\lambda^{-1}x)
    \right)_{\vert x = 0}
    \\
    & =
    (-1)^{{\vert \alpha \vert}}
    \lambda^{\omega - n - {\vert \alpha\vert}}
    \frac{
      \partial^{{\vert \alpha \vert}}
    }{
     \partial^{\alpha_1} x^1  \cdots \partial^{\alpha_n}x^n
    }
    b(0)
  \end{aligned}
  \,,
$$

where in the last step we used the [[chain rule]] of [[differentiation]]. It is clear that this goes to zero with $\lambda$ as long as $\omega \gt n + {\vert \alpha\vert}$. Hence $sd(\partial_{\alpha} \delta_0) = n + {\vert \alpha \vert}$.

=--

+-- {: .num_example #FeynmanPropagatorOnMinkowskiScalingDegree}
###### Example
**([[scaling degree of a distribution|scaling degree]] of [[Feynman propagator]] on [[Minkowski spacetime]])**

Let

$$
  \Delta_F(x)
  \;=\;
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
  }
  \, d k_0 \, d^p \vec k
$$

be the [[Feynman propagator]] for the massive [[free field|free]] [[real scalar field]] on $n = p+1$-dimensional [[Minkowski spacetime]] (prop. \ref{FeynmanPropagatorAsACauchyPrincipalvalue}). Its [[scaling degree of a distribution|scaling degree]] is

$$
  \begin{aligned}
    sd(\Delta_{F})
    & = n - 2
    \\
    & = p -1
  \end{aligned}
  \,.
$$

=--

([Brunetti-Fredenhagen 00, example 3 on p. 22](renormalization#BrunettiFredenhagen00))

+-- {: .proof}
###### Proof

Regarding $\Delta_F$ as a [[generalized function]] via the given [[Fourier transform of distributions|Fourier-transform]] expression, we find by [[change of integration variables]] in the Fourier integral that in the scaling limit the Feynman propagator becomes that for vannishing [[mass]], which scales homogeneously:

$$
  \begin{aligned}
    \underset{\lambda \to 0}{\lim}
    \left(
    \lambda^\omega
    \;
    \Delta_F(\lambda x)
    \right)
    & =
    \underset{\lambda \to 0}{\lim}
    \left(
    \lamba^{\omega}
    \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
    \frac{+i}{(2\pi)^{p+1}}
    \int
    \int_{-\infty}^\infty
    \frac{
       e^{i k_\mu \lambda x^\mu}
    }{
      - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
    }
    \, d k_0 \, d^p \vec k
    \right)
    \\
    & =
    \underset{\lambda \to 0}{\lim}
    \left(
    \lambda^{\omega-n}
    \;
    \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
    \frac{+i}{(2\pi)^{p+1}}
    \int
    \int_{-\infty}^\infty
    \frac{
       e^{i k_\mu \lambda x^\mu}
    }{
      - (\lambda^{-2}) k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
    }
    \, d k_0 \, d^p \vec k
    \right)
    \\
    & =
    \underset{\lambda \to 0}{\lim}
    \left(
    \lambda^{\omega-n + 2 }
    \;
    \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
    \frac{+i}{(2\pi)^{p+1}}
    \int
    \int_{-\infty}^\infty
    \frac{
       e^{i k_\mu \lambda x^\mu}
    }{
      - k_\mu k^\mu + i \epsilon
    }
    \, d k_0 \, d^p \vec k
    \right)
    \,.
  \end{aligned}
$$

=--

+-- {: .num_prop #ScalingDegreeOfDistributionsBasicProperties}
###### Proposition
**(basic properties of [[scaling degree of distributions]])**

Let $X \subset \mathbb{R}^n$ and $u \in \mathcal{D}'(X)$ be a [[distribution]] as in def. \ref{RescaledDistribution}, such that its [[scaling degree of a distribution|scaling degree]] is finite: $sd(u) \lt \infty$ (def. \ref{ScalingDegree}). Then

1. For $\alpha \in \mathbb{N}^n$, the [[partial derivative|partial]] [[derivative of distributions]] $\partial_\alpha$ increases scaling degree at most by ${\vert \alpha\vert }$:

   $$
     deg(\partial_\alpha u) \;\leq\; deg(u) + {\vert \alpha\vert}
   $$

1. For $\alpha \in \mathbb{N}^n$, the [[product of distributions]] with the smooth coordinate functions $x^\alpha$ decreases scaling degree at least by ${\vert \alpha\vert }$:


   $$
     deg(x^\alpha u) \;\leq\; deg(u) - {\vert \alpha\vert}
   $$

1. Under [[tensor product of distributions]] their scaling degrees add:

   $$
     sd(u \otimes v) \leq sd(u) + sd(v)
   $$

   for $v \in \mathcal{D}'(Y)$ another distribution on $Y \subset \mathbb{R}^{n'}$;

1. $deg(f u) \leq deg(u) - k$ for $f \in C^\infty(X)$ and $f^{(\alpha)}(0) = 0$ for ${\vert \alpha\vert} \leq k-1$;

=--

([Brunetti-Fredenhagen 00, lemma 5.1](renormalization#BrunettiFredenhagen00), [Dütsch 18, exercise 3.34](renormalization#Duetsch18))



+-- {: .proof}
###### Proof

The first three statements follow with manipulations as in example \ref{NonSingularDistributionsScalingDegree} and example \ref{DerivativesOfDeltaDistributionScalingDegree}.

For the fourth...

=--




+-- {: .num_prop #ScalingDegreeOfProductDistribution}
###### Proposition
**([[scaling degree of distributions|scaling degree]] of [[product of distributions|product distribution]])**

Let $u,v \in \mathcal{D}'(\mathbb{R}^n)$ be two [[distributions]] such that

1. both have finite [[degree of divergence of a distribution|degree of divergence]] (def. \ref{ScalingDegree})

   $$
     deg(u), deg(v) \lt \infty
   $$

1. their [[product of distributions]] is well-defined

   $$
     u v \in \mathcal{D}'(\mathbb{R}^n)
   $$

   (in that their [[wave front sets]] satisfy [[Hörmander's criterion]])

then the product distribution has [[degree of divergence of a distribution|degree of divergence]] bounded by the sum of the separate degrees:

$$
  deg(u v)
  \;\leq\;
  deg(u) + deg(v)
  \,.
$$

=--


With the concept of [[scaling degree of distributions]] in hand, we may now discuss [[extension of distributions]]:

+-- {: .num_defn #ExtensionOfDistributions}
###### Definition
**([[extension of distributions]])**

Let $X \overset{\iota}{\subset} \hat X$ be an inclusion of [[open subsets]] of some [[Cartesian space]]. This induces the operation of [[restriction of distributions]]

$$
  \mathcal{D}'(\hat X)
    \overset{\iota^\ast}{\longrightarrow}
  \mathcal{D}'(X)
  \,.
$$

Given a [[distribution]] $u \in \mathcal{D}'(X)$, then an _[[extension]]_ of $u$ to $\hat X$ is a distribution $\hat u \in \mathcal{D}'(\hat X)$ such that

$$
  \iota^\ast \hat u
  \;=\;
  u
  \,.
$$

=--


+-- {: .num_prop #ExtensionUniqueNonPositiveDegreeOfDivergence}
###### Proposition
**(unique [[extension of distributions]] with negative [[degree of divergence of a distribution|degree of divergence]])**

For $n \in \mathbb{N}$, let $u \in \mathcal{D}'(\mathbb{R}^n \setminus \{0\})$ be a [[distribution]] on the [[complement]] of the origin, with [[negative number|negative]] [[degree of divergence of a distribution|degree of divergence]] at the origin

$$
  deg(u) \lt 0
  \,.
$$

Then $u$ has a _unique_ [[extension of distributions]] $\hat u \in \mathcal{D}'(\mathbb{R}^n)$ to the origin with the same degree of divergence

$$
  deg(\hat u) = deg(u)
  \,.
$$

=--

([Brunetti-Fredenhagen 00, theorem 5.2](renormalization#BrunettiFredenhagen00), [Dütsch  18, theorem 3.35 a)](renormalization#Duetsch18))

+-- {: .proof}
###### Proof

Regarding uniqueness:

Suppose $\hat u$ and ${\hat u}^\prime$ are two extensions of $u$ with $deg(\hat u) = deg({\hat u}^\prime)$. Both being extensions of a distribution defined on $\mathbb{R}^n \setminus \{0\}$, this difference has [[support of a distribution|support]] at the origin $\{0\} \subset \mathbb{R}^n$. By prop. \ref{PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions} this implies that it is a linear combination of [[derivative of a distribution|derivatives]] of the [[delta distribution]] [[support of a distribution|supported]] at the origin:

$$
  {\hat u}^\prime - \hat u
  \;=\;
  \underset{
    {\alpha \in \mathbb{N}^n}
  }{\sum}
  c^\alpha \partial_\alpha \delta_0
$$

for constants $c^\alpha \in \mathbb{C}$. But by example \ref{DerivativesOfDeltaDistributionScalingDegree} the [[degree of divergence of a distribution|degree of divergence]] of these [[point-supported distributions]] is non-negative

$$
  deg( \partial_\alpha \delta_0)
  =
  {\vert \alpha\vert} \geq 0
  \,.
$$

This implies that $c^\alpha = 0$ for all $\alpha$, hence that the two extensions coincide.


Regarding existence:


Let

$$
  b \in C^\infty_{cp}(\mathbb{R}^n)
$$

be a [[bump function]] which is $\leq 1$ and [[constant function|constant]] on 1 over a [[neighbourhood]] of the origin. Write

$$
  \chi \coloneqq 1 - b \;\in\; C^\infty(\mathbb{R}^n)
$$

<center>
<img src="https://ncatlab.org/nlab/files/PointExtensionOfDistributions.png" >
</center>

> graphics grabbed from [Dütsch 18, p. 108](renormalization#Duetsch18)

and for $\lambda \in (0,\infty)$ a [[positive real number]], write

$$
  \chi_\lambda(x)
  \coloneqq
  \chi(\lambda x)
  \,.
$$

Since the [[product of distributions|product]] $\chi_\lambda u$ has [[support of a distribution]] on a [[complement]] of  a [[neighbourhood]] of the origin, we may extend it by zero to a distribution on all of $\mathbb{R}^n$, which we will denote by the same symbols:

$$
  \chi_\lambda u \in \mathcal{D}'(\mathbb{R}^n)
  \,.
$$

By construction $\chi_\lambda u$ coincides with $u$ away from a neighbourhood of the origin, which moreover becomes arbitrarily small as $\lambda$ increases.  This means that if the following [[limit of a sequence|limit]] exists

$$
  \hat u
  \;\coloneqq\;
  \underset{\lambda \to \infty}{\lim}
   \chi_\lambda u
$$

then it is an extension of $u$.

To see that the limit exists, it is sufficient to observe that we have a [[Cauchy sequence]], hence that for all $b\in C^\infty_{cp}(\mathbb{R}^n)$ the difference

$$
  (\chi_{n+1} u - \chi_n u)(b)
  \;=\;
  u(b)( \chi_{n+1} + \chi_n )
$$

becomes arbitrarily small.

It remains to see that the unique extension $\hat u$ thus established has the same scaling degree as $u$. This is shown in ([Brunetti-Fredenhagen 00, p. 24](extension+of+distributions#BrunettiFredenhagen00)).

=--


+-- {: .num_prop #SpaceOfPointExtensions}
###### Proposition
**(space of [[point-extensions of distributions]])

For $n \in \mathbb{N}$, let $u \in \mathcal{D}'(\mathbb{R}^n \setminus \{0\})$ be a [[distribution]] of [[scaling degree of a distribution|degree of divergence]] $deg(u) \lt \infty$.

Then $u$ does admit at least one [[extension of distributions|extension]] (def. \ref{ExtensionOfDistributions}) to a distribution $\hat u \in \mathcal{D}'(\mathbb{R}^n)$, and every choice of extension has the same [[degree of divergence of a distribution|degree of divergence]] as $u$

$$
  deg(\hat u) = deg(u)
  \,.
$$

Moreover, any two such extensions $\hat u$ and ${\hat u}^\prime$ differ by a linear combination of [[partial derivatives|partial]] [[derivatives of distributions]] of order $\leq deg(u)$ of the [[delta distribution]] $\delta_0$ [[support of a distribution|supported]] at the origin:

$$
  {\hat u}^\prime
  -
  \hat u
  \;=\;
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha\vert} \leq deg(u) }
  }{\sum}
  q^\alpha
  \partial_\alpha \delta_0
  \,,
$$

for a finite number of constants $q^\alpha \in \mathbb{C}$.

=--

This is essentially ([Hörmander 90, thm. 3.2.4](renormalization#Hoermander90)). We follow ([Brunetti-Fredenhagen 00, theorem 5.3](renormalization#BrunettiFredenhagen00)), which was inspired by ([Epstein-Glaser 73, section 5](#EpsteinGlaser73)). Review of this approach is in ([Dütsch 18, theorem 3.35 (b)](renormalization#Duetsch18)), see also remark \ref{WExtensions} below.


+-- {: .proof}
###### Proof


For $f \in C^\infty(\mathbb{R}^n)$ a [[smooth function]], and $\rho \in \mathbb{N}$, we say that _$f$ vanishes to order $\rho$_ at the origin if all [[partial derivatives]] with multi-index $\alpha \in \mathbb{N}^n$ of total order ${\vert \alpha\vert} \leq \rho$ vanish at the origin:

$$
  \partial_\alpha f (0) = 0
  \phantom{AAA}
  {\vert \alpha\vert} \leq \rho
  \,.
$$

By [[Hadamard's lemma]], such a function may be written in the form

$$
  \label{ForVanishingOrderRhoHadamardExpansion}
  f(x)
  \;=\;
  \underset{
    {\alpha \in \mathbb{N}^n}
    \atop
    { {\vert \alpha \vert} = \rho + 1 }
  }{\sum}
  x^\alpha
  r_\alpha(x)
$$

for [[smooth functions]] $r_\alpha \in C^\infty_{cp}(\mathbb{R}^n)$.

Write

$$
  \mathcal{D}_\rho(\mathbb{R}^n)
    \hookrightarrow
  \mathcal{D}(\mathbb{R}^n)
    \coloneqq
  C^\infty_{cp}(\mathbb{R}^n)
$$

for the subspace of that of all [[bump functions]] on those that vanish to order $\rho$ at the origin.

By definition this is equivalently the joint [[kernel]] of the [[partial derivative|partial]] [[derivatives of distributions]] of order ${\vert \alpha\vert}$ of the [[delta distribution]] $\delta_0$ [[support of a distribution|supported]] at the origin:

$$
  b \in \mathcal{D}_\rho(\mathbb{R}^n)
  \phantom{AA}
  \Leftrightarrow
  \phantom{AA}
  \underset{
    {\alpha \in \mathbb{N}^n}
      \atop
    { {\vert \alpha\vert} \leq \rho }
  }
  {\forall}
    \left\langle \partial_\alpha \delta_0, b \right\rangle
  = 0
  \,.
$$

Therefore every [[continuous linear map|continuous linear]] [[projection]]

$$
  \label{ForExtensionOfDistributionsProjectionMaps}
  p_\rho
   \;\colon\;
  \mathcal{D}(\mathbb{R}^n)
    \longrightarrow
  \mathcal{D}_\rho(\mathbb{R}^n)
$$

may be obtained from a choice of _dual basis_ to the $\{\partial_\alpha \delta_0\}$, hence a choice of smooth functions

$$
  \left\{
    w^\beta \in C^\infty_{cp}(\mathbb{R}^n)
  \right\}_{ { \beta \in \mathbb{N}^n } \atop { {\vert \beta\vert} \leq \rho } }
$$

such that

$$
  \left\langle
    \partial_\alpha \delta_0
    \,,\,
    w^\beta
  \right\rangle
  \;=\;
  \delta_\alpha^\beta
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \partial_\alpha w^\beta(0)
    \;=\;
  \delta_\alpha^\beta
  \phantom{AAAA}
  \text{for}\, {\vert \alpha\vert} \leq \rho
  \,,
$$

by setting

$$
  \label{SpaceOfSmoothFunctionsOfGivenVaishingOrderProjector}
  p_\rho
  \;\coloneqq\;
  id
  \;-\;
  \left\langle
  \underset{
    {\alpha \in \mathbb{N}^n}
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  w^\alpha \partial_\alpha \delta_0
  \,,\,
  (-)
  \right\rangle
  \,,
$$

hence

$$
  p_\rho
  \;\colon\;
  b
    \mapsto
  b
    -
  \underset{
    {\alpha \in \mathbb{N}^n}
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  (-1)^{{\vert \alpha\vert}} w^\alpha \partial_\alpha b(0)
  \,.
$$

Together with [[Hadamard's lemma]] in the form (eq:ForVanishingOrderRhoHadamardExpansion) this means that every $b \in \mathcal{D}(\mathbb{R}^n)$ is decomposed as

$$
  \label{ForExtensionOfDistributionsTestFunctionDecomposition}
  \begin{aligned}
  b(x)
  & =
  p_\rho(b)(x)
  \;+\;
  (id - p_\rho)(b)(x)
  \\
  & =
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha \vert} = \rho + 1 }
  }{\sum}
  x^\alpha r_\alpha(x)
  \;+\;
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha \vert} \leq \rho }
  }{\sum}
  (-1)^{{\vert \alpha \vert}}
  w^\alpha \partial_\alpha b(0)
  \end{aligned}
$$

Now let

$$
  \rho
  \;\coloneqq\;
  deg(u)
  \,.
$$

Observe that (by prop. \ref{ScalingDegreeOfDistributionsBasicProperties}) the [[degree of divergence of a distribution|degree of divergence]] of the [[product of distributions]] $x^\alpha u$ with ${\vert \alpha\vert} = \rho + 1$ is [[negative number|negative]]


$$
  \begin{aligned}
    deg\left(
      x^\alpha u
    \right)
    & =
    \rho - {\vert \alpha \vert}
    \leq
    -1
 \end{aligned}
$$

Therefore prop. \ref{ExtensionUniqueNonPositiveDegreeOfDivergence} says that each $x^\alpha u$ for ${\vert \alpha\vert} = \rho + 1$ has a unique extension $\widehat{ x^\alpha u}$ to the origin. Accordingly the composition $u \circ p_\rho$ has a unique extension, by (eq:ForExtensionOfDistributionsTestFunctionDecomposition):

$$
  \label{ExtensionOfDitstributionsPointFixedAndChoice}
  \begin{aligned}
  \left\langle
    \hat u
    \,,\,
    b
  \right\rangle
  & =
  \left\langle
    \hat u
    ,
    p_\rho(b)
  \right\rangle
  +
  \left\langle
    \hat u
    ,
    (id - p_\rho)(b)
  \right\rangle
  \\
  & =
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha \vert} = \rho + 1 }
  }{\sum}
  \underset{
    \text{unique}
  }{
  \underbrace{
    \left\langle
     \widehat{x^\alpha u}
      \,,\,
      r_\alpha
    \right\rangle
  }
  }
  \;+\;
  \underset{
    { \alpha \in \mathbb{N}^n }
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  \underset{
    {  q^\alpha }
    \atop
    { \text{choice} }
  }{
  \underbrace{
  \langle
    \hat u
    \,,\,
    w^\alpha
  \rangle
  }
  }
  \left\langle
    \partial_\alpha \delta_0
    \,,\,
    b
  \right\rangle
  \end{aligned}
$$

That says that $\hat u$ is of the form

$$
  \hat u
  \;=\;
  \underset{
    \text{unique}
  }{
  \underbrace{
    \widehat{
      u \circ p_\rho
    }
  }
  }
  +
  \underset{
    { \alpha \in \mathbb{N}^n  }
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  c^\alpha
  \,
  \partial_\alpha \delta_0
$$

for a finite number of constants $c^\alpha \in \mathbb{C}$.

Notice that for any extension $\hat u$ the exact value of the $c^\alpha$ here depends on the arbitrary choice of dual basis $\{w^\alpha\}$ used for this construction. But the uniqueness of the first summand means that for any two choices of extensions $\hat u$ and ${\hat u}^\prime$, their difference is of the form

$$
  {\hat u}^\prime - \hat u
  \;=\;
  \underset{
    { \alpha \in \mathbb{N}^n  }
    \atop
    { {\vert \alpha\vert} \leq \rho }
  }{\sum}
  ( (c')^\alpha - c^\alpha )
  \,
  \partial_\alpha \delta_0
  \,,
$$

where the constants $q^\alpha \coloneqq ( (c')^\alpha - c^\alpha ) \in \mathbb{C}$ are independent of any choices.


It remains to see that all these $\hat u$ in fact have the same degree of divergence as $u$.

By example \ref{DerivativesOfDeltaDistributionScalingDegree} the degree of divergence of the point-supported distributions on the right is $deg(\partial_\alpha \delta_0) = {\vert \alpha\vert} \leq \rho$.

Therefore to conclude it is now sufficient to show that

$$
  deg\left(
    \widehat{
      u \circ p_\rho
    }
  \right)
  \;=\;
  \rho
  \,.
$$

This is shown in ([Brunetti-Fredenhagen 00, p. 25](extension+of+distributions#BrunettiFredenhagen00)).

=--


+-- {: .num_remark #WExtensions}
###### Remark
**("W-extensions")**

Since in [Brunetti-Fredenhagen 00, (38)](renormalization#BrunettiFredenhagen00) the projectors (eq:SpaceOfSmoothFunctionsOfGivenVaishingOrderProjector) are denoted "$W$", the construction of [[extensions of distributions]] via the proof of prop. \ref{SpaceOfPointExtensions} has come to be called "W-extensions" (e.g [Dütsch 18](renormalization#Duetsch18)).

=--

In conclusion we obtain the central theorem of [[causal perturbation theory]]:

+-- {: .num_theorem #ExistenceRenormalization}
###### Theorem
**(existence and choices of [[renormalization|("re"-)normalization]] of [[S-matrices]]/[[perturbative QFTs]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[gauge fixing|gauge-fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]], according to def. \ref{VacuumFree}, such that the underlying [[spacetime]] is
[[Minkowski spacetime]] and the [[Wightman propagator]] $\Delta_H$ is translation-invariant.

Then:

1. an [[S-matrix scheme]] $\mathcal{S}$ (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) around this vacuum exists;

1. for $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$ a [[local observable]]
   as in def. \ref{FormalParameters}, regarded
   as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]], the space of possible choices
   of [[S-matrices]]

   $$
     \mathcal{S}(g S_{int} + j A)
     \;\in\;
     PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]
   $$

   hence of the corresponding [[perturbative QFTs]], by prop. \ref{InteractingFieldAlgebraOfObservablesIsFormalDeformationQuantization},   is, [[induction|inductively]] in $k \in \mathbb{N}$, a [[finite dimensional vector space|finite dimensional]] [[affine space]],
   parameterizing the [[extension of distributions|extension]] of the [[time-ordered product]] $T_k$ to the locus of
   coinciding interaction points.

=--


+-- {: .proof}
###### Proof

By prop. \ref{FeynmanPropagatorOnMinkowskiScalingDegree} the [[Feynman propagator]] is finite [[scaling degree of a distribution]],
so that by prop. \ref{ScalingDegreeOfProductDistribution} the binary [[time-ordered product]] away from the diagonal
$T_2(-,-)\vert_{\Sigma^2 \setminus diag(\Sigma)} = (-) \star_{F} (-)$ has finite scaling degree.

By prop. \ref{ScalingDegreeOfProductDistribution} this implies  that in the inductive
description of the time-ordered products by prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal},
each induction step is the [[extension of distributions]] of finite [[scaling degree of a distribution]] to the point.
By prop. \ref{SpaceOfPointExtensions} this always exists.

This proves the first statement.

Now if a polynomial local interaction is fixed, then via remark \ref{TimeOrderedProductOfFixedInteraction}
each induction step involved extending a finite number of distributions, each of finite scaling degree.
By prop. \ref{SpaceOfPointExtensions} the corresponding space of choices is in each step
a finite-dimensional affine space.


=--


$\,$


**[[Stückelberg-Petermann renormalization group]]**
 {#SPRenormalizationGroup}

A genuine re-normalization is the passage from one [[S-matrix]] [[renormalization scheme|("re"-)normalization scheme]]
$\mathcal{S}$ to another such scheme $\mathcal{S}'$. The [[induction|inductive]] [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-normalization)]] construction (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}) shows that the difference between
any $\mathcal{S}$ and $\mathcal{S}'$ is inductively in $k \in \mathbb{N}$ a choice of extra term in the
[[time-ordered product]] of $k$ factors, equivalently in the [[Feynman amplitudes]] for [[Feynman diagrams]] with
$k$ [[vertices]], that contributes when all $k$ of these vertices coincide in [[spacetime]] (prop. \ref{SpaceOfPointExtensions}).

A natural question is whether these additional interactions that appear when several interaction vertices coincide
may be absorbed into a re-definition of the original interaction $g S_{int} + j A$. Such an
_[[interaction vertex redefinition]]_ (def. \ref{InteractionVertexRedefinition} below)

$$
  \mathcal{Z}
  \;\colon\;
  g S_{int} + j A
  \;\mapsto\;
  g S_{int} + j A
  \;+\;
  \text{higher order corrections}
$$

should perturbatively send [[local observables|local]] interactions to local interactions with higher order corrections.

The _[[main theorem of perturbative renormalization]]_ (theorem \ref{PerturbativeRenormalizationMainTheorem} below)
says that indeed under mild conditions every re-normalization $\mathcal{S} \mapsto \mathcal{S}'$ is induced by such an [[interaction vertex redefinition]] in that
there exists a _unique_ such redefinition $\mathcal{Z}$ so that for every local interaction $g S_{int} +  j A$ we have
that [[scattering amplitudes]] for the interaction $g S_{int} + j A$ computed with the [[renormalization scheme|("re"-)normalization scheme]]
$\mathcal{S}'$ equal those computed with $\mathcal{S}$ but applied
to the [[interaction vertex redefinition|re-defined interaction]] $\mathcal{Z}(g S_{int} + j A)$:

$$
  \mathcal{S}'
  \left(
    {\, \atop \,}
    g S_{int} +  j A
    {\, \atop \,}
  \right)
  \;=\;
  \mathcal{S}\left( {\, \atop \,} \mathcal{Z}(g S_{int} + j A) {\, \atop \,} \right)
  \,.
$$

This means that the [[interaction vertex redefinitions]] $\mathcal{Z}$ form a [[group]] under [[composition]]
which [[action|acts]] [[transitive action|transitively]] and [[free action|freely]], hence [[regular action|regularly]], on the
set of [[S-matrix]] [[renormalization schemes|("re"-)normalization schemes]];
this is called the _[[Stückelberg-Petermann renormalization group]]_ (theorem \ref{PerturbativeRenormalizationMainTheorem} below).



$\,$

+-- {: .num_defn #InteractionVertexRedefinition}
###### Definition
**([[perturbative interaction vertex redefinition]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] (def. \ref{VacuumFree}).

A _[[perturbative interaction vertex redefinition]]_ (or just _[[vertex redefinition]]_, for short) is an [[endofunction]]

$$
  \mathcal{Z}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

on [[local observables]] with formal parameters adjoined (def. \ref{FormalParameters}) such that there exists a sequence $\{Z_k\}_{k \in \mathbb{N}}$ of [[continuous linear functionals]], symmetric in their arguments, of the form

$$
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [ \hbar, g, j] ]}}
  \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

such that for all $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle$ the following conditions hold:

1. (perturbation)

   1. $Z_0(g S_{int + j A}) = 0$

   1. $Z_1(g S_{int} + j A) = g S_{int} + j A$

   1. and

      $$
        \begin{aligned}
          \mathcal{Z}(g S_{int} + j A)
          & =
          Z \exp_\otimes( g S_{int} + j A )
          \\
          &
          \coloneqq
          \underset{k \in \mathbb{N}}{\sum}
          \frac{1}{k!}
          Z_k(
            \underset{
              k \, \text{args}
            }{
              \underbrace{
                g S_{int} + j A , \cdots, g S_{int} + j A
              }
            }
          )
        \end{aligned}
      $$

1. (field independence) The [[local observable]] $\mathcal{Z}(g S_{int} + j A)$ depends on the [[field histories]] only through its argument $g S_{int} + j A $, hence by the [[chain rule]]:

   $$
     \label{FieldIndependenceVertexRedefinition}
     \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
     \mathcal{Z}(g S_{int} + j A)
     \;=\;
     \mathcal{Z}'_{g S_{int} + j A}
     \left(
         \frac{\delta}{\delta \mathbf{\Phi}^a(x)} (g S_{int} + j A)
     \right)
   $$

=--

The following proposition should be compared to the axiom of _[[causal additivity]]_ of the [[S-matrix]] scheme (eq:CausalAdditivity):

+-- {: .num_prop #InteractionVertexRedefinitionAdditivity}
###### Proposition
**(local additivity of [[vertex redefinitions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] (def. \ref{VacuumFree}) and let $\mathcal{Z}$ be a [[vertex redefinition]] (def. \ref{InteractionVertexRedefinition}).

Then for all [[local observables]] $O_0, O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g, j\rangle$ with spacetime support denoted $supp(O_i) \subset \Sigma$ (def. \ref{SpacetimeSupport}) we have

1. (local additivity)

   $$
     \begin{aligned}
       &
       \left(
         supp(O_1)
         \cap
         supp(O_2)
         =
         \emptyset
       \right)
       \\
       &
         \Rightarrow
       \phantom{AA}
       \mathcal{Z}( O_0 + O_1 + O_2)
       =
       \mathcal{Z}( O_0 + O_1 ) - \mathcal{Z}(O_0) + \mathcal{Z}(O_0 + O_2)
     \end{aligned}
     \,.
   $$

1. (preservation of spacetime support)

   $$
     supp
     \left(
       {\, \atop \,}
         \mathcal{Z}(O_0 + O_1)
         -
         \mathcal{Z}(O_0)
       {\, \atop \,}
     \right)
     \;\subset\;
     supp(O_1)
   $$

   hence in particular

   $$
     supp
     \left(
       {\, \atop \,}
       \mathcal{Z}(O_1)
       {\, \atop \,}
     \right) = supp(O_1)
   $$

=--

([Dütsch 18, exercise 3.98](renormalization#Duetsch18))

+-- {: .proof}
###### Proof

Under the inclusion

$$
  LocObs(E_{\text{BV-BRST}})
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})
$$

of [[local observables]] into [[polynomial observables]] we may think of each $Z_k$ as a [[generalized function]], as for [[time-ordered products]] in remark \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}.

Hence if

$$
  O_j = \underset{\Sigma}{\int} j^\infty_\Sigma( \mathbf{L}_j )
$$

is the [[transgression of variational differential forms|transgression]] of a [[Lagrangian density]] $\mathbf{L}$ we get

$$
  Z_k(
    (O_1 + O_2 + O_3)
    ,
    \cdots
    ,
    (O_1 + O_2 + O_3)
  )
  =
  \underset{
    j_1, \cdots, j_k \in \{0,1,2\}
  }{\sum}
  \underset{\Sigma^{k}}{\int}
    Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
  \,.
$$

Now by definition $Z_k(\cdots)$ is in the subspace of [[local observables]], i.e. those [[polynomial observables]] whose [[coefficient]] [[distributions]] are [[support of a distribution|supported]] on the [[diagonal]], which means that

$$
  \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
  \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
  Z_{k}(\cdots)
  =
  0
  \phantom{AA}
  \text{for}
  \phantom{AA}
  x \neq y
$$

Together with the axiom "field independence" (eq:FieldIndependenceVertexRedefinition) this means that the support of these generalized functions in the [[integrand]] here must be on the [[diagonal]], where $x_1 = \cdots = x_k$.

By the assumption that the spacetime supports of $O_1$ and $O_2$ are disjoint, this means that only the summands with $j_1, \cdots, j_k \in \{0,1\}$ and those with $j_1, \cdots, j_k \in \{0,2\}$ contribute to the above sum. Removing the overcounting of those summands where all $j_1, \cdots, j_k \in \{0\}$ we get


$$
  \begin{aligned}
    & Z_k\left(
      {\, \atop \,}
      (O_1 + O_2 + O_3)
      ,
      \cdots
      ,
      (O_1 + O_2 + O_3)
      {\, \atop \,}
    \right)
    \\
    & =
    \underset{
      j_1, \cdots, j_k \in \{0,1\}
    }{\sum}
    \underset{\Sigma^{k}}{\int}
      Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
    \\
    & \phantom{=}
    -
    \underset{
      j_1, \cdots, j_k \in \{0\}
    }{\sum}
    \underset{\Sigma^{k}}{\int}
      Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
    \\
    & \phantom{=}
    -
    \underset{
      j_1, \cdots, j_k \in \{0,2\}
    }{\sum}
    \underset{\Sigma^{k}}{\int}
      Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
    \\
    & =
    Z_k\left( {\, \atop \,} (O_0 + O_1), \cdots, (O_0 + O_1) {\, \atop \,}\right)
    -
    Z_k\left( {\, \atop \,} O_0, \cdots,  O_0 {\, \atop \,} \right)
    +
    Z_k\left( {\, \atop \,} (O_0 + O_2), \cdots, (O_0 + O_2) {\, \atop \,} \right)
  \end{aligned}
  \,.
$$

This directly implies the claim.

=--

As a corollary we obtain:

+-- {: .num_prop #CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition}
###### Proposition
**([[composition]] of [[S-matrix]] scheme with [[vertex redefinition]] is again [[S-matrix]] scheme)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] (def. \ref{VacuumFree}) and let $\mathcal{Z}$ be a [[vertex redefinition]] (def. \ref{InteractionVertexRedefinition}).

Then for

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

and [[S-matrix]] scheme (def. \ref{LagrangianFieldTheoryPerturbativeScattering}), the [[composition|composite]]

$$
  \mathcal{S} \circ \mathcal{Z}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \overset{\mathcal{Z}}{\longrightarrow}
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \overset{\mathcal{S}}{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

is again an [[S-matrix]] scheme.

Moreover, if $\mathcal{S}$ satisfies the [[renormalization condition]] "field independence" (prop. \ref{BasicConditionsRenormalization}), then so does $\mathcal{S} \circ \mathcal{Z}$.

=--

(e.g [Dütsch 18, theorem 3.99 (b)](renormalization#Duetsch18))

+-- {: .proof}
###### Proof

It is clear that [[causal order]] of the spacetime supports implies that they are in particular [[disjoint subset|disjoint]]

$$
  \left(
    {\, \atop \,}
    supp(O_1)
    {\vee\!\!\!\wedge}
    supp(O_2)
    {\, \atop \,}
  \right)
  \phantom{AA}
  \Rightarrow
  \phantom{AA}
  \left(
    {\, \atop \,}
    supp(O_1)
      \cap
    supp(O_)
    \;=\;
    \emptyset
    {\, \atop \,}
  \right)
$$

Therefore the local additivity of $\mathcal{Z}$ (prop. \ref{InteractionVertexRedefinitionAdditivity})
and the [[causal factorization]] of the [[S-matrix]] (remark \ref{DysonCausalFactorization})
imply the causal factorization of the composite:

$$
  \begin{aligned}
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_1 + O_2)
      {\, \atop \,}
    \right)
    & =
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_1)
      +
      \mathcal{Z}(O_2)
      {\, \atop \,}
    \right)
    \\
    & =
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_1)
      {\, \atop \,}
    \right)
    \,
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_2)
      {\, \atop \,}
    \right)
    \,.
  \end{aligned}
$$

But by prop. \ref{CausalFactorizationAlreadyImpliesSMatrix} this implies in turn [[causal additivity]]
and hence that $\mathcal{S} \circ \mathcal{Z}$ is itself an S-matrix scheme.

Finally that $\mathcal{S} \circ \mathcal{Z}$ satisfies "field indepndence" if $\mathcal{S}$ does is immediate by the [[chain rule]], given that $\mathcal{Z}$ satisfies this condition by definition.

=--


+-- {: .num_prop #AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}
###### Proposition
**(any two [[S-matrix]] [[renormalization schemes]] differ by unique [[vertex redefinition]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] (def. \ref{VacuumFree}).

Then for $\mathcal{S}, \mathcal{S}'$ any two [[S-matrix]] schemes (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) which both satisfy the [[renormalization condition]] "field independence", the  there exists a unique [[vertex redefinition]] $\mathcal{Z}$ (def. \ref{InteractionVertexRedefinition}) relating them by [[composition]], i. e. such  that

$$
  \mathcal{S}'
  \;=\;
  \mathcal{S} \circ \mathcal{Z}
  \,.
$$

=--


+-- {: .proof}
###### Proof

By applying both sides of the equation to linear combinations of local observables of the form $\kappa_1 O_1 + \cdots + \kappa_k O_k$ and then taking [[derivatives]] with respect to $\kappa$ at $\kappa_j = 0$ (as in example \ref{TimeOrderedProductsFromSMatrixScheme}) we get that the equation in question implies

$$
  (i \hbar)^k
  \frac{
    \partial^k
  }{
    \partial \kappa_1 \cdots \partial \kappa_k
  }
  \mathcal{S}'( \kappa_1 O_1 + \cdots + \kappa_k O_k )
  \vert_{\kappa_1, \cdots, \kappa_k = 0}
  \;=\;
  (i \hbar)^k
  \frac{
    \partial^k
  }{
    \partial \kappa_1 \cdots \partial \kappa_k
  }
  \mathcal{S} \circ \mathcal{Z}( \kappa_1 O_1 + \cdots + \kappa_k O_k )
  \vert_{\kappa_1, \cdots, \kappa_k = 0}
$$

which in components means that

$$
  \begin{aligned}
    T'_k( O_1, \cdots, O_k )
    & =
    \underset{
      2 \leq n \leq k
    }{\sum}
      \frac{1}{n!}
      (i \hbar)^{k-n}
      \underset{
        { { I_1 \sqcup \cdots \sqcup I_n } \atop { =  \{1, \cdots, k\}, } }
        \atop
        { I_1, \cdots, I_n \neq \emptyset }
      }{\sum}
      T_n
      \left(
        {\, \atop \,}
        Z_{{\vert I_1\vert}}\left( (O_{i_1})_{i_1 \in I_1} \right),
        \cdots,
        Z_{{\vert I_n\vert}}\left( (O_{i_n})_{i_n \in I_n} \right),
        {\, \atop \,}
      \right)
  \\
  & \phantom{=}
    +
    Z_k( O_1,\cdots, O_k )
  \end{aligned}
$$

where $\{T'_k\}_{k \in \mathbb{N}}$ are the [[time-ordered products]] corresponding to $\mathcal{S}'$ (by example \ref{TimeOrderedProductsFromSMatrixScheme}) and $\{T_k\}_{k \in \mathcal{N}}$ those correspondong to $\mathcal{S}$.

Here the sum on the right runs over all ways that in the composite $\mathcal{S} \circ \mathcal{Z}$ a $k$-ary operation arises as the composite of an $n$-ary time-ordered product applied to the ${\vert I_i\vert}$-ary components of $\mathcal{Z}$, for $i$ running from 1 to $n$; except for the case $k = n$, which is displayed separately in the second line

This shows that if $\mathcal{Z}$ exists, then it is unique, because its coefficients $Z_k$ are [[induction|inductively]] in $k$
given by the expressions

$$
  \label{MainTheoremPerturbativeRenormalizationInductionStep}
  \begin{aligned}
    & Z_k( O_1,\cdots, O_k )
    \\
    & =
    T'_k( O_1, \cdots, O_k )
    \;-\;
    \underset{
      (T \circ \mathcal{Z}_{\lt k})_k
    }{
    \underbrace{
    \underset{
      2 \leq n \leq k
    }{\sum}
      \frac{1}{n!}
      (i \hbar)^{k-n}
      \underset{
        { { I_1 \sqcup \cdots \sqcup I_n } \atop { =  \{1, \cdots, k\}, } }
        \atop
        { I_1, \cdots, I_n \neq \emptyset }
      }{\sum}
      T_n
      \left(
        Z_{{\vert I_1\vert}}( (O_{i_1})_{i_1 \in I_1} ),
        \cdots,
        Z_{{\vert I_n\vert}}( (O_{i_n})_{i_n \in I_n} ),
      \right)
    }
    }
  \end{aligned}
$$

(The symbol under the brace is introduced as a convenient shorthand for the term above the brace.)

Hence it remains to see that the $Z_k$ defined this way satisfy the conditions in def. \ref{InteractionVertexRedefinition}.

The condition "perturbation" is immediate from the corresponding condition on $\mathcal{S}$ and $\mathcal{S}'$.

Similarly the condition "field independence" follows immediately from the assumoption that $\mathcal{S}$ and $\mathcal{S}'$ satisfy this condition.

It only remains to see that $Z_k$ indeed takes values in [[local observables]]. Given that the [[time-ordered products]] a priori take values in the larrger space of [[microcausal polynomial observables]] this means to show that the spacetime support of $Z_k$ is on the [[diagonal]].

But observe that, as indicated in the above formula, the term over the brace may be understood as the coefficient at order $k$ of the [[exponential series]]-expansion of the [[composition|composite]] $\mathcal{S} \circ \mathcal{Z}_{\lt k}$, where

$$
  \mathcal{Z}_{\lt k}
  \;\coloneqq\;
  \underset{
    n \in \{1, \cdots, k-1\}
  }{\sum}
  \frac{1}{n!} Z_n
$$

is the truncation of the [[vertex redefinition]] to degree $\lt k$. This truncation is clearly itself still
a vertex redefinition (according to def. \ref{InteractionVertexRedefinition}) so that the composite $\mathcal{S} \circ \mathcal{Z}_{\lt k}$
is still an [[S-matrix]] scheme (by prop. \ref{CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition})
so that the $(T \circ \mathcal{Z}_{\lt k})_k$ are [[time-ordered products]] (by example \ref{TimeOrderedProductsFromSMatrixScheme}).

So as we solve $\mathcal{S}' = \mathcal{S} \circ \mathcal{Z}$ inductively in degree $k$, then for the induction step in degree $k$ the expressions $T'_{\lt k}$ and $(T \circ \mathcal{Z})_{\lt k}$ agree and are both time-ordered products.
By prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal} this implies that  $T'_{k}$ and $(T \circ \mathcal{Z}_{\lt k})_{k}$ agree away from the diagonal. This means that their difference $Z_k$ is supported on the diagonal, and hence is indeed local.

=--

In conclusion this establishes the following pivotal statement of [[perturbative quantum field theory]]:

+-- {: .num_theorem #PerturbativeRenormalizationMainTheorem}
###### Theorem
**([[main theorem of perturbative renormalization]] -- [[Stückelberg-Petermann renormalization group]] of [[vertex redefinitions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] (def. \ref{VacuumFree}).

1. the [[vertex redefinitions]] $\mathcal{Z}$ (def. \ref{InteractionVertexRedefinition}) form a [[group]] under [[composition]];

1. the set of [[S-matrix]] [[renormalization schemes|("re"-)normalization schemes]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}), remark \ref{calSFunctionIsRenormalizationScheme}) satisfying the [[renormalization condition]] "field independence" (prop. \ref{BasicConditionsRenormalization}) is a [[torsor]] over this group,
hence equipped with a [[regular action]] in that

   1. the set of [[S-matrix schemes]] is [[inhabited set|non-empty]];

   1. any two [[S-matrix]] [[renormalization scheme|("re"-)normalization schemes]] $\mathcal{S}$, $\mathcal{S}'$  are related by a _unique_
      [[vertex redefinition]] $\mathcal{Z}$ via [[composition]]:

      $$
        \mathcal{S}' \;=\; \mathcal{S} \circ \mathcal{Z}
        \,.
      $$

This group is called the _[[Stückelberg-Petermann renormalization group]]_.

Typically one imposes a set of [[renormalization conditions]] (def. \ref{RenormalizationConditions})
and considers the corresponding [[subgroup]] of [[vertex redefinitions]] preserving these conditions.

=--

+-- {: .proof}
###### Proof

The [[group]]-[[structure]] and [[regular action]] is given by  prop. \ref{CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition} and prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}.
The existence of S-matrices follows is the statement of [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]]
in theorem \ref{ExistenceRenormalization}.

=--

$\,$


**[[UV-regularization|UV-Regularization]] via [[counterterms]]**
 {#UVRegularizationViaZ}

While [[Epstein-Glaser renormalization]] (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal})
gives a transparent picture on the space of choices in [[renormalization|("re"-)normalization]]
(theorem \ref{ExistenceRenormalization}) the physical nature of the higher interactions that it introduces at
coincident interaction points (via the [[extensions of distributions]] in prop. \ref{SpaceOfPointExtensions}) remains more implicit. But the
[[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}),
which re-expresses the _difference_ between any two such choices as an [[interaction vertex redefinition]],
suggests that already the choice of [[renormalization|("re"-)normalization]] itself should have an incarnation in terms
of [[interaction vertex redefinitions]].

This may be realized via a construction of [[renormalization|("re"-)normalization]] in terms
of _[[UV-regularization]]_ (prop. \ref{UVRegularization} below): For any choice of "[[UV-cutoff]]", given by an
approximation of the [[Feynman propagator]] $\Delta_F$ by [[non-singular distributions]] $\Delta_{F,\Lambda}$
(def. \ref{CutoffsUVForPerturbativeQFT} below) there is a unique "[[effective S-matrix]]" $\mathcal{S}_\Lambda$
induced at each cutoff scale (def. \ref{SMatrixEffective} below). While
the "UV-limit" $\underset{\Lambda \to \infty}{\lim} \mathcal{S}_\Lambda$ does not in general exist,
it may be "regularized" by applying suitable [[interaction vertex redefinitions]] $\mathcal{Z}_\Lambda$;
if the higher-order corrections that these introduce serve to "[[counterterms|counter]]"
(remark \ref{TermCounter} below) the coresponding UV-divergences.

This perspective of [[renormalization|("re"-)normalization via]] via _[[counterterms]]_ is often regarded as
the primary one.
Its elegant proof in prop. \ref{UVRegularization} below, however relies on the [[Epstein-Glaser renormalization]]
via inductive [[extensions of distributions]] and uses the same kind of argument as in the
proof of the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem} via prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}) that establishes the [[Stückelberg-Petermann renormalization group]].


$\,$


+-- {: .num_defn #CutoffsUVForPerturbativeQFT}
###### Definition
**([[UV cutoffs]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] over [[Minkowski spacetime]] $\Sigma$ (according to def. \ref{VacuumFree}), where $\Delta_H = \tfrac{i}{2}(\Delta_+ - \Delta_-) + H$ is the corresponding [[Wightman propagator]] inducing the [[Feynman propagator]]

$$
  \Delta_F \in \Gamma'_{\Sigma \times \Sigma}(E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}})
$$

by $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$.

Then a choice of _[[UV cutoffs]] for [[perturbative QFT]]_ around this vacuum is a
collection of [[non-singular distributions]] $\Delta_{F,\Lambda}$ parameterized by [[positive real numbers]]

$$
  \array{
    (0, \infty)
      &\overset{}{\longrightarrow}&
    \Gamma_{\Sigma \times \Sigma,cp}(E_{\text{BV-BRST}} \boxtimes E_{\text{BV-BRST}})
    \\
    \Lambda &\mapsto& \Delta_{F,\Lambda}
  }
$$

such that:

1. each $\Delta_{F,\Lambda}$ satisfies the following basic properties

   1. (translation invariance)

      $$
        \Delta_{F,\Lambda}(x,y) = \Delta_{F,\Lambda}(x-y)
      $$


   1. (symmetry)

      $$
        \Delta^{b a}_{F,\Lambda}(y, x)
        \;=\;
        \Delta^{a b}_{F,\Lambda}(x, y)
      $$

      i.e.

      $$
        \Delta_{F,\Lambda}^{b a}(-x)
        \;=\;
        \Delta_{F,\Lambda}^{a b}(x)
      $$

1. the $\Delta_{F,\Lambda}$ interpolate between zero and the Feynman propagator, in that, in the [[Hörmander topology]]:

   1. the [[limit of a sequence|limit]] as $\Lambda \to 0$ exists and is zero

      $$
        \underset{\Lambda \to \infty}{\lim} \Delta_{F,\Lambda}
        \;=\;
        0
        \,.
      $$


   1. the [[limit of a sequence|limit]] as $\Lambda \to \infty$ exists and is the [[Feynman propagator]]:

      $$
        \underset{\Lambda \to \infty}{\lim} \Delta_{F,\Lambda}
        \;=\;
        \Delta_F
        \,.
      $$

=--

([Dütsch 10, section 4](renormalization#Duetsch10))


+-- {: .num_example}
###### Example
**(relativistic momentum cutoff)**

Recall from [this prop.](Feynman+propagator#FeynmanPropagatorAsACauchyPrincipalvalue)
that the [[Fourier transform of distributions]] of the [[Feynman propagator]] for the [[real scalar field]] on [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ is, 


$$
  \begin{aligned}
  \widehat{\Delta}_F(k)
  & =  
  \frac{+i}{(2\pi)^{p+1}}
  \frac{
     1
  }{
    - \eta(k,k) - \left( \tfrac{m c}{\hbar} \right)^2 + i 0
  }
  \end{aligned}
$$

To produce a [[UV cutoff]]  in the sense of def. \ref{CutoffsUVForPerturbativeQFT} we would like to set this function to zero for [[wave numbers]] $\vert \vec k\vert$ (hence [[momenta]] $\hbar\vert \vec k\vert$) larger than a given $\Lambda$.

This needs to be done with due care: First, the [[Paley-Wiener-Schwartz theorem]] (prop. \ref{PaleyWienerSchwartzTheorem}) says that  $\Delta_{F,\Lambda}$ to be a test function and hence compactly supported, its [[Fourier transform of distributions|Fourier transform]] $\widehat{\Delta}_{F,\Lambda}$ needs to be smooth and of bounded growth. So instead of multiplying $\widehat{\Delta}_F$ by a [[step function]] in $k$, we may multiply it with an exponential damping.

=--

([Keller-Kopper-Schophaus 97, section 6.1](UV+regularization#KellerKopperSchophaus97), [Dütsch 18, example 3.126](renormalization#Duetsch18))


+-- {: .num_defn #SMatrixEffective}
###### Definition
**([[effective S-matrix scheme]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

We say that the _[[effective S-matrix scheme]]_ $\mathcal{S}_\Lambda$ at cutoff scale $\Lambda \in [0,\infty)$

$$
  \array{
    PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]
     &\overset{\mathcal{S}_{\Lambda}}{\longrightarrow}&
    PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]
    \\
    O &\mapsto& \mathcal{S}_\Lambda(O)
  }
$$

is the [[exponential series]]

$$
  \label{EffectiveSMatrixScheme}
  \begin{aligned}
    \mathcal{S}_\Lambda(O)
    & \coloneqq
    \exp_{F,\Lambda}\left( \frac{1}{i \hbar} O \right)
    \\
    & =
    1
      +
    \frac{1}{i \hbar} O
      +
    \frac{1}{2} \frac{1}{(i \hbar)^2} O \star_{F,\Lambda} O
      +
    \frac{1}{3!} \frac{1}{(i \hbar)^3} O \star_{F,\Lambda} O \star_{F,\Lambda} 0
      +
    \cdots
  \end{aligned}
  \,.
$$

with respect to the [[star product]] $\star_{F,\Lambda}$ induced by the $\Delta_{F,\Lambda}$ (def. \ref{PropagatorStarProduct}).

This is evidently defined on all [[polynomial observables]] as shown, and restricts to an endomorphism on
[[microcausal polynomial observables]] as shown, since the contraction coefficients $\Delta_{F,\Lambda}$ are [[non-singular distributions]],
by definition of [[UV cutoff]].

=--

([Dütsch 10, (4.2)](renormalization#Duetsch10))

+-- {: .num_prop #UVRegularization}
###### Proposition
**([[renormalization|("re"-)normalization]] via [[UV regularization]])**


Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$ a polynomial [[local observable]] as in def. \ref{FormalParameters}, regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Let moreover $\{\Delta_{F,\Lambda}\}_{\Lambda \in [0,\infty)}$ be a [[UV cutoff]] (def. \ref{CutoffsUVForPerturbativeQFT}); with $\mathcal{S}_\Lambda$ the induced [[effective S-matrix schemes]] (eq:EffectiveSMatrixScheme).


Then

1. there exists a $[0,\infty)$-parameterized [[interaction vertex redefinition]] $\{\mathcal{Z}_\Lambda\}_{\Lambda \in \mathbb{R}_{\geq 0}}$ (def. \ref{InteractionVertexRedefinition})
such that the [[limit of a sequence|limit]] of [[effective S-matrix schemes]]  $\mathcal{S}_{\Lambda}$ (eq:EffectiveSMatrixScheme) applied to the $\mathcal{Z}_\Lambda$-[[vertex redefinition|redefined interactions]]

   $$
     \mathcal{S}_\infty
     \;\coloneqq\;
     \underset{\Lambda \to \infty}{\lim}
     \left(
       \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda
     \right)
   $$

   exists and is a genuine [[S-matrix scheme]] around the given vacuum (def. \ref{LagrangianFieldTheoryPerturbativeScattering});

1. every [[S-matrix scheme]] around the given vacuum arises this way.

These $\mathcal{Z}_\Lambda$ are called _[[counterterms]]_ (remark \ref{TermCounter} below) and the composite
$\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$ is called a _[[UV regularization]]_ of the [[effective S-matrices]] $\mathcal{S}_\Lambda$.

Hence [[UV-regularization]] via [[counterterms]] is a method of [[renormalization|("re"-)normalization]] of [[perturbative QFT]] (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}).

=--

This was claimed in ([Brunetti-Dütsch-Fredenhagen 09, (75)](renormalization#BrunettiDuetschFredenhagen09)), a proof was indicated in ([Dütsch-Fredenhagen-Keller-Rejzner 14, theorem A.1](renormalization#DuetschFredenhagenKellerRejzner14)).

+-- {: .proof}
###### Proof

Let $\{p_{\rho_{k}}\}_{k \in \mathbb{N}}$ be a sequence of projection maps as in (eq:ForExtensionOfDistributionsProjectionMaps) defining an [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}) of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ as [[extensions of distributions]] of the $T_k$, regarded as distributions via remark \ref{TimeOrderedProductOfFixedInteraction}, by the choice $q_k^\alpha = 0$ in (eq:ExtensionOfDitstributionsPointFixedAndChoice).

We will construct that $\mathcal{Z}_\Lambda$ in terms of these projections $p_\rho$.

First consider some convenient shorthand:

For $n \in \mathbb{N}$, write $\mathcal{Z}_{\leq n} \coloneqq \underset{1 \in \{1, \cdots, n\}}{\sum} \frac{1}{n!} Z_n$.
Moreover, for $k \in \mathbb{N}$ write $(T_\Lambda \circ \mathcal{Z}_{\leq n})_k$ for the $k$-ary coefficient in the
expansion of the composite $\mathcal{S}_\Lambda \circ \mathcal{Z}_{\leq n}$,
as in equation (eq:MainTheoremPerturbativeRenormalizationInductionStep) in the proof of the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}, via prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}).

In this notation we need to find $\mathcal{Z}_\Lambda$ such that for each $n \in \mathbb{N}$ we have

$$
  \label{CountertermsInductionAssumption}
  \underset{\Lambda \to \infty}{\lim}
  \left(
    T_\Lambda \circ \mathcal{Z}_{\leq n, \Lambda}
  \right)_n
  \;=\;
  T_n
  \,.
$$

We proceed by [[induction]] over $n \in \mathbb{N}$.

Since by definition $T_0 = const_1$, $T_1 = id$ and  $Z_0 = const_0$, $Z_1 = id$ the statement is trivially true for
$n = 0$ and $n = 1$.

So assume now $n \in \mathbb{N}$ and $\{Z_{k}\}_{k \leq n}$ has
been found such that (eq:CountertermsInductionAssumption) holds.

Observe that with the chosen renormalizing projection $p_{\rho_{n+1}}$ the time-ordered product $T_{n+1}$ may be expressed as follows:

$$
  \label{RenormalizedSMatrixAsLimitOfEffectiveSMatricesEvaluatedOnProjection}
  \begin{aligned}
  T_{n+1}(O, \cdots, O)
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_k}(O \otimes \cdots \otimes O)
  \right\rangle
  \\
  & =
  \left\langle
  \underset{\Lambda \to \infty}{\lim}
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_k}(O \otimes \cdots \otimes O)
  \right\rangle
  \end{aligned}
  \,.
$$

Here in the first step we inserted the causal decomposition (eq:TimeOrderedProductsAwayFromDiagonalByInduction)
of $T_{n+1}$ in terms of the $\{T_k\}_{k \leq n}$
away from the diagonal, as in the proof of prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal},
which is admissible because the image of $p_{\rho_{n+1}}$ vanishes on the diagonal. In the second step
we replaced the star-product of the Feynman propagator $\Delta_F$ with the limit over the star-products
of the regularized propagators $\Delta_{F,\Lambda}$, which converges by the nature of the [[Hörmander topology]]
(which is assumed by def. \ref{CutoffsUVForPerturbativeQFT}).

Hence it is sufficient to find $Z_{n+1,\Lambda}$ and $K_{n+1,\Lambda}$ such that

$$
  \label{CountertermsAndCorrectionTerm}
  \begin{aligned}
  \left\langle
    \left(
      T_{\Lambda} \circ \mathcal{Z}_{\Lambda}
    \right)_{n+1}
    \,,\,
    (-, \cdots, -)
  \right\rangle
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{k}}\left( -, \cdots, - \right)
  \right\rangle
  \\
  & \phantom{=}
  +
  K_{n+1,\Lambda}(-, \cdots, -)
  \end{aligned}
$$

subject to these two conditions:

1. $\mathcal{Z}_{n+1,\Lambda}$ is local;

1. $\underset{\Lambda \to \infty}{\lim} K_{n+1,\Lambda} = 0$.


Now by expanding out the left hand side of (eq:CountertermsAndCorrectionTerm) as

$$
  (T_\Lambda \circ \mathcal{Z}_\Lambda)_{n+1}
  \;=\;
  Z_{n+1,\Lambda}
    \;+\;
  (T_\Lambda \circ Z_{\leq n, \Lambda})_{n+1}
$$

(which uses the condition $T_1 = id$) we find the unique solution of (eq:CountertermsAndCorrectionTerm) for $Z_{n+1,\Lambda}$, in terms of the $\{Z_{\leq n,\Lambda}\}$
and $K_{n+1,\Lambda}$ (the latter still to be chosen) to be:

$$
  \label{CountertermOrderByOrderInTermsOfCorrectionTerm}
  \begin{aligned}
  \left\langle
    Z_{n+1,\Lambda}
    ,
    (-,\cdots, -)
  \right\rangle
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-, \cdots, -)
  \right\rangle
  \\
  & \phantom{=}
  -
  \left\langle
    \left(
      T_{\Lambda} \circ \mathcal{Z}_{\leq n,\Lambda}
    \right)_{n+1}
    \,,\,
    (-, \cdots, -)
  \right\rangle
  \\
  & \phantom{=}
  +
  \left\langle
    K_{n+1, \Lambda},
    (-, \cdots, -)
  \right\rangle
  \end{aligned}
  \,.
$$

We claim that the following choice works:

$$
  \label{LocalityCorrection}
  \begin{aligned}
  K_{n+1, \Lambda}(-, \cdots, -)
  & \coloneqq
  \left\langle
    \left(
      T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda}
    \right)_{n+1}
    \,,\,
    p_{\rho_{n+1}}(-, \cdots, -)
  \right\rangle
  \\
  & \phantom{=}
  -
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-, \cdots, -)
  \right\rangle
  \end{aligned}
  \,.
$$

To prove this, we need to show that 1) the resulting $Z_{n+1,\Lambda}$ is local and 2) the limit of $K_{n+1,\Lambda}$ vanishes as $\Lambda \to \infty$.

First regarding the locality of $Z_{n+1,\Lambda}$: By inserting (eq:LocalityCorrection) into (eq:CountertermOrderByOrderInTermsOfCorrectionTerm)
we obtain

$$
  \begin{aligned}
    \left\langle
      Z_{n+1,\Lambda}
      \,,\,
      (-,\cdots,-)
    \right\rangle
    & =
    \left\langle
      \left(
        T_{\Lambda} \circ \mathcal{Z}_{\leq n}
      \right)_{n+1}
      \,,\,
      p(-, \cdots, -)
    \right\rangle
    -
    \left\langle
      \left(
        T_{\Lambda} \circ \mathcal{Z}_{\leq n}
      \right)_{n+1}
      \,,\,
      (-, \cdots, -)
    \right\rangle
    \\
    & =
    \left\langle
      \left(
        T_{\Lambda} \circ \mathcal{Z}_{\leq n}
      \right)_{n+1}
      \,,\,
      ( p_{\rho_{n+1}} - id)(-, \cdots, -)
    \right\rangle
  \end{aligned}
$$

By definition $p_{\rho_{n+1}} - id$ is the identity on test functions (adiabatic switchings) that vanish at the diagonal. This means that $Z_{n+1,\Lambda}$ is [[support of a distribution|supported]] on the diagonal, and is hence local.

Second we need to show that $\underset{\Lambda \to \infty}{\lim} K_{n+1,\Lambda} = 0$:

By applying the analogous causal decomposition (eq:TimeOrderedProductsAwayFromDiagonalByInduction)
to the regularized products, we find

$$
  \label{InductionStepForCounterterms}
  \begin{aligned}
  &
  \left\langle
    (T_\Lambda \circ \mathcal{Z}_{\leq n, \Lambda})_{n+1}
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \,.
  \end{aligned}
$$

Using this we compute as follows:

$$
  \label{CorrectionTermForCountertermsVanishesAsCutoffIsRemoved}
  \begin{aligned}
  &
  \left\langle
    \underset{\Lambda \to \infty}{\lim}
    (T_\Lambda \circ \mathcal{Z}_{\leq n, \Lambda})_{n+1}
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{\Lambda \to \infty}{\lim}
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { I, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \chi_i(\mathbf{X})\,
    \underset{
      T_{{\vert \mathbf{I}\vert}}(\mathbf{I})
    }{
    \underbrace{
    \left(
      \underset{\Lambda \to \infty}{\lim}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{{\vert \mathbf{I}\vert}} (\mathbf{I})
    \right)
    }}
    \left(
      \underset{\Lambda \to \infty}{\lim}
      \star_{F,\Lambda}
    \right)
    \underset{
      T_{{\vert \overline{\mathbf{I}}\vert}}(\overline{\mathbf{I}})
    }{
    \underbrace{
    \left(
      \underset{\Lambda \to \infty}{\lim}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
    \right)
    }}
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{\Lambda \to \infty}{\lim}
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { I, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \chi_i(\mathbf{X})\,
    T_{ { \vert \mathbf{I} \vert } }( \mathbf{I} )
      \star_{F,\Lambda}
    T_{ {\vert  \overline{\mathbf{I}} \vert} }( \overline{\mathbf{I}} )
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \end{aligned}
  \,.
$$

Here in the first step we inserted (eq:InductionStepForCounterterms); in the second step we used that in the [[Hörmander topology]] the [[product of distributions]] preserves limits in each variable and in the third step we used the induction assumption (eq:CountertermsInductionAssumption)
and the definition of [[UV cutoff]] (def. \ref{CutoffsUVForPerturbativeQFT}).

Inserting this for the first summand in (eq:LocalityCorrection) shows that $\underset{\Lambda \to \infty}{\lim} K_{n+1, \Lambda} = 0$.

In conclusion this shows that a consistent choice of [[counterterms]] $\mathcal{Z}_\Lambda$ exists to produce
_some_ S-matrix $\mathcal{S} = \underset{\Lambda \to \infty }{\lim} (\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda)$.
It just remains to see that for _every_ other S-matrix $\widetilde{\mathcal{S}}$ there exist counterterms
$\widetilde{\mathcal{Z}}_\lambda$ such
that $\widetilde{\mathcal{S}} = \underset{\Lambda \to \infty }{\lim} (\mathcal{S}_\Lambda \circ \widetilde{\mathcal{Z}}_\Lambda)$.

But by the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem})
we know that there exists a [[vertex redefinition]] $\mathcal{Z}$ such that

$$
  \begin{aligned}
    \widetilde{\mathcal{S}}
    & = \mathcal{S} \circ \mathcal{Z}
    \\
    & =
    \underset{\Lambda \to \infty}{\lim}
    \left(
      \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda
    \right)
    \circ
    \mathcal{Z}
    \\
    & =
    \underset{\Lambda \to \infty}{\lim}
    (
      \mathcal{S}_\Lambda
        \circ
      (
        \underset{
          \widetilde{\mathcal{Z}}_\Lambda
        }{
        \underbrace{
        \mathcal{Z}_\Lambda
          \circ
        \mathcal{Z}
        }
        }
      )
    )
  \end{aligned}
$$

and hence with counterterms $\mathcal{Z}_\Lambda$ for $\mathcal{S}$ given, then counterterms for any $\widetilde{\mathcal{S}}$ are given by the composite $\widetilde{\mathcal{Z}}_\Lambda \coloneqq \mathcal{Z}_\Lambda \circ \mathcal{Z}$.


=--


+-- {: .num_remark #TermCounter}
###### Remark
**([[counterterms]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

Consider

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle
$$

a [[local observable]], regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Then prop. \ref{UVRegularization} says that there exist [[vertex redefinitions]] of this [[interaction]]

$$
  \mathcal{Z}_\Lambda(g S_{int} + j A)
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle
$$

parameterized by $\Lambda \in [0,\infty)$, such that the [[limit of a sequence|limit]]

$$
  \mathcal{S}_\infty(g S_{int} + j A)
  \;\coloneqq\;
  \underset{\Lambda \to \infty}{\lim}
  \mathcal{S}_\Lambda\left( \mathcal{Z}_\Lambda( g S_{int} + j A )\right)
$$

exists and is an [[S-matrix]] for [[perturbative QFT]] with the given [[interaction]] $g S_{int} + j A$.

In this case the difference

$$
  \begin{aligned}
    S_{counter, \Lambda}
    & \coloneqq
    \left(
      g S_{int} + j A
    \right)
    \;-\;
    \mathcal{Z}_{\Lambda}(g S_{int} + j A)
    \;\;\;\;\;\in\;
    Loc(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g^2, j^2, g j\rangle
  \end{aligned}
$$

(which by the axiom "perturbation" in def. \ref{InteractionVertexRedefinition} is at least of second order in the [[coupling constant]]/[[source field]], as shown)
is called a choice of _[[counterterms]]_ at cutoff scale $\Lambda$. These are new interactions which are added to the given interaction at cutoff scale $\Lambda$

$$
  \mathcal{Z}_{\Lambda}(g S_{int} + j A)
  \;=\;
  g S_{int} + j A
  \;+\;
  S_{counter,\Lambda}
  \,.
$$


In this language prop. \ref{UVRegularization} says that for every free field vacuum and every choice of local interaction, there is a choice of counterterms to the interaction that defines a corresponding [[renormalization|("re"-)normalized]] [[perturbative QFT]], and every [[renormalization|(re"-)normalized]] [[perturbative QFT]] arises from some choice of counterterms.

=--


$\,$


**[[effective quantum field theory|Wilson-Polchinski effective QFT flow]]**
 {#EffectiveQFTFlowWislonian}

We have seen [above](#UVRegularizationViaZ) that a choice of [[UV cutoff]] induces [[effective S-matrix schemes]] $\mathcal{S}_\Lambda$
at cutoff scale $\Lambda$ (def. \ref{SMatrixEffective}). To these one may associated non-local [[relative effective actions]]
$S_{eff,\Lambda}$ (def. \ref{EffectiveActionRelative} below) which are such that their effective [[scattering amplitudes]]
at scale $\Lambda$ coincide with the true scattering amplitudes of a genuine [[local observable|local]] interaction
as the cutoff is removed. This is the Wilsonian picture of _[[effective quantum field theory]]_ at a given cutoff scale (remark \ref{pQFTEffective} below). Crucially the "flow" of the [[relative effective actions]] with the cutoff scale satisfies
a [[differential equation]] that in itself is independent of the full UV-theory; this is
_[[Polchinski's flow equation]]_ (prop. \ref{FlowEquationPolchinski} below). Solving this equation for given choice
of initial value data is hence another way of choosing [[renormalization|("re"-)normalization]] constants.

$\,$


+-- {: .num_prop #EffectiveSmatrixSchemeInvertible}
###### Proposition
**([[effective S-matrix schemes]] are [[inverse|invertible functions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

Write

$$
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]
$$

for  the subspace of the space of [[formal power series]] in $\hbar, g, j$ with [[coefficients]] [[polynomial observables]]
on those which are at least of first order in $g,j$, i.e. those that vanish for $g, j = 0$ (as in def. \ref{FormalParameters}).

Write moreover

$$
  1 + PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]
$$

for the subspace of polynomial observables which are the sum of 1 (the multiplicative unit) with an
observable at least linear n $g,j$.

Then the [[effective S-matrix schemes]] $\mathcal{S}_\Lambda$ (def. \ref{SMatrixEffective}) [[restriction|restrict]] to
[[linear isomorphisms]] of the form

$$
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle
   \underoverset{\simeq}{\phantom{AA}\mathcal{S}_\Lambda \phantom{AA} }{\longrightarrow}
  1
    +
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle
  \,.
$$

=--

([Dütsch 10, (4.7)](renormalization#Duetsch10))

+-- {: .proof}
###### Proof

Since each $\Delta_{F,\Lambda}$ is symmetric (def. \ref{CutoffsUVForPerturbativeQFT})
if follows by general properties of [[star products]] (prop. \ref{SymmetricContribution})
just as for the genuine [[time-ordered product]] on [[regular polynomial observables]] (prop. \ref{IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise}) that
eeach the "effective time-ordered product" $\star_{F,\Lambda}$ is [[isomorphism|isomorphic]]
to the pointwise product $(-)\cdot (-)$ (def. \ref{Observable})

$$
  A_1 \star_{F,\Lambda} A_2
  \;=\;
  \mathcal{T}_\Lambda
  \left(
    \mathcal{T}_\Lambda^{-1}(A_1)
    \cdot
    \mathcal{T}_\Lambda^{-1}(A_2)
  \right)
$$

for

$$
  \mathcal{T}_\Lambda
  \;\coloneqq\;
  \exp
  \left(
    \tfrac{1}{2}\hbar
    \underset{\Sigma}{\int}
    \Delta_{F,\Lambda}^{a b}(x,y)
    \frac{\delta^2}{\delta \mathbf{\Phi}^a(x) \delta \mathbf{\Phi}^b(y)}
  \right)
$$

as in (eq:OnRegularPolynomialObservablesPointwiseTimeOrderedIsomorphism).

In particular this means that the [[effective S-matrix]] $\mathcal{S}_\Lambda$ arises from the [[exponential series]] for the pointwise product by [[conjugation]] with $\mathcal{T}_\Lambda$:

$$
  \mathcal{S}_\Lambda
  \;=\;
  \mathcal{T}_\Lambda \circ \exp_\cdot\left( \frac{1}{i \hbar}(-) \right) \circ \mathcal{T}_\Lambda^{-1}
$$

(just as for the genuine S-matrix on [[regular polynomial observables]] in def. \ref{OnRegularObservablesPerturbativeSMatrix}).

Now the exponential of the pointwise product on
$1 + PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$
has as [[inverse function]] the [[natural logarithm]] [[power series]], and
since $\mathcal{T}$ evidently preserves powers of $g,j$ this [[conjugation|conjugates]]
to an inverse at each UV cutoff scale $\Lambda$:

$$
  \label{InverseOfEffectiveSMatrixByLogarithm}
  \mathcal{S}_\Lambda^{-1}
  \;=\;
  \mathcal{T}_\Lambda
    \circ
  \ln\left( i \hbar (-) \right)
    \circ
  \mathcal{T}_\Lambda^{-1}
  \,.
$$

=--


+-- {: .num_defn #EffectiveActionRelative}
###### Definition
**([[relative effective action]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

Consider

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BrST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Then for

$$
  \Lambda,\, \Lambda_{vac} \;\in\; (0, \infty)
$$

two [[UV cutoff]]-scale parameters, we say the _[[relative effective action]]_ $S_{eff, \Lambda, \Lambda_0}$ is the image of this interaction under the [[composition|composite]]
of the [[effective S-matrix scheme]] $\mathcal{S}_{\Lambda_0}$ at scale $\Lambda_0$ (eq:EffectiveSMatrixScheme) and the [[inverse function]] $\mathcal{S}_\Lambda^{-1}$ of the [[effective S-matrix scheme]] at scale $\Lambda$ (via prop. \ref{EffectiveSmatrixSchemeInvertible}):

$$
  \label{RelativeEffectiveActionComposite}
  S_{eff,\Lambda, \Lambda_0}
  \;\coloneqq\;
  \mathcal{S}_{\Lambda}^{-1} \circ \mathcal{S}_{\Lambda_0}(g S_{int} + j A)
  \phantom{AAA}
  \Lambda, \Lambda_0 \in [0,\infty)
  \,.
$$

For chosen  [[counterterms]] (remark \ref{TermCounter}) hence for chosen [[UV regularization]] $\mathcal{S}_\infty$ (prop. \ref{UVRegularization}) this makes sense also for $\Lambda_0 = \infty$ and we write:

$$
  \label{RelativeEffectiveActionRelativeToInfinity}
  S_{eff,\Lambda}
  \;\coloneqq\;
  S_{eff,\Lambda, \infty}
  \;\coloneqq\;
  \mathcal{S}_{\Lambda}^{-1} \circ \mathcal{S}_{\infty}(g S_{int} + j A)
  \phantom{AAA}
  \Lambda  \in [0,\infty)
$$

=--

([Dütsch 10, (5.4)](renormalization#Duetsch10))

+-- {: .num_remark #pQFTEffective}
###### Remark
**([[effective quantum field theory]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}), let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum  (def. \ref{CutoffsUVForPerturbativeQFT}), and let $\mathcal{S}_\infty = \underset{\Lambda \to \infty}{\lim} \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$ be a corresponding [[UV regularization]] (prop. \ref{UVRegularization}).

Consider a [[local observable]]

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BrST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Then def. \ref{CutoffsUVForPerturbativeQFT} and def. \ref{EffectiveActionRelative} say that
for any $\Lambda \in (0,\infty)$ the [[effective S-matrix]] (eq:EffectiveSMatrixScheme) of the
[[relative effective action]] (eq:RelativeEffectiveActionComposite) equals the genuine [[S-matrix]] $\mathcal{S}_\infty$
of the genuine [[interaction]] $g S_{int} + j A$:

$$
  \mathcal{S}_\Lambda( S_{eff,\Lambda} )
  \;=\;
  \mathcal{S}_\infty\left( g S_{int} + j A  \right)
  \,.
$$

In other words the [[relative effective action]] $S_{eff,\Lambda}$
encodes what the actual [[perturbative QFT]] defined by $\mathcal{S}_\infty\left( g S_{int} + j A  \right)$
_effectively_ looks like at [[UV cutoff]] $\Lambda$.

Therefore one says that $S_{eff,\Lambda}$ defines _[[effective quantum field theory]]_ at [[UV cutoff]] $\Lambda$.

Notice that in general $S_{eff,\Lambda}$ is _not a [[local observable|local]] [[interaction]]_ anymore:
By prop. \ref{EffectiveSmatrixSchemeInvertible} the [[image]] of the [[inverse]] $\mathcal{S}^{-1}_\Lambda$ of the [[effective S-matrix]]
is [[microcausal polynomial observables]] in $1 + PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle$
and there is no guarantee that this lands in the subspace of [[local observables]].

Therefore [[effective quantum field theories]] at finite [[UV cutoff]]-scale $\Lambda \in [0,\infty)$ are in general
_not_ [[local field theories]], even if their [[limit of a sequence|limit]] as $\Lambda \to \infty$ is, via prop. \ref{UVRegularization}.


=--



+-- {: .num_prop #EffectiveActionAsRelativeEffectiveAction}
###### Proposition
**([[effective action]] is [[relative effective action]] at $\Lambda = 0$)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).


Then the [[relative effective action]] (def. \ref{EffectiveActionRelative}) at $\Lambda = 0$ is the actual [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}) in the sense of the the [[Feynman perturbation series]] of
[[Feynman amplitudes]] $\Gamma(g S_{int} + j A)$ (def. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) for [[connected graph|connected]] [[Feynman diagrams]] $\Gamma$:

$$
  \begin{aligned}
    S_{eff,0}
    & \coloneqq\;
    S_{eff,0,\infty}
    \\
    & = S_{eff} \;\coloneqq\;
    \underset{\Gamma \in \Gamma_{conn}}{\sum}
    \Gamma(g S_{int} + j A)
    \,.
  \end{aligned}
$$

More generally this holds true for any $\Lambda \in [0, \infty) \sqcup \{\infty\}$

$$
  \begin{aligned}
    S_{eff,0,\Lambda}
    & =
    \underset{\Gamma \in \Gamma_{conn}}{\sum}
    \Gamma_\Lambda(g S_{int} + j A)
    \,,
  \end{aligned}
$$

where $\Gamma_\Lambda( g S_{int} + j A)$ denotes the evident version of the [[Feynman amplitude]] (def. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) with [[time-ordered products]] replaced by
effective time ordered product at scale $\Lambda$ as in (def. \ref{SMatrixEffective}).

=--

([Dütsch 18, (3.473)](renormalization#Duetsch18))

+-- {: .proof}
###### Proof

Observe that the [[effective S-matrix scheme]] at scale $\Lambda = 0$ (eq:EffectiveSMatrixScheme)
is the [[exponential series]] with respect to the pointwise product (def. \ref{Observable})

$$
  \mathcal{S}_0(O) = \exp_\cdot( O )
  \,.
$$

Therefore the statement to be proven says equivalently that the [[exponential series]]
of the [[effective action]] with respect to the pointwise product is the [[S-matrix]]:

$$
  \exp_\cdot\left( \frac{1}{i \hbar} S_{eff} \right)
  \;=\;
  \mathcal{S}_\infty\left( g S_{int} + j A \right)
  \,.
$$

That this is the case is the statement of prop. \ref{LogarithmEffectiveAction}.

=--



The definition of the [[relative effective action]] $\mathcal{S}_{eff,\Lambda} \coloneqq \mathcal{S}_{eff,\Lambda, \infty}$ in def. \ref{EffectiveActionRelative}
invokes a choice of [[UV regularization]] $\mathcal{S}_\infty$ (prop. \ref{UVRegularization}).
While (by that proposition and the [[main theorem of perturbative renormalization]], theorem \ref{PerturbativeRenormalizationMainTheorem} )this is guaranteed to exist,
in practice one is after methods for constructing this without specifying it a priori.

But the collection [[relative effective actions]] $\mathcal{S}_{eff,\Lambda, \Lambda_0}$ for $\Lambda_0 \lt \infty$
"flows" with the cutoff-parameters $\Lambda$ and in particular also with $\Lambda_0$ (remark \ref{GroupoidOfEFTs} below)
which suggests that examination of this flow yields information about full theory at $\mathcal{S}_\infty$.


This is made precise by _[[Polchinski's flow equation]]_ (prop. \ref{FlowEquationPolchinski} below),
which is the [[infinitesimal]] version of the "Wilsonian RG flow" (remark \ref{GroupoidOfEFTs}).
As a [[differential equation]] it is _independent_ of the choice of $\mathcal{S}_{\infty}$ and hence may
be used to solve for the Wilsonian RG flow without knowing $\mathcal{S}_\infty$ in advance.

The freedom in choosing the initial values of this differential equation corresponds to
the [[renormalization|("re"-)normalization freedom]] in choosing the [[UV regularization]] $\mathcal{S}_\infty$.
In this sense "Wilsonian RG flow" is a method of [[renormalization|("re"-)normalization]] of [[perturbative QFT]]
(def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}).


+-- {: .num_remark #GroupoidOfEFTs}
###### Remark
**(Wilsonian [[groupoid]] of [[effective quantum field theories]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

Then the [[relative effective actions]] $\mathcal{S}_{eff,\Lambda, \Lambda_0}$ (def. \ref{EffectiveActionRelative}) satisfy

$$
  S_{eff, \Lambda', \Lambda_0}
  \;=\;
  \left(
    \mathcal{S}_{\Lambda'}^{-1}
    \circ
    \mathcal{S}_\Lambda
  \right)
  \left(
    S_{eff, \Lambda, \Lambda_0}
  \right)
  \phantom{AAA}
  \text{for}
  \,
  \Lambda,\Lambda' \in [0,\infty)
  \,,\,
  \Lambda_0 \in [0,\infty) \sqcup \{\infty\}
  \,.
$$


This is similar to a [[group]] of UV-cutoff scale-transformations. But since the [[composition]] operations are only sensible when the UV-cutoff labels match, as shown, it is really a [[groupoid]] [[groupoid action|action]].

This is often called the _Wilsonian RG_.

=--

We now consider the [[infinitesimal]] version of this "flow":

+-- {: .num_prop #FlowEquationPolchinski}
###### Proposition
**([[Polchinski's flow equation]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}), let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum  (def. \ref{CutoffsUVForPerturbativeQFT}), such that $\Lambda \mapsto \Delta_{F,\Lambda}$ is [[differentiable function|differentiable]].

Then for _every_ choice of [[UV regularization]] $\mathcal{S}_\infty$ (prop. \ref{UVRegularization}) the
corresponding [[relative effective actions]] $S_{eff,\Lambda}$ (def. \ref{EffectiveActionRelative}) satisfy the following [[differential equation]]:

$$
  \frac{d}{d \Lambda}
  S_{eff,\Lambda}
  \;=\;
  -
  \frac{1}{2} \frac{1}{i \hbar}
  \frac{d}{d \Lambda'}
  \left(
    S_{eff,\Lambda}
      \star_{F,\Lambda'}
    S_{eff,\Lambda}
  \right)\vert_{\Lambda' = \Lambda}
  \,,
$$

where on the right we have the [[star product]] induced by $\Delta_{F,\Lambda'}$ (def. \ref{PropagatorStarProduct}).

=--

This goes back to ([Polchinski 84, (27)](#Polchinski84)). The rigorous formulation and proof is due to ([Brunetti-Dütsch-Fredenhagen 09, prop. 5.2](renormalization#BrunettiDuetschFredenhagen09), [Dütsch 10, theorem 2](renormalization#Duetsch10)).

+-- {: .proof}
###### Proof

First observe that for any [[polynomial observable]] $O \in PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]$ we have

$$
  \begin{aligned}
  &
  \frac{1}{(k+2)!}
  \frac{d}{d \Lambda}
  (
    \underset{
      k+2 \, \text{factors}
    }{
    \underbrace{
      O
        \star_{F,\Lambda}
        \cdots
        \star_{F,\Lambda}
      O
    }
    }
  )
  \\
  & =
  \frac{1}{(k+2)!}
  \frac{d}{d \Lambda}
  \left(
    prod
    \circ
    \exp\left(
      \hbar
      \underset{1 \leq i \lt j \leq k}{\sum}
      \left\langle
         \Delta_{F,\Lambda}
         ,
         \frac{\delta}{\delta \mathbf{\Phi}_i}
         \frac{\delta}{\delta \mathbf{\Phi}_j}
      \right\rangle
    \right)
    (
      \underset{
        k + 2 \, \text{factors}
      }{
      \underbrace{
        O \otimes \cdots \otimes O
      }
      }
    )
  \right)
  \\
  & =
  \underset{
    = \frac{1}{2} \frac{1}{k!}
  }{
  \underbrace{
    \frac{1}{(k+2)!}
    \left(
      k + 2
      \atop
      2
    \right)
  }}
  \left(
    \frac{d}{d \Lambda}
    O
     \star_{F,\Lambda}
    O
  \right)
    \star_{F,\Lambda}
  \underset{
    k \, \text{factors}
  }{
  \underbrace{
  O
    \star_{F,\Lambda}
    \cdots
    \star_{F,\Lambda}
  O
  }
  }
  \end{aligned}
$$

Here $\frac{\delta}{\delta \mathbf{\Phi}_i}$ denotes the functional derivative of the $i$th tensor factor of $O$, and the binomial coefficient counts the number of ways that an unordered pair of distinct labels of tensor factors may be chosen from a total of $k+2$ tensor factors, where we use that the [[star product]] $\star_{F,\Lambda}$ is commutative (by symmetry of $\Delta_{F,\Lambda}$) and associative (by prop. \ref{AssociativeAndUnitalStarProduct}).

With this and the defining equality $\mathcal{S}_\Lambda(S_{eff,\Lambda}) =  \mathcal{S}(g S_{int} + j A)$ (eq:RelativeEffectiveActionRelativeToInfinity) we compute as follows:

$$
  \begin{aligned}
    0
    & =
    \frac{d}{d \Lambda} \mathcal{S}(g S_{int} + j A)
    \\
    & =
    \frac{d}{d \Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    \\
    & =
    \left(
      \frac{1}{i \hbar}
      \frac{d}{d \Lambda} S_{eff,\Lambda}
    \right)
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    +
    \left(
      \frac{d}{d \Lambda}
      \mathcal{S}_{\Lambda}
   \right)
   \left( S_{eff, \Lambda} \right)
    \\
    & =
    \left(
      \frac{1}{i \hbar}
      \frac{d}{d \Lambda} S_{eff,\Lambda}
    \right)
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    \;+\;
    \frac{1}{2}
    \frac{d}{d \Lambda'}
    \left(
      \frac{1}{i \hbar} S_{eff,\Lambda}
        \star_{F,\Lambda'}
      \frac{1}{i \hbar} S_{eff, \Lambda}
    \right)
    \vert_{\Lambda' = \Lambda}
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda
    \left(
      S_{eff, \Lambda}
    \right)
  \end{aligned}
$$

Acting on this equation with the multiplicative inverse $(-) \star_{F,\Lambda} \mathcal{S}_\Lambda( - S_{eff,\Lambda} )$ (using that $\star_{F,\Lambda}$ is a commutative product, so that exponentials behave as usual) this yields the claimed equation.

=--

$\,$


**[[renormalization group flow]]**
 {#RGFlowGeneral}


In [[perturbative quantum field theory]] the construction of the [[scattering matrix]] $\mathcal{S}$, hence of the [[interacting field algebra of observables]] for a given [[interaction]] $g S_{int}$ [[perturbation theory|perturbing]] around a given [[free field theory|free field]] [[vacuum]], involves choices of _normalization_ of [[time-ordered products]]/[[Feynman diagrams]] (traditionally called _[[renormalization|"re"-normalizations]]_) encoding new [[interactions]] that appear where several of the original interaction vertices defined by $g S_{int}$ coincide.

Whenever a [[group]] $RG$ [[action|acts]] on the space of [[observables]] of the theory such that [[conjugation]] by this action takes [[renormalization scheme|("re"-)normalization schemes]] into each other, then these  choices of [[renormalization|("re"-)normalization]]  are parameterized by -- or "flow with" -- the elements of $RG$.  This is called _renormalization group flow_  (prop.
\ref{FlowRenormalizationGroup} below); often called _RG flow_, for short.

The archetypical example here is the [[group]] $RG$ of [[scaling transformations]] on [[Minkowski spacetime]] (def. \ref{ScalingTransformations} below), which induces a [[renormalization group flow]] (prop. \ref{RGFlowScalingTransformations} below) due to the particular nature of the [[Wightman propagator]] resp. [[Feynman propagator]] on [[Minkowski spacetime]] (example \ref{ScalarFieldMassDimensionOnMinkowskiSpacetime} below). In this case the choice of [[renormalization|("re"-)normalization]] hence "flows with scale".

Now the _[[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}) states that (if only the basic [[renormalization condition]] called "field independence" is satisfied) any two choices of [[renormalization scheme|("re"-)normalization schemes]] $\mathcal{S}$ and $\mathcal{S}'$ are related by a unique [[interaction vertex redefinition]] $\mathcal{Z}$, as

$$
  \mathcal{S}' = \mathcal{S} \circ \mathcal{Z}
  \,.
$$

Applied to a parameterization/flow of renormalization choices by a group $RG$ this hence induces an [[interaction vertex redefinition]] as a function of $RG$. One may think of the shape of the interaction vertices as fixed and only their ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] as changing under such an [[interaction vertex redefinition]], and hence then one has [[coupling constants]] $g_j$ that are parameterized by elements $\rho$ of $RG$:

$$
  \mathcal{Z}_{\rho_{vac}}^\rho
  \;\colon\;
  \{g_j\}
    \mapsto
  \{g_j(\rho)\}
$$

This dependendence is called _running of the coupling constants_ under the renormalization group flow (def. \ref{CouplingRunning} below).

One example of [[renormalization group flow]] is that induced by [[scaling transformations]] (prop. \ref{RGFlowScalingTransformations} below). This is the original and main example of the concept ([Gell-Mann & Low 54](#GellMannLow54))

In this case the [[running of the coupling constants]] may be understood as expressing how "more" [[interactions]] (at higher energy/shorter [[wavelength]]) become visible (say to [[experiment]]) as the scale resolution is increased. In this case the dependence of the coupling $g_j(\rho)$ on the parameter $\rho$ happens to be [[differentiable function|differentiable]]; its [[logarithm|logarithmic]] [[derivative]] (denoted "$\psi$" in [Gell-Mann & Low 54](#GellMannLow54)) is known as the _[[beta function]]_ ([Callan 70](#Callan70), [Symanzik 70](#Symanzik70)):

$$
  \beta(g) \coloneqq \rho \frac{\partial g_j}{\partial \rho}
  \,.
$$

The [[running of the coupling constants]] is not quite a [[representation]] of the [[renormalization group flow]],
but it is a "twisted" representation, namely a [[group cocycle|group 1-cocycle]] (prop. \ref{CocycleRunningCoupling} below). For the case of [[scaling transformations]] this may be called the _[[Gell-Mann-Low renormalization cocycle]]_ ([Brunetti-Dütsch-Fredenhagen 09](renormalization#BrunettiDuetschFredenhagen09)).

$\,$


+-- {: .num_prop #FlowRenormalizationGroup}
###### Proposition
**([[renormalization group flow]])**

Let

$$
  vac
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]].

Consider a [[group]] $RG$ equipped with an [[action]] on the [[Wick algebra]] of [[off-shell]] [[microcausal polynomial observables]] with formal parameters adjoined (as in def. \ref{FormalParameters})

$$
  rg_{(-)}
  \;\colon\;
  RG \times PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ]
  \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ \hbar, g, j ] ]
  \,,
$$

hence for each $\rho \in RG$ a [[continuous linear map]] $rg_\rho$ which has an [[inverse]] $rg_\rho^{-1} \in RG$ and is a [[homomorphism]] of the [[Wick algebra]]-product (the [[star product]] $\star_H$ induced by the [[Wightman propagator]] of the given vauum $vac$)

$$
  rg_\rho( A_1 \star_H A_2 )
  \;=\;
  rg_\rho(A_1) \star_H rg_\rho(A_2)
$$

such that the following conditions hold:

1. the action preserves the subspace of [[off-shell]] polynomial [[local observables]], hence it [[restriction|restricts]] as

   $$
     rg_{(-)}
     \;\colon\;
     RG \times LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g,j\rangle
     \longrightarrow
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g,j\rangle
   $$

1. the action respects the [[causal order]] of the spacetime support (def. \ref{SpacetimeSupport}) of local observables, in that for $O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]$ we have

   $$
     \left(
       supp(O_1)
       \,{\vee\!\!\!\wedge}\,
       supp(O_2)
     \right)
     \phantom{A}
       \Rightarrow
     \phantom{A}
     \left(
       supp(rg_\rho(O_1))
       \,{\vee\!\!\!\wedge}\,
       supp(rg_\rho(O_2))
     \right)
   $$

   for all $\rho \in RG$.

Then:

The operation of [[conjugation]] by this action on [[observables]] induces an [[action]] on the [[set]] of [[S-matrix]] [[renormalization schemes]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}, remark \ref{calSFunctionIsRenormalizationScheme}),
in that for

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})( (\hbar) )[ [ g, j] ]
$$

a perturbative [[S-matrix scheme]] around the given [[free field theory|free field]] [[vacuum]] $vac$, also the [[composition|composite]]

$$
  \mathcal{S}^\rho
  \;\coloneqq\;
  rg_\rho \circ \mathcal{S} \circ rg_{\rho}^{-1}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})( (\hbar) )[ [ g, j] ]
$$

is an [[S-matrix]] scheme, for all $\rho \in RG$.

More generally, let

$$
  vac_\rho
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}'_\rho, \Delta_{H,\rho} )
$$

be a collection of [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]] parameterized by elements $\rho \in RG$,
all with the same underlying [[field bundle]]; and
consider $rg_\rho$ as above, except that it is not an [[automorphism]] of any [[Wick algebra]],
but an [[isomorphism]] between the [[Wick algebra]]-structures on various vacua, in that

$$
  \label{IntertwiningWickProductsActionRG}
  rg_{\rho}( A_1 \star_{H, \rho^{-1} \rho_{vac}} A_2 )
  \;=\;
  rg_{\rho}(A_1) \star_{H, \rho_{vac}} rg_{\rho}(A_2)
$$

for all $\rho, \rho_{vac} \in RG$

Then if

$$
  \{ \mathcal{S}_{\rho} \}_{\rho \in RG}
$$

is a collection of [[S-matrix schemes]], one around each of the [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]]
$vac_\rho$, it follows that for all pairs of group elements $\rho_{vac}, \rho \in RG$ the [[composition|composite]]

$$
  \label{RGConjugateSmatrix}
  \mathcal{S}_{\rho_{vac}}^\rho
  \;\coloneqq\;
  rg_\rho \circ \mathcal{S}_{\rho^{-1}\rho_{vac}} \circ rg_\rho^{-1}
$$

is an [[S-matrix scheme]] around the vacuum labeled by $\rho_{vac}$.


Since therefore each element $\rho \in RG$ in the [[group]] $RG$ picks a different choice of [[renormalization|normalization]]
of the [[S-matrix]] scheme around a given vacuum at $\rho_{vac}$, we call the assignment $\rho \mapsto \mathcal{S}_{\rho_{vac}}^{\rho}$
a _[[renormalization group flow|re-normalization group flow]]_.



=--

([Brunetti-Dütsch-Fredenhagen 09, sections 4.2, 5.1](renormalization#BrunettiDuetschFredenhagen09), [Dütsch 18, section 3.5.3](renormalization#Duetsch18))

+-- {: .proof}
###### Proof

It is clear from the definition that each $\mathcal{S}^{\rho}_{\rho_{vac}}$ satisfies the axiom "perturbation" (in def. \ref{LagrangianFieldTheoryPerturbativeScattering}).

In order to verify the axiom "[[causal additivity]]",
observe, for convenience, that by prop. \ref{CausalFactorizationAlreadyImpliesSMatrix} it is sufficient to check [[causal factorization]].

So consider $O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$
two local observables whose spacetime support is in [[causal order]].

$$
  supp(O_1)
  \;{\vee\!\!\!\wedge}\;
  supp(O_2)
  \,.
$$

We need to show that the

$$
  \mathcal{S}_{\rho_{vac}}^{\rho}(O_1 + O_2)
  =
  \mathcal{S}_{\rho_{vac}}^\rho(O_1)
    \star_{H,\rho_{vac}}
  \mathcal{S}_{vac_e}^\rho(O_2)
$$

for all $\rho, \rho_{vac} \in RG$.

Using the defining properties of $rg_{(-)}$ and the [[causal factorization]] of $\mathcal{S}_{\rho^{-1}\rho_{vac}}$ we directly compute as follows:


$$
  \begin{aligned}
    \mathcal{S}_{\rho_{vac}}^\rho(O_1 + O_2)
    & =
    rg_\rho
      \circ
    \mathcal{S}_{\rho^{-1} \rho_{vac}}
      \circ
    rg_\rho^{-1}( O_1 + O_2 )
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1}\rho_{vac}}
      \left(
        rg_\rho^{-1}(O_1) + rg_\rho^{-1}(O_2)
      \right)
      {\, \atop \,}
    \right)
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \left(
        \mathcal{S}_{\rho^{-1}\rho_{vac}}\left(rg_\rho^{-1}(O_1)\right)
      \right)
        \star_{H, \rho^{-1} \rho_{vac}}
      \left(
        \mathcal{S}_{ \rho^{-1} \rho_{vac} }\left(rg_\rho^{-1}(O_2)\right)
      \right)
      {\, \atop \,}
    \right)
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1} \rho_{vac}}\left(rg_{\rho^{-1}}(O_1)\right)
      {\, \atop \,}
    \right)
    \star_{H, \rho_{vac}}
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1} \rho_{vac}}\left( rg_\rho^{-1}(O_2)\right)
      {\, \atop \,}
    \right)
    \\
    & =
    \mathcal{S}^\rho_{\rho_{vac}}( O_1 )
      \,
      \star_{H, \rho_{vac}}
      \,
     \mathcal{S}_{\rho_{vac}}^\rho(O_2)
    \,.
  \end{aligned}
$$

=--

+-- {: .num_defn #CouplingRunning}
###### Definition
**([[running coupling constants]])**

Let

$$
  vac
  \coloneqq
  vac_e
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to def. \ref{VacuumFree}) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]], let $\mathcal{S}$ be an [[S-matrix]] scheme
around this vacuum and let $rg_{(-)}$ be a [[renormalization group flow]] according to prop. \ref{FlowRenormalizationGroup}, such that each re-normalized [[S-matrix scheme]] $\mathcal{S}_{vac}^\rho$ satisfies the [[renormalization condition]] "field independence".

Then by the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}, via prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}) there is for every [[pair]] $\rho_1, \rho_2 \in RG$ a unique [[interaction vertex redefinition]]

$$
  \mathcal{Z}_{\rho_{vac}}^{\rho}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
    \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]
$$

which relates the corresponding two [[S-matrix]] schemes via

$$
  \label{SMatrixScemesRelatedByRunningFunction}
  \mathcal{S}_{\rho_{vac}}^{\rho}
  \;=\;
  \mathcal{S}_{\rho_{vac}}
    \circ
  \mathcal{Z}_{\rho_{vac}}^\rho
  \,.
$$

If one thinks of an [[interaction]] vertex, hence a [[local observable]] $g S_{int}+ j A$, as specified by the ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] $g_j \in C^\infty_{cp}(\Sigma)\langle g \rangle$ multiplying the corresponding [[interaction]] [[Lagrangian densities]] $\mathbf{L}_{int,j} \in \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})$ as

$$
  g S_{int}
  \;=\;
  \underset{j}{\sum} \tau_\Sigma \left( g_j \mathbf{L}_{int,j} \right)
$$

(where $\tau_\Sigma$ denotes [[transgression of variational differential forms]]) then $\mathcal{Z}_{\rho_1}^{\rho_2}$ exhibits a dependency of the ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] $g_j$ of the [[renormalization group flow]] parameterized by $\rho$. The corresponding functions

$$
  \mathcal{Z}_{\rho_{vac}}^{\rho}(g S_{int})
    \;\colon\;
   (g_j)
     \mapsto
   (g_j(\rho))
$$

are then called _[[running coupling constants]]_.

=--

([Brunetti-Dütsch-Fredenhagen 09, sections 4.2, 5.1](renormalization#BrunettiDuetschFredenhagen09), [Dütsch 18, section 3.5.3](renormalization#Duetsch18))


+-- {: .num_prop #CocycleRunningCoupling}
###### Proposition
**([[running coupling constants]] are  [[group cocycle]] over [[renormalization group flow]])**

Consider [[running coupling constants]]

$$
   \mathcal{Z}_{\rho_{vac}}^{\rho}
   \;\colon\;
   (g_j)
     \mapsto
   (g_j(\rho))
$$

as in def. \ref{CouplingRunning}. Then for all $\rho_{vac}, \rho_1, \rho_2 \in RG$ the following equality is satisfied
by the "running functions" (eq:SMatrixScemesRelatedByRunningFunction):

$$
  \mathcal{Z}_{\rho_{vac}}^{\rho_1 \rho_2}
  \;=\;
  \mathcal{Z}_{\rho_{vac}}^{\rho_1}
    \circ
  \left(
    \sigma_{\rho_1}
      \circ
    \mathcal{Z}_{\rho^{-1} \rho_{vac}}^{\rho_2}
      \circ
    \sigma_{\rho_1}^{-1}
  \right)
  \,.
$$

=--

([Brunetti-Dütsch-Fredenhagen 09 (69)](renormalization#BrunettiDuetschFredenhagen09), [Dütsch 18, (3.325)](renormalization#Duetsch18))

+-- {: .proof}
###### Proof

Directly using the definitions, we compute as follows:

$$
  \begin{aligned}
    \mathcal{S}_{\rho_{vac}}
      \circ
    \mathcal{Z}_{\rho_{vac}}^{\rho_1 \rho_2}
    & =
    \mathcal{S}_{\rho_{vac}}^{\rho_1 \rho_2 }
    \\
    & =
    \sigma_{\rho_1}
      \circ
    \underset{
      =
      \mathcal{S}_{\rho_1^{-1} \rho_{vac}}^{\rho_2}
        =
      \mathcal{S}_{\rho_1^{-1} \rho_{vac}}
        \circ
      \mathcal{Z}_{\rho_1^{-1} \rho_vac}^{\rho_2}
    }{
    \underbrace{
      \sigma_{\rho_2}
        \circ
      \mathcal{S}_{\rho_2^{-1}\rho_1^{-1}\rho_{vac}}
        \circ
      \sigma_{\rho_2}^{-1}
    }}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & =
    \underset{
      =
      \mathcal{S}_{\rho_{vac}}
        \circ
      \mathcal{Z}_{\rho_{vac}}^{\rho_1}
        \circ
      \sigma_{\rho_1}
    }{
    \underbrace{
      \sigma_{\rho_1}
        \circ
      \mathcal{S}_{\rho_1^{-1} \rho_{vac}}
        \circ
      \overset{ = id }{
        \overbrace{
          \sigma_{\rho_1}^{-1}
            \circ
          \sigma_{\rho_1}
        }
    }
    }}
      \circ
      \mathcal{Z}_{\rho_1^{-1} \rho_{vac}}^{\rho_2}
      \circ
      \sigma_{\rho_1}^{-1}
    \\
    & =
    \mathcal{S}_{\rho_{vac}}
      \circ
    \mathcal{Z}_{\rho_{vac}}^{\rho_1}
      \circ
    \underbrace{
      \sigma_{\rho_1}
        \circ
      \mathcal{Z}_{\rho_1^{-1} \rho_{vac}}^{\rho_2}
        \circ
      \sigma_{\rho_1}^{-1}
    }
  \end{aligned}
$$

This demonstrates the equation between vertex redefinitions to be shown after [[composition]] with an S-matrix scheme. But by the uniqueness-clause in the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}) the composition operation $\mathcal{S}_{\rho_{vac}} \circ (-)$ as a function from [[vertex redefinitions]] to S-matrix schemes is [[injective function|injective]]. This implies the equation itself.

=--

$\,$


**[[Gell-Mann-Low renormalization cocycles|Gell-Mann & Low RG flow]]**
 {#ScalingTransformatinRGFlow}


We discuss (prop. \ref{RGFlowScalingTransformations} below) that, if the field species involved have well-defined [[mass dimension]] (example \ref{ScalarFieldMassDimensionOnMinkowskiSpacetime} below) then [[scaling transformations]] on [[Minkowski spacetime]] (example \ref{ScalingTransformations} below) induce a [[renormalization group flow]] (def. \ref{FlowRenormalizationGroup}). This is the original and main example of [[renormalization group flows]] ([Gell-Mann& Low 54](#GellMannLow54)).



+-- {: .num_example #ScalingTransformations}
###### Example
**([[scaling transformations]] and [[mass dimension]])**

Let

$$
  E \overset{fb}{\longrightarrow} \Sigma
$$

be a [[field bundle]] which is a [[trivial vector bundle]] over [[Minkowski spacetime]] $\Sigma = \mathbb{R}^{p,1} \simeq_{\mathbb{R}} \mathbb{R}^{p+1}$.

For $\rho \in (0,\infty) \subset \mathbb{R}$ a [[positive real number]],
write

$$
  \array{
    \Sigma
      &\overset{\rho}{\longrightarrow}&
    \Sigma
    \\
    x &\mapsto& \rho x
  }
$$

for the operation of multiplication by $\rho$ using the [[real vector space]]-[[structure]] of the [[Cartesian space]] $\mathbb{R}^{p+1}$ underlying [[Minkowski spacetime]].

By [[pullback of differential forms|pullback]] this acts on [[field histories]] ([[sections]] of the [[field bundle]]) via

$$
  \array{
    \Gamma_\Sigma(E)
      &\overset{\rho^\ast}{\longrightarrow}&
    \Gamma_\Sigma(E)
    \\
    \Phi &\mapsto& \Phi(\rho(-))
  }
  \,.
$$

Let then

$$
  \rho
    \mapsto
  vac_\rho
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}'_{\rho}, \Delta_{H,\rho} )
$$

be a 1-parameter collection of [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacua]] on that field bundle, according to def. \ref{VacuumFree}, and consider a decomposition into a set $Spec$ of field species (def. \ref{VerticesAndFieldSpecies}) such that for each $sp \in Spec$ the collection of [[Feynman propagators]] $\Delta_{F,\rho,sp}$ for that species _scales homogeneously_ in that there exists

$$
  dim(sp) \in \mathbb{R}
$$

such that for all $\rho$ we have (using [[generalized functions]]-notation)

$$
  \label{FeynmanPropagatorScalingBehaviour}
  \rho^{ 2 dim(sp) }  \Delta_{F, 1/\rho, sp}( \rho x )
  \;=\;
  \Delta_{F,sp, \rho = 1}(x)
  \,.
$$

Typically $\rho$ rescales a [[mass]] parameter, in which case $dim(sp)$ is also called the _[[mass dimension]]_ of the field species $sp$.

Let finally

$$
  \array{
    PolyObs(E)
    &
      \overset{
        \sigma_\rho
      }{\longrightarrow}
    &
    PolyObs(E)
    \\
    \mathbf{\Phi}_{sp}^a(x)
      &\mapsto&
    \rho^{- dim(sp)} \mathbf{\Phi}^a( \rho^{-1} x )
  }
$$

be the [[function]] on [[off-shell]] [[polynomial observables]] given on [[field observables]] $\mathbf{Phi}^a(x)$ by [[pullback of differential forms|pullback]] along $\rho^{-1}$ followed by multiplication by $\rho$ taken to the negative power of the [[mass dimension]], and extended from there to all [[polynomial observables]] as an [[associative algebra|algebra]] [[homomorphism]].

This constitutes an [[action]] of the [[group]]

$$
  RG
    \coloneqq
  \left(
    \mathbb{R}_+, \cdot
  \right)
$$

of [[positive real numbers]] (under [[multiplication]]) on [[polynomial observables]], called the group of _[[scaling transformations]]_ for the given choice of field species and [[mass]] parameters.

=--

([Dütsch 18, def. 3.19](renormalization#Duetsch18))


+-- {: .num_example #ScalarFieldMassDimensionOnMinkowskiSpacetime}
###### Example
**([[mass dimension]] of [[scalar field]])**

Consider the [[Feynman propagator]] $\Delta_{F,m}$ of the [[free field theory|free]] [[real scalar field]] on [[Minkowski spacetime]] $\Sigma = \mathbb{R}^{p,1}$  for [[mass]] parameter $m \in (0,\infty)$; a [[Green function]] for the [[Klein-Gordon equation]].

Let the group $RG \coloneqq (\mathbb{R}_+, \cdots)$ of [[scaling transformations]] $\rho \in \mathbb{R}_+$ on [[Minkowski spacetime]] (def. \ref{ScalingTransformations}) act on the mass parameter by inverse multiplication

$$
  (\rho , \Delta_{F,m})
    \mapsto
  \Delta_{F,\rho^{-1}m}(\rho (-))
  \,.
$$

Then we have

$$
  \Delta_{F,\rho^{-1}m}(\rho (-))
  \;=\;
  \rho^{-(p+1) + 2}
  \Delta_{F,1}(x)
$$

and hence the corresponding [[mass dimension]] (def. \ref{ScalingTransformations}) of the [[real scalar field]] on $\mathbb{R}^{p,1}$ is

$$
  dim(\text{scalar field})
  =
  (p+1)/2 - 1
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{FeynmanPropagatorAsACauchyPrincipalvalue} the [[Feynman propagator]] in question is given by the [[Cauchy principal value]]-formula (in [[generalized function]]-notation)

$$
  \begin{aligned}
  \Delta_{F,m}(x)
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \,.
  \end{aligned}
$$

By applying [[change of integration variables]] $k \mapsto \rho^{-1} k$ in the [[Fourier transform of distributions|Fourier transform]] this becomes

$$
  \begin{aligned}
  \Delta_{F,\rho^{-1}m}(\rho x)
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu \rho x^\mu}
  }{
    - k_\mu k^\mu - \left( \rho^{-1} \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \rho^{-(p+1)}
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - \rho^{-2} k_\mu k^\mu - \rho^{-2} \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \rho^{-(p+1)+2}
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu -  \left( \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \\
  & =
  \rho^{-(p+1) + 2}
  \Delta_{F,m}(x)
  \end{aligned}
$$

=--

+-- {: .num_prop #RGFlowScalingTransformations}
###### Proposition
**([[scaling transformations]] are [[renormalization group flow]])**

Let

$$
  vac \coloneqq vac_m
  \coloneqq (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_{H,m})
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacua]] on that field bundle, according to def. \ref{VacuumFree} equipped with a decomposition into a set $Spec$ of field species (def. \ref{VerticesAndFieldSpecies}) such that for each $sp \in Spec$ the collection of [[Feynman propagators]] the corresponding field species has a well-defined [[mass dimension]] $dim(sp)$ (def. \ref{ScalingTransformations})

Then the [[action]] of the [[group]] $RG \coloneqq (\mathbb{R}_+, \cdot)$ of [[scaling transformations]] (def. \ref{ScalingTransformations}) is a [[renormalization group flow]] in the sense of prop. \ref{FlowRenormalizationGroup}.

=--

([Dütsch 18, exercise 3.20](renormalization#Duetsch18))


+-- {: .proof}
###### Proof

It is clear that rescaling preserves [[causal order]] and the [[renormalization condition]] of "field indepencen".

The condition we need to check is that for $A_1, A_2 \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]$ two [[microcausal polynomial observables]]  we have for any $\rho, \rho_{vac} \in \mathbb{R}_+$ that

$$
  \sigma_\rho
  \left(
    A_1 \star_{H, \rho^{-1} \rho_{vac} c} A_2
  \right)
  \;=\;
  \sigma_\rho(A_1)
    \star_{H,\rho_{vac}}
  \sigma_\rho(A_2)
  \,.
$$

By the assumption of decomposition into free field species $sp \in Spec$, it is sufficient to check this for each species $\Delta_{H,sp}$.
Moreover, by the nature of the [[star product]] on [[polynomial observables]], which is given by iterated contractions with the [[Wightman propagator]], it is sufficient to check this for one such contraction.

Observe that the scaling behaviour of the [[Wightman propagator]] $\Delta_{H,m}$ is the same as the behaviour (eq:FeynmanPropagatorScalingBehaviour) of the correspponding [[Feynman propagator]]. With this we directly compute as follows:

$$
  \begin{aligned}
    \sigma_\rho (\mathbf{\Phi}(x))
     \star_{F, \rho_{vac} m}
    \sigma_\rho (\mathbf{\Phi}(y)
    & =
    \rho^{-2 dim }
    \mathbf{\Phi}(\rho^{-1} x)
      \star_{F, \rho_{vac} m}
    \mathbf{\Phi}(\rho^{-1} y)
    \\
    & =
    \rho^{-2 dim }
    \Delta_{F, \rho_{vac} m}(\rho^{-1}(x-y))
    \\
    & =
    \Delta_{F, \rho^{-1}\rho_{vac}m }(x,y) \mathbf{1}
    \\
    & =
    rg_{\rho}\left(
     \Delta_{F, \rho^{-1}\rho_{vac}m }(x,y) \mathbf{1}
    \right)
    \\
    & =
    rg_{\rho}
    \left(
      \mathbf{\Phi}(x)
        \star_{F, \rho^{-1} \rho_{vac} m}
      \mathbf{\Phi}(y)
    \right)
  \end{aligned}
  \,.
$$

=--

$\,$


This concludes our discussion of [[renormalization]].



