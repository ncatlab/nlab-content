

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

In [[perturbative quantum field theories]] various concepts of "renormalization groups" describe the choices of [[renormalization|("re"-)normalization]] and their behaviour under [[scaling transformations]] or choices of cutoffs.

There are at least three different concepts referred to as "the renormalization group", only the first is in general really a [[group]]: 

1. the [[Stückelberg-Petermann renormalization group]] ([Stückelberg-Petermann 53](#StueckelbergPetermann53), historically the origin of the concept)

   this is literally the [[group]] of _re-normalizations_, whose elements relate any two given [[renormalization scheme|normalization schemes]] $\mathcal{S}$ and $\mathcal{S}'$ by [[precomposition]] with a transformation $\mathcal{Z}$ of the space of [[local observable|local]] [[interaction]] [[action functionals]];

1. [[renormalization group flow]], say along [[scaling transformations]] yielding the [[Gell-Mann-Low renormalization cocycle]]

1. the [[Wilsonian RG]] of [[effective quantum field theories]] defined with a [[UV cutoff]].

(e.g. [Brunetti-Dütsch-Fredenhagen 09, p. 10](#BrunettiDuetschFredenhagen09))

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

## Related concepts

* [[renormalization]]

* [[renormalization group flow]]

* [[asymptotic safety]]

* [[cosmic Galois group]]


## References

The [[Stückelberg-Petermann renormalization group]] is due to

* {#StueckelbergPetermann53} [[Ernst Stückelberg]], [[André Petermann]], _La normalisation des constantes dans la theorie des quanta_, Helv. Phys. Acta 26 (1953), 499–520

The relation of the [[Stückelberg-Petermann renormalization group]] to [[renormalization group flow]] ([[Gell-Mann-Low renormalization cocycles]]) 

* {#GellMannLow54} [[Murray Gell-Mann]] and F. E. Low, _Quantum Electrodynamics at Small Distances_, Phys. Rev. 95 (5) (1954), 1300–1312 ([pdf](http://www.fafnir.phyast.pitt.edu/py3765/GellManLow.pdf))

as well as to [[Wilsonian RG]] of [[effective quantum field theories]] is due to

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy.
55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))

reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.5.1 of _[[From classical field theory to perturbative quantum field theory]]_, 2018


See also

* Kiyoshi Higashijima, Kazuhiko Nishijima, _Renormalization Groups of Gell-Mann and  Low and of Callan  and Symanzik_, Progress in theoretical physics, vol. 64, no. 6, December 1980 ([pdf](https://academic.oup.com/ptp/article-pdf/64/6/2179/5275368/64-6-2179.pdf))

* {#Shomer07} Assaf Shomer, _A pedagogical explanation for the non-renormalizability of gravity_ ([arXiv:0709.3555](https://arxiv.org/abs/0709.3555))

* Alessandro Giuliani, Vieri Mastropietro, Slava Rychkov, _Gentle introduction to rigorous Renormalization Group: a worked fermionic example_ ([arXiv:2008.04361](https://arxiv.org/abs/2008.04361))


* Wikipedia _[Renormalization group](http://en.wikipedia.org/wiki/Renormalization_group)_



[[!redirects renormalization groups]]

