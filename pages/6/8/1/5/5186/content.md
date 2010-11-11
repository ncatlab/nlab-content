
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

The _relativistic particle_ in [[physics]]s is a model for the dynamics of a single [[particle]] that is propagating in a [[spacetime]] subject to [[force]]s such as [[gravity]] and (if it is charged) the [[electromagnetic field]].

## Definition

Let $(X,g)$ be a [[spacetime]] and $\nabla$ a [[connection on a bundle|connection]] on a [[circle group]]-[[principal bundle]] over $X$.

A _trajectory_ of the relativistic particle on $X$ is a map

$$
  \gamma : [0,1] \to X
  \,.
$$

The exponentiated [[action functional]] $\exp S$ of the relativistic particle is the [[functional]] on the [[mapping space]] $[[0,1], X]$ given by

$$
  \exp S : \gamma \mapsto (\exp i S_{kin}(\gamma)) (\exp i S_\nabla(\gamma))
$$

where $S_{kin} = length_g(\gamma)$ is the invariant [[length]] of $\gamma$ and $\exp i S_\nabla(\gamma) = tra_\nabla(\gamma)$ is the [[parallel transport]] of $\nabla$ along $\gamma$.

Alternatively (and mandatorily for vanishing [[mass]] parameter), the kinitec action is replaced by the corresponding [[Polyakov action functional]].

The mapping space equipped with this action functional constitutes the data of a [[sigma-model]] [[quantum field theory]]. Its [[quantization]] is the _quantum relativistic particle_ .

## Properties

A _classical trajectory_ of the relativistic particle is a curve that extremizes the [[action functional]] (that solves the [[Euler-Lagrange equation]]s).

In the absence of an electromagnetic field or other forces except gravity, this is a [[geodesic]] in the [[spacetime]] which is

* lightlike if the particle is massless;

*  timelike if it has non-vanishing mass 

See [[Lorentzian space]] for these notions.

 
## References

* Giulio Ruffini, _Four approaches to quantization of the relativistic particle_ ([arXiv:gr-qc/9806058](http://arxiv.org/abs/gr-qc/9806058))

[[!redirects relativistic particles]]

[[!redirects quantum relativistic particle]]
[[!redirects quantum relativistic particles]]
