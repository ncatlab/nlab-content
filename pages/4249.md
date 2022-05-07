

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


# Mass
* table of contents
{: toc}


## Definitions

The __mass__ of a [[physics|physical]] system is its intrinsic [[energy]].

It is a somewhat arbitrary choice, made necessary by the theory of [[relativity]], to decide whether the old term 'mass' should be used for intrinsic energy or total energy; one may clarify that intrinsic energy is __rest mass__ while total energy is __relativistic mass__.

Traditionally, mass and energy are measured in different units related by the [[speed of light]]: $E = m c^2$.  Thus one may call a system\'s mass its __rest energy__ when it is measured in units of energy; conversely, one may call a systems\'s total energy its __relativistic mass__ when it is measured in units of mass.

The __[[kinetic energy]]__ of a system is the difference between its total energy and its mass (or rest energy).  Thus the kinetic energy is the energy due to the motion of the system (or better, due to the relative motion of the system and the observer).

When a system is thought of as the combination of several [[subsystem]]s, then its mass also may be broken into several pieces:

*  for each subsystem, its mass,
*  for each subsystem, its kinetic energy due to relative motion of the subsystem,
*  for each pair of subsystems, the [[potential energy]] of their interaction.

The latter entry may be positive (in which case the system is liable to separate into its component parts, at least at sufficiently high [[temperature]], giving off energy) or negative (in which case the system is __bound__ and can be expected to remain together until additional energy is added).


## Formulas

Mass $m$ may be given in terms of energy $E$ and [[linear momentum]] $\mathbf{p}$ as
$$ m = \sqrt {E^2 - {|\mathbf{p}|}^2} .$$
As $\mathbf{p} = E \mathbf{v}$ for $\mathbf{v}$ the linear [[velocity]], we also have
$$ m = E \sqrt {1 - {|\mathbf{v}|}^2} .$$
(For nonrelativistic units, change $E$ to $E/c^2$, $\mathbf{p}$ to $\mathbf{p}/c$, and $\mathbf{v}$ to $\mathbf{v}/c$.)

For a particle travelling at the [[speed of light]], we therefore have $m = 0$.  When $\mathbf{v} = 0$, we have $m = E$.  When $0 \lt {|\mathbf{v}|} \ll c$, we still have $ m \approx E$.  However, in nonrelativistic physics, it is much more useful to use [[kinetic energy]] $K = E - m$ instead of the total energy $E$; then we have
$$ m = K \frac { 1 - {|\mathbf{v}|}^2 + \sqrt {1 - {|\mathbf{v}|^2}} } { {|\mathbf{v}|}^2 } $$
exactly and
$$ m \approx 2 \frac K { {|\mathbf{v}|}^2 } $$
when $0 \lt {|\mathbf{v}|} \ll c$.  Notice that this last expression makes sense already in nonrelativistic units.

For a system made up of subsystems (indexed by $i,j,\ldots$), we have
$$ m = \sum_i m_i + \sum_i \tilde{K}_i + \sum_{i,j} U_{i,j} ,$$
where $m_i$ is the mass of subsystem $i$, $\tilde{K}_i$ is the kinetic energy of subsystem $i$ relative to the whole system, and $U_{i,j}$ is the potential energy of the [[forces]] between system $i$ and system $j$.  The sum
$$ - \sum_{i,j} U_{i,j} = \sum_i m_i + \sum_i \tilde{K}_i - m $$
is the __[[binding energy]]__ of the system; when it is positive, it gives the minimum energy that must be added to the system to break it into components that do not interact.  In many cases, the relative kinetic energies $\tilde{K}_i$ are negligible, so we can calculate binding energy by subtracting masses as
$$ - \sum_{i,j} U_{i,j} \approx \sum_i m_i - m .$$
In nonrelativistic physics, where kinetic energy is always negligible, the $U_{i,j}$ are *also* negligible compared to the masses, so it is not possible at all to calculate the sign of the binding energy using masses.  Instead, we have
$$ m \approx \sum_i m_i ,$$
the statement of nonrelativistic __conservation of mass__.

Many of the formulas above rely on ${|\mathbf{v}|} \leq c$, or equivalently ${|\mathbf{p}|} \leq E$.  For [[tachyon]]s, where this is violated, the mass becomes an [[imaginary number]].  For this reason, it may make more sense to work with $m^2$ (which is always real) than with $m$ itself.  We also implicitly assume that $E \gt 0$; for [[exotic particle]]s in which $E \lt 0$, it is convenient also to take $m \lt 0$.  (In this case, of course, it is *not* sufficient to work only with $m^2$.)

## Related entries

* [[Higgs mechanism]]

* [[ADM mass]]

* [[massive Yang-Mills theory]]

* [[space]], [[time]]

* [[spacetime]]

[[!include fundamental scales -- contents]]



[[!redirects mass]]
[[!redirects masses]]

[[!redirects rest mass]]
[[!redirects rest masses]]
