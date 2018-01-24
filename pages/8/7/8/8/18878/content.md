

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

In [[perturbative quantum field theory]] the _Stückelberg-Petermann renormalization group_ ([Stückelberg-Petermann 53](#StiecelbergPetermann53)) is the (original) incarnation of the [[renormalization group]] in the perspective of [[causal perturbation theory]]: It is a group of formal deformations of [[interaction]] [[Lagrangian densities]] which is such that any two choices of [[renormalization|renormalized]] perturbative [[S-matrices]] differ by precomposition with a unique group element. This is the statement of the [[main theorem of perturbative renormalization]].

A priori the Stückelberg-Petermann renormalization group is not about [[scaling transformations]]. But if [[scaling transformations]] happen to produce new S-matrices/renormalization schemes from given ones, then the [[main theorem of perturbative renormalization]] induces for each such scaling transformation a re-definition of interaction Lagrangian densities, this is the [[Gell-Mann-Low renormalization cocycle]] ([Gell-Mann & Low 54](#GellMannLow54), [Brunetti-Dütsch-Fredenhagen 09](#BrunettiDuetschFredenhagen09)) for review see ([Dütsch 18, section 3.5.3](#Duetsch18)).
In more detail:

Let 

$$
  vac 
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}_{kin}, \Delta_H )
$$ 

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]].

Then a [[perturbative S-matrix]] scheme/[[renormalization scheme|("re"-)normalization scheme]] around this vacuum ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering)) is a function

$$
  \array{
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g, j \rangle
      & \overset{\mathcal{S}_{vac}}{\longrightarrow} &
    PolyObs(E_{\text{BV-BRST}})_{mc}( ( \hbar ) )[ [ g, j ] ]
    \\
    g S_{int} + j A
     &\mapsto&
    \mathcal{S}_{vac}(g S_{int} + j A)
  }
$$

from [[local observables]], regared as [[adiabatic switching|adiatically switched]] [[interaction]] [[action functionals]]  to [[Wick algebra]]-elements $\mathcal{S}( g S_{int} + j A)$, encoding [[scattering amplitudes]] in the given vacuum $\mathbf{L}'$ for the given interaction $g S_{int} + j A$, with formal parameters adjoined as indicated.

The _[[Stückelberg-Petermann renormalization group]]_ is a group of transformations

$$
  \array{
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j \rangle
      &\overset{Z}{\longrightarrow}& 
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g, j \rangle
    \\
    g S_{int} + J A
      &\mapsto& 
    \mathcal{Z}(g S_{int} + j A)
  }
$$

such that for $\mathcal{S}$ and $\mathcal{S}'$ two [[renormalization schemes|normalization schemes]]/[[S-matrix]] schemes, there is a unique $\mathcal{Z}$ relating them by [[precomposition]], in that

$$
  \label{SMatricesRelatedBySPRenormalizationGroupElement}
  \mathcal{S}(g S_{int} + j A)
    \;=\; 
  \mathcal{S}'\left( \mathcal{Z}(g S_{int} + j A) \right)
$$

for all $g S_{int} + j A$. This is the _[[main theorem of perturbative renormalization]]_. Hence this says that any two ways of choosing [[interactions]] at coincident interaction points are related by a re-definition of the original [[interaction]] $g S_{int} + j A$.

Now it may happen that 

1. the [[free field]] [[vacuum]] $vac = vac(m)$ depends on a [[mass]] parameter, and with it the choice $\mathcal{S}_{vac(m)}$ of [[renormalization scheme|normalization scheme]], 

1. under [[scaling transformations]] on [[local observables]] $\sigma_\rho$ ([Dütsch 18, def. 3.19](#Duetsch18))  we have that with $\mathcal{S}_{vac(m)}$ a [[perturbative S-matrix]] scheme perturbing around $vac(m)$ also

   $$
     \sigma_\rho \circ \left(\mathcal{S}_{vac(m/\rho)}\right) \circ \sigma_\rho^{-1}
   $$

   is a perturbative S-matrix around $L_{kin}(m)$. 

In this case the above statement of the [[main theorem of perturbative renormalization]] implies with (eq:SMatricesRelatedBySPRenormalizationGroupElement) that there exists a unique transformation $\mathcal{Z}^m_\rho$ of the space of [[local observable|local]] [[interaction]] [[action functionals]] such that

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

for all $g S_{int} + j A$. 

These $\mathcal{Z}^m_\rho$ are the _[[Gell-Mann-Low cocycle]]_ elements. They do not actually form a [[group]], unless $m = 0$, but satisfy the relation

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


## Related cocepts

* [[main theorem of perturbative renormalization]]

## References

The original article on the Stückelberg-Petermann renormalization group is

* {#StueckelbergPetermann53} [[Ernst Stückelberg]], [[André Petermann]], _La normalisation des constantes dans la theorie des quanta_, Helv. Phys. Acta 26 (1953), 499–520

The relation of the Stückelberg-Petermann renormalization group to [[scale transformations]] and the [[Gell-Mann-Low renormalization cocycle]] is due to

* {#GellMannLow54} [[Murray Gell-Mann]] and F. E. Low, _Quantum Electrodynamics at Small Distances_, Phys. Rev. 95 (5) (1954), 1300–1312 ([pdf](http://www.fafnir.phyast.pitt.edu/py3765/GellManLow.pdf))

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

Review includes

* {#Duetsch18} [[Michael Dütsch]], section 3.5.1 of _[[From classical field theory to perturbative quantum field theory]]_, 2018


See also

* {#Duetschfredenhagen07} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Action Ward Identity and the Stückelberg-Petermann renormalization group_, Prog. Math. 251:113-124,2007



[[!redirects Stueckelberg-Pe]]