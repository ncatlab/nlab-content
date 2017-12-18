
> for other concepts of a similar name see at _[[polarization]]_

***

#Contents#
* table of contents
{:toc}

## Idea

A _[[plane wave]]_ with more than one component, i.e. being a [[section]] of a [[trivial vector bundle]], is characterized not just by its [[wave vector]] $k$, but also by that component vector $e$. Broadly speaking this $e$ is the _polarization_ of the wave.

Specifically a [[plane wave]] with [[coefficients]] in the [[cotangent bundle]] of a [[Minkowski spacetime]] $\Sigma$, such as an [[electromagnetic field|electromagnetic]] [[field history]] "[[vector potential]]" $A \in \Gamma_\Sigma(T^\ast \Sigma)$ is given by

$$
  A_\mu(x) = e_\mu e^{i k_\mu x^\mu}
  \,.
$$

In the case of [[free field theory|free]] [[electromagnetic waves]] the [[wave vector]] $k$ is [[light-like]], $k_\mu k^\mu = 0$, and in [[Gaussian-averaged Lorenz gauge]] the polarization vector $e$ has to satisfy $e^\mu k_\mu = 0$ and polarization vectors proportional to the wave vector $e_\mu \propto k_\mu$ are [[gauge equivalence|gauge equivalent]] to [[zero]]. Therefore in this case the space of physically distinguishable polarizations for given [[wave vector]] $k$ is the [[quotient space]]

$$
  \frac{
    \left\{ e \,\vert\, e^\mu k_\mu = 0 \right\}
  }{
    \left\{ e \,\vert\, e_\mu \propto k_\mu \right\}
  }
  \,.
$$

This is also called the space of _transversal polarizations_.

If one chooses [[coordinates]] such that $k = (\kappa, 0, \cdots, 0, \kappa)$ then this may be identified with the space of vectors of the form $e = (0, *, \cdots, *, 0)$.


## References

* Wikipedia, _<a href="http://en.wikipedia.org/wiki/Polarization_(waves)">Polarization (waves)</a>_

* {#Dermisek09} [[Radovan Dermisek]], _Quantum Electrodynamics (QED)_ ([pdf](http://www.physics.indiana.edu/~dermisek/QFT_09/qft-II-5-4p.pdf), [[DermisekQED.pdf:file]])


[[!redirects wave polarizations]]


[[!redirects transversal polarization]]
[[!redirects transversal polarizations]]

