

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

In [[scattering theory]] the _Møller operator_ [[intertwiner|intertwines]] the [[observables]] of the [[free field theory|free]] [[theory (physics)|theory]] with those of the [[interaction|interacting]] theory.

## Details

### In quantum mechanics

The [[quantum states]] $\vert \psi(t)\rangle_I$ in the [[interaction picture]] of [[quantum mechanics]] are by definition ([this equation](Dirac+interaction+picture#eq:StateInTheInteractionPicture)) related to the asymptotic free states $\vert\psi\rangle$ by

$$
  \vert \psi(t)\rangle_I
  \;=\;
  \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) 
  \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
  \vert \psi \rangle 
$$

and conversely

$$
  \vert \psi \rangle 
  \;=\;
  \underbrace{
    \exp\left({\tfrac{- t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
    \exp\left({\tfrac{+ t}{i \hbar} H_{free}}\right) 
  }
  \vert \psi(t)\rangle_I
$$

the suitable [[limit of a sequence|limit]] for $t \to \mp \infty$ of the operator under the brace is called the _Møller operator_ 

$$
  \Omega{\pm}
  \;\coloneqq\;
  \underset{t \to \mp \infty}{\lim}
    \exp\left({\tfrac{- t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)
    \exp\left({\tfrac{+ t}{i \hbar} H_{free}}\right) 
$$

(e.g. [BEM 01](#BEM01))

### In quantum field theory

In [[perturbative quantum field theory]] the maps that intertwine the [[Wick algebra]] of [[quantum observables]] of the [[free field theory]] with the [[interacting field algebra]] are, on [[regular polynomial observables]]. the [[derivatives]] of the [[Bogoliubov formula]] of the given [[S-matrix]] $\mathcal{S}$ for the given [[interaction]] $S_{int}$ with respect to [[source fields]]:

$$
  \mathcal{R}(-)
    \;\coloneqq\;
  \mathcal{S}(S_{int})^{-1} 
    \star_H 
  (\mathcal{S}(S_{int}) \star_F (-))
$$

(Here $\star_H$ denotes the [[star product]] induced by the [[Wightman propagator]], hence the [[Wick algebra]]-product, while $\star_F$ denotes the [[star product]] induced by the [[Feynman propagator]], hence the [[time-ordered product]]. The [[inverse]] $(-)^{-1}$ is taken with respect to $\star_H$.)

This $\mathcal{R}(-)$ is referred to as the _quantum Møller operator_ in ([Hawkins-Rejzner 16, below def. 5.1](#HawkinsRejzner16)). (But notice that in many previous articles in [[perturbative AQFT]], by the same authors and by others, the very same operator is referred to just as the "intertwining operator", or similar.)

## Related concepts

* [[quantum master equation]]

## References

Discussion in [[quantum mechanics]]:

* {#BEM01} A. Baute, I. Egusquiza, J. Muga, _Møller operators and Lippmann-Schwinger equations for step-like potentials_ ([arXiv:quant-ph/0104043](https://arxiv.org/abs/quant-ph/0104043))

Discussion in [[relativistic field theory|relativistic]] [[perturbative quantum field theory]] in the rigorous formulation of [[causal perturbation theory]]/[[perturbative AQFT]]:

* {#HawkinsRejzner16} [[Eli Hawkins]], [[Kasia Rejzner]], _The Star Product in Interacting Quantum Field Theory_ ([arXiv:1612.09157](https://arxiv.org/abs/1612.09157))


[[!redirects Møller operators]]


[[!redirects quantum Møller operator]]
[[!redirects quantum Møller operators]]

[[!redirects Moller operator]]
[[!redirects Moller operators]]

[[!redirects quantum Moller operator]]
[[!redirects quantum Moller operators]]


