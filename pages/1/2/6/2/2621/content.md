#Idea#

_Perturbation theory_ is a method to make sense of and handle the [[path integral]] involved in the [[quantization]] of [[classical field theory]] to [[quantum field theory]].

It is based on the observation that the [[quantization]] of free [[classical field theory|classical field theories]], whose [[action functional]] contains only the kinetic term, is well understood, and that therefore the quantization of a functional consisting of a kinetic term and polynomial interaction terms may be expanded like a [[Taylor series]] in the interaction terms thus yielding what looks like a series of [[correlator]]s in a free field theory. If the **coupling constant** -- the parameter in fron of the interaction terms -- is small enough, one says one is in the _weakly coupled regime_ of the theory and expects this perturbation series to approximate the desired answer. Usually, even for that to work the [[action functional]] first has to be subjected to [[renormalization]].

#More details#

Suppose we're working with a quantum system that's nearly a [[quantum harmonic oscillator]], but not quite; that is, the quadratic potential $V_0 = \frac{1}{2}k x^2 - \frac{1}{2}$ is only a good local approximation to the real potential $V_0 + \lambda V$.  Then we can write the total as $H = H_0 + \lambda V,$ where $V$ is a function of position and momentum, or equivalently of $z$ and $\frac{d}{dz},$ and $\lambda$ is small.

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

[[!redirects Feynman perturbation series]]