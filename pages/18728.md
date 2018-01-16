
{:summary: .un_remark style="border:solid #000000;background: #ffffff;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: summary}
###### Summary
**[[Feynman diagrams]] in [[causal perturbation theory]]**

In [[perturbative quantum field theory]], **[[Feynman diagrams]]** are labeled [[graphs]] that encode [[product of distributions|products of]] [[Feynman propagators]] as they arise in the expansion -- the _[[Feynman perturbation series]]_-- of the _[[S-matrix]]_ of a given [[interaction]] [[Lagrangian density]] $L_{int}$

$$
  \mathcal{S}
  \left(
    S_{int}
  \right)
  = 
  \underset{k \in \mathbb{N}}{\sum} 
  \frac{1}{k!}
  \frac{1}{(i \hbar)^k}
  T( \underset{k \, \text{factors}}{\underbrace{S_{int}, \cdots S_{int}}} )
$$

in terms of the _[[time-ordered products]]_ $T(\cdots)$ given by the [[star product]] with the [[Feynman propagator]] $\Delta_F$:

$$
  T(S_{int}, \cdots, S_{int}) 
  \;=\; 
  prod \circ \exp
  \left( 
     \hbar 
      \int \Delta_{F}^{a b}(x,y) 
        \frac{\delta}{\delta \mathbf{\Phi}^a(x)} 
          \otimes 
        \frac{\delta}{\delta \mathbf{\Phi}(y)}  
    \right) 
    ( S_{int} \otimes \cdots \otimes S_{int} )
   \,.
$$

Each [[edge]] in the [[Feynman diagram]] [[graph]] corresponds to a factor of a [[Feynman propagator]] $\omega_F$ in $T( \underset{k \, \text{factors}}{\underbrace{L_{int} \cdots L_{int}}} )$, being a [[distribution of two variables]]; and each [[vertex]] corresponds to a factor of the [[interaction]] [[Lagrangian density]] $L_{int}$ evaluated at one of the integration-variables $x_i$. 

For example a typical [[Feynman diagram]] as in [[quantum electrodynamics]], where $L_{int} \propto \underset{\text{fermionic}}{\underbrace{\overline{\psi}}} \underset{\text{bosonic}}{\underbrace{A}} \underset{\text{fermionic}}{\underbrace{\psi}}$ looks as follows (with internal indices notationally suppressed):

<img src="https://ncatlab.org/nlab/files/FeynmanDiagramGlobal.jpg" width="560"/>

Here the [[Feynman propagators]] for [[fermion fields]] $\omega_F(-,-) = \Delta(-,-)$ are drawn as solid lines...

<img src="https://ncatlab.org/nlab/files/FeynmanDiagramComponent1.jpg" width="560"/>

...while the [[Feynman propagators]] $\omega_F(-,-) = G(-,-)$ for [[bosons]] are drawn as wiggly lines:

<img src="https://ncatlab.org/nlab/files/FeynmanDiagramComponentTwo.jpg" width="560"/>

This way each part of the [[Feynman diagram]] [[graph]] corresponds to a [[product of distributions]]:

<img src="https://ncatlab.org/nlab/files/FeynmanDiagramComponentThree.jpg" width="560"/>

> graphics grabbed from  [Brouder 10](Feynman+diagram#Brouder10)

A priori this [[product of distributions]] is defined away from coincident vertices: $x_i \neq x_j$. The definition at coincident vertices $x_i = x_j$ requires a choice of _[[extension of distributions]]_ to the [[diagonal]] locus. This choice is the [[renormalization|("re-")normalization]] of the Feynman diagram.

=--
