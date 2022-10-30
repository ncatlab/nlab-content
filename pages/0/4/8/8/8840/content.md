
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Aharonov-Bohm effect_ is a configuration of the [[electromagnetic field]] which has vanishing electric/magnetic [[field strength]] (vanishing [[Faraday tensor]] $F = 0$) and but is nevertheless non-trivial, in that the [[vector potential]] $A$ is non-trivial. Since the vector potential affects the [[phase|quantum mechanical phase]] on the [[wavefunction]] of [[electrons]] moving in an electromagnetic field, in such a configuration classical physics sees no effect, but the phase of quantum particles, which may be observed as a [[quantum interference|interference]] pattern on some screen, does.

More technically, a configuration of the [[electromagnetic field]] is generally given by a [[circle]]-[[principal connection]] and an Aharonov-Bohm configuration is one coming from a [[flat connection]], whose [[curvature]]/[[field strength]] hence vanishes, but which is itself globally non-trivial. This is only possible on [[spaces]] ([[spacetimes]]) which have a non-trivial [[fundamental group]], hence for instance it does never happen on [[Minkowski spacetime]].

In practice one imagines an idealized [[electric current]]-carrying [[solenoid]] in [[Euclidean space]]. Away from the solenoid itself the [[magnetic field]] produced by it gives such a configuration.

## Details

Let $\mathbb{R}^2 - \{0\}$ be the [[plane]] with the origin removed, and consider the space $(\mathbb{R}^2 - \{0\}) \times \mathbb{R}$ (thought of as 3d [[Cartesian space]] with the z-axis removed) and [[spacetime]] $(\mathbb{R}^2 - \{0\}) \times \mathbb{R}^2$ (thought of as the previous configuration statically moving in time).

For the following argument only the topological structure of the space matters, and nothing needs to explicitly depend on the $z$-[[coordinate]] and the time-coordinate, so for notational simplicity we may suppress these and consider just $\mathbb{R}^2 - \{0\}$.

On this space minus the x-axis consider the [[polar coordinates]]  $(\phi,r)$ with

$$
  x = r cos(\phi)\,,\;\;\; y = r sin(\phi)
  \,.
$$

Accordingly we have the [[differential 1-forms]]

$$
  \mathbf{d}x = cos(\phi)\mathbf{d}r - r sin(\phi) \mathbf{d}\phi
$$

$$
  \mathbf{d}y = sin(\phi)\mathbf{d}r + r cos(\phi) \mathbf{d}\phi
$$

hence 

$$
  \begin{aligned}
    \mathbf{d}\phi 
     & = 
     \frac{1}{r}cos(\phi)\mathbf{d}y - \frac{1}{r}sin(\phi) \mathbf{d}x
     \\
     & = 
     \frac{1}{r^2} x \mathbf{d}y - \frac{1}{r^2} y \mathbf{d}x
  \end{aligned}
  \,.
$$

Here the expression on the right extends smoothly also to the $x$-axis and this extension we call 

$$
  \theta \coloneqq 
  \frac{1}{r^2} x \mathbf{d}y - \frac{1}{r^2} y \mathbf{d}x
  \;\;
  \in \Omega^1(\mathbb{R}^2 - \{0\})
  \,.
$$

From the way this is constructed it is clear that $\theta$ is a closed differential form

$$
  \mathbf{d}\theta = 0
  \,.
$$

However, on $\mathbb{R}^2 - \{0\}$ this is not an exact form. In other words, if one regards $\theta$ as the [[vector potential]] being the configuration of an  [[electromagnetic field]]

$$
  A \coloneqq \theta
$$

then:

1. the [[field strength]] vanishes $F = \mathbf{d}A = 0$;

1. but there is no [[gauge transformation]] relating $A$ to the trivial field configuration.

This is possible because $\mathbb{R}^2 - \{0\}$ is not [[simply connected topological space|simply connected]] and hence the [[Poincaré lemma]] does not apply.

## Related concepts

* [[Dirac charge quantization]], [[magnetic monopole]]

## References

* Wikipedia, _[Aharonov-Bohm effect](http://en.wikipedia.org/wiki/Aharonov&#8211;Bohm_effect)_
