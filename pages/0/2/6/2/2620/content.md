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
This way of representing the state of a QHO is known as the "Fock basis".

Now suppose that we don't have the ideal system, that the quadratic potential $V_0 = \frac{1}{2}kx^2 - \frac{1}{2}$ is only a good local approximation to the real potential $V_0 + \lambda V$.  Then we can write the total as $H = H_0 + \lambda V,$ where $V$ is a function of position and momentum, or equivalently of $z$ and $\frac{d}{dz},$ and $\lambda$ is small.

Now we solve Schr&#246;dinger's equation perturbatively.  We know that
\[\psi(t) = e^{-itH} \psi(0),\]
and we assume that
\[e^{-itH}\psi(t) \approx e^{-itH_0} \psi(t)\]
so that it makes sense to solve it perturbatively.  Define
\[\psi_1(t) = e^{itH_0} e^{-itH}\psi(t)\]
and
\[V_1(t) = e^{itH_0} \lambda V e^{-itH_0}.\]
After a little work, we find that
\[\frac{d}{dt}\psi_1(t) = -i V_1(t) \psi_1(t),\]
and integrating, we get
\[\psi_1(t) = -i\int_0^t V_1(t_0) \psi_1(t_0) dt_0 + \psi(0).\]
We feed this equation back into itself recursively to get
\[\array{ \psi_1(t) & = & -i \int_0^t V_1(t_0) \left[-i\int_0^{t_0} V_1(t_1) \psi_1(t_1) dt_1 + \psi(0) \right] dt_0 + \psi(0) \\ & = & \left[\psi(0)\right] + \left[\int_0^t i^{-1} V_1(t_0)\psi(0) dt_0\right] + \left[\int_0^t\int_0^{t_0} i^{-2} V_1(t_0)V_1(t_1) \psi_1(t_1) dt_1 dt_0\right] \\ & = & \sum_{n=0}^{\infty} \int_{t \ge t_0 \ge \ldots \ge t_{n-1} \ge 0} i^{-n} V_1(t_0)\cdots V_1(t_{n-1}) \psi(0) dt_{n-1}\cdots dt_0 \\ & = & \sum_{n=0}^{\infty} (-\lambda i)^n \int_{t \ge t_0 \ge \ldots \ge t_{n-1} \ge 0} e^{-i(t-t_0)H_0} V e^{-i(t_0-t_1)H_0} V \cdots V e^{-i(t_{n-1}-0)H_0} \psi(0) dt_{n-1}\cdots dt_0. }\]
So here we have a sum of a bunch of terms; the $n$th term involves $n$ interactions with the potential interspersed with evolving freely between the interactions, and we integrate over all possible times at which those interactions could occur.

Here's an example Feynman diagram for this simple system, representing the fourth term in the sum above:
<p style="text-align:center;"><img src="http://reperiendi.wordpress.com/files/2009/10/3.gif" alt="Three interactions with the perturbation." title="3" width="10" height="200" class="size-full wp-image-798" /></p>
The lines represent evolving under the free Hamiltonian $H_0$, while the dots are interactions with the potential $V$.

As an example, let's consider $V = (z + \frac{d}{dz})$ and choose $\lambda = \frac{1}{\sqrt{2}}$ so that $\lambda V = p.$  When $V$ acts on a state $\psi = z^n,$ we get $V \psi = z^{n+1} + nz^{n-1}.$  So at each interaction, the system either gains a photon or changes phase and loses a photon.