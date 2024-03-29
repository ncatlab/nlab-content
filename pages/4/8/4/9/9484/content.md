
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometric quantum theory
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[physics]], a _semiclassical state_ is the approximation to a [[quantum state]] in [[semiclassical approximation]].

In the original sense of the [[WKB approximation]], in the [[Schrödinger picture]] a semiclassical state is a [[wave function]] which solves the [[Schrödinger equation]] to first order in [[Planck's constant]] $\hbar$.

In the broader formalization of quantum physics in [[symplectic geometry]]/[[geometric quantization]] one finds that such WKB semiclassical states are formalized as being [[Lagrangian submanifolds]] of the given [[phase space]] [[symplectic manifold]] equipped with with a [[half-density]].

## Definition

We first give the traditional definition of semiclassical states according to the [[WKB method]] for a non-relativistic [[particle]] propagating on the [[Euclidean space]] $\mathbb{R}^n$ with its standard [[kinetic action]] and some arbitrary [[force]] potential

* [Of a non-relativistic particle in a potential](#TraditionalInSchr&#246;dingerPicture)

Then we discuss the formalization of this in the broader context of [[symplectic geometry]]/[[geometric quantization]] in 

* [In symplectic geometry](#InSymplecticGeometry)



### Semiclassical state of the non-relativistic particle in a potential
 {#TraditionalInSchr&#246;dingerPicture}


Consider the [[physical system]] given by a non-relativistic [[particle]] of [[mass]] $m$ propagating on the [[Cartesian space]] $\mathbb{R}^n$ with standard [[kinetic action]] and sunbject to a [[force]] induced by a given potential [[smooth function]] $V \colon \mathbb{R}^n \to \mathbb{R}$.

#### As a wave function

The [[Hamilton operator]] for this system is the standard

$$
  \hat H \coloneqq 
  -
  \frac{\hbar^2}{2 m} \Delta  + V
  \,,
$$

where 

$$
  \Delta = \mathbf{d}^\dagger \mathbf{d}  =   \sum_{i = 1}^n \frac{\partial}{\partial x^i} \frac{\partial}{\partial x^i}
$$

is the [[Laplace operator]] on $\mathbb{R}^n$ regarded as a [[Riemannian manifold]] with its canonical flat [[metric]] ($\mathbf{d}$ is the [[de Rham differential]]).


Then for 

$$
  \psi \colon \mathbb{R}^n \times \mathbb{R} \to \mathbb{C}
$$

a smooth 1-parameter collection of [[smooth functions]] (of [[wave functions]]), the [[Schrödinger equation]] is

$$
  i \hbar \frac{d}{ dt} \psi 
  = 
  \hat H \psi
  \,,
$$

where $\frac{d}{d t}$ is the [[differentiation]] with respect to the additional parameter ([[time]]).

We say that $\psi$ is a _stationary solution_ to the Schr&#246;dinger equation if it is a solution of the form

$$
  \psi(x, t) = \phi(x)\exp(- i \omega t)
$$

for some $\omega \in \mathbb{R}$. For the following it is useful to decompose the remaining [[complex number|complex]]-valued [[smooth function]] 

$$
  \phi \colon \mathbb{R}^n \to \mathbb{C} 
$$

into its modulus and phase by writing it as

$$
  \phi(x)  = \exp(i S(x)/\hbar) a(x)
$$

for two smooth functions $S \colon \mathbb{R}^n \to \mathbb{R}$ and $a \colon \mathbb{R}^n \to \mathbb{R}_{\geq 0}$. 

In fact it is often useful (such as in the symplecto-geometric interpretation that we turn to [below](#InSymplecticGeometry)) to restrict attention to non-vanishing solutions (or else to solutions restricted to their [[support]]) in which case we can regard $\phi$ as a function of the form

$$
  \phi \colon \mathbb{R}^n \to \mathbb{C}^\times \simeq U(1) \times \mathbb{R}_{\gt 0}
$$

and then this decomposition is unique up to a global global offset of $S$ by $2\pi i \cdot n$ for  $n \in \mathbb{Z}$.

In terms of this decomposition the [[Schrödinger equation]] becomes

$$
  \begin{aligned}
    0
    &= 
    \left(i \hbar \frac{d}{dt} - \hat H\right) \psi
    \\
    & =
    \left(
      \left(
        \frac{{\vert \mathbf{d} S \vert}^2 }{2 m }
        + 
        (V - \hbar \omega)
      \right)
      -
      \frac{i \hbar}{ 2m a}
      \mathbf{d}^\dagger \left(a^2 \mathbf{d} S\right)
    \right)
    \exp( i S / \hbar ) a
    +
    \mathcal{O}(\hbar^2 )
  \end{aligned}
  \,,
$$

where $\mathbf{d} S$ is the [[gradient]] [[covector field]] of $S$, where $\mathbf{d}^\dagger ( a^2 \mathbf{d}S)$ is the [[divergence]] of $a ^2 \mathbf{d}S$, and where $\mathcal{O}(\hbar^2)$ denotes all further terms that are non-linear in $\hbar$.

This means that $\psi(-,t) = \exp(i S / \hbar) a \exp(- i \omega )$ is a **semiclassical stationary state** with [[energy]]

$$
  E \coloneqq \hbar \omega
$$

if the phase $S$ and the modulus $a$ satisfy the following two conditions:

1. The phase function $S$ satisfies the [[Hamilton-Jacobi equation]] or [[eikonal]] equation

   $$
     H(x, \nabla S(x)) = 
     \frac{\vert \mathbf{d} S\vert^2}{2 m } + V = 
     E
     \,,
   $$

1. The modulus $a$ is such that $a^2 \mathbf{d} S$ satisfies the homogeneous [[transport equation]] in that it is a [[divergence]]-free [[vector field]]. 


#### As a Lagrangian submanifold of phase space equipped with a half-density

The above characterization of semiclassical [[wave functions]]
of the non-relativistic particle in a potential 
has a natural equivalent reformulation in terms of 
[[symplectic geometry]]/[[geometric quantization]].

The [[phase space]] is

$$
  T^* \mathbb{R}^n \simeq \mathbb{R}^{2 n}
  \,.
$$

Into this space is canonically embedded as the 0-section:

$$
  0
  = 
 (x \mapsto (x, p = 0))
  \;
  \colon 
  \;
  \mathbb{R}^n 
   \hookrightarrow
  T^* \mathbb{R}^n
$$

which is a [[Lagrangian submanifold]]. 

Now every phase function $S \colon \mathbb{R}^n \to \mathbb{R}$ as above induces a deformation of this by regarding the [[de Rham differential]] $\mathbf{d}S$ as a [[section]] of the [[cotangent bundle]]

$$
  \mathbf{d}S \colon \mathbb{R}^n \hookrightarrow T^* X
$$

(This is what related [[phase and phase space in physics]].)

This is again a [[Lagrangian submanifold]]. We write

$$
  \pi \colon im(\mathbf{d}S) \to \mathbb{R}^n
$$

for the restriction of the [[cotangent bundle]] projection to this Lagrangian submanifold.

The fact that $S$ satisfies the [[Hamilton-Jacobi equation]] means equivalently that this Lagrangian submanifold is the level-set of the [[Hamiltonian]] $H \colon \mathbb{R}^n \to \mathbb{R}$ at energy $E = \hbar \omega$

$$
  im(\mathbf{d}S) = H^{-1}(E)
  \,.
$$

For the interpretation of the modulus function $a$ in this reformulation, first notice that for $vol$ the canonical [[volume form]] on $\mathbb{R}^n$, the homogeneous transport equation

$$
  div(  a^2 \mathbf{d}S) = 0
$$

is equivalent to 

$$
  \mathcal{L}_{\nabla S} ( a^2 vol ) = 0
$$

where on the left we have the [[Lie derivative]] along the [[gradient]] of $S$. Next observe that 

$$
  \nabla S = \pi_* (v_H)|_{im(\mathbf{d}S)}
$$

where $v_{H}$ is the [[Hamiltonian vector field]] corresponding to $H$.

This means that the transport equation is equivalently

$$
  \mathcal{L}_{(v_H)} \pi^* (a^2 vol) = 0
  \,.
$$

Hence this says that $\pi^* a^2 vol$ is a [[volume form]] on $im(\mathbf{d}S)$ which is invariant with respect to the Hamiltonian flow of time evolution. 

Finally, if instead of a [[volume form]] we choose a [[half-density]] $\sqrt{vol}$, then $a \sqrt{vol}$ is another half-density and the condition is that this be invariant under the Hamiltonian flow.

In summary then, the semiclassical wave fuction is equivalently

1. a [[Lagrangian submanifold]]

   * which is a level-set of the [[Hamiltonian]] at the given [[energy]]

1. such that $\mathbf{a} \coloneqq a \sqrt{vol}$ is a [[half-density]] on the Lagranian submaifold

   * which in addition is invariant under the Hamiltonian flow.

This formulation now suggests a more general definition of semiclassical states in [[symplectic geometry]]/[[geometric quantization]].


### In symplectic geometry / geometric quantum theory
 {#InSymplecticGeometry}

(...)

abstracting the above we have that

(...)




## Related concepts

[[!include classical-to-quantum notions - table]]


## References

An introduction to the formulation of semiclassical states in [[symplectic geometry]] is in the first section of 

* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_ ([pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf))


[[!redirects semiclassical states]]
