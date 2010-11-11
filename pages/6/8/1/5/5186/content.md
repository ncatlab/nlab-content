
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

A first simple definition in the framework of [[general relativity]] is this: A _relativistic particle with zero rest mass_ is a lightlike curve in a [[spacetime]]. A _relativistic particle with nonzero rest mass_ is a timelike curve in a [[spacetime]]. For the definition of lightlike and timelike curves see [[smooth Lorentzian space]].

A more "full-fledged" definition is this:

The _relativistic particle_ propagating on a [[spacetime]] $(X,g)$ is the 1-[[dimension]]al [[sigma-model]] whose kinetic part of the [[action functional]] is the [[length]] functional, as given by the [[pseudo-Riemannian metric]] $g$ and whose gauge-coupling to an [[electromagnetic field]] on $X$ given by a [[line bundle]] with [[connection on a bundle|connection]] $\nabla$ on $X$ is the [[parallel transport]] of that connection:

$$
  \exp S : \gamma \mapsto \exp i S_{kin}(\gamma) \exp i S_\nabla(\gamma)
$$

where $S_{kin} = length_g(\gamma)$ and $\exp i S_\nabla(\gamma) = tra_\nabla(\gamma)$.
 
## References

* Giulio Ruffini, _Four approaches to quantization of the relativistic particle_ ([arXiv:gr-qc/9806058](http://arxiv.org/abs/gr-qc/9806058))

[[!redirects relativistic particles]]

[[!redirects quantum relativistic particle]]
[[!redirects quantum relativistic particles]]
