"Harmonic oscillator" is a fancy name for a rock on a spring.  The force exerted by a spring is proportional to how far you stretch it:
\[F = kx.\]
The potential energy stored in a stretched spring is the integral of that:
\[V_0 = \frac{1}{2}kx^2 + C,\]
and to make things work out nicely, we're going to choose $C = -1/2.$  The total energy $H_0$ is the sum of the potential and the kinetic energy:
\[H_0 = V_0 + T = \frac{1}{2}kx^2 + \frac{1}{2}mv^2 - \frac{1}{2}.\]
By choosing units so that $k = m = 1,$ we get
\[H_0 = \frac{x^2}{2} + \frac{p^2}{2} - \frac{1}{2},\]
where $p$ is momentum.

Next we quantize, getting a quantum harmonic oscillator, or QHO.  We set $p = -i \frac{\partial}{\partial x},$ taking units where $\hbar = 1.$  Now 
\[\array{ [x, p]x^n & = & xp - px \\ & = &(- x i \frac{\partial}{\partial x} + i \frac{\partial}{\partial x} x)x^n \\ & = & -i(nx^n - (n+1)x^n) \\ & = & ix^n. }\]

If we define a new observable $z = \frac{p + ix}{\sqrt{2}},$ then 
\[\array{ z z^* & = & \frac{(p + ix)}{\sqrt{2}} \frac{(p - ix)}{\sqrt{2}} \\ & = & \frac{1}{2}(p^2 + i(xp - px) + x^2) \\ & = & \frac{1}{2}(p^2 -1 + x^2) \\ & = & H_0. }\]
We can think of $z^*$ as $\frac{d}{dz}$ and write the energy eigenvectors as polynomials in $z:$
\[H_0 z^n = z \frac{d}{dz} z^n = n z^n.\]  
The creation operator $z$ adds a photon to the mix; there's only one way to do that, so $z\cdot z^n = 1 z^{n+1}.$  The annihilation operator $\frac{d}{dz}$ destroys one of the photons; in the state $z^n$, there are $n$ photons to choose from, so $\frac{d}{dz} z^n = n z^{n-1}.$

Schr&#246;dinger's equation says $i \frac{d}{dt} \psi = H_0 \psi,$ so 
\[\psi(t) = \sum_{n=0}^{\infty} e^{-itn} a_n z^n.\]
This way of representing the state of a QHO is known as the _Fock basis_.

[Baez](John+Baez)'s [Fall '03](http://math.ucr.edu/home/baez/qg-fall2003/) Quantum gravity seminar relates wavefunctions expressed in the Fock basis to [[structure types]].