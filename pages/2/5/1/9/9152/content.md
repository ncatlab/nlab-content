
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _polar coordinate system_ for [[Cartesian space]] $\mathbb{R}^{n+1}$ is a [[coordinate system]] adapted to the decomposition of the [[complement]] $\mathbb{R}^{n+1} \setminus \{0\}$ of the origin as a [[Cartesian product]] of the [[unit sphere|unit]] [[n-sphere]] times the [[positive real numbers]] inside the [[real line]]:

$$
  \mathbb{R}^{n+1} \setminus \{0\}
  \;\simeq\;
  S^n \times \mathbb{R}_{\gt 0}
  \,.
$$

If $dvol_{S^n} \in \Omega^n(S^n)$ denotes the standard [[volume form]] on the [[unit sphere|unit]] [[n-sphere]], then the standard [[volume form]] $dvol_{\mathbb{R}^{n+1}}$ of [[Cartesian space]] in polar coordinates is

$$
  dvol_{\mathbb{R}^{n+1}}
  \;=\;
  r^n d r \wedge dvol_{S^n}
  \,,
$$ 

where $r \colon \mathbb{R}_{\gt 0} \to \mathbb{R}$ denotes the canonical [[coordinate function]] along the [[radius|radial]] direction.

If a [[smooth function]] $\mathbb{R}^{n+1} \to \mathbb{R}$ depends at most on the [[radius]] coordinate $r$ and the [[angle]] $\theta$ of [[vectors]] in $\mathbb{R}^{n+1}$ to any fixed line through the origin, then 

$$
  \label{VolumeElementForFunctionDependingOnRadiusandTheta}
  \begin{aligned}
    f(\vec x) dvol_{\mathbb{R}^{n+1}}
      & =
    f(r,\theta) 
   \,\, (r \sin(\theta))^{n-1} dvol_{S^{n-1}} \,\wedge r d\theta\, \wedge d r
  \end{aligned}
$$

> sign correct?

## Related concepts

* [[coordinates]]

## References

See also

* Wikipedia, _[Polar coordinate system](http://en.wikipedia.org/wiki/Polar_coordinate_system)_

* Wikipedia, _[Spherical coordinare system](https://en.wikipedia.org/wiki/Spherical_coordinate_system)_

[[!redirects polar coordinate system]]
[[!redirects polar coordinate systems]]

[[!redirects spherical coordinate]]
[[!redirects spherical coordinates]]
[[!redirects spherical coordinate systems]]
[[!redirects spherical coordinate system]]
[[!redirects spherical coordinate systems]]

