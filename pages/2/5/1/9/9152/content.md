
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Spheres
+-- {: .hide}
[[!include spheres -- contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


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
  r^n\, d r \wedge dvol_{S^n}
  \,,
$$ 

where $r \colon \mathbb{R}^{n+1} \to \mathbb{R}_{\gt 0}$ denotes the canonical [[coordinate function]] along the [[radius|radial]] direction.

If a [[smooth function]] $\mathbb{R}^{n+1} \to \mathbb{R}$ depends at most on the [[radius]] coordinate $r$ and the [[angle]] $\theta$ of [[vectors]] in $\mathbb{R}^{n+1}$ to any fixed line through the origin, then 

$$
  \label{VolumeElementForFunctionDependingOnRadiusandTheta}
  \begin{aligned}
    f(\vec x)\, dvol_{\mathbb{R}^{n+1}}
      & =
    f(r,\theta) 
   \,\, (r \sin(\theta))^{n-1}\, r d \theta \wedge dvol_{S^{n-1}} \,\wedge d r
  \end{aligned}
$$


## Spherical coordinates

One particular polar coordinate system on $\mathbb{R}^{n+1}$ goes by the name of _spherical coordinates_.  This may be defined by induction (on $n$) as follows:

For $n=1$, we use the essentially unique polar coordinate system on the plane $\mathbb{R}^2$, that is $(r,\theta_1)$, where $r$ is the distance from the origin and $\theta_1$ is the signed angle from the positive first-coordinate axis, with orientation pointing towards the positive second-coordinate axis.

For $n=k+1$, we use $(r,\theta_2,\ldots,\theta_n,\theta_1)$, where $r$ gives the distance from the origin, $\theta_1,\ldots,\theta_{n-1}$ are given by projection onto $\mathbb{R}^n$ along the *last* coordinate axis, and $\theta_n$ is the *unsigned* angle from the last coordinate axis.

Notice that $\theta_1$ is treated differently from the other angles.  For $k \gt 1$, we have $0 \leq \theta_k \leq \pi$, but we have $0 \leq \theta_1 \lt 2 \pi$ instead (or sometimes people use $-\pi \lt \theta_1 \leq \pi$).  For $k \gt 1$, $\theta_k$ is determined relative to the $(k+1)$-th coordinate axis (if we number these from $1$ to $n+1$), but $\theta_1$ is determined relative to the first coordinate axis.  To get the standard orientation on $\mathbb{R}^n$, $\theta_1$ also has to come after all of the other angles.  And the system doesn\'t work at all for $\mathbb{R}^1$ ($n = 0$).

(The axis to measure spherical coordinates from is a matter of historical convention, and sometimes people use different conventions.  But a polar coordinate system for $\mathbb{R}^1$ is technically impossible, since one coordinate must be the distance from the origin, which is not enough information on its own, and yet there isn\'t room for another coordinate.  In terms of the decomposition $\mathbb{R}^1 \setminus \{0\} \simeq S^0 \times \mathbb{R}_{\gt0}$, the problem is that $S^0$ is a disconnected discrete space and so has no global coordinate system, even allowing for degeneracy.)


## Related concepts

* [[coordinates]]


## References

See also

* Wikipedia, _[Polar coordinate system](http://en.wikipedia.org/wiki/Polar_coordinate_system)_

* Wikipedia, _[Spherical coordinate system](https://en.wikipedia.org/wiki/Spherical_coordinate_system)_


[[!redirects polar coordinate]]
[[!redirects polar coordinates]]
[[!redirects polar coordinate systems]]
[[!redirects polar coordinate systems]]

[[!redirects spherical coordinate]]
[[!redirects spherical coordinates]]
[[!redirects spherical coordinate system]]
[[!redirects spherical coordinate systems]]
