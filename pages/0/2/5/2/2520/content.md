
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Let $\mathbf{H}$ be the ambient [[(∞,1)-topos]] with a [[natural numbers object]] and equipped with a [[line object]] $\mathbb{A}^1$. Let $C \in \mathbf{H}$ be the [[configuration space]] of a physical system. Then an **action functional** is a morphism

$$
  \exp(i S(-)) : C \to \mathbb{A}^1 / \mathbb{Z}
  \,
$$

If $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] then there is an <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">intrinsic differential</a> of the action functional to a morphism

$$
  d \exp(i S(-)) : C \to \mathbf{\flat}_{dR}\mathbb{A}^1/\mathbb{Z}
  \,.
$$


This is the [[Euler-Lagrange equation]] of the system. The [[homotopy fiber]]

$$
  P \to C
$$

of this morphism is the [[covariant phase space]] inside the configuration space: the space of classically realized trajectories/histories of the system.



## Local action functionals

The action functional $\exp(i S(-)) : C \to \mathbb{A}^1 / \mathb{Z}$ for a [[quantum field theory]] on a parameter space $X$ with [[configuration space]] of fields $C$ on $X$  is usually required to be a **local functional** given by a **[[Lagrangean]] density**: a [[differential form]] $L(\phi)$ on $X$ of degree $dim X$ depending on the fields in $C$, such that 

$$
  S : \phi \mapsto \int_X L(\phi)
  \,.
$$

For a more manifestly [[general relativity|relativistic]] formulation, we may obtain the action functional by integrating the Lagrangean density on [[spacetime]].

1. $ S(q) = \int_a^b L(q,\dot{q}) \,\mathrm{d}t $, where $q$ is a path through configuration space, on the time interval $[a,b]$, with derivative $\dot{q} = \mathrm{d}q/\mathrm{d}t$.  When minimising the action, we fix the values of $q(a)$ and $q(b)$.
2. $ L(q,\dot{q}) = \int_{S} \mathcal{L}(q,\dot{q}) \,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z $, where now $q$ is a configuration of fields on $S$, which is a region of space.  We fix boundary conditions on the boundary of $S$ (typically that $q$ and $\dot{q}$ go to zero if $S$ is all of space).
3. $ S(q) = \int_{R} \mathcal{L}(q,\dot{q}) \,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t $, where now $q$ is a configuration of fields on $R$, which a region of spacetime, with time derivative $\dot{q} = \partial{q}/\partial{t}$.  We fix boundary conditions on the boundary of $R$.

The formulation of (3) above is still not manifestly coordinate indepdendent.  However, $\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t$ is simply the [[volume form]] on spacetime and $\dot{q}$ is merely one choice of coordinate on [[configuration space|state space]] and could just as easily be replaced by a derivative with respect to any timelike coordinate on spacetime (or drop coordinates altogether).


## Examples

A large class of examples of action functionals arises in [[schreiber:∞-Chern-Simons theory]]. See there for details.


[[!redirects action functionals]]