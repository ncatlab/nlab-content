
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


In formulas in [[thermodynamics]] it is often the (multiplicative) inverse of the [[temperature]] $T$ that is the natural [[variable]], then traditionally abbreviated

$$
  \beta
  \;\coloneqq\;
  \frac{1}{k T}
  \,,
$$

where $k$ denotes the [[Boltzmann constant]], a [[physical unit]] which for purposes of pure mathematics may be identified with unity and hence omitted from the formula.

This inverse temperature appears, in particular, in the formula for the [[Boltzmann distribution]], which is the [[probability distribution]] such that the [[probability density]] for a [[physical system]] to be in a [[state]] with [[energy]] $E$ is proportional to the [[exponential]] of $E$ weighted by minus the inverse temperature:

$$
  d p \;=\; e^{- \beta E} \, d E
  \,.
$$

Essentially a special case of this is the formula for the [[heat kernel]] on a [[Riemannian manifold]], which is an [[integral kernel]] proportial to the [[exponential]] of the Riemannian [[distance]] squared and again weighted by minus the inverse temperature.

$$
  K_{Heat}(x,y) \;\propto\; e^{  - \beta \cdot d(x,y)^2 }
  \,.
$$

Extrapolating from this case, the scale of the exponent in various [[kernel method|kernels]] may often be understood as akin to inverse temperature.

Finally, when understanding [[thermal field theory|thermal]]/[[Euclidean field theory]] as the result of [[Wick rotation]] of [[relativistic field theory]] (when possible), the inverse temperature $\beta$ is proportional to the [[radius]] of the "thermal circle" on which the [[Euclidean field theory]] must be understood to be [[Kaluza-Klein compactification|KK-compactified]], see [there](Euclidean+field+theory#TemporalCompactificationToThermalRelativisticFieldTheory) for more.


## Related concepts

* [[temperature]], [[absolute zero]]

* [[thermal field theory]], [[infinite-temperature thermal field theory]]

* [[kernel methods]]

[[!redirects inverse temperatures]]


