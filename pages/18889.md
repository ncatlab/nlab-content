
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


+-- {: .num_example #ScalingTransformations}
###### Example
**([[scaling transformations]] on [[observables]])**

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
  \rho \mapsto (E_{\text{BV-BRST}}, \mathbf{L}'_{\rho}, \Delta_{H,\rho} )
$$ 

be a 1-parameter collection of [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacua]] on that field bundle, according to def. \ref{VacuumFree}, and consider a decomposition into a set $Spec$ of field species ([this def.](S-matrix#VerticesAndFieldSpecies)) such that for each $sp \in Spec$ the collection of [[Feynman propagators]] $\Delta_{F,\rho,sp}$ for that species satisfies

$$
  \rho^{ mdim_{sp} }  \Delta_{F, 1/\rho, sp}( \rho x )
  \;=\;
  \Delta_{F,1,sp}(x)
$$

for some $mdim \in \mathbb{R}$, called the _mass dimension_ of the field species $sp$.


Let accordingly

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
    \rho^{-mdim_{sp}} \mathbf{\Phi}^a( \rho^{-1} x )
  }
$$

be the [[function]] on [[off-shell]] [[polynomial observables]] given on [[field observables]] as shown.

=--

([Dütsch 18, def. 3.19](#Duetsch18))




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

* {#Duetsch18} [[Michael Dütsch]], section 3.5.1 of _[[From classical field theory
to perturbative quantum field theory]]_, 2018

[[!redirects Gell-Mann-Low renormalization cocycles]]

[[!redirects Gell-Mann-Low cocycle]]
[[!redirects Gell-Mann-Low cocycles]]

[[!redirects Gell-Mann-Low renormalization group]]
[[!redirects Gell-Mann-Low renormalization groups]]

[[!redirects running coupling constant]]
[[!redirects running coupling constants]]

[[!redirects running of the coupling constant]]
[[!redirects running of the coupling constants]]

