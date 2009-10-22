Momentum is, according to [[Isaac Newton|Newton]], the 'amount of motion' in an object.  For particles it is  proportional to the object\'s [[mass]] and to its [[velocity]], and thus measured in units of mass times velocity. For photons it is proportional to the frequency of the photon. 


In [[Lagrangean mechanics]] (including relativistic and quantum versions), to every (generalized) coordinate $q_i$ one associates a (generalized) momentum 
$$
p_i = \frac{\partial L}{\partial \dot{q}^i}
$$
where $L$ is the [[Lagrangean]] of the system.  More generally, we can say that $p_i$ is the coordinate of $\mathrm{d}q^i$ in the [[action functional|action form]].

If $L$ takes the form $\frac{1}{2} \sum_i m_i \dot{q}_i^2 - U(q_1,\ldots,q_n)$, then we have $p_i = m_i \dot{q}_i$.  Thus, the __linear momentum__ of a point particle in Newtonian mechanics is traditionally *defined* as the intrinsic [[mass]] $m$ times the [[velocity]] $\vec{\dot{q}}$.  However, this breaks down in some situations:

*  Relativistically, the velocity factor is more complicated (tending to $\infty$ as velocity tends to the [[speed of light]]).  However, it is possible to keep $p = m v$ using a velocity-dependent relativistic mass (especially since the mass may depend on other dynamical considerations).

   +-- {: .query}
   Zoran: still with rescaled mass the space-components of the momentum are mass times velocity. Of course one can talk about 4-momentum as well but this is a different issue. 

   _Toby_:  True, but the modern use of 'mass' is for the *intrinsic* property of a particle, so this is not true.  The rescaled ('relativistic') mass varies with speed, so we don\'t capture the dependence of momentum on velocity by saying that they are proportional.

    Zoran: well for the trivial purposes like the tables of particles of course zero-velocity mass is used. But if we are talking about the laws of MECHANICS and basics of these notions than the the mass does really depend on the dynamics, not only in relativity but even for quasiparticles in condensed matter physics. If you call by modern textbooks for cooks it may be true, but among us theoretical physicists, the mass is defined by the peculiarities of the dynamics, it is subject to renormalization, which will in QFT in general depend even on the temperature. 

   _Toby_:  OK, what do you think about it now?
   =--

*  In the presence of velocity-dependent forces (notably those produced by a [[magnetic field]]), there is an additional position-dependent term.
*  In nonlinear coordinates (such as for [[angular momentum]]), one not only needs to use a nonlinear velocity (such as [[angular velocity]]) but also replace mass with something more complicated (such as [[moment of inertia]]) which is often position-dependent.


In [[Hamiltonian mechanics]], the momentum coordinates are half of the basic coordinates on [[phase space]].  If phase space is derived as the [[cotangent bundle]] of a [[configuration space]], then the momentum coordinates are the new coordinates on the cotangent bundle, dual to the original coordinates on configuration space; we have the [[symplectic form]] $\sum_i p_i \mathrm{d}q^i$.  However, Hamiltonian mechanics cares only about phase space as a [[symplectic manifold]] with a [[Hamiltonian]]; there is no inherent distinction between position and momentum coordinates, and you can even make a [[canonical transformation]] that swaps them (up to a minus sign).

+-- {: .query}
Zoran: there is no a priori way in general to tell which ones are momentum coordinates. There is no way to tell. This depends on choice of coordinates. Phase space is a symplectic manifold and you can make a canonical transformation where momenta become positions and positions minus momenta and the same equations of motion. IF THE SPACE IS TRANSLATION HOMOGENEUOUS then the momenta conjugate to the positions in that space are the conserved quantities. So in this sense in that special case, the "usual" momenta are distinguished.

_Toby_:  Do you like how it is written now?

Z: Yes, it is correct. I only changed canonical coordinate transformation to more customary canonical transformation. 
=--


In [[quantum mechanics]], the [[canonical quantization]] process formally replaces momentum by $-i \hbar \frac{\partial}{\partial x},$ where $x$ is position.  (Equivalently, in [[momentum space]], canonical quantization replaces $x$ by $i \hbar \frac{\partial}{\partial p}.)$  In this situation, position and momentum [[canonical commutation relation|fail to commute]].
