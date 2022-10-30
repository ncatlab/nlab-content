## ScatteringfCollin

In the [previous chapter](#FreeQuantumFields) we have found the [[quantization]] of _[[free field theories|free]]_ [[Lagrangian field theories]] by first choosing a [[gauge fixing|gage fixed]] [[BV-BRST complex|BV-BRST]]-[[homological resolution|resolution]] of the [[algebra of observables|algebra of]] [[gauge invariance|gauge invariant]] [[on-shell]] observabes, then applying [[algebraic deformation quantization]] induced by the resulting [[Peierls-Poisson bracket]] on the graded [[covariant phase space]] to pass to a [[non-commutative algebra]] of quantum observables, such that the [[BV-BRST differential]] is respected.

Of course most [[quantum field theories]] of interest are non-[[free field theories|free]]; they are _[[interacting field theories]]_ whose [[equations of motion]] is a _non-linear_ differential equation. The archetypical example is the coupling of the [[Dirac field]] to the [[electromagnetic field]] via the [[electron-photon interaction]], to the [[interacting field theory]] called _[[quantum electrodynamics]]_ (discussed [below](#QuantumElectrodynamics)).

In principle the [[perturbative quantum field theory|perturbative]] [[quantization]] of such non-[[free field theory]] [[interacting field theories]] proceeds the same way: One picks a [[BV-BRST complex|BV-BRST]]-[[gauge fixing]], computes the [[Peierls-Poisson bracket]] on the resulting [[covariant phase space]] ([Khavkine 14](Peierls+bracket#Khavkine14)) and then finds a [[formal deformation quantization]] of this [[Poisson structure]] to obtain the quantized [[non-commutative algebra]] of [[quantum observables]], as [[formal power series]] in [[Planck's constant]] $\hbar$.

It turns out ([Collini 16](perturbative+algebraic+quantum+field+theory#Collini16), [Hawkins-Rejzner 16](perturbative+algebraic+quantum+field+theory#HawkinsRejzner16)) that the resulting [[interacting field theory|interacting]] [[formal deformation quantization]] may equivalently be expressed in terms of _[[scattering amplitudes]]_: These are the [[probability amplitudes]] for [[plane waves]] of [[free fields]] to in from the far [[past]], then [[interaction|interact]] in a compact region of [[spacetime]] via the given [[interaction]] ([[adiabatic switching|adiabatically switched-off]] outside that region) and emerge again as [[free fields]] into the far [[future]]. 

The collection of all these [[scattering amplitudes]], as the [[types]] and  [[wave vectors]] of the incoming and outgoing [[free fields]] varies, is called the _[[perturbative S-matrix|perturbative scattering matrix]]_ of the [[interacting field theory]], or just _[[S-matrix]]_ for short. It may equivalently be expressed as the [[exponential]] of [[time-ordered products]] of the [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]] with itself. The [[combinatorics]] of the terms in this exponential is captured by _[[Feynman diagrams]]_, which with some care, may be thought of as [[graphs]] whose [[edges]] are [[worldlines]] of [[virtual particles]] and whose [[vertices]] are the [[interactions]] that these particles undergo. This we discuss below in the chapter _[Feynman diagram](#FeynmanDiagram)_.  

The [[axiom|axiomatic]] definition of [[S-matrices]] for [[relativistic field theory|relativistic]] [[Lagrangian field theories]] and their rigorous construction via [[renormalization]] of [[time-ordered products]] is called _[[causal perturbation theory]]_, due to ([Epstein-Glaser 73](causal+perturbation+theory#EpsteinGlaser73)). This makes precise and well-defined the would-be [[path integral quantization]] of [[interacting field theories]] and removes the puzzlements (expressed in [Feynman 85](Schwinger-Tomonaga-Feynman-Dyson#Feynman85SuchABunchOfWords)) that plagued the original informal conception of [[perturbative quantum field theory]] due to [[Schwinger-Tomonaga-Feynman-Dyson]]. 

The equivalent re-formulation of the [[formal deformation quantization]] of [[interacting field theories]] in terms of [[scattering amplitudes]] of [[free fields]] scattering according to an [[adiabatic switching|adiabatically switched]] [[interaction]] ([Collini 16](perturbative+algebraic+quantum+field+theory#Collini16), [Hawkins-Rejzner 16](perturbative+algebraic+quantum+field+theory#HawkinsRejzner16)) has the advantage that it gives a direct handle on those [[observables]] that are measured in [[scattering]] [[experiments]], such as the [[LHC]]-experiment. The bulk of mankinds knowledge about realistic [[perturbative quantum field theory]] -- such as notably the [[standard model of particle physics]] -- is reflected in sch [[scattering amplitudes]] given via their [[Feynman perturbation series]] in [[formal power series|formal powers]] of [[Planck's constant]] and the [[coupling constant]].

Moreover, the mathematical passage from [[scattering amplitudes]] to the actual [[interacting field algebra]] [[algebra of quantum observables|of quantum observables]] corresponding to the [[formal deformation quantization]] is well understood, given via "[[Bogoliubov's formula]]" by the _[[quantum Møller operators]]_. This we discuss in the [next chapter](#QuantumObservables). Here we focus on the [[scattering theory]] itself.



We consider now the [[axioms]] for a perturbative S-matrix of a [[Lagrangian field theory]]
as used in  [[causal perturbation theory]] (def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} below).
Since, by definition, the S-matrix is a formal sum of multi-[[linear continuous functionals]],
it is convenient to impose axioms on these directly: this is the axiomatics for _[[time-ordered products]]_
in def. \ref{TimeOrderedProduct} below. That these latter axioms already imply the former
is the statement of prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below. Its proof
requires a close look at the "reverse-time ordered products" for the inverse S-matrix (def. \ref{ReverseTimeOrderedProduct} below)
and their induced reverse-causal factorization (prop. \ref{ReverseCausalFactorizationOfReverseTimeOrderedProducts} below).

The axioms we consider here are just the bare minimum of [[causal perturbation theory]], sufficient to
imply that the induced perturbative [[quantum observables]]
organize into a [[causally local net of quantum observables]] (discussed [below](#QuantumObservables)).

In applications one considers further axioms, in particular compatibility of the S-matrix with
[[spacetime]] [[symmetry]]. This is needed for the proof of the [[main theorem of perturbative renormalization]]
(see [below](#Renormalization)).


+-- {: .num_defn #PerturbativeSMatrixOnMinkowskiSpacetime}
###### Definition
**([[perturbative S-matrix]])**

Let $\mathcal{W}$ be a [[Wick algebra]]
encoding the quantization of [[free fields]] in $E$, with

$$
  \mathcal{F}_{loc} \overset{:(-):}{\longrightarrow} \mathcal{W}
$$

the quantization map (def. \ref{CompactlySupportedPolynomialLocalDensities}).

Then a _Lagrangian S-matrix for fields of type $E$ perturbing the free fields encoded by $\mathcal{W}$_, is a [[functional]]

$$
  S
    \;\colon\;
  \mathcal{F}_{loc}\otimes ( \langle g,j\rangle  ) \longrightarrow \mathcal{W}[ [ g/\hbar, j/\hbar ] ]
$$

(on [[local observables]] (def. \ref{CompactlySupportedPolynomialLocalDensities})
times the coupling constant $g$ or source strength $j$
with values in the algebra of [[formal power series]] in the formal variables $g/\hbar$
and $j/\hbar$  in the given [[Wick algebra]])
such that the following conditions hold for fixed $L_{int}, \{ J_n\}_{n = 1}^N$:

1. (perturbation)

   There exist [[distributions]] ([[multilinear map|multi-]] [[linear continuous functionals]]) of the form

   $$
     T \;\colon\; (\mathcal{F}_{loc} \otimes ( \langle g,j \rangle ) )^{\otimes^k} \longrightarrow \mathcal{W}[ [ g/\hbar, j/\hbar ] ]
   $$

   for all $k \in \mathbb{N}$, such that:

   1. The unary operation is the quantization map

      $$
        T(L + A) = :L: + :A:
      $$

   1. The S-matrix is the [[exponential]] of "time-ordered products" in that  for $L, A  \in \mathcal{F}_{loc}$

      $$
        \begin{aligned}
          S( g L + j A )
          & =
          T\left( \exp_{\otimes}\left( \tfrac{1}{i \hbar} \left( g L + j A\right) \right) \right)
          \\
          & \coloneqq
          \underoverset{k = 0}{\infty}{\sum} \tfrac{1}{k!}
          \frac{1}{(i \hbar)^k}
          T(\underset{k\, \text{arguments}}{\underbrace{ (g L + j A) \cdots (g L + j A) }})
        \end{aligned}
      $$

1. (normalization)

   $$
     S(0) = 1
   $$

1. ([[causal additivity]])

  For all $J_1, J_2, L \in \mathcal{F}_{loc}$ we have

   $$
     \left( supp(J_1) \geq supp(J_2) \right)
     \;\; \Rightarrow \;\;
     \left(
       \underset{L \in \mathcal{F}_{loc}}{\forall}
       \left(
         S(L + J_1 + J_2)
         =
         S(L + J_1) S(L)^{-1} S(L + J_2)
       \right)
     \right)
     \,.
   $$

Given such perturbative $S$-matrix, then we say that the _[[generating function]]_
(for [[quantum observables]], see def. \ref{GeneratingFunctionsForCorrelationFunctions} below) that it induces is the functional

$$
  \label{GeneratingFunctionInducedFromSMatrix}
  Z
    \;\colon\;
  \mathcal{F}_{loc} \langle g \rangle
    \times
  \mathcal{F}_{loc} \langle j \rangle
    \longrightarrow
  \mathcal{W}[ [ g/\hbar] ][ [ j/\hbar ] ]
$$

given by

$$
  Z_{g_{sw}L_{int}}(j_{sw}A)
  \;\coloneqq\;
  S(g_{sw}L_{int})^{-1} S( g_{sw}L_{int} + j_{sw}A )
  \,.
$$


=--

Def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} is due to ([Epstein-Glaser 73 (1)](causal+perturbation+theory#EpsteinGlaser73))
(in view of prop. \ref{CausalLocalityOfThePerturbativeSMatrix} below), except that these authors
remain a little vague on the nature of the domain.
The domain $\mathcal{F}_{loc}$ is made explicit (in terms of axioms
for the [[time-ordered products]], see def. \ref{TimeOrderedProduct} below),
in ([Brunetti-Fredenhagen 99, section 3](S-matrix#BrunettiFredenhagen99), [D&#252;tschFredenhagen 04, appendix E](S-matrix#DuetschFredenhagen04),
[Hollands-Wald 04,  around (20)](S-matrix#HollandsWald04)); for review see ([Rejzner 16, around def. 6.7](perturbative+algebraic+quantum+field+theory#Rejzner16)).

+-- {: .num_remark}
###### Remark
**(further axioms)**

The list of axioms in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime},
similarly those for the [[time-ordered products]] below in def. \ref{TimeOrderedProduct}, is just the bare
minimum which implies that the corresponding [[quantum observables]]
organize into a [[causally local net]] (discussed [below](#CausalLocality)).
In applications such as in discussion of [[renormalization]] ([below](#Renormalization))
one considers further axioms, such a unitarity and compatibility with spacetime symmetry.

=--


+-- {: .num_remark #PerturbativeSMatrixInverse}
###### Remark
**(invertibility of the [[perturbative S-matrix]])**

The mutliplicative inverse $S(-)^{-1}$ of the perturbative S-matrix in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}
always exists: By the axioms "perturbation" and "normalization" this follows with the usual formula
for the multiplicative inverse of [[formal power series]] that are non-vanishing in degree 0:

If we write

$$
  S(g L +  j A) \coloneqq 1 + D(g L + j A)
$$

then

$$
  \label{InfverseOfPerturbativeSMatrix}
  \begin{aligned}
    S(g L + j A)^{-1} &= (1 + D(j L + j A))^{-1}
    \\
    & =
    \underoverset{r = 0}{\infty}{\sum} (-D(g L + j A))^r
    \\
    & =
    \underoverset{r = 0}{\infty}{\sum} (1 - S(g L + j A))^r
    \,,
  \end{aligned}
$$

where the last sum does exist in $\mathcal{W}[ [ g/\hbar, j/\hbar] ]$ because by
the axiom "normalization"
$D(L)$ has vanishing coefficient in zeroth order, so that
only a finite sub-sum of the formal infinite sum contributes in each order.

=--


+-- {: .num_remark #InterpretationOfPerturbativeSMatrix}
###### Remark
**(intuitive interpretation of the [[perturbative S-matrix]] as a "[[path integral  ]]")**

In traditional informal discussion of [[perturbative quantum field theory]],
the [[S-matrix]] from def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} is thought of as a "[[path integral]]",
written

$$
  S\left(
    \tfrac{g}{\hbar} L_{int} + j
  \right)
  \;\overset{\text{not really!}}{=}\;
  \underset{\Phi \in \Gamma_\Sigma(E)_{asmpt}}{\int}
  \exp\left(
    \int_X
    \left(
      \tfrac{g}{i \hbar} L_{int}(\Phi) + j A(\Phi)
    \right)
  \right)  e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]
  \,,
$$

where the integration is thought to be over the [[space of field histories]] $\Gamma_\Sigma(E)_{asmpt}$
("field paths", example \ref{DiffeologicalSpaceOfFieldHistories})
which satisfy given asymptotic conditions at $x^0 \to \pm \infty$; and as these boundary conditions
vary the above is regarded as an integral kernel that defines the required operator in $\mathcal{W}$
(e.g. [Weinberg 95, around (9.3.10) and (9.4.1)](S-matrix#Weinberg95)).

Here the local density $g_{sw}L_{int}$ has the interpretation of an
[[interaction]] [[Lagrangian density]] $L_{int}$ [[adiabatic switching|adiabatically switched]] by a
spacetime-dependent [[coupling constant|coupling]] "constant",  and $j_{sw}$ has the interpretation of a [[source field]]  strength.

On the other hand, the [[kinetic action|kinetic]] or [[free field]] Lagrangian $L_{free}$, which in the
axiomatic description of def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} is implicit in the [[Wick algebra]]
$\mathcal{W}$ is interpreted as determining the would-be [[Gaussian integral|Gaussian measure]]
"$e^{\tfrac{1}{i \hbar}\int_X L_{free}(\Phi) }D[\Phi]$" for the [[path integral]].

Since this [[measure]] does not actually exist, in general (or is not known to exist),
we may instead think of the axioms for the [[S-matrix]] in def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime} as rigorously _defining_
the [[path integral]], not as an actual [[integration]], but "[[synthetic mathematics|synthetically]]"
by characterizing the behaviour of the _result_ of the would-be integration.

See also remark \ref{InterpretationOfBogoliubovFormulaAsPathIntegral} below.

=--

Definition \ref{PerturbativeSMatrixOnMinkowskiSpacetime} suggests to focus on the
multilinear operations $T(...)$ which define the perturbative S-matix order-by-order:


+-- {: .num_defn #TimeOrderedProduct}
###### Definition
**([[time-ordered product]])**

Let $\mathcal{W}$ be a [[Wick algebra]]
encoding the quantization of [[free fields]] in $E$ (def. \ref{CompactlySupportedPolynomialLocalDensities}).

A _[[time-ordered product]]_ is a sequence of [[distributions]] ([[multilinear map|multi-]] [[linear continuous functionals]]) of the form

$$
  T_k \;\colon\; \mathcal{F}_{loc}^{\otimes^k} \longrightarrow \mathcal{W}[ [ g/\hbar ] ]
$$

for all $k \in \mathbb{N}$, such that:

1. (perturbation) $T_1(g L + j A) =  :g L: +  :j A:$

1. (normalization) $T_0 = 1$

1. (symmetry) each $T_k$ is symmetric in its arguments

1. ([[causal factorization]]) If $supp(L_1) \cup \cdots \cup supp(L_r) \;\geq\; supp(L_{r+1}) \cup \cdots \cup supp(L_k)$ then

   $$
     T((g L_1 + j A_1)  \cdots (g L_k + j A_k) )
       =
     T( (g L_1 + j A_1)  \cdots (g L_r + j A_r) )
     T( (g L_{r+1} + j A_{r+1})  \cdots ( g L_k + j A_{k} ) )
     \,.
   $$

=--

+-- {: .num_defn #NotationForTimeOrderedProductsAsGeneralizedFunctions}
###### Definition
**(notation for time-ordered products as [[generalized functions]])**

It will be convenient (as in [Epstein-Glaser 73](causal+perturbation+theory#EpsteinGlaser73)) to think of the time-ordered products, being [[operator-valued distributions]], as [[generalized functions]] with dependence on spacetime points:

$$
  \begin{aligned}
    & \int_{\Sigma^{r+s}}
      T_{L_1, \cdots, L_r, A_1, \cdots, A_s}(x_1, \cdots, x_{r}, y_1, \cdots, y_s)
      g_{sw,1}(x_1) \cdots g_{sw, r}(x_r)
      j_{sw,1}(y_1) \cdots j_{sw,s}(y_s)
    dvol_\Sigma(x_1, \cdots, x_r, y_1, \cdots, y_s)
    \\
    & \coloneqq
    T( g_{sw,1} L_1 \cdots g_{sw,k} L \cdot j_{sw,1} A_1 \cdots j_{sw,s}A_s )
  \end{aligned}
  \,.
$$

Moreover, the subscripts on these [[generalized functions]] will always be
clear from the context, so that in computations we will notationally suppress these.

Finally, due to the "symmetry" axiom in def. \ref{TimeOrderedProduct}, a time-ordered product
depends only on its [[set]] of arguments, not on the order of the arguments. We will write
$\mathbf{X} \coloneqq \{x_1, \cdots, x_r\}$ and $\mathbf{Y} \coloneqq \{y_1, \cdots y_r\}$
for sets of spacetime points, and hence abbreviate the expression for the "value" of the
generalized function in the above as $T(\mathbf{X}, \mathbf{Y})$ etc.

In this condensed notation the above reads

$$
    \int_{\Sigma^{r+s}}
      T(\mathbf{X}, \mathbf{Y})
      \,
      g_{sw,1}(x_1) \cdots g_{sw, r}(x_r)
      \,
      j_{sw,1}(y_1) \cdots j_{sw,s}(y_s)
    dvol_\Sigma(\mathbf{X},\mathbf{Y})
  \,.
$$

=--

This condensed notation turns out to be greatly simplify computations, as it absorbs all the "relative"
combinatorial prefactors:

+-- {: .num_example #ProductOfPerturbationSeriesInGenealizedFunctionNotation}
###### Example
**(product of perturbation series in generalized function notation)**

Let

$$
  U(g)
  =
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int U(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

and

$$
  V(g)
  =
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int V(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

be power series of distributions in formal power series in $g/\hbar$ as in def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}.
Then the product $W(g) \coloneqq U(g) V(g)$ with expansion

$$
  W(g)
  =
  \underoverset{n = 0}{\infty}{\sum}
   \frac{1}{n!}
   \int W(x_1, \cdots, x_n)
   \,
   g(x_1) \cdots g(x_n) \, dvol
$$

is given simply by

$$
  W(\mathbf{X})
    \;=\;
  \underset{\mathbf{I} \subset \mathbf{X}}{\sum} U(\mathbf{I}) V(\mathbf{X} \setminus \mathbf{I})
  \,.
$$

([Epstein-Glaser 73 (5)](causal+perturbation+theory#EpsteinGlaser73))

This is because for fixed cardinality ${\vert \mathbf{I} \vert} = n_1$
this sum over all subsets $\mathbf{I} \subset \mathbf{X}$ overcounts the sum over
partitions of the coordinates as $(x_1, \cdots x_{n_1}, x_{n_1 + 1}, \cdots x_n)$ precisely by the
[[binomial coefficient]] $\frac{n!}{n_1! (n - n_1) !}$. Here the factor of $n!$ cancels
against the "global" combinatorial prefactor in the above expansion of $W(g)$, while the remaining
factor $\frac{1}{n_1! (n - n_1) !}$ is just the "relative" combinatorial prefactor seen at total order $n$
when expanding the product $U(g)V(g)$.


=--



+-- {: .num_remark #TheTraditionalErrorThatLeadsToTheNotoriouDivergencies}
###### Remark
**(the traditional error that leads to the notorious divergencies)**

Naively it might seem that the time-ordered products of def. \ref{TimeOrderedProduct}
are given simply by multiplication with [[step functions]], in the notation as
generalized functions (def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}):

$$
  T(x_1, x_2)
  \overset{\text{no!}}{=}
  \theta(x_1^0 - x_2^0) T(x_1) T(x_2)
  +
  \theta(x_2^0 - x_1^0) T(x_2) T(x_1)
$$

etc. (for instance [Weinberg 95, p. 143, between (3.5.9) and (3.5.10)](#Weinberg95)).

This however is simply a mathematical error, in general: Both $T(-,-)$ as well as $\theta$
are [[distributions]] and their [[product of distributions]] is in general not defined.
The notorious "divergencies which plague quantum field theory" are the signature
of this ill defined operation.

On the other hand, when both distributions are restricted to the [[complement]] of the [[diagonal]]
(i.e. restricted away from $x_1 = x_2$) then the above expression happens to be well defined and does
solve the axioms for time-ordered products.

Hence what needs to be done to properly define the time-ordered product is to
choose an [[extension of distributions]] of the above expression from the complement of the
diagonal to the diagonal. Any such extension will produce time-ordered products.
There are in general several different such extensions. This freedom of choice is the freedom
of [[renormalization]]; or equivalently, by the [[main theorem of perturbative renormalization theory]],
this is the freedom of choosing "counter terms" for the local interaction. This we discuss below in
_[Feynman diagrams and (re-)normalization](#Renormalization)_.


=--

In order to prove that the axioms for time-ordered products do imply those for a perturbative S-matrix
(prop. \ref{TimeOrderedProductInducesPerturbativeSMatrix} below) we need to consider
the corresponding reverse-time ordere products:


+-- {: .num_defn #ReverseTimeOrderedProduct}
###### Definition
**(reverse-time ordered product)**

Given a time-ordered product $T = \{T_k\}_{k \in \mathbb{N}}$ (def. \ref{TimeOrderedProduct}),
its _reverse-time ordered product_

$$
  \overline{T}_k \;\colon\; \mathcal{F}_{loc}^{\otimes^k} \longrightarrow \mathcal{W}[ [ g/\hbar ] ]
$$

for $k \in \mathbb{N}$ is defined by

$$
  \overline{T}( L_1 \cdots L_n )
  \;\coloneqq\;
  \left\{
    \array{
      \underoverset{r = 1}{n}{\sum}
      (-1)^r
      \underset{\sigma \in Unshuffl(n,r)}{\sum}
      T( L_{\sigma(1)} \cdots L_{\sigma(k_1)} )
      \,
      T( L_{\sigma(k_1 + 1)} \cdots L_{\sigma(k_2)} )
      \cdots
      T( L_{\sigma(k_{r-1}+1)} \cdots L_{\sigma_{k_r}}  )
      &\vert& k \geq 1
      \\
      1 &\vert& k = 0
    }
  \right.
  \,,
$$

where the sum is over all [[unshuffles]] $\sigma$ of $(1 \leq \cdots \leq n)$ into $r$ non-empty
ordered subsequences. Alternatively, as a generalized function as in def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}, this reads

$$
  \overline{T}( \mathbf{X} )
  =
  \underoverset{r = 1}{{\vert \mathbf{X} \vert}}{\sum}
  (-1)^r
  \underset{ \array{
    \mathbf{I}_1, \cdots, \mathbf{I}_r \neq \emptyset
    \\
    \underset{j \neq k}{\forall}\left( \mathbf{I}_j \cap \mathbf{I}_k = \emptyset  \right)
    \\
    \mathbf{I}_1 \cup \cdots \cup \mathbf{I}_r = \mathbf{X}
  } }{\sum}  T( \mathbf{I}_1 ) \cdots T(\mathbf{I}_r)
$$

=--

(e.g. [Epstein-Glaser 73 (11)](causal+perturbation+theory#EpsteinGlaser73))

+-- {: .num_prop #ReverseTimOrderedProductsGiveReverseSMatrix}
###### Proposition
**(reverse-time ordered products express inverse S-matrix)**

Given a time-ordered products $T(-)$ (def. \ref{TimeOrderedProduct}), then the
corresponding reverse time-ordered product $\overline{T}(-)$ (def. \ref{ReverseTimeOrderedProduct})
expresses the [[inverse]] $S(-)^{-1}$ (according to remark \ref{PerturbativeSMatrixInverse}) of the corresponding
perturbative S-matrix $S(L) \coloneqq \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{k!} T(\underset{k\,\text{args}}{\underbrace{L \cdots L}})$:

$$
  S(L)^{-1}
  =
  \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{k!} \overline{T}( \underset{k \, \text{args}}{\underbrace{L \cdots L}} )
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition we have

$$
  \underset{k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \overline{T}( \underset{k \, \text{args}}{\underbrace{L \cdots L}} )
  =
  \underset{ k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \underoverset{r = 1}{k}{\sum}
    (-1)^r
    \underset{\sigma \in Unshuffl(k,r)}{\sum}
    T( L_{\sigma(1)} \cdots L_{\sigma(k_1)} )
    T( L_{\sigma(k_1 + 1)} \cdots L_{\sigma(k_2)} )
    \cdots
    T( L_{\sigma(k_{r-1}+1)} \cdots L_{\sigma_{k_r}} )
$$

where $\underset{k \in \{1 , \cdots, n\}}{\forall} L_k \coloneqq L$.

If instead of unshuffles (i.e. partitions into non-empty subsequences preserving the original order) we took
partitions into arbitrarily ordered subsequences,
we would be overcounting by the factorial of the length of the subsequences, and hence the
above may be equivalently written as:

$$
  \cdots
  =
  \underset{k \in \mathbb{N}}{\sum}
    \tfrac{1}{k!}
    \underoverset{r = 1}{k}{\sum}
    (-1)^r
    \underset{ {\sigma \in \Sigma(k)} \atop { { k_1 + \cdots + k_r = k } \atop { \underset{i}{\forall} (k_i \geq 1) } } }{\sum}
    \tfrac{1}{k_1!} \cdots \tfrac{1}{k_r !}
    \,
    T( L_{\sigma(1)} \cdots L_{\sigma(k_1)} )
    \,
    T( L_{\sigma(k_1 + 1)} \cdots L_{\sigma(k_2)} )
    \cdots
    T( L_{\sigma(k_{r-1}+1)} \cdots L_{\sigma_{k_r}} )
    \,,
$$

where $\Sigma(k)$ denotes the [[symmetric group]] (the collection of all [[permutations]] of $k$ elements).

Moreover, since all the $L_k$ are equal, the sum is in fact independent of $\sigma$, it only depends
on the length of the subsequences. Since there are $k!$ permutations of $k$ elements
the above reduces to

$$
  \begin{aligned}
    \cdots
    & =
    \underset{k \in \mathbb{N}}{\sum}
      \underoverset{r = 1}{k}{\sum}
      (-1)^r
      \underset{  k_1 + \cdots + k_r = k }{\sum}
      \tfrac{1}{k_1!} \cdots \tfrac{1}{k_r !}
      T( \underset{k_1 \, \text{factors}}{\underbrace{ L \cdots L }}  )
      T( \underset{k_2 \, \text{factors}}{\underbrace{ L \cdots L }}  )
      \cdots
      T( \underset{k_r \, \text{factors}}{\underbrace{ L \cdots L }}  )
    \\
    & =
      \underoverset{\infty}{r = 0}{\sum}
      \left(
        - \underoverset{k = 0}{\infty}{\sum} T ( \underset{k\,\text{factors}}{\underbrace{L \cdots L}}   )
      \right)^r
    \\
    & =
      S(L)^{-1}
      \,,
  \end{aligned}
$$

where in the last line we used (eq:InfverseOfPerturbativeSMatrix).


=--

In fact prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix} is a special case of the
following more general statement:

+-- {: .num_prop #InversionFormulaForTimeOrderedProducts}
###### Proposition
**(inversion relation for reverse-time ordered products)**

Let $\{T_k\}_{k \in \mathbb{N}}$ be [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then the reverse-time ordered products according to def. \ref{ReverseTimeOrderedProduct}
satisfies the following inversion relation for all $\mathbf{X} \neq \emptyset$
(in the condensed notation of def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions})

$$
  \underset{\mathbf{J} \subset \mathbf{X}}{\sum}
    T(\mathbf{J}) \overline{T}(\mathbf{X} \setminus \mathbf{J})
  \;=\;
  0
$$

and

$$
  \underset{\mathbf{J} \subset \mathbf{X}}{\sum}
    \overline{T}(\mathbf{X} \setminus \mathbf{J})  T(\mathbf{J})
  \;=\;
  0
$$

=--

+-- {: .proof}
###### Proof

This is immediate from unwinding the definitions.


=--

+-- {: .num_prop #ReverseCausalFactorizationOfReverseTimeOrderedProducts}
###### Proposition
**(reverse [[causal factorization]] of reverse-time ordered products)**

Let $\{T_k\}_{k \in \mathbb{N}}$ be [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then the reverse-time ordered products according to def. \ref{ReverseTimeOrderedProduct} satisfies
reverse-[[causal factorization]].

=--

([Epstein-Glaser 73, around (15)](causal+perturbation+theory#EpsteinGlaser73))

+-- {: .proof}
###### Proof

In the condensed notation of def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions},
we need to show that for $\mathbf{X} = \mathbf{P} \cup \mathbf{Q}$ with $\mathbf{P} \cap \mathbf{Q} = \emptyset$
then

$$
  \left(
    \mathbf{P} \geq \mathbf{Q}
  \right)
  \;\Rightarrow\;
  \left(
    \overline{T}(\mathbf{X})
     =
    \overline{T}(\mathbf{Q}) \overline{T}(\mathbf{P})
  \right)
  \,.
$$

We proceed by [[induction]]. If ${\vert \mathbf{X}\vert} = 1$ the statement is immediate.
So assume that the statement is true for sets of [[cardinality]] $n \geq 1$ and consider
$\mathbf{X}$ with ${\vert \mathbf{X}\vert} = n+1$.

We make free use of the condensed notation as in example \ref{ProductOfPerturbationSeriesInGenealizedFunctionNotation}.

From the formal inversion

$$
  \underset{\mathbf{J} \subset \mathbf{X}}{\sum} \overline{T}(\mathbf{J}) T(\mathbf{X}\setminus \mathbf{J})
  = 0
$$

(which uses the induction assumption that ${\vert \mathbf{X}\vert} \geq 1$) it follows that

$$
  \begin{aligned}
    \overline{T}(\mathbf{X})
      & =
    - \underset{ { \mathbf{J} \subset \mathbf{X} } \atop { \mathbf{J} \neq \mathbf{X} }  }{\sum}
     \overline{T}(\mathbf{J}) T( \mathbf{X} \setminus \mathbf{J} )
     \\
     & =
    - \underset{
        { \mathbf{J} \cup \mathbf{J}' = \mathbf{X} }
        \atop
        {
          { \mathbf{J} \cap \mathbf{J}' = \emptyset }
          \atop
          { \mathbf{J}' \neq \emptyset }
        }
     }{\sum}
     \overline{T}( \mathbf{Q} \cap \mathbf{J} )
     \overline{T}( \mathbf{P} \cap \mathbf{J} )
               T ( \mathbf{P} \cap ( \mathbf{J}' ) )
               T ( \mathbf{Q} \cap ( \mathbf{J}' ) )
     \\
     & =
    - \underset{
      { \mathbf{L} \cup \mathbf{L}' = \mathbf{Q} \,,\, \mathbf{L} \cap \mathbf{L}' = \emptyset }
      \atop
      { \mathbf{L}' \neq \emptyset }
    }{\sum}
     \overline{T}( \mathbf{L} )
     \underset{ = 0}{
       \underbrace{
         \left(
          \underset{
              \mathbf{K} \subset \mathbf{P}
           }{\sum}
           \overline{T}( \mathbf{K} ) T( \mathbf{P} \setminus \mathbf{K})
         \right)
       }
     }
     T(\mathbf{L'})
    -
    \overline{T}(\mathbf{Q})
    \underset{
      = - \overline{T}(\mathbf{P})
    }{
    \underbrace{
      \underset{
        {\mathbf{K} \subset \mathbf{P}}
        \atop
        { \mathbf{K} \neq \emptyset }
      }{\sum}
      \overline{T}(\mathbf{K})
                T (\mathbf{P} \setminus \mathbf{K} )
    }}
    \\
    & =
    \overline{T}(\mathbf{Q}) \overline{T}(\mathbf{P})
  \end{aligned}
   \,.
$$

Here

1. in the second line we used that $\mathbf{X} = \mathbf{Q} \sqcup \mathbf{P}$, together with the
causal factorization property of $T(-)$ (which holds by general assumption) and that of $\overline{T}(-)$
(which holds by the induction assumption, using that $\mathbf{J} \neq \mathbf{X}$ hence that
${\vert \mathbf{J}\vert} \lt {\vert \mathbf{X}\vert}$).

1. in the third line we decomposed the sum over $\mathbf{J}, \mathbf{J}' \subset \mathbf{X}$
into two sums over subsets of $\mathbf{Q}$ and $\mathbf{P}$:

   1. The first summand in the third line is the contribution where $\mathbf{J}'$ has a non-empty intersection with $\mathbf{Q}$. This makes $\mathbf{K}$ range without constraint, and therefore the sum in the middle vanishes, as indicated, as it is the contribution at order ${\vert \mathbf{Q}\vert}$ of the inversion formula from prop. \ref{InversionFormulaForTimeOrderedProducts}

   1. The second summand in the third line is the contribution where $\mathbf{J}'$ does not intersect $\mathbf{Q}$.
     Now the sum over $\mathbf{K}$ is the inversion formula from prop. \ref{InversionFormulaForTimeOrderedProducts} except for one term, and so it equals that term.

=--

Using these facts about the reverse-time ordered products,
we may finally prove that [[time-ordered products]] indeed do induced a perturbative S-matrix:

+-- {: .num_prop #TimeOrderedProductInducesPerturbativeSMatrix}
###### Proposition
**([[time-ordered products]] induce [[perturbative S-matrix]])**

Let $\{T_k\}_{k \in \mathbb{N}}$ be a system of [[time-ordered products]] according to def. \ref{TimeOrderedProduct}.
Then

$$
  \begin{aligned}
    S(-)
    & \coloneqq
    T \exp\left(
      \tfrac{1}{i \hbar}(-)
      \right)
    \\
    &
    \coloneqq \underset{k \in \mathbb{N}}{\sum} \tfrac{1}{(i \hbar)^k} \tfrac{1}{k!} T( \underset{k \, \text{factors}}{\underbrace{- \cdots -}} )
  \end{aligned}
$$

is indeed a perturbative S-matrix according to def. \ref{PerturbativeSMatrixOnMinkowskiSpacetime}.

=--

+-- {: .proof}
###### Proof

The axiom "perturbation" and "normalization" for the S-matrix are
immediate from the corresponding axioms of the time-ordered products.
What requires proof is that [[causal additivity]] of the S-matrix follows from
the causal factorization property of the time-ordered products.

Notice that also the simple causal factorization property of the S-matrix

$$
  (supp(g_{sw_1}L_1) \geq supp(g_{sw,}L_2))
    \;\Rightarrow\;
  \left(
    S(g_{sw,1}L_1 + g_{sw,2}L_2)
    =
    S(g_{sw,1}L_1) S(g_{sw,2}L_2)
  \right)
$$

is immediate from the time-ordering axiom of the time-ordered products.

But [[causal additivity]] is stronger. It is remarkable that this, too,
follows from just the time-ordering ([Epstein-Glaser 73, around (73)](causal+perturbation+theory#EpsteinGlaser73)):

To see this, first expand the
generating functional $Z$ (eq:GeneratingFunctionInducedFromSMatrix)  into
powers of $(g/\hbar)$ and $(j/\hbar)$

$$
  Z_{L}(L + A)
  \;=\;
  \underoverset{n,m = 0}{\infty}{\sum}
   \frac{1}{n! m!}
   R(  \underset{n\, \text{factors}}{\underbrace{L \cdots L}},  ( \underset{m \, \text{factors}}{ \underbrace{ A \cdots A } }  ) )
$$

and then compare order-by-order with the given time-ordered product $T$ and
its induced reverse-time ordered product (def. \ref{ReverseTimeOrderedProduct}) via prop. \ref{ReverseTimOrderedProductsGiveReverseSMatrix}.
(These $R(-,-)$ are also called the "generating [[retarded products]], discussed in their own right around def. \ref{RetardedProductFromPerturbativeSMatrix} below.)

In the condensed notation of
def. \ref{NotationForTimeOrderedProductsAsGeneralizedFunctions}
and its way of absorbing combinatorial prefactors as in example \ref{ProductOfPerturbationSeriesInGenealizedFunctionNotation}
this
yields at order $(g/\hbar)^{\vert \mathbf{Y}\vert} (j/\hbar)^{\vert \mathbf{X}\vert}$ the coefficient

$$
  \label{CoefficientOfgeneratingRetardedProduct}
  R(\mathbf{Y}, \mathbf{X})
   \;=\;
  \underset{\mathbf{I} \subset \mathbf{Y}}{\sum}
    \overline{T}(\mathbf{I})
    T( (\mathbf{Y} \setminus \mathbf{I}) , \mathbf{X} )
  \,.
$$

We claim now that the [[support of a distribution|support]] of $R$ is inside the subset for which
$\mathbf{Y}$ is in the [[causal past]] of $\mathbf{X}$. This will imply the claim, because by
multi-linearity of $R(-,-)$ it then follows that

$$
  \left(J_1 \geq J_2\right) \Rightarrow \left( Z_{L + J_1}(J_2) = Z_L(J_2) \right)
$$

and by prop. \ref{CausalLocalityOfThePerturbativeSMatrix} this is equivalent to [[causal additivity]] of the S-matrix.

It remains to prove the claim:

Consider $\mathbf{X}, \mathbf{Y} \subset \Sigma$ such that the subset $\mathbf{P} \subset \mathbf{Y}$
of points not in the past of $\mathbf{X}$ (def. \ref{CausalOrdering}), hence the maximal subset with

$$
  \mathbf{P} \geq \mathbf{X}
  \,,
$$

is non-empty. We need to show that in this case $R(\mathbf{Y}, \mathbf{X}) = 0$ (in the sense of generalized functions).

Write $\mathbf{Q} \coloneqq \mathbf{Y} \setminus \mathbf{P}$
for the complementary set of points, so that all points of $\mathbf{Q}$ are in the past of $\mathbf{X}$.
Notice that this implies that $\mathbf{P}$ is also not in the past of $\mathbf{Q}$:

$$
  \mathbf{P} \geq \mathbf{Q}
  \,.
$$

With this decomposition of $\mathbf{Y}$, the sum in (eq:CoefficientOfgeneratingRetardedProduct)
over subsets $\mathbf{I}$ of $\mathbf{Y}$ may be decomposed into a sum over
subsets $\mathbf{J}$ of $\mathbf{P}$ and $\mathbf{K}$ of $\mathbf{Q}$, respectively.
These subsets inherit the above causal ordering, so that by the causal factorization property of
$T(-)$ (def. \ref{TimeOrderedProduct}) and $\overline{T}(-)$ (prop. \ref{ReverseCausalFactorizationOfReverseTimeOrderedProducts})
the time-ordered and reverse time-ordered products
factor on these arguments:

$$
  \begin{aligned}
    R(\mathbf{Y}, \mathbf{X})
    & =
    \underset{ {\mathbf{J} \subset \mathbf{P}} \atop { \mathbf{K} \subset \mathbf{Q} } }{\sum}
     \,
     \overline{T}( \mathbf{J} \cup \mathbf{K} )
     T( (\mathbf{P} \setminus \mathbf{J}) \cup (\mathbf{Q} \setminus \mathbf{K}), \mathbf{X} )
     \\
     & =
     \underset{ {\mathbf{J} \subset \mathbf{P}} \atop { \mathbf{K} \subset \mathbf{Q} } }{\sum}
     \,
     \overline{T}( \mathbf{K} )
     \overline{T}( \mathbf{J} )
     T( \mathbf{P} \setminus \mathbf{J} )
     T( \mathbf{Q} \setminus \mathbf{K}, \mathbf{X} )
     \\
     & =
     \underset{ \mathbf{K} \subset \mathbf{Q} }{\sum}
     \overline{T}(\mathbf{K})
     \underset{= 0}{
     \underbrace{
     \left(
       \underset{\mathbf{J} \subset \mathbf{P}}{\sum}
       \overline{T}(\mathbf{J})
       T( \mathbf{P} \setminus \mathbf{J} )
     \right)
     }}
     T(\mathbf{Q} \setminus \mathbf{K}, \mathbf{X})
  \end{aligned}
  \,.
$$

Here the sub-sum in brackets vanishes by the inversion formula, prop. \ref{InversionFormulaForTimeOrderedProducts}.

=--

$\,$
