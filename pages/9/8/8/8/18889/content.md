
> under construction

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

In [[perturbative quantum field theory]] the _Gell-Mann-Low renormalization cocycle_ or "running of the [[coupling constants]]" describes [[interaction vertex redefinitions]] in dependence of [[scale transformations]] on [[spacetime]] which relate corespondingly rescaled [[renormalization schemes]] to each other.


## Definition

A priori the [[Stückelberg-Petermann renormalization group]] is not about [[scaling transformations]]. But if [[scaling transformations]] happen to produce new S-matrices/renormalization schemes from given ones, then the [[main theorem of perturbative renormalization]] induces for each such scaling transformation a re-definition of interaction Lagrangian densities, this is the [[Gell-Mann-Low renormalization cocycle]] ([Gell-Mann & Low 54](#GellMannLow54), [Brunetti-Dütsch-Fredenhagen 09](#BrunettiDuetschFredenhagen09)) for review see ([Dütsch 18, section 3.5.3](#Duetsch18)).


### Renormalization group flow

+-- {: .num_prop #FlowRenormalizationGroup}
###### Proposition
**([[renormalization group flow]])**

Let

$$
  vac
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]].

Consider a [[group]] $RG$ equipped with an [[action]] on the [[Wick algebra]] of [[off-shell]] [[microcausal polynomial observables]]

$$
  rg_{(-)}
  \;\colon\;
  RG \times PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ]
  \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ \hbar, g, j ] ]
  \,,
$$

hence for each $\rho \in RG$ a [[continuous linear map]] $rg_\rho$ which is an [[automorphism]] of the [[Wick algebra]]-product

$$
  rg_\rho( A_1 \star_H A_2 )
  \;=\;
  rg_\rho(A_1) \star_H rg_\rho(A_2)
$$

such that moreover

1. the action preserves the subspace of [[off-shell]] polynomial [[local observables]]

   $$
     rg_{(-)}
     \;\colon\;
     RG \times LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g,j\rangle
     \longrightarrow
     LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g,j\rangle
   $$

1. the action respects the [[causal order]] of the spacetime support of
   local observables, in that for $O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]$

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

Then [[conjugation]] by this action induces an [[action]] on the [[set]] of [[S-matrix]] [[renormalization schemes]],
in that for

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar , g, j] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})( (\hbar) )[ [ g, j] ]
$$

a perturbative [[S-matrix scheme]] around the given [[free field theory|free field]] [[vacuum]], also the [[composition|composite]]

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

be a collection of [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]]
parameterized by elements $\rho \in RG$,
all with the same underlying [[field bundle]]; and
consider $rg_\rho$ as above, except that it is not an [[automorphism]] of any [[Wick algebra]],
but an [[isomorphism]] between the [[Wick algebra]]-structures on various vacua, in that

$$
  rg_{\rho_1}( A_1 \star_{H, \rho_2} A_2 )
  \;=\;
  rg_{\rho_1}(A_1) \star_{H, \rho_1 \rho_2} rg_{\rho_2}(A_2)
$$

for all $\rho_1, \rho_2 \in RG$

Then if

$$
  \{ \mathcal{S}_{vac_\rho} \}_{\rho \in RG}
$$

is a collection of [[S-matrix schemes]], one around each of the [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]]
$vac_\rho$, it follows that for each $\rho \in RG$ the [[composition|composite]]

$$
  \mathcal{S}_{vac_e}^\rho
  \;\coloneqq\;
  \rg_\rho \circ \mathcal{S}_{vac_{\rho^{-1}}} \circ rg_\rho^{-1}
$$

is an S-matrix scheme around the vacuum $vac_e$ (labeled by the [[neutral element]] of $RG$).

=--

+-- {: .proof}
###### Proof

It is clear from the definition that $\mathcal{S}_\rho$ satisfies the axiom "perturbation" (in [this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering))

In order to verify the axiom "[[causal additivity]]", 
observe, for convenience, that by [this example](S-matrix#TimeOrderedProductsFromSMatrixScheme) it is sufficient to check [[causal factorization]]. 

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
  \mathcal{S}_{vac_e}^{\rho}(O_1 + O_2)
  =
  \mathcal{S}_{vac_e}^\rho(O_1) \star_{H,e} \mathcal{S}_{vac_e}^\rho(O_2)
$$

for all $\rho \in RG$

Using the defining properties of $rg_{(-)}$ and the [[causal factorization]] of $\mathcal{S}$
we directly compute as follows:



$$
  \begin{aligned}
    \mathcal{S}_{vac_e}^\rho(O_1 + O_2)
    & =
    rg_\rho \circ \mathcal{S}_{vac_{\rho^{-1}}} \circ rg_\rho^{-1}( O_1 + O_2 )
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{vac_{\rho^{-1}}}(rg_\rho^{-1}(O_1)) + rg_\rho^{-1}(O_2)
      {\, \atop \,}
    \right)
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{\rho^{-1}}(rg_\rho^{-1}(O_1))
        \star_{H,\rho^{-1}}
      \mathcal{S}_{vac_{\rho^{-1}}}(rg_\rho^{-1}(O_2))
      {\, \atop \,}
    \right)
    \\
    & =
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{vac_{\rho^{-1}}}(rg_{\rho^{-1}}(O_1)
      {\, \atop \,}
    \right)
    \star_{H,e}
    rg_\rho
    \left(
      {\, \atop \,}
      \mathcal{S}_{vac_{\rho^{-1}}}(rg_\rho^{-1}(O_2))
      {\, \atop \,}
    \right)
    \\
    & =
    \mathcal{S}^\rho_{vac_e}( O_1 )\, \mathcal{S}^\rho_{vac_e}(O_2)
    \,.
  \end{aligned}
$$

Since therefore each element $\rho \in RG$ in the [[group]] $RG$ picks a different choice of [[renormalization|normalization]]
of the [[S-matrix]] scheme around $vac_e$, we call the assignment $\rho \mapsto \mathcal{S}_\rho$
a _[[renormalization group flow|re-normalization group flow]]_.


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

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]], let $\mathal{S}$ be an [[S-matrix]] scheme
around this vacuum and let $rg_{(-)}$ be a [[renormalization group flow]] according to prop. \ref{FlowRenormalizationGroup}, such that each re-normalized [[S-matrix scheme]] $\mathcal{S}_\rho$ satisfies the [[renormalization condition]] "field independence".

Then by the [[main theorem of perturbative renormalization]] there is for every [[pair]] $\rho_1, \rho_2 \in RG$ a unique [[interaction vertex redefinition]] $\mathcal{Z}_{\rho_1}^{\rho_2}$ which relates the correspond to [[S-matrix]] schemes via

$$
  \mathcal{S}_{\rho_2}
  \;=\;
  \mathcal{S}_{\rho_1}
    \circ
  \mathcal{Z}_{\rho_1}^{\rho_2}
  \,.
$$

If one thinks of an [[interaction]] vertex, hence a [[local observable]] $g S_{int}+ j A$ as specified by the ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] $g$ multiplying the corresponding [[interaction]] [[Lagrangian densities]] $\mathbf{L}_{int}$ in

$$
  g S_{int}
  =
  \underset{j}{\sum} \tau_\Sigma \left( g_j \mathbf{L}_{int,j} \right)
$$

(where $\tau_\Sigma$ denotes [[transgression of variational differential forms]]) then $\mathcal{Z}_{\rho_1}^{\rho_2}$ exhibits a dependency of the ([[adiabatic switching|adiabatically switched]]) [[coupling constants]] $g_j$ of the [[renormalization group flow]] parameterized by $\rho_1, \rho_2$. One speaks of _[[running coupling constants]]_.

=--

### Scaling transformations

> under construction

+-- {: .num_example #ScalingTransformations}
###### Example
**([[scaling transformations]] and [[mass dimension]])**

Let

$$
  E \overset{fb}{\longrightarrow} \Sigma
$$

be a [[field bundle]] which is a [[trivial vector bundle]] over [[Minkowski spacetime]].

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

for the operation of multiplication by $\rho$ using the [[real vector space]]-[[structure]] of the [[Cartesian space]] $\mathbb{R}^{p+1}$.

By [[pullback of differential forms|pullback]] this acts on [[field histories]] by

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
  vac(\rho)
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}'_{\rho}, \Delta_{H,\rho} )
$$

be a 1-parameter collection of [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacua]] on that field bundle, according to [this def.](S-matrix#VacuumFree), and consider a decomposition into a set $Spec$ of field species ([this def.](S-matrix#VerticesAndFieldSpecies)) such that for each $sp \in Spec$ the collection of [[Feynman propagators]] $\Delta_{F,\rho,sp}$ for that species _scales homogeneously_ in that there exists

$$
  dim(sp) \in \mathbb{R}
$$

such that for all $\rho$ we have

$$
  \rho^{ 2 dim(sp) }  \Delta_{F, 1/\rho, sp}( \rho x )
  \;=\;
  \Delta_{F,sp, \rho = 1}(x)
  \,.
$$

Typically $\rho$ rescales the [[mass]] parameter and then $dim(sp)$ is called the _[[mass dimension]]_ of the field species $sp$.

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

be the [[function]] on [[off-shell]] [[polynomial observables]] given on [[field observables]] as shown.

=--

([Dütsch 18, def. 3.19](#Duetsch18))

+-- {: .num_example}
###### Example
**([[mass dimension]] of [[scalar field]])**

The [[Feynman propagator]] of the [[real scalar field]] on [[Minkowski spacetime]] is ([this prop.](Feynman+propagator#FeynmanPropagatorAsACauchyPrincipalvalue))

$$
  \begin{aligned}
  \Delta_{F,\rho}(x)
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{+i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu x^\mu}
  }{
    - k_\mu k^\mu - \left( \rho \tfrac{m c}{\hbar} \right)^2 \pm i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \end{aligned}
$$

hence

$$
  \begin{aligned}
  \Delta_{F,\rho^{-1}}(\rho x)
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
  \Delta_{F,1}(x)
  \end{aligned}
$$

Hence the mass dimension of the real scalar field on $p+1$-dimensional [[Minkowski spacetime]] is

$$
  dim(\text{scalar field})
  \;=\;
  (p+1)/2 - 1
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Let $\rho \mapsto vac(\rho)$ be a 1-paramter collection of [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacua]] according to def. \ref{ScalingTransformations}.

Then for each pair

$$
  A_1, A_2 \;\in\; PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]
$$

of [[polynomial observables]] such that their [[star product]] induced by the [[Feynman propagator]] $\Delta_{F,\rho}$ is defined for all $\rho$, it satisfies

$$
  \sigma_\rho
  \left(
    A_1
     \star_{F,1/\rho}
     \cdots
     \star_{F, 1/\rho}
     A_n
  \right)
  \;=\;
  \left(
    \sigma_\rho A_1
  \right)
    \star_{F,1}
    \cdots
    \star_{F,1}
  \left(
    \sigma_\rho A_n
  \right)
  \,.
$$

In particular the unique [[S-matrix]] [[renormalization scheme|("re"-)normalization scheme]] away from coinciding interaction points ([this prop.](S-matrix#TimeOrderedProductAwayFromDiagonal)) satisfies

$$
  \sigma_\rho \circ T_{k, 1/\rho} \circ \sigma_\rho^{-1}
  \;=\;
  T_{k, \rho = 1}
  \phantom{AAA}
  \text{away from fat diagonal}
$$


$$
  \sigma_\rho \circ \mathcal{S}_{1/\rho} \circ \sigma_\rho^{-1}
  \;=\;
  \mathcal{S}_{\rho = 1}
  \phantom{AAA}
  \text{away from fat diagonal}
$$

=--

+-- {: .proof}
###### Proof

It is sufficient to check this on the contraction of a pair of [[field observables]]:

$$
  \begin{aligned}
    \sigma_\rho (\mathbf{\Phi}(x))
     \star_{F,1}
    \sigma_\rho (\mathbf{\Phi}(y)
    & =
    \rho^{-2 dim }
    \mathbf{\Phi}(\rho^{-1} x)
      \star_{F,1}
    \mathbf{\Phi}(\rho^{-1} y)
    \\
    & =
    \rho^{-2 dim }
    \Delta_{F,1}(\rho^{-1}(x-y))
    \\
    & =
    \sigma_\rho
    \left(
      \Delta_{F, \rho}(x,y)
    \right)
  \end{aligned}
$$

=--

consider the massless case:

$$
  supp(O_1) {\vee\!\!\!\wedge} supp(O_2)
$$

then

$$
  \begin{aligned}
    \sigma_\rho \circ \mathcal{S} \circ \sigma_\rho^{-1}( O_1 + O_2 )
    & =
    \sigma_\rho \mathcal{S}(\sigma_\rho^{-1}(O_1) + \sigma_\rho^{-1}(O_2))
    \\
    & =
    \sigma_\rho \left(
      \mathcal{S}(\sigma_\rho^{-1} O_1)
      \star_{H}
      \mathcal{S}(\sigma_\rho^{-1} O_2)
    \right)
    \\
    & =
    \sigma_\rho \left(
      \mathcal{S}(\sigma_\rho^{-1} O_1)
    \right)
      \star_{H}
    \sigma_\rho\left(
      \mathcal{S}(\sigma_\rho^{-1} O_2)
    \right)
  \end{aligned}
$$

### Running couplings


+-- {: .num_defn #GellMannLowTransformations}
###### Definition
**([[running coupling constants]] under [[scale transformations]])**

Let

$$
  vac
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}_{kin}, \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]].

Assume that in fact

1. the [[free field]] [[vacuum]] $vac = vac(m)$ depends on a [[mass]] parameter, and with it the choice $\mathcal{S}_{vac(m)}$ of [[renormalization scheme|normalization scheme]],

1. under [[scaling transformations]] on [[local observables]] $\sigma_\rho$ (def. \ref{ScalingTransformations}) we have that with $\mathcal{S}_{vac(m)}$ a [[perturbative S-matrix]] scheme perturbing around $vac(m)$ also

   $$
     \sigma_\rho \circ \left(\mathcal{S}_{vac(m/\rho)}\right) \circ \sigma_\rho^{-1}
   $$

   is a perturbative S-matrix around $L_{kin}(m)$.

In this case the [[main theorem of perturbative renormalization]] ([this prop.](Stückelberg-Petermann+renormalization+group#AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition)) says that there exists for each scale $\rho$ a unique
[[interaction vertex redefinition]] $\mathcal{Z}^m_\rho$ (def. \ref{InteractionVertexRedefinition}) such that

$$
  \begin{aligned}
    &
    \sigma_\rho
      \circ
    \mathcal{S}_{vac(m/\rho)}
      \circ
    \sigma_\rho^{-1}( g S_{int} + j A )
    \\
    & =
    \mathcal{S}_{vac(m)}(\mathcal{Z}^m_\rho(g S_{int} + j A))
  \end{aligned}
$$

for all [[interaction]] [[action functionals]] $g S_{int} + j A$.

These $\mathcal{Z}^m_\rho$ are the _[[Gell-Mann-Low renormalization cocycle]]_ elements.

The [[interaction vertex redefinitions]] $\mathcal{Z}^m_\rho$ as a function of the [[rescaling]]
is known as the _[[running coupling constants]]_.

=--

+-- {: .num_prop}
###### Proposition
**(cocycle property of [[running coupling constants]])**

In the situation of def. \ref{GellMannLowTransformations}, the [[Gell-Mann-Low renormalization cocycles]] ([[running coupling constants]])
$\mathcal{Z}^m_\rho$ satisfy the relation

$$
  \mathcal{Z}^m_{\rho_1 \rho_2}
  \;=\;
  \mathcal{Z}^m_{\rho_1}
    \circ
  \left(
    \sigma_{\rho_1}
      \circ
    \mathcal{Z}^{m/\rho_1}_{\rho_2}
      \circ
    \sigma_{\rho_2}
  \right)
$$

Hence only for vaishing [[mass]] do these "renormalization cocycles" themselves form an actual [[renormalization group]].

=--

([Brunetti-Dütsch-Fredenhagen 09 (69)](#BrunettiDuetschFredenhagen09), [Dütsch 18 (3.325)](#Duetsch18))

+-- {: .proof}
###### Proof

From the definition we have

$$
  \begin{aligned}
    \mathcal{S}_{vac(m)}
      \circ
    \mathcal{Z}^m_{\rho_1 \rho_2}
    & =
    \sigma_{\rho_1}
      \circ
    \underset{
      \mathcal{S}_{vac(m/\rho_1)}
        \circ
      \mathcal{Z}^{m/\rho_1}_{\rho_2}
    }{
    \underbrace{
      \sigma_{\rho_2}
        \circ
      \mathcal{S}_{vac(m/\rho_1\rho_2)}
        \circ
      \sigma_{\rho_2}^{-1}
    }}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & =
    \underset{
      =
      \mathcal{S}_{vac(m)}
        \circ
      \mathcal{Z}^m_{\rho_1}
        \circ
      \sigma_{\rho_1}
    }{
    \underbrace{
      \sigma_{\rho_1}
        \circ
      \mathcal{S}_{vac(m/\rho_1)}
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
    \mathcal{Z}^{m/\rho_1}_{\rho_2}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & =
    \mathcal{S}_{vac(m)}
      \circ
    \mathcal{Z}^m_{\rho_1}
      \circ
    \sigma_{\rho_1}
      \circ
    \mathcal{Z}^{m/\rho_1}_{\rho_2}
      \circ
    \sigma_{\rho_1}^{-1}
  \end{aligned}
$$

To conclude, it is now sufficient to see that the perturbative S-matrix $S_{vac(m)}$, as a function form [[interaction]] [[Lagrangian densities]] to [[Wick algebra]]-elements, is an [[injective function]]. (...)

=--

## References


* {#GellMannLow54} [[Murray Gell-Mann]] and F. E. Low, _Quantum Electrodynamics at Small Distances_, Phys. Rev. 95 (5) (1954), 1300–1312 ([pdf](http://www.fafnir.phyast.pitt.edu/py3765/GellManLow.pdf))

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.5.3 of _[[From classical field theory
to perturbative quantum field theory]]_, 2018

[[!redirects Gell-Mann-Low renormalization cocycles]]

[[!redirects Gell-Mann-Low cocycle]]
[[!redirects Gell-Mann-Low cocycles]]

[[!redirects Gell-Mann-Low renormalization group]]
[[!redirects Gell-Mann-Low renormalization groups]]

[[!redirects mass dimension]]
[[!redirects mass dimensions]]

[[!redirects running coupling constant]]
[[!redirects running coupling constants]]

[[!redirects running of the coupling constant]]
[[!redirects running of the coupling constants]]

