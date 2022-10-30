
# Energy
* table of contents
{: toc}

## Idea

In [[physics]], the __energy__ of a [[physical system]] is one of its most basic [[observable]] properties, an [[extensive quantity]] roughly measuring how much stuff is in the system.

The term 'energy' is also used in [[Riemannian geometry]] and [[statistics]] in vague analogy with the concept from physics.


## Conservation

As a system [[time evolution|evolves]] without interacting with its environment, its energy remains constant.  If different systems [[interaction|interact]], then they may exchange energy, but the total energy remains constant; equivalently, we may combine the interacting systems into a supersystem whose energy is the sum of the energies of its parts, and this supersystem's energy is conserved.

Through [[Noether's theorem]], conservation of energy corresponds to [[time]] invariance.  If a system\'s equations of motion are *not* invariant with time, then the system will not exhibit energy conservation, and physically we conclude that the system must be interacting with something else.

In [[continuum physics]], conservation of energy may be treated locally: the change in energy in any region over a period of time must equal the total flux of energy through the region\'s boundary over that time.  In [[general relativity]], this makes sense (in general) only as a [[differential equation]] involving both the [[stress-energy tensor]] and the [[Levi-Civita connection]].


## Relationship to mass

Energy is distinguished from [[mass]] in various ways:

*  __Relativistic mass__ is the same as energy, although conventionally measured in different [[unit of measurement|units]].  We have $E = m c^2$ in conventional units, or simply $E = m$ in units where the [[speed of light]] is $c = 1$.

*  __[[rest mass|Rest mass]]__ (the usual meaning of 'mass' in modern physics) is the minimum energy inherent in a system; whereas energy is relative, rest mass is absolute.  Here we have
   \[ E = m c^2 \sqrt{1 - \frac {v^2} {c^2}} \label{emcg} \]
   in conventional units, or
   \[ E = m \sqrt{1 - v^2} \label{emg} \]
   if $c = 1$.

*  In the non-relativistic limit, energy splits into two independently conserved quantities: mass (relativistic or rest, it makes no difference) and energy proper.  That is, expanding (eq:emcg) as a [[power series]] in $v$, we have
   $$ E = m c^2 + \frac 1 2 m v^2 + \frac 3 8 m \frac {v^4} {c^2} + \cdots ;$$
as $c \to \infty$, this splits into the quantities $m$, $(1/2) m v^2$, $(3/8) m v^4$, etc.  The first of these is the non-relativistic mass, the second is the [[kinetic energy]] $K$, the next is simply $3 K^2 / 2 m$, and all subsequent terms are also determined by $m$ and $K$.

   However, the kinetic energy $K$ is not the *total* energy in non-relativistic physics.  Any entities with a rest mass of $0$ (or approaching zero in the limit) will still have energy and so must be treated separately from kinetic energy (which is proportional to mass).  Non-relativistically, these may be viewed as [[field theory|fields]] with energy of their own, or (if the field strengths are derived entirely from interacting massive bodies) this energy may be attributed to the massive bodies in the system as [[potential energy]].  Thus the total energy of the system is $E = K + U$, where $K$ is total kinetic energy and $U$ is total potential or field energy.


## Relationship to momentum

In relativistic physics, energy is relative, the timelike part of a [[4-vector]] quantity whose spacelike parts comprise [[linear momentum]].  If we also take into account the distribution of energy and momentum across space, this give a symmetric second-rank [[tensor]], the [[stress-energy tensor]].

Even in non-relativistic physics, there is an analogy between energy and linear momentum.  In [[Hamiltonian mechanics]], both energy and linear momentum are examples of [[generalized momentum|generalised momenta]]; energy corresponds to [[time]] while linear momentum corresponds to position in [[physical space|space]].  However, the special treatment accorded to time and energy in the usual formulation of Hamiltonian mechanics obscures this; we also have (oddly) that the precise generalised momentum corresponding to the time variable $t$ is not the total energy $H$ but $-H$ instead.

This analogy from [[classical mechanics]] also applies to [[quantum mechanics]] and is particularly evident in Schr&#246;dinger's original formulation of his quantum theory.


## In general relativity

In [[general relativity]], the concept of total energy of a system does not make sense, except in certain special cases.  General relativity is a [[field theory]] in which energy appears only as one of $10$ (or $({n \atop 2})$ in $n$ [[dimensions]] of [[spacetime]]) independent components of the [[stress-energy tensor]].  Mathematically, it makes no sense to integrate just this component over a region of space to determine a total energy in that region.  This makes it difficult to interpret general relativity in frameworks such as [[Hamiltonian mechanics]] and [[thermodynamics]] where energy is a primary concept.  This is called the [[problem of time]] (since energy and [[time]] are conjugate observables and the problem occurs with both).


[[!redirects energy]]
[[!redirects energies]]

[[!redirects relativistic mass]]
[[!redirects relativistic masses]]
