
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


A system of [[physics]] has a [[space]] of possible _configurations_ or _hostories_ or _trajectories_ . This is called the _configuration space_ .

More specifically, for a system described by an [[action functional]] the configuration space is the domain space of that functional.

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

[[!redirects configuration spaces]]

[[!redirects space of field configurations]]
[[!redirects spaces of field configurations]]