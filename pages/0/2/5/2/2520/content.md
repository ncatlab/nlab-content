
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

In [[physics]] the dynamics of a system may be encoded by a [[functional]] -- called the **action functional** on its [[configuration space]]:

* in [[classical mechanics]] and [[classical field theory]] -- by the **action principle** or **principle of least action** -- the extrema of the action functional -- obtained by [[variational calculus]] and given by [[Euler-Lagrange equation]]s -- encode the physically observable configurations  ;

* in [[quantum mechanics]] and [[quantum field theory]] the evolution of the [[quantum state]]s is encoded by the integral -- the [[path integral]] -- of the exponentiated action functional over the space of field configurations.

For emphasis the description of dynamics by action functionals is called the **Lagrangean** approach. Another forumlation of dynamics in physics that does not involve an action functional explicitly is [[Hamiltonian mechanics]] on [[phase space]]. At least in certain classes of cases the relation and equivalence of both approaches is understood. Generally the formulation of [[quantum field theory]] in terms of action functionals suffers from a lack of precise understanding of what the [[path integral]] over the action functional really means. 


## Definition

Let $\mathbf{H}$ be the ambient [[(∞,1)-topos]] with a [[natural numbers object]] and equipped with an additive [[line object]] $\mathbb{A}^1$ (see there). Let $C \in \mathbf{H}$ be the [[configuration space]] of a physical system. Then an **action functional** is a morphism

$$
  \exp(i S(-)) : C \to \mathbb{A}^1 / \mathbb{Z}
  \,
$$

If $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] then there is an <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">intrinsic differential</a> of the action functional to a morphism

$$
  d \exp(i S(-)) : C \to \mathbf{\flat}_{dR}\mathbb{A}^1/\mathbb{Z}
  \,.
$$

This is the [[Euler-Lagrange equation]] of the system. The [[critical locus]] of $S$ is the [[covariant phase space]] inside the configuration space: the space of classically realized trajectories/histories of the system. If $\mathbf{H}$ models [[derived geometry]] then this critical locus is presented by a [[BRST-BV complex]].


## Local action functionals
 {#LocalActionFunctional}

An action functional is called **local** if it arises from integration of a [[Lagrangian]].

More precisely, an action functional $S : C \to \mathbb{A}^1$ is called local if

* the [[configuration space]] $C$ is the space $C = \Gamma_X(E)$ of [[section]]s of a [[fiber bundle]] $E \to X$ over some parameter space ([[spacetime]] $X$);

* there is a [[Lagrangian]] density $J_\infty(E) \to \Omega^{\dim X}(X)$ on the [[jet bundle]] of $E$;

* on a section/field configuration $\phi : X \to E$ the action $S$ takes the value

  $$
    S(\phi) = \int_X L(j_\infty(\phi))
    \,,
  $$

  where $j_\infty(\phi) = (\phi, \partial_i \phi, \cdots)$ is the jet-prolongation of $\phi$ (the collection of all its higher partial derivatives).

Consider action functional for on a configuration space of 
[[smooth function]]s from the line to a [[smooth manifold]] $X$.

We can consider

1. $ S(q) = \int_a^b L(q,\dot{q}) \,\mathrm{d}t $, where $q$ is a path through configuration space, on the time interval $[a,b]$, with derivative $\dot{q} = \mathrm{d}q/\mathrm{d}t$.  When minimising the action, we fix the values of $q(a)$ and $q(b)$.
2. $ L(q,\dot{q}) = \int_{S} \mathcal{L}(q,\dot{q}) \,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z $, where now $q$ is a configuration of fields on $S$, which is a region of space.  We fix boundary conditions on the boundary of $S$ (typically that $q$ and $\dot{q}$ go to zero if $S$ is all of space).
3. $ S(q) = \int_{R} \mathcal{L}(q,\dot{q}) \,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t $, where now $q$ is a configuration of fields on $R$, which a region of spacetime, with time derivative $\dot{q} = \partial{q}/\partial{t}$.  We fix boundary conditions on the boundary of $R$.

The formulation of (3) above is still not manifestly coordinate independent.  However, $\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t$ is simply the [[volume form]] on spacetime and $\dot{q}$ is merely one choice of coordinate on [[configuration space|state space]] and could just as easily be replaced by a derivative with respect to any timelike coordinate on spacetime (or drop coordinates altogether).


## Examples

A large class of examples of action functionals arises in [[schreiber:∞-Chern-Simons theory]]. See there for details.


## Related concepts

* [[effective action functional]], [[background field formalism]]


[[!redirects action functionals]]

[[!redirects local action functional]]
[[!redirects local action functionals]]