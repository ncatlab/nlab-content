
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[physics]] the term [[phase]] appears prominently in two superficially different uses: 

Inside the term "[[phase space]]", introduced by [[Boltzmann]] in 1872 in the context of [[classical mechanics]], it refers to the instantaneous position [[coordinates]] and [[momenta]] of a [[particle]]; its _Bewegungsphase_, it _phase of motion_. ([Nolte, p. 4](#Nolte10)).

But the term "[[phase]]" re-appeared, independently, with the advent of [[quantum physics]]: it refers to the [[complex phase]] of the [[complex numbers]] that [[wave functions]] take values in.

But it turns out that in the [[semiclassical approximation]] to [[quantum physics]] the phase of wave functions (or rather its [[derivative]]) precisely parametrizes points in [[phase space]]! Even though this is historically a pure coincidence of terminology, fortunately it matches to some extent.

This relation is discussed in some detail at _[[semiclassical state]]_. It is an old observation that drove the pre-history of [[quantum mechanics]] at a time when this was discovered by drawing analogies with [[wave mechanics|wave]] [[optics]]: 

the [[derivative]] of the [[phase]] (as in: [[complex numbers]]) of a [[wave function]] is (locally, or else in semiclassical approximation) the [[momentum]] of the corresponding [[particle]] (of which the wave function is the [[quantum state]]).  This momentum is, in addition to the spatial dependence of the wave function, what parameterizes [[phase space]].

More precisely: a stationary [[semiclassical state]] of a [[particle]] propagating on some [[Riemannian manifold]] $(X,g)$ (and subject to some [[force]] given by some scalar potential but *not* charged under a [[gauge field]]) is a [[wave function]] of the form 

$$
  \psi \colon (x,t) \mapsto \exp(i S(x)/\hbar) a(x) \exp(-i \omega t)
  \,,
$$

where $S$ and $A$ are real-valued functions. The [[de Rham differential]] of the **[[complex phase]]-function** 

$$
  S\;\colon\; X \to \mathbb{R}
$$ 

appearing here defines a map from $X$ into its [[phase space]], which here is the [[cotangent bundle]] over $X$:

$$
  \mathbf{d}S \;\colon\; X \to T^\ast X
  \,.
$$

The phase-space image of $X$ defined this way is the level set of the given [[Hamiltonian]] $H \colon T^* X \to \mathbb{R}$ at [[energy]] $E = \hbar \omega$.

So the de Rham differential $\mathbf{d}S$ of the complex phase function $S$ of a semiclassical wave function precisely parametrizes this semiclassical state as a submanifold in phase space.


## References

The origin of the term "phase" in "phase space" is discussed in

* David Nolte, _The tangled tale of phase space_, Physics Today (April 2010) ([pdf](http://www.physics.purdue.edu/nlo/NoltePT10.pdf))
 {#Nolte10}

The close relation between complex phases of semiclassical wave functions and phase space points is discussed for instance in the introduction (around p. 9) of 

* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_ ([pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf))


[[!redirects phase and phase space in physics]]

[[!redirects phases and phase spaces in physics]]

[[!redirects phase (physics)]]

