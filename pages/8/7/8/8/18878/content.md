

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


## Definition


+-- {: .num_defn #InteractionVertexRedefinition}
###### Definition
**([[perturbative interaction vertex redefinition]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)).

A _[[perturbative interaction vertex redefinition]]_ or just _[[vertex redefinition]]_, for short is and [[endofunction]]

$$
  \mathcal{Z}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle  
$$

on [[local observables]] with formal parameters adjoined ([this def.](S-matrix#FormalParameters)) such that there exists a sequence $\{Z_k\}_{k \in \mathbb{N}}$ of [[continuous linear functional]], symmetric in their arguments, of the form

$$
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [ \hbar, g, j] ]}}
  \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

such that for all $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle$ we have

1. $Z_0(g S_{int + j A}) = 0$

1. $Z_1(g S_{int} + j A) = g S_{int} + j A$

1. and

   $$
     \begin{aligned}
       \mathcal{Z}(g S_{int} + j A)
       & =
       Z \exp_\otimes( g S_{int} + j A )
       \\
       & =
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

=--

The following proposition should be compared to the axiom of _[[causal additivity]]_ of the [[S-matrix]] scheme ([this equation](S-matrix#eq:CausalAdditivity)).

+-- {: .num_prop #InteractionVertexRedefinitionAdditivity}
###### Proposition
**(local additvity of [[vertex redefinitions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)) and let $\mathcal{Z}$ be a [[vertex redefinition]] (def. \ref{InteractionVertexRedefinition}).

Then for all $O_0, O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g, j\rangle$ we have

$$
  \begin{aligned}
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

=--

([Dütsch 18, exercise 3.98 (a)](#Duetsch18))

+-- {: .proof}
###### Proof

Under the inclusion

$$
  LocObs(E_{\text{BV-BRST}})
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})
$$

of [[local observables]] into [[polynomial observables]] we may think of each $Z_k$ as a [[generalized functions]], just as for [[time-ordered products]] in [this remark](S-matrix#NotationForTimeOrderedProductsAsGeneralizedFunctions). 

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

But now since $Z_k$ in fact takes values just in the subspace of local observables, the support of these generalized functions in the [[integrand]] here must be on the [[diagonal]], where $x_1 = \cdots = x_k$.

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
    Z_k\left( {\, \atop \,} (O_0 + O_1), \cdots, (O_0 + O_1) {\, \atop \,} \right)
  \end{aligned}
  \,.
$$

This directly implies the claim.

=--

+-- {: .num_cor}
###### Corollary

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)) and let $\mathcal{Z}$ be a [[vertex redefinition]] (def. \ref{InteractionVertexRedefinition}).

Then for

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

and [[S-matrix]] scheme ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering)), also the [[composition|composite]]
$$
  \mathcal{S} \circ \mathcal{Z}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \overset{\mathcal{Z}}{\longrightarrow}
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \overset{\mathcal{S}}{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

is an S-matrix scheme.

=--

+-- {: .proof}
###### Proof

The condition "perturbation" is immediate from the definitions and the usual combinatorics of [[exponential series]].

The condition "[[causal additivity]]" for $\mathcal{S} \circ \mathcal{Z}$ follows directly from the causal additivity of $\mathcal{S}$ and the local additivity of $\mathcal{Z}$ (prop. \ref{InteractionVertexRedefinitionAdditivity}).

=--



## Properties

### Relation to scaling transformations

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

[[!redirects Stückelberg-Petermann renormalization groups]]

[[!redirects Stueckelberg-Petermann renormalization group]]
[[!redirects Stueckelberg-Petermann renormalization groups]]

[[!redirects perturbative interaction vertex redefinition]]
[[!redirects perturbative interaction vertex redefinitions]]

[[!redirects interaction vertex redefinition]]
[[!redirects interaction vertex redefinitions]]

[[!redirects vertex redefinition]]
[[!redirects vertex redefinitions]]


