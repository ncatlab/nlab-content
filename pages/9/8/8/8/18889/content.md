
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

