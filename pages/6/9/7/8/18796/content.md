

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For [[vectors]] in [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ (regarded as the [[inner product space]] $(\mathbb{R}^{p+1}, \eta)$ for $\eta$ the [[Minkowski metric]]) _rapidity_ is the analog in [[Lorentzian geometry]] of what in [[Euclidean geometry]] would be the _[[angle]]_ to the [[time]]-axis. If vectors in $\mathbb{R}^{p,1}$ are thought of as [[tangent vectors]] to [[trajectories]] in [[Minkowski spacetime]], their rapidity is a measure for the _[[velocity]]_ of the trajectory, which is well-adapted to [[Lorentz transformations]].

## Definition

Let $x = (x^0, \vert x) \in \mathbb{R}^{p,1}$ be a [[vector]] with [[Minkowski metric|Minkowski norm]]-square

$$
  -{\vert x\vert}_\eta^2 \coloneqq (x^0)^2 - {\vert \vec x\vert}^2 \;\geq 0\;
  \,.
$$

and

$$
  x^0 \geq 0
  \,.
$$

Them its _rapidity_ is the unique $z \in \mathbb{R}$ such that

$$
  x^0 = \sqrt{-{\vert x\vert}^2_\eta} \, \cosh(z)
$$

and

$$
  {\vert \vec x\vert} = \sqrt{-{\vert x\vert}^2} \, \sinh(z)
$$

where $\cosh, \sinh$ denote the [[hyperbolic cosine]] and [[hyperbolic sine]], respectively.


In contrast, the [[velocity]] of $x$ is the product of the [[speed of light]] $c$ with the [[hyperbolic tangent]] of the rapidity:

$$
  \begin{aligned}
    v 
    & \coloneqq 
    \frac{ { \vert \vec x\vert} }{t}
    \\
    & =
    c \frac{ {\vert \vec x\vert} }{x^0}
    \\
    & =
    c \frac{ \sinh(z) }{ \cosh(z)}  
    \\
    & =
    c \tanh(z)
  \end{aligned}
$$

## Related concepts

* [[velocity]], [[speed]]

* [[special relativity]]

* [singular support of causal propagator](causal+propagator#SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone)

## References

* Wikipedia, _[Rapidity](https://en.wikipedia.org/wiki/Rapidity)_

[[!redirects rapidities]]