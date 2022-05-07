
### Transveral Dp-D(p+2)-brane intersections in fuzzy funnels

The [[boundary condition]] in the [[nonabelian DBI model]] of [[coincident brane|coincident]] [[D-branes|Dp-branes]] describing their transversal [[intersecting branes|intersection/ending]] [[Dp-D(p+2)-brane bound states|with/on D(p+2)-branes]] is controled by [[Nahm's equation]] and thus exhibits the [[intersecting branes|brane intersection]]-locus equivalently as:

1. a [[fuzzy funnel]] [[noncommutative geometry]] interpolating between the $\mathrm{D}p$- and the $\mathrm{D}(p+2)$-brane worldvolumes;

1. [[geometric engineering of QFT|geometric engineering]] of [[Yang-Mills monopoles]] in the [[worldvolume]]-theory of the ambient $D(p+2)$-branes.

([Diaconescu 97](Dp-Dpplus2-brane+bound_state#Diaconescu97), 
[Constable-Myers-Fafjord 99](Dp-Dpplus2-brane+bound+state#ConstableMyers99), [Hanany-Zaffaroni 99](Dp-Dpplus2-brane+bound+state#HananyZaffaroni99), [Gaiotto-Witten 08, Section 2.4](Dp-Dpplus2-brane+bound+state#GaiottoWitten08), [HLPY 08](Dp-Dpplus2-brane+bound+state#HLPY08), [GZZ 09](Dp-Dpplus2-brane+bound+state#GZZ09))


More explicitly, for $y \in (0,\infty ]$ the transversal distance along the stack of $N$ $\mathrm{D}p$-branes away from the $\mathrm{D}(p+2)$-brane, and for 

$$
  X^i \in C^\infty\big( (0,\infty], \mathfrak{u}(N) \big)
  \phantom{AAA}
  i \in \{1,2,3\}
$$

the three scalar fields on the worldvolume, the [[boundary condition]] is:

$$
  \frac{d}{d y}
  X^3
  +
  [X^1, X^2]
  \;=\;
  0
  \,,
  \;\;\;
  \frac{d}{d y}
  X^1
  +
  [X^2, X^3]
  \;=\;
  0
  \,,
  \;\;\;
  \frac{d}{d y}
  X^2
  +
  [X^3, X^1]
  \;=\;
  0
$$

as $y \to 0$. These are _[[Nahm's equations]]_, solved by

$$
  X^i(y) = \frac{1}{y} \rho^i + \text{non-singular}
$$

where

$$
  \rho \;\colon\; \mathfrak{su}(2) \longrightarrow \mathfrak{u}(N)
$$

is a Lie algebra homomorphism from [[su(2)]] to the [[unitary Lie algebra]], and

$$
  \rho^i \coloneqq \rho(\sigma^i)
$$

is its complex-linear combination of values on the canonical [[Pauli matrix]] [[linear basis|basis]].

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/FuzzyFunnelFromChordDiagram.jpg" width="420">
</div>


{#FuzzyFunnelEmerges} Equivalently. $\rho$ is an $N$-[[dimension|dimensional]] [[complex numbers|complex]] [[Lie algebra representation]] of [[su(2)]]. Any such is [[reducible representation|reducible]] as a [[direct sum]] of [[irreducible representations]] $\mathbf{N}^{(M5)}$, for which there is exactly one, up to [[isomorphism]], in each dimension $N^{(M5)} \in \mathbb{N}$:

\[
  \label{rhoAsADirectSumOfsu2Irreps}
  \rho 
  \;\simeq\;
  \underset{
    i 
  }{\bigoplus}
  \big(
    N_i^{(M2)}
    \cdot 
    \mathbf{N}_i^{(M5)}
  \big)
  \,.
\]

(Here the notation follows the discussion at _[M2/M5-brane bound states in the BMN model](BMN+matrix+model#M2M5BraneBoundStatesInTheBMNMatrixModel)_, which is the [[duality between M-theory and type IIA string theory|M-theory lift]] of the present situation).



Now each [[irrep]] $\mathbf{N}_i^{(M5)}$ may be interpreted as a [[fuzzy 2-sphere]] of [[radius]] $\propto \sqrt{ \left( N_i^{(M5)}\right)^2 - 1 }$, hence as the section of a [[fuzzy funnel]] at given $y = \epsilon$, whence the totality of (eq:rhoAsADirectSumOfsu2Irreps) represents a system of concentric [[fuzzy 2-spheres]]/[[fuzzy funnels]].

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

\linebreak

Moreover, since the [[complexification]] of [[su(2)]] is the [[sl(2)|complex special linear Lie algebra]] $\mathfrak{sl}(2,\mathbb{C})$ ([here](su2#Complexification)) the solutions to the boundary conditions are also identified with [[finite-dimensional vector space|finite-dimensional]] $\mathfrak{sl}(2,\mathbb{C})$ [[Lie algebra representations]]:

\[
  \label{RhoAsAnsl2Rep}
  \rho \;\in\; \mathfrak{sl}(2,\mathbb{C}) Rep
  \,.
\]

\linebreak

This is what many authors state, but it is not yet the full picture: 

{#ParallelCPField} Also the worldvolume [[Chan-Paton gauge field]] component $A$ along $y$ participates in the brane intersection

$$
  A \in C^\infty\big( (0,\infty], \mathfrak{u}(N) \big)
$$

its boundary condition being that 

$$
  [A, X^i] \;=\; 0
  \phantom{AAAA}
  \text{for all}\; i \in \{1,2,3\}
$$

as $y \to 0$ ([Constable-Myers 99, Section 3.3](Dp-Dpplus2-brane+bound+state#ConstableMyers99), [Thomas-Ward 06, p. 16](Dp-Dpplus2-brane+bound+state#ThomasWard06), [Gaiotto-Witten 08, Section 3.1.1](Dp-Dpplus2-brane+bound+state#GaiottoWitten08))

Together with (eq:RhoAsAnsl2Rep) this means that the quadruple of fields $(X^1,X^2,X^3,A)$ constitutes a [[Lie algebra representation]] of the [[general linear Lie algebra]]

$$
  \mathfrak{gl}(2,\mathbb{C})
  \;\simeq\;
  \underset{
    \langle 
      X^1, X^2, X^3
    \rangle
  }{
  \underbrace{
    \mathfrak{sl}(2,\mathbb{C})
  }
  }
  \oplus
  \underset{
    \langle A \rangle
  }{
    \underbrace{
      \mathbb{C}
    }
  }
$$

This makes little difference as far as bare [[Lie algebra representations]] are concerned, but it does make a crucial difference when these are regarded as [[metric Lie representations]] of [[metric Lie algebras]], since $\mathfrak{gl}(2,\mathbb{C})$ admits further invariant metrics...

\linebreak
