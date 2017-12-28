
#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theories]] various concepts of "renormalization groups" describe the choices of [[renormalization]] and their behaviour under [[scaling transformations]] or choices of cutoffs.

There are at least three different concepts referred to as "the renormalization group", only the first is in general really a [[group]]: 

1. the [[Stückelberg-Petermann renormalization group]]

1. the [[Gell-Mann-Low renormalization cocycle]]

1. the rg group of Wilsonian [[effective field theory]]

(e.g. [Brunetti-Dütsch-Fredenhagen 09, p. 10](#BrunettiDuetschFredenhagen09))

For $(E,\mathbf{L}_{kin})$ a [[free field theory|free]] [[Lagrangian field theory]] on some [[spacetime]] with [[Green hyperbolic differential equations|Green hyperbolic]] [[equations of motion]], the [[renormalization|renormalized]] [[perturbative S-matrix]], in its dependency of a [[adiabatic switching|adiabically switched]] [[interaction]] [[Lagrangian densities]] $g L_{int}$ to do [[perturbative quantum field theory|perturbation theory]] about, a function on the space $\mathcal{F}_{loc}$ of [[formal power series]] in [[Planck's constant]] of [[polynomial observable|polynomial]] [[local observables]], taking values in the [[Wick algebra]] of $(E,L_{int})$:

$$
  S_{L_{int}} \;\colon\;
  \mathcal{F}_{loc} \longrightarrow \mathcal{W}
  \,.
$$


The [[Stückelberg-Petermann renormalization group]] is a group of transformations  

$$
  \array{
    \mathcal{F}_{loc} &\overset{Z}{\longrightarrow}& \mathcal{F}_{loc}
    \\
    \mathbf{L}_{int} &\mapsto& Z(\mathbf{L}_{int})
  }
$$

on the space of [[interaction]] [[local Lagrangian densities]] $\mathbf{L}_{int}$ such that for $S_{\mathbf{L}_{kin}}$ and $S'_{\mathbf{L}_{kin}}$ two [[renormalization|renormalized]] [[perturbative S-matrices]] perturbing around the same given [[Green hyperbolic differential equation|Green hyperbolic]] [[free field theory]] [[Lagrangian field theory]] $(E,\mathbf{L}_{int})$ (hence two different [[renormalization]] schemes) there is a unique $Z$ relatin them, in that

$$
  \label{SMatricesRelatedBySPRenormalizationGroupElement}
  S(\mathbf{L}_{int}) = S' \circ Z(\mathbf{L}_{int}))
$$

for all $L_{int}$. This is the _[[main theorem of perturbative renormalization]]_.

Now it may happen that $\mathbf{L}_{kin} = \mathbf{L}_{kin}(m)$ depends on a [[mass]] parameter and that under [[scaling transformations]] on [[local observables]] ([Dütsch 18, def. 3.19](#Duetsch18)) $\sigma_\rho$ we have that with $S_{L_{kin}(m)}$ a [[perturbative S-matrix]] perturbing around $L_{kin}(m)$ that also

$$
  \sigma_\rho \circ \left(S_{L_{kin}(m/\rho)}\right) \circ \sigma_\rho^{-1}
$$

is a perturbative S-matrix around $L_{kin}(m)$. Therefore in this case the [[main theorem of perturbative renormalization]] implies with (eq:SMatricesRelatedBySPRenormalizationGroupElement) that there exists a unique transformation $Z^m_\rho$ of the space of interaction Lagrangians such that

$$
  \sigma_\rho \circ S_{L_{kin}(m/\rho)} \circ \sigma_\rho^{-1}(\mathbf{L}_{int})
  =
  S_{L_{kin}(m)}(Z^m_\rho(\mathbf{L}_{int}))
$$

for all $\mathbf{L}_{int}$. These $Z^m_\rho$ are the [[Gell-Mann-Low cocycle]] elements. These do not actually form a [[group]], unless $m = 0$, but satisfy the relation

$$
  Z^m_{\rho_1 \rho_2}
  \;=\;
  Z^m_{\rho_1}
    \circ
  \left(
    \sigma_{\rho_1} \circ Z^{m/\rho_1}_{\rho_2} \circ \sigma_{\rho_2}
  \right)
$$

([Brunetti-Dütsch-Fredenhagen 09 (69)](#BrunettiDuetschFredenhagen09), [Dütsch 18 (3.325)](#Duetsch18))

+-- {: .proof}
###### Proof

From the definition we have

$$
  \begin{aligned}
    S_{L_{kin}(m)} \circ Z^m_{\rho_1 \rho_2}
    & =
    \sigma_{\rho_1} 
      \circ 
    \underset{
      S_{L_{kin}(m/\rho_1)} \circ Z^{m/\rho_1}_{\rho_2}
    }{
    \underbrace{
      \sigma_{\rho_2}
        \circ 
      S_{L_{kin}(m/\rho_1\rho_2)}
        \circ 
      \sigma_{\rho_2}^{-1}
    }}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & = 
    \underset{= S_{L_{int}(m)} \circ Z^m_{\rho_1} \circ \sigma_{\rho_1}}{
    \underbrace{
    \sigma_{\rho_1} \circ S_{L_{kin}(m/\rho_1)}
    \circ
    \overset{ = id }{
      \overbrace{
        \sigma_{\rho_1}^{-1} \circ \sigma_{\rho_1}
      }
    }
    }}
      \circ 
    Z^{m/\rho_1}_{\rho_2}
      \circ 
    \sigma_{\rho_1}^{-1}
    \\
    & = 
    S_{L_{int}(m)} \circ Z^m_{\rho_1}
    \circ
    \sigma_{\rho_1} \circ Z^{m/\rho_1}_{\rho_2} \circ \sigma_{\rho_1}^{-1}
  \end{aligned}
$$

Now the claim follows with the fact that the perturbative S-matrix $S_{L_{int}(m)}$, as a function form [[interaction]] [[Lagrangian densities]] to [[Wick algebra]]-elements, is an [[injective function]].

=--

## Related concepts

* [[renormalization]]

* [[asymptotic safety]]

* [[cosmic Galois group]]


## References

The [[Stückelberg-Petermann renormalization group]] is due to

* {#StueckelbergPetermann53} [[Ernst Stückelberg]] and A. Petermann, _La normalisation des constantes dans la theorie des quanta_, Helv. Phys. Acta 26 (1953), 499–520

The relation of the [[Stückelberg-Petermann renormalization group]] to [[scale transformations]] and the [[Gell-Mann-Low renormalization cocycle]] 
* {#GellMannLow54} [[Murray Gell-Mann]] and F. E. Low, _Quantum Electrodynamics at Small Distances_, Phys. Rev. 95 (5) (1954), 1300–1312 ([pdf](http://www.fafnir.phyast.pitt.edu/py3765/GellManLow.pdf))

is due to

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

reviewed in

* {#Duetsch18} [[Michael Dütsch]], section 3.5.1 of _[[From classical field theory
to perturbative quantum field theory]]_, 2018

Review of the Wilsonian picture of RG-flow includes

* {#Abdesselam13} [[Abdelmalek Abdesselam]], _QFT, RG, and all that, for mathematicians, in eleven pages_ ([arXiv:1311.4897](https://arxiv.org/abs/1311.4897))

See also

* Kiyoshi Higashijima, Kazuhiko Nishijima, _Renormalization Groups of Gell-Mann and  Low and of Callan  and Symanzik_, Progress in theoretical physics, vol. 64, no. 6, December 1980 ([pdf](https://academic.oup.com/ptp/article-pdf/64/6/2179/5275368/64-6-2179.pdf))


* {#Shomer07} Assaf Shomer, _A pedagogical explanation for the non-renormalizability of gravity_ ([arXiv:0709.3555](https://arxiv.org/abs/0709.3555))


* Wikipedia _[Renormalization group](http://en.wikipedia.org/wiki/Renormalization_group)_



[[!redirects renormalization groups]]

[[!redirects renormalization group flow]]
[[!redirects renormalization group flows]]
