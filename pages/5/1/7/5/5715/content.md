
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

The _configuration space_ of a physical system is the [[space]] of all possible states of a physical system. For a [[classical mechanics|classical mechanical]] system with $n$-degrees of freedom it is a manifold of dimension $n$. 

For some purposes, like in relativistic field theory it is convenient to consider not space of states at the point in time, but rather the space 
of _histories_ or _trajectories_.

In mathematics, one often talks about the configuration space of $N$ distinct points in a manifold $M$, see [[Fadell's configuration space]]. 

#### Idea of histories variant

For a system described by an [[action functional]] the configuration space is the domain space of that functional.

More precisely, let $\mathbf{H}$ be the ambient [[(∞,1)-topos]] with a [[natural numbers object]] and equipped with a [[line object]] $\mathbb{A}^1$. Then an [[action functional]] is a morphism

$$
  \exp(i S(-)) : C \to \mathbb{A}^1/\mathbb{Z}
$$

in $\mathbf{H}$. The _configuration space_ is the domain $C$ of this functional. 

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

## Related concepts

* [[configuration space (mathematics)]]

* [[phase space]]

[[!redirects space of field configurations]]
[[!redirects spaces of field configurations]]