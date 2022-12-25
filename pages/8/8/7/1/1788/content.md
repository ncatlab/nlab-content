
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The _covariant phase space_ of a system in [[physics]] is the [[space]] of all of its solutions to its [[classical mechanics|classical equations of motion]], the _[[space of trajectories]]_ of the system.  Often one considers a parameterization of this by boundary data or choice of a [[Cauchy surface]]. This parameterization is what traditionally is just called a "phase space". The "covariant" in "covariant phase space" is to indicated that it comes without any unnatural choices.

For a system described by [[Lagrangian]] mechanics, the covariant phase space comes canonically equipped with a [[presymplectic structure]]. A proper _phase space_ or _[[reduced phase space]]_ is a [[quotient space]] of the covariant phase space on which the presymplectic structure refines to a [[symplectic manifold|symplectic structure]] or [[Poisson manifold|Poisson strucure]]. 

Typically these phase spaces are (locally) naturally parameterized by the suitable boundary conditions which uniquely determine the corresponding history of the physical system. Much of the literature on phase spaces deals with parameterizing these boundary conditions. 

For instance for a non-relativistic [[particle]] propagating on a [[Riemannian manifold]] $X$ with the usual [[action functional]], a trajectory is uniquely fixed by the position $x \in X$ and the momentum $p \in T^*_x X$ of the particle at a given time. Correspondingly the space of all solutions and hence the (covariant) phase space of the system may be identified with the [[cotangent bundle]] $T^* X$ of $X$.  
 
(The term "phase" in "phase space" can be related to the phase of [[complex numbers]] in this example, see at _[[phase and phase space in physics]]_.)

However, even [[reduced phase spaces]] are not all cotangent bundles, typically not, for instance, if they are obtained by [[symplectic reduction]]. This way a finite-dimensional phase space can sometimes describe continuous systems (e.g. in hydrodynamics) whch have infinitely many degrees of freedom; that phase space is however not a cotangent bundle of something in general. 


## Covariant phase space

There are two main routes to the construction of the covariant phase space, 

* (S) via [[presymplectic structure]];

* (P) via [[Poisson algebra]] structure.

### (S) Via pre-symplectic structures
 {#ViaSymplecticStructure}

We describe the canonical [[presymplectic structure]] on the covariant phase space of a [[local action functional]]. The _covariant phase space_ is defined as the space of critical points of an action functional or, equivalently, the space of solutions of its [[Euler-Lagrange equation]]s, also known as the _shell_. The shell is naturally embedded as a subset of the space of all field configurations. Below, terminology and notation are as in the discussion at [[variational bicomplex]].

Let $E \to X$ be a smooth [[fiber bundle]] over an $n$-dimensional [[spacetime]] $X$ and $j_\infty E$ the corresponding [[jet bundle]]. The total [[de Rham differential]] on $j_\infty E$ decomposes, $\mathbf{d} = d + \delta$, into the anti-commuting horizontal and vertical differentials, $d$ and $\delta$. The [[local action functional]]

$$
  S : \Gamma(E) \to \mathbb{R}
$$

is by definition given by a [[Lagrangian]]

$$
  L : \Gamma(j_\infty E) \to \Omega^{n}(X)
$$

as

$$
  S : \phi \mapsto \int_X L(j_\infty(\phi))
  \,.
$$

The [[variational calculus|variation]] of the action $S$ can be written in terms of the vertical differential:

$$
  \delta S (\phi) = \int_X (\delta L)(j_\infty(\phi)) \,,
$$
where the first $\delta$ the variational differential (as interpreted in the [bicomplex definition](variational+bicomplex#BicomplexDefinition)) and the second $\delta$ is the vertical differential. Thus, for the purposes of variational calculus, we can concentrate purely on the vertical differential of the Lagrangian, which canonically decomposes as follows:

$$
  \delta L = EL(\phi)\delta\phi - d \theta(\phi) \,,
$$

where $EL(\phi) = 0$ is the [[Euler-Lagrange equation]] on $\phi$, and where $EL(\phi)\delta\phi$ is a degree-$(n,1)$ and $\theta$ is a degree-$(n-1,1)$ element in the [[variational bicomplex]] (one variational form degree and, respectively, $n$ or $(n-1)$-spacetime form degrees).

+-- {: .num_remark #CanonicalThetaDensityInLocalCoordinates}
###### Remark 


On a local [[coordinate]] patch $\{x^i\}$ for $X$ the form $\theta$ here is given by

$$
  \theta(\phi) 
    = 
  (\iota_{\partial_i} \frac{\delta L}{\delta  \phi^a_{,i}} )
  \wedge
   \delta \phi^a
  \,.
$$

If $L = L_{kin} + L_{pot}$ is the sum of a standard [[kinetic Lagrangian]] for a [[free field theory]] and a potential term that only depends on the fields themselves and not on their derivatives,  then this is at the same time the canonical [[multisymplectic form]] for the given [[field bundle]]. See at _[[multisymplectic geometry]]_ the section _[Examples -- Free field theory](#CanonicalThetaDensityInLocalCoordinates)_ for more on this relation.

=--


The above definition of $EL$ and $\theta$ in terms of $\delta L$ yields the following identity upon taking another exterior variational derivative of both sides

$$
  \delta(\delta L) = 0
  = \delta(EL(\phi)) \wedge \delta\phi
    + d \delta \theta(\phi)
  \,,
$$

where the first term on the right clearly vanishes when pulled back to the shell, $EL(\phi)=0$ on $X$. The above wedge product between variational forms is inherited from the wedge product on $\Omega^\bullet(j_\infty E)$. This implies that the [[presymplectic current]], $\omega(\phi) = \delta(\theta(\phi))$, is horizontally closed on shell:

$$
\begin{aligned}
  d \iota^* \omega(\phi)
  &= d \iota^* (\delta \theta(\phi)) \\
  &= \iota^* d (\delta \theta(\phi)) \\
  &= -\iota^* \delta(EL(\phi)) \wedge \delta\phi \\
  &= 0
  \, ,
\end{aligned}
$$

where $\iota: \mathcal{S}_L \to \Gamma(E)$ is the embedding of the solutions of the [[Euler-Lagrange equation]]s  (the shell) into the space of all field configurations. The reason is that $\iota^* \delta(EL(\phi)) = 0$ for each $x\in X$, since the functions $EL(\phi)$ are all constant (in fact $0$) on solutions.

The variational 1-form on the space of field configurations

$$
  \Theta = \int_{X|_{in}} \theta(\phi)
$$

given by an [[integration]] over a [[Cauchy surface]] $X|_{in}$ is the potential for the presymplectic form 

$$
  \Omega = \delta \Theta = \int_{X|_{in}} \delta(\theta(\phi))
  = \int_{X|_{in}} \omega(\phi)
$$

on the space of field configurations. Since $\omega(\phi)$ is horizontally closed on shell, the the pullback of the presymplectic form $\iota^* \Omega$ is independent of the choice of the surface $X|_{in}$ (provided the choice is restricted to a single homology class of surfaces).

+-- {: .un_claim}
###### Claim

The presymplectic form $\iota^* \Omega$ on the covariant phase space is symplectic iff the linearized [[Euler-Lagrange equation]]s, $EL(\phi)=0$, have a locally well-posed initial value problem on $X|_{in}$. In particular, in the presence of gauge symmetries, due to the failure of uniqueness of solutions for given initial data on $X|_{in}$, the form $\iota^*\Omega$ is only presymplectic.

=--

However, the infinitesimal actions of gauge symmetries exhaust the kernel of the $\iota^* \Omega$ and upon performing [[symplectic reduction]], we obtain the space of orbits of solutions under the action of gauge symmetries, which is the _physical_ or _[[reduced phase space]]_.

Notice that the form $\Omega$, on the field configuration space, does depend on the choice of Cauchy surface. Performing [[symplectic reduction]] gives the symplectic space of equivalence classes of solutions of equations of motion modulo [[gauge transformation]]s, and hence also the _[[reduced phase space]]_. Thus, the end point of the reduction no longer depends on the choice of the Cauchy surface.


