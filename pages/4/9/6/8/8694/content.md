
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

## Definition

The [[electromagnetic field]] on a [[spacetime]] $X$ is mathematically modeled by a [[circle bundle with connection]] $\nabla$ on $X$. If the underlying bundle is trivial, or else on local [[coordinate patches]] $\mathbb{R}^n \hookrightarrow X$ over which it is so, this [[connection on a bundle|connection]] is equivalently a [[differential 1-form]] $A \in \Omega^1(\mathbb{R}^n)$. 

This is then called the **electromagnetic potential** of the [[electromagnetic field]] (sometimes: "vector potential" or "[[gauge potential]] of the electromagnetic field"). 

Its [[de Rham differential]]

$$
  F \coloneqq \mathbf{d}A
$$

is the actual [[field strength]] of the electromagnetic field.

On a 4-dimensiona [[Minkowski spacetime]] with its canonical [[coordinates]] $\{t,x^1, x^2, x^3\}$, the electromagnetic potential $A$ is naturally expanded into corredinate components, traditionally written as

$$
  A = \phi \mathbf{d}t + A_1 \mathbf{d}x^1 + A_2 \mathbf{d}x^2 + A_3 \mathbf{d}x^3
  \,.
$$

Here 

* $\phi$ is the **electric potential** 

* $\vec A = [A_1, A_2, A_3]$ is the **magnetic potential** 

(for this choice of [[coordinates]]).

## Related concepts

* [[gauge potential]]

* [[Aharonov-Bohm effect]]

## References

The identification of [[gauge potentials]] with [[connections]] on [[fiber bundles]] is due to:

* {#WuYang75} [[Tai Tsun Wu]], [[Chen Ning Yang]], *Concept of nonintegrable phase factors and global formulation of gauge fields*, Phys. Rev. D **12** (1975) 3845 &lbrack;[doi:10.1103/PhysRevD.12.3845](https://doi.org/10.1103/PhysRevD.12.3845)&rbrack;

See also at *[[fiber bundles in physics]]*.

History:

> (The notion of electromagnetic potential has roots in the somewhat vague notion of the "electrotonic state" of [[Michael Faraday]].)

* A. C. T. Wu, [[Chen Ning Yang]], *Evolution of the concept of vector potential in the description of the fundamental interactions*,  International Journal of Modern Physics A **21** 16 (2006) 3235-3277 &lbrack;[doi:10.1142/S0217751X06033143](https://doi.org/10.1142/S0217751X06033143)&rbrack;

* [[Chen Ning Yang]]: *Vector Potentials and Connections*, talk at 13th Annual Geometry Festival *Connections in Modern Mathematics and Physics*, Stony Brook University (April 1998) &lbrack;video:[YT](https://youtu.be/uaBVQe7w2Hs)&rbrack;

* [[Chen Ning Yang]], *The conceptual origins of Maxwell’s equations and gauge theory*, Phyics Today **67** 11 (2014) &lbrack;[doi:10.1063/PT.3.2585](https://doi.org/10.1063/PT.3.2585), [pdf](http://home.ustc.edu.cn/~lxsphys/2021-3-18/The%20conceptual%20origins%20of%20Maxwell%27s%20equations%20and%20gauge%20theory.pdf)&rbrack;


Review:

* [[Theodore Frankel]], Section 5 of: _[[The Geometry of Physics - An Introduction]]_

* [[geometry of physics]], _[The electromagnetic field strength](geometry+of+physics#ElectromagneticFieldStrength)_

* Wikipedia, *[Magnetic vector potential](https://en.wikipedia.org/wiki/Magnetic_vector_potential)*

[[!redirects electromagnetic potentials]]

[[!redirects vector potential]]

[[!redirects vector potentials]]
