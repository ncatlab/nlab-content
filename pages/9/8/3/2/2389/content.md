
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Harmonic analysis
+-- {: .hide}
[[!include harmonic analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An [[oscillation]] is a *periodic motion of a physical system*, i.e. as a function of time, the position of the system of particles expressed as a coordinate in a configuration space depends as $t\mapsto x(t)$ where $x(t) = x(t+I)$ where $I$ is a constant called the period of the motion. The motion can pertain to a system of particles, to the coordinates determining the position of a rigid body or can express the magnitude of some physical quantity like pressure which evolves in time. In a mechanical system, the point in which the potential energy is minimal is called the equlibrium position; the relative position with respect to the equilibrium position is called the __elongation__. The maximal elongation is usually called the __amplitude of oscillation__.

A __wave__ is the (result of) *propagation of oscillations through an extended medium*.
Examples of extended media are a liquid, the vacuum (where physical fields can propagate, for example the electromagnetic field) or a discrete grid of interacting particles. Many partial differential equations for the mechanics of extended objects have wave solutions. Waves are typically viewed via quantity called __amplitude__ which describes the relative position of each particle in a continuum system from its equilibrium position (this conflicts a bit with the terminology on oscillations, where the amplitude would be the maximnal one). The amplitude depends both on the time and the position in space. Most typical wave propagation is of the form $A(x,t) = f(x-vt)$ where $x$ is the position, $v$ is the speed of propagation (which may depend on the direction of propagation, and for inhomogeneous systems on the coordinate) and $t$ is the time. Partial differential equations (PDE) which have __wave solutions__ are typically parabolic or hyperbolic PDEs. Here wave solutions are recognized by their form (variations of the formula $f(x-vt)$ from above). Wave solutions can add up together linearly or not; in both cases the phenomenon is called __superposition__. Finite superpositions have many typical features (e.g. Lissajous figures). 
The superposition can stretch over infinite families of waves, then the sum passes into the integral and many periodic modes add up to something what is not periodic whatsoever, and may be even localized. One then talks about a __wave packet__. A wave packet can from far away look like a point particle. Wave packets can decay (damp) quickly as they propagate and in nonlinear situations can be unstable under collisions with other waves. In simple linear cases, the individual cases in the wave packet correspond to elements of a basis in a Hilbert space of functions, then the expression of a wave packet in terms of basic waves (say plane waves) amount to a case of [[Fourier transform|Fourier mode expansion]]. 

In some special circumstances, the waves can preserve their features in nonlinear situations even asymptotically after collisions, in that case we talk about [[soliton]]s. Solitons and multisolitons 
are especially well-known in gauge theories (including the 4d case localized in time, so called instantons) and in many [[integrable systems]] like the [[sine-Gordon equation]], KdV and the nonlinear Schroedinger equation. The inverse scattering method in those cases can be interpreted as the existence of a certain nonlinear analogue of the Fourier transform (the spectral transform) for the nonlinear wave solutions. 

The [[quantum mechanics]], when described mathematically via the solutions of a time-dependent Schroedinger equation, is a wave mechanics where the modulus square of the amplitude is interpreted as the density of probability to find the particle in the corresponding position. Linear superposition is thus one of the basic features of quantum mechanics. 

## Related concepts

* [[plane wave]], [[wave vector]]

* [[harmonic analysis]], [[Fourier analysis]]

* [[oscillation]], 

* [[semiclassical approximation]]

* [[geometrical optics]]

* [[soliton]]

* [[Stokes phenomenon]]

* [[Berry's phase]].

* [[wave function]]

## References

* [[Howard Georgi]], *The Physics of Waves*, Prentice Hall (1993) $[$[web](https://www.people.fas.harvard.edu/~hgeorgi/new.htm), [pdf](https://www.people.fas.harvard.edu/~hgeorgi/onenew.pdf)$]$

[[!redirects waves]]

[[!redirects wave mechanics]]
