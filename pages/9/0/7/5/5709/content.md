


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

While fundamental [[physics]] is at some level well described by [[quantum field theory]], a typical [[Lagrangian]] used to define such a QFT can reasonably be expected to define only degrees of freedom and interactions that are relevant up to some given [[energy]] scale. In this perspective one speaks of the theory as being the _effective quantum field theory_ of some -- possibly known but possibly unspecified -- more fundamental theory.

An example (historically the first to be successfully considered) is the [[Fermi theory of beta decay]] of hadrons: this contains interactions of four [[fermion]]s at a time, for instance a process in which a [[neutron]] decays into a collection consisting of a [[proton]], an [[electron]] and a [[neutrino]]. Later it was discovered that, more fundamentally, this is not a single reaction but is composed out of several other interactions that involve exchanges of [[W-boson]]s between these four particles. Nevertheless, Fermi's original _effective_ theory made very precise predictions at energy scales less than 10 [[MeV]]. The reason is that the $W$-boson has mass several orders of magnitude higher than that (about 80 [[GeV]]) and was thus _effectively_ invisible at these low energies.

The low energy expansion of any unitary, relativistic, [[crossing symmetry|crossing symmetric]] [[S-matrix]] can be described by an effective quantum field theory.

In the perspective of effective field theory notably  [[renormalizable interaction|non-renormalizable]] [[interaction]]  Lagrangians can still make perfect sense as effective theories and give rise to well defined predictions: they can be effective approximations to [[renormalizable interaction|renormalizable]] more fundamental theories. This is sometimes called a [[UV completion]] of the given effective theory.

For instance [[quantum gravity]] -- which is notoriously [[non-renormalizable interacton|non-renormalizable]] -- makes perfect sense as an effective field theory (see for instance the introduction in ([Donoghue](#DonoghueIntroduction)). It is in principle possible that there is some more fundamental theory with plenty of excitations at high energies that is however degreewise finite in [[perturbation theory]], whose _effective_ description at low energy is given by the [[renormalizable interaction|non-renormalizable]] [[Einstein-Hilbert action]]. (For instance, [[string theory]] is meant to be such a theory.)



## Details

The concept of effective [[perturbative QFT]] has a precise formulation in the rigoruous context of [[causal perturbation theory]]/[[perturbative AQFT]]:

* _[Effective pQFT in Causal perturbation theory](#InCausalPerturbationTheory)_

Effective quantum field theory has traditioanlly been discussed informally, referring to [[path integral]] intuition:

* _[Traditional informal arguments](#TraditionalInformalDiscussion)-

### In causal perturbation theory
 {#InCausalPerturbationTheory}

We discuss the rigorous formulation of effective [[perturbative QFT]] in terms of [[causal perturbation theory]]/[[perturbative AQFT]], due to ([Brunetti-Dütsch-Fredenhagen 09, section 5.2](#BrunettiDuetschFredenhagen09), [Dütsch 10](#Duetsch10)), reviewed in [Dütsch 18, section 3.8](#Duetsch18)).

#### ("Re"-)Normalization via UV-Regularization
 {#UVRegularization}

+-- {: .num_defn #CutoffsUVForPerturbativeQFT}
###### Definition
**([[UV cutoffs]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] over [[Minkowski spacetime]] $\Sigma$ (according to [this def.](S-matrix#VacuumFree)), where $\Delta_H = \tfrac{i}{2}(\Delta_+ - \Delta_-) + H$ is the corresponding [[Wightman propagator]] inducing the [[Feynman propagator]]

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

   1. (bounded [[degree of divergence of a distribution|degree of divergence]])

      $$
        deg(\Delta_{F,\Lambda})
        \;\leq\;
        deg(\Delta_{F})
      $$

1. the [[limit of a sequence|limit]] of the $\Delta_{F,\Lambda}$ as $\Lambda \to 0$ exists and is zero

   $$
     \underset{\Lambda \to \infty}{\lim} \Delta_{F,\Lambda}
     \;=\;
     0
     \,.
   $$


1. the [[limit of a sequence|limit]] of the $\Delta_{F,\Lambda}$ as $\Lambda \to \infty$ exists and is the [[Feynman propagator]]:

   $$
     \underset{\Lambda \to \infty}{\lim} \Delta_{F,\Lambda}
     \;=\;
     \Delta_F
     \,.
   $$

=--

([Dütsch 10, section 4](#Duetsch10))

example:  relativistic momentum cutoff with $\epsilon$-regularization ([Keller-Kopper-Schophaus 97, section 6.1](#KellerKopperSchophaus97), [Dütsch 18, example 3.126](#Duetsch18))


+-- {: .num_defn #SMatrixEffective}
###### Definition
**([[effective S-matrix scheme]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

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

with respect to the [[star product]] $\star_{F,\Lambda}$ induced by the $\Delta_{F,\Lambda}$ ([this def.](star+product#PropagatorStarProduct)).

This is evidently defined on all [[polynomial observables]] as shown, and restricts to an endomorphism on
[[microcausal polynomial observables]] as shown, since the contraction coefficients $\Delta_{F,\Lambda}$ are [[non-singular distributions]],
by definition of [[UV cutoff]].

=--

([Dütsch 10, (4.2)](#Duetsch10))


+-- {: .num_prop #UVRegularization}
###### Proposition
**([[renormalization|("re"-)normalization]] via [[UV regularization]])**


Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$ a polynomial [[local observable]], regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Let moreover $\{\Delta_{F,\Lambda}\}_{\Lambda \in [0,\infty)}$ be a [[UV cutoff]]; with $\mathcal{S}_\Lambda$ the induced [[effective S-matrix schemes]] ([this def.](effective+quantum+field+theory#EffectiveSMatrixScheme)).


Then

1. there exists a $[0,\infty)$-parameterized [[interaction vertex redefinition]] $\{\mathcal{Z}_\Lambda\}_{\Lambda \in \mathbb{R}_{\geq 0}}$ ([this def.](Stückelberg-Petermann+renormalization+group#InteractionVertexRedefinition))
such that the [[limit of a sequence|limit]] of [[effective S-matrix schemes]]  $\mathcal{S}_{\Lambda}$ (eq:EffectiveSMatrixScheme) applied to the $\mathcal{Z}_\Lambda$-[[vertex redefinition|redefined interactions]]

   $$
     \mathcal{S}_\infty
     \;\coloneqq\;
     \underset{\Lambda \to \infty}{\lim}
     \left(
       \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda
     \right)
   $$

   exists and is a genuine [[S-matrix scheme]] around the given vacuum ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering));

1. every [[S-matrix scheme]] around the given vacuum arises this way.

Hence UV-regularization via [[counterterms]] is a method of [[renormalization|("re"-)normalization]] of [[perturbative QFT]] ([this def.](S-matrix#ExtensionOfTimeOrderedProoductsRenormalization)).

=--

This was claimed in ([Brunetti-Dütsch-Fredenhagen 09, (75)](#BrunettiDuetschFredenhagen09)), a proof was indicated in ([Dütsch-Fredenhagen-Keller-Rejzner 14, theorem A.1](#DuetschFredenhagenKellerRejzner14)).

+-- {: .proof}
###### Proof

Let $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ be a sequence of projection maps as in [this equation](renormalization#) defining an [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] ([this prop.](renormalization#RenormalizationIsInductivelyExtensionToDiagonal)) of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ as [[extensions of distributions]] of the $T_k$, regarded as distribution via [this remark](renormalization#TimeOrderedProductOfFixedInteraction), by the choice $q_k^\alpha = 0$ in [this equation](renormalization#eq:ExtensionOfDitstributionsPointFixedAndChoice).

By the proof of [that prop.](renormalization#SpaceOfPointExtensions) the extension of the time ordered products after the $p_\rho$-projections is unique, so that the actual S-matrix may be written as

$$
  \mathcal{S}(O)
  \;=\;
  \underset{\Lambda \to \infty}{\lim}
  \underset{k}{\sum}
  \frac{1}{k!} \frac{1}{(i \hbar)!}
  {T_{k,\Lambda}} \circ p_{\rho_k} ( \underset{k \, \text{factors}}{\underbrace{O \otimes \cdots \otimes O} })
$$

where 

$$
  T_{k,\Lambda}(O_1, \cdots, O_k)
  \;=\;
  O_1 
    \star_{F,\Lambda}
    \cdots
    \star_{F,\Lambda}
  O_k
$$

is the effective time-ordered product at cutoff scale $\Lambda$ as in [this def.](renormalization#SMatrixEffective).

With this it is now sufficient to find $\mathcal{Z}_\Lambda$ such that

$$
  T_{k+1,\Lambda} \circ \mathcal{Z}_{\leq k+1, \Lambda}
  \;=\;
  T_{k+1, \Lambda} \circ p
  \,,
$$

where on the left we mean the $(k+1)$-ary coefficient of $\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$, in the same way as in the proof of the [[main theorem of perturbative renormalization]] ([this prop.](Stückelberg-Petermann+renormalization+group#AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition)).

Further proceeding as in that proof, by [[induction]] over the arity of the time-ordered products, this implies that $Z_{n+1,\Lambda}$ is fixed to be

$$
  Z_{n+1,\Lambda}
  \;=\;
  T_{n+1,\Lambda} \circ p 
  -
  T_{n+1, \Lambda} \circ \mathcal{Z}_{\leq n}
  +
  K_\Lambda
$$

where we need to choose $K_\Lambda$ such that

1. $\underset{\Lambda \to \infty}{\lim} K_\Lambda = 0$;

1. $Z_{n+1,\Lambda}$ is local.

Consider

$$
  K_\Lambda
  \;\coloneqq\;
  T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} \circ p
  -
  T_{n+1,\Lambda} \circ p
$$

In fact $K_\Lambda = 0$ independent of $\Lambda$, since $p$ projects away from the diagonal, but a vertex redefinition $\mathcal{Z}_{\leq n}$ only acts non-trivially on the diagonal, by definition.

Hence we may take

$$
  \begin{aligned}
    Z_{n+1,\Lambda}
    & =
    T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} \circ p 
    -
    T_{n+1, \Lambda} \circ \mathcal{Z}_{\leq n}
    \\
    & =
    T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} \circ ( p - id)
  \end{aligned}
$$

By by definition $p - id$ is the identity on test functions (adiabatic switchings) that vanish at the diagonal. This means that $Z_{n+1,\Lambda}$ is indeed local.


This shows that a consistent choice of $\mathcal{S}_\Lambda$ exists. To see that every [[S-matrix scheme]] arises this way from choice of $\mathcal{Z}_\Lambda$ it is now sufficient, by the above proof, to see that every S-matrix scheme  comes from vanishing renormalization constants $q^\alpha_k$ in [this equation](renormalization#eq:ExtensionOfDitstributionsPointFixedAndChoice) for _some_ sequence of projections $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ (in the notation of the proof of [that prop.](renormalization#SpaceOfPointExtensions)). This is pretty clear...

=--



+-- {: .num_remark #TermCounter}
###### Remark
**([[counterterms]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

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

(which by the axiom "perturbation" in [this def.](Stückelberg-Petermann+renormalization+group#InteractionVertexRedefinition) is at least of second order in the [[coupling constant]]/[[source field]], as shown)
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


#### Effective quantum field theory
 {#RelativeEffectiveAction}

+-- {: .num_prop #EffectiveSmatrixSchemeInvertible}
###### Proposition
**([[effective S-matrix schemes]] are [[inverse|invertible functions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

Write

$$
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]
$$

for  the subspace of the space of [[formal power series]] in $\hbar, g, j$ with [[coefficients]] [[polynomial observables]]
on those which are at least of first order in $g,j$, i.e. those that vanish for $g, j = 0$ (as in [this def.](S-matrix#FormalParameters)).

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
   \underoverset{\simeq}{\mathcal{S}_\Lambda}{\longrightarrow}
  1
    +
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g, j] ]\langle g,j\rangle
  \,.
$$

=--

([Dütsch 10, (4.7)](#Duetsch10))

+-- {: .proof}
###### Proof

Since each $\Delta_{F,\Lambda}$ is symmetric (def. \ref{CutoffsUVForPerturbativeQFT})
if follows by general properties of [[star products]] ([this prop.](star+product#SymmetricContribution))
just as for the genuine [[time-ordered product]] on [[regular polynomial observables]] ([this prop.](Wick+algebra#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise)) that
eeach the "effective time-ordered product" $\star_{F,\Lambda}$ is [[isomorphism|isomorphic]]
to the pointwise product $(-)\cdot (-)$ ([this def.](A+first+idea+of+quantum+field+theory#Observable))

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

(as in [this equation](Wick+algebra#eq:OnRegularPolynomialObservablesPointwiseTimeOrderedIsomorphism)).

In particular this means that the [[effective S-matrix]] $\mathcal{S}_\Lambda$ arises from the [[exponential series]] for the pointwise product by [[conjugation]] with $\mathcal{T}_\Lambda$:

$$
  \mathcal{S}_\Lambda
  \;=\;
  \mathcal{T}_\Lambda \circ \exp_\cdot\left( \frac{1}{i \hbar}(-) \right) \circ \mathcal{T}_\Lambda^{-1}
$$

(just as for the genuine S-matrix on [[regular polynomial observables]] in [this def.](S-matrix#OnRegularObservablesPerturbativeSMatrix)).

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
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

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

([Dütsch 10, (5.4)](#Duetsch10))

+-- {: .num_remark #pQFTEffective}
###### Remark
**([[effective quantum field theory]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)), let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum  (def. \ref{CutoffsUVForPerturbativeQFT}), and let $\mathcal{S}_\infty = \underset{\Lambda \to \infty}{\lim} \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$ be a corresponding [[UV regularization]] (prop. \ref{UVRegularization}).

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
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).


Then the [[relative effective action]] (def. \ref{EffectiveActionRelative}) at $\Lambda = 0$ is the actual [[effective action]] ([this def.](S-matrix#InPerturbationTheoryActionEffective)) being $i \hbar$ times the [[Feynman perturbation series]] of
[[Feynman amplitudes]] $\Gamma(g S_{int} + j A)$ for [[connected graph|connected]] [[Feynman diagrams]] $\Gamma$:

$$
  \begin{aligned}
    S_{eff,0}
    & \coloneqq\;
    S_{eff,0,\infty}
    \\
    & = S_{eff} \;\coloneqq\;
    \underset{\Gamma \in \Gamma_{conn}}{\sum}
    \Gamma(g S_{int} + j A)
  \end{aligned}
  \,.
$$

=--

([Dütsch 18, (3.473)](#Duetsch18))

+-- {: .proof}
###### Proof

Observe that the [[effective S-matrix scheme]] at scale $\Lambda = 0$ (eq:EffectiveSMatrixScheme)
is the [[exponential series]] with respect to the pointwise product ([this def.](A+first+idea+of+quantum+field+theory#Observable))

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

That this is the case is the statement of [this prop.](S-matrix#LogarithmEffectiveAction).

=--


#### ("Re"-)Normalization via Wilsonian RG flow

The definition of the [[relative effective action]] $\mathcal{S}_{eff,\Lambda} \coloneqq \mathcal{S}_{eff,\Lambda, \infty}$ in def. \ref{EffectiveActionRelative}
invokes a choice of [[UV regularization]] $\mathcal{S}_\infty$ (prop. \ref{UVRegularization}).
While (by that proposition and the [[main theorem of perturbative renormalization]] this is guaranteed to exist,
in practice one is after methods for constructing this without specifying it a priori.

But the collection [[relative effective actions]] $\mathcal{S}_{eff,\Lambda, \Lambda_0}$ for $\Lambda_0 \lt \infty$
"flows" with the cutoff-parameters $\Lambda$ and in particular also with $\Lambda_0$ (remark \ref{GroupoidOfEFTs} below)
which suggests that examination of this flow yields information about full theory at $\mathcal{S}_\infty$.

This is made precise by _[[Polchinski's flow equation]]_ (prop. \ref{FlowEquationPolchinski} below),
which is the [[infinitesimal]] version of the "[[Wilsonian RG flow]]" (remark \ref{GroupoidOfEFTs}).
As a [[differential equation]] it is _independent_ of the choice of $\mathcal{S}_{\infty}$ and hence may
be used to solve for the [[Wilsonian RG flow]] without knowing $\mathcal{S}_\infty$ in advance.

The freedom in choosing the initial values of this differential equation corresponds to
the [[renormalization|("re"-)normalization freedom]] in choosing the [[UV regularization]] $\mathcal{S}_\infty$.
In this sense "[[Wilsonian RG flow]]" is a method of [[renormalization|("re"-)normalization]] of [[perturbative QFT]]
([this def.](S-matrix#ExtensionOfTimeOrderedProoductsRenormalization)).


+-- {: .num_remark #GroupoidOfEFTs}
###### Remark
**(Wilsonian [[groupoid]] of [[effective quantum field theories]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) and let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum (def. \ref{CutoffsUVForPerturbativeQFT}).

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

This is often called the _Wilsonian RG_, following ([Wilson 71](#Wilson71)).

=--

We now consider the [[infinitesimal]] version of this "flow":

+-- {: .num_prop #FlowEquationPolchinski}
###### Proposition
**([[Polchinski's flow equation]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$
be a [[gauge fixing|gauge fixed]] [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)), let $\left\{ \Delta_{F,\Lambda}\right\}_{\Lambda \in [0,\infty)}$ be a choice of [[UV cutoffs]] for [[perturbative QFT]] around this vacuum  (def. \ref{CutoffsUVForPerturbativeQFT}), such that $\Lambda \mapsto \Lambda_{F,\Lambda}$ is [[differentiable function|differentiable]].

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

where on the right we have the [[star product]] induced by $\Delta_{F,\Lambda'}$ ([this def.](star+product#PropagatorStarProduct)).

=--

This goes back to ([Polchinski 84, (27)](#Polchinski84)). The rigorous formulation and proof is due to ([Brunetti-Dütsch-Fredenhagen 09, prop. 5.2](#BrunettiDuetschFredenhagen09), [Dütsch 10, theorem 2](#Duetsch10)).

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

Here $\frac{\delta}{\delta \mathbf{\Phi}_i}$ denotes the functional derivative of the $i$th tensor factor of $O$, and the binomial coefficient counts the number of ways that an unordered pair of distinct labels of tensor factors may be chosen from a total of $k+2$ tensor factors, where we use that the [[star product]] $\star_{F,\Lambda}$ is commutative (by symmetry of $\Delta_{F,\Lambda}$) and associative (by [this prop.](star+product#AssociativeAndUnitalStarProduct)).

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

### Traditional informal discussion
 {#TraditionalInformalDiscussion}

Traditional informal discussion of effective field theory proceeds from the following claim

_For a given set of asymptotic states, [[perturbation theory]] with the most
general [[Lagrangian]] containing all terms allowed by the assumed symmetries
will yield the most general [[S-matrix]] elements consistent with
analyticity, [[perturbative unitarity]], [[cluster decomposition]] and the assumed symmetries._

This is due to ([Weinberg 1979](#Weinberg79)) and ([Leutwyler94](#Leutwyler94)); reviewed in [Pich, p. 6](#Pich).

Based on this, one argues to obtains an effective approximation to a given more fundamental theory (which may or may not be actually known) by

1. choosing the (sub)set of fields to be considered;

1. writing down a [[Lagrangian]]

   $$
     L_{eff} = \sum_i c_i O_i
   $$

   that contains _all_ the possible polynomial interaction terms $O_i$ of these fields scaled by their expected/known energy scale $[O_i] = d_i$, up to a maximal energy scale

   (this will in general contain lots of direct interaction that in the fundamental theory are really compound interactions)

    with $c_i \propto \frac{1}{\Lambda^{d_i - dim X}}$;

1. finally one fixes all the coupling constants of all these interactions by

   * either deriving them from a known fundamental theory by _integrating out_ higher energy effects in that theory;

   * or, otherwise, measuring them in the laboratory. The point being that due to the energy cutoff, this is guaranteed to be a finite number of parameters. After these have been determined, all remaining quantities given by the Lagrangian are then predictions of the effective theory.


## Examples

### Light-by-light scattering

([Pich, section 2.1](#Pich))

### Rayleigh scattering

([Pich, section 2.2](#Pich))


### Fermi theory of weak interactions

* [[Fermi theory of beta decay]]

([Pich, section 2.3](#Pich))


### Chiral perturbation theory

[[chiral perturbation theory]] is an effective approximation of [[QCD]] in the light [[quark]] sector.


### Heavy quark effective field theory

(...)

### Neutrino masses (?)

On [[neutrino]] [[masses]] and the [[standard model of particle physics]] as an effective field theory:

> I also noted at the same time that interactions between a pair of lepton doublets and a pair of scalar doublets can generate a neutrino mass, which is suppressed only by a factor $M^{-1}$, and that therefore with a reasonable estimate of $M$ could produce observable neutrino oscillations. The subsequent confirmation of neutrino oscillations lends support to the view of the Standard Model as an effective field theory, with M somewhere in the neighborhood of $10^{16} GeV$. ([Weinberg 09, p. 15](#Weinberg09))


### String theory and gravity coupled to gauge theory
 {#StringTheoryAndGravityCoupledToGaugeTheory}

The [[string scattering amplitudes]] for [[superstrings]] are finite (fully proven so for low loop order and with various plausibility arguments for higher loop order, see at _[[string scattering amplitudes]]_ for more), hence define a UV-complete [[S-matrix]]. The corresponding low energy effective field theories are theories of [[supergravity]] coupled to [[gauge theory]]. ([[type II supergravity]], [[heterotic supergravity]]).

See also at _[string theory FAQ -- What is string theory?](string+theory+FAQ#WhatIsStringTheory)_.

## Related concepts

* [[effective action]]

* [[higher order curvature corrections]]

* [[Stückelberg-Petermann renormalization group]]

* [string theory FAQ -- What is the relationship between quantum field theory and string theory?](string+theory+FAQ#RelationshipBetweenQuantumFieldTheoryAndStringTheory)

## References

### General

The modern picture of effective low-energy QFT goes back to

* L. P. Kadanoff, _Scaling laws for Ising models near $T_c$_ , Physica 2 (1966);

* {#Wilson71} [[Kenneth Wilson]], _Renormalization group and critical phenomena_ , I., Physical review B 4(9) (1971).

* {#Polchinski84} [[Joseph Polchinski]], _Renormalization and effective Lagrangians_ , Nuclear Phys. B B231, 1984 ([pdf](http://max2.physics.sunysb.edu/~rastelli/2016/Polchinski.pdf))

* {#Weinberg79} [[Steven Weinberg]], Physica 96 A (1979) 327

* {#Leutwyler94} H. Leutwyler, Ann. Phys., NY 235 (1994) 165.

Review includes

* {#Weinberg09} [[Steven Weinberg]], _Effective Field Theory, Past and Future_ ([arXiv:0908.1964](http://arxiv.org/abs/0908.1964))

* {#Pich} A. Pich, _Effective Field Theory_ ([arXiv:hep-ph/9806303](http://arxiv.org/abs/hep-ph/9806303))
 
* {#Abdesselam13} [[Abdelmalek Abdesselam]], _QFT, RG, and all that, for mathematicians, in eleven pages_ ([arXiv:1311.4897](https://arxiv.org/abs/1311.4897))

* [[Daniel Freed]], _Lecture 5 of [[Five lectures on supersymmetry]]_

A standard textbook adopting this perspective is

* [[Steven Weinberg]], _The Quantum Theory of Fields_ (Cambridge University
Press,Cambridge,1995).

whose author describes his goal as:

> This is intended to be a book on quantum field theory for the era of effective field theory.  

Another book which takes the effective-field-theory approach to QFT is

* Anthony Zee, _Quantum Field Theory in a Nutshell_ (Princeton University Press, second edition, 2010).

See also

* {#KellerKopperSchophaus97} Georg Keller, Christoph Kopper, Clemens Schophaus, _Perturbative Renormalization with Flow Equations in Minkowski Space_, Helv.Phys.Acta 70 (1997) 247-274 ([arXiv.hep-th/9605137](https://arxiv.org/abs/hep-th/9605137))


### In causal perturbation theory
 {#ReferencesInCausalPerturbationTheory}

Discussion of [[perturbative QFT|perturbative]] effective QFT in the rigorous context of [[causal perturbation theory]]/[[perturbative AQFT]] and its relation to the [[Stückelberg-Petermann renormalization group]] is due to

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], section 5.2 of _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* {#Duetsch10} [[Michael Dütsch]], _Connection between the renormalization groups of Stückelberg-Petermann and Wilson_, Confluentes Mathematici, Vol. 4, No. 1 (2012) 12400014 ([arXiv:1012.5604](https://arxiv.org/abs/1012.5604))

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], appendix A of _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy. 55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))


reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.8 of _[[From classical field theory to perturbative quantum field theory]]_, 2018


The point that perturbatively [[renormalization|non-renormalizable]] theories may be regarded as effective field theories at each energy scale was highligted in

* J. Gomis and [[Steven Weinberg]], _Are nonrenormalizable gauge theories renormalizable?_, Nucl. Phys. B 469 (1996) 473.


Notably the theory of [[gravity]] based on the standard [[Einstein-Hilbert action]] may be regarded as just an effective QFT, which makes some of its notorious problems be non-problems:

* {#DonoghueIntroduction} [[John Donoghue]], _Introduction to the Effective Field Theory Description of Gravity_ ([arXiv:gr-qc/9512024](http://arxiv.org/abs/gr-qc/9512024))


* {#AtanceCortes96} Mario Atance, Jose Luis Cortes, _Effective Field Theory of pure Gravity and the Renormalization Group_ ([arXiv:hep-th/9604076](http://arxiv.org/abs/hep-th/9604076))


and in the context of [[perturbation theory]] in [[AQFT]]:

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Quantum gravity from the point of view of locally covariant quantum field theory_ ([arXiv:1306.1058](http://arxiv.org/abs/1306.1058))


Comments on this point are also in

* [[Jacques Distler]], blog posts

  * _[Motivation](http://golem.ph.utexas.edu/~distler/blog/archives/000639.html)_

  * _[Effective field theory and gravity](http://golem.ph.utexas.edu/~distler/blog/archives/001255.html)_

* [[Kevin Costello]], _[[Renormalization and Effective Field Theory]]_

See also

* [[Alastair Hamilton]], _On two constructions of an effective field theory_ ([arXiv:1502.05790](http://arxiv.org/abs/1502.05790))

### For string theory

Discussion of the effective field theories induced by [[string theory]] includes

* [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], _String Scattering Amplitudes and Low Energy Effective Field Theory_, chapter 16 in _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics pp 585-639 Springer 2013

For more see at _[[landscape of string theory vacua]]_.

[[!redirects effective quantum field theories]]

[[!redirects effective QFT]]
[[!redirects effective QFTs]]

[[!redirects UV cutoff]]
[[!redirects UV cutoffs]]

[[!redirects UV cut-off]]
[[!redirects UV cut-offs]]

[[!redirects UV-cutoff]]
[[!redirects UV-cutoffs]]

[[!redirects UV regularization]]
[[!redirects UV regularizations]]

[[!redirects UV-regularization]]
[[!redirects UV-regularizations]]


[[!redirects effective S-matrix]]
[[!redirects effective S-matrices]]

[[!redirects effective S-matrix scheme]]
[[!redirects effective S-matrix schemes]]

[[!redirects effective field theory]]
[[!redirects effective field theories]]


[[!redirects effective low-energy quantum field theory]]
[[!redirects effective low-energy field theory]]


[[!redirects UV-completion]]
[[!redirects UV completion]]
[[!redirects UV-completions]]
[[!redirects UV completions]] 