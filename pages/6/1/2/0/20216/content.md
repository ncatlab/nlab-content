
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The Poincaré–Hopf theorem says that given a [[vector field]] $v \in \Gamma(T X)$ with isolated vanishing points $\{x_i\}$ on a [[differential manifold]] $X$, the [[sum]] over over the $x_i \in X$ of the [[degree of a continuous function|degrees]] of the vector in the vicinity of these points, regarded as [[cohomotopy]] classes 

$$
  v/{\vert v\vert} 
  \;\colon\;
  \partial D_{x_i} \longrightarrow S(T_{x_i} X)
  \,,
$$

is given by the [[Euler characteristic]], hence by the value of the [[Euler class]] on the [[tangent bundle]]:

$$
  \chi(X)
  \coloneqq
  \chi[T X]
  \;=\;
  \underset{
    {\text{isolated zero}}
    \atop
    { x_i }
  }{\sum}
  deg\big(  v/{\vert v\vert}|_{x_i} \big)
  \,.
$$

In particular, the existence of a nowhere vanishing [[vector field]] (for which the above [[sum]] is empty) implies that the [[Euler characteristic]] vanishes.

## References

Named after [[Henri Poincaré]] and [[Heinz Hopf]].

Review includes

* Jonathan Libgober, _The Euler characteristic, Poincaré–Hopf theorem, and applications_ ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2010/REUPapers/Libgober.pdf))

A comment on the version for complex vector fields is in 

* Howard Jacobowitz, _Non-vanishing complex vector fields and the Euler characteristic_ ([arXiv:0901.0893](https://arxiv.org/abs/0901.0893)) 

See also

* Wikipedia, _[Poincaré–Hopf theorem](https://en.wikipedia.org/wiki/Poincar%C3%A9%E2%80%93Hopf_theorem)_