
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Aharonov-Bohm effect_ is a configuration of the [[electromagnetic field]] which has vanishing electric/magnetic [[field strength]] (vanishing [[Faraday tensor]] $F = 0$) and but is nevertheless non-trivial, in that the [[vector potential]] $A$ is non-trivial. Since the vector potential affects the [[phase|quantum mechanical phase]] on the [[wavefunction]] of [[electrons]] moving in an electromagnetic field, in such a configuration classical physics sees no effect, but the phase of quantum particles, which may be observed as a [[quantum interference|interference]] pattern on some screen, does.

More technically, a configuration of the [[electromagnetic field]] is generally given by a [[circle]]-[[principal connection]] and an Aharonov-Bohm configuration is one coming from a [[flat connection]], whose [[curvature]]/[[field strength]] hence vanishes, but which is itself globally non-trivial. This is only possible on [[spaces]] ([[spacetimes]]) which have a non-trivial [[fundamental group]], hence for instance it doesn't happen on [[Minkowski spacetime]].

In practice one imagines an idealized [[electric current]]-carrying [[solenoid]] in [[Euclidean space]]. Away from the solenoid itself the [[magnetic field]] produced by it gives such a configuration.

## Details

Let $\mathbb{R}^2 - \{0\}$ be the [[plane]] with the origin removed, and consider the space $(\mathbb{R}^2 - \{0\}) \times \mathbb{R}$ (thought of as 3d [[Cartesian space]] with the z-axis removed) and [[spacetime]] $(\mathbb{R}^2 - \{0\}) \times \mathbb{R}^2$ (thought of as the previous configuration statically moving in time).

For the following argument only the topological structure of the space matters, and nothing needs to explicitly depend on the $z$-[[coordinate]] and the time-coordinate, so for notational simplicity we may suppress these and consider just $\mathbb{R}^2 - \{0\}$.

On this space minus the x-axis consider the [[polar coordinates]]  $(\phi,r)$ with

$$
  x = r cos(\phi)\,,\;\;\; y = r sin(\phi)
  \,.
$$

Accordingly we have the [[differential 1-forms]]

$$
  \mathbf{d}x = cos(\phi)\mathbf{d}r - r sin(\phi) \mathbf{d}\phi
$$

$$
  \mathbf{d}y = sin(\phi)\mathbf{d}r + r cos(\phi) \mathbf{d}\phi
$$

hence 

$$
  \begin{aligned}
    \mathbf{d}\phi 
     & = 
     \frac{1}{r}cos(\phi)\mathbf{d}y - \frac{1}{r}sin(\phi) \mathbf{d}x
     \\
     & = 
     \frac{1}{r^2} x \mathbf{d}y - \frac{1}{r^2} y \mathbf{d}x
  \end{aligned}
  \,.
$$

Here the expression on the right extends smoothly also to the $x$-axis and this extension we call 

$$
  \theta \coloneqq 
  \frac{1}{r^2} x \mathbf{d}y - \frac{1}{r^2} y \mathbf{d}x
  \;\;
  \in \Omega^1(\mathbb{R}^2 - \{0\})
  \,.
$$

From the way this is constructed it is clear that $\theta$ is a closed differential form

$$
  \mathbf{d}\theta = 0
  \,.
$$

However, on $\mathbb{R}^2 - \{0\}$ this is not an exact form. In other words, if one regards $\theta$ as the [[vector potential]] being the configuration of an  [[electromagnetic field]]

$$
  A \coloneqq \theta
$$

then:

1. the [[field strength]] vanishes $F = \mathbf{d}A = 0$;

1. but there is no [[gauge transformation]] relating $A$ to the trivial field configuration.

This is possible because $\mathbb{R}^2 - \{0\}$ is not [[simply connected topological space|simply connected]] and hence the [[Poincaré lemma]] does not apply.

## Related concepts

* [[fiber bundles in physics]]

* [[Dirac charge quantization]], [[magnetic monopole]]

* [[cosmic topology]]

* anyonic [[braid group statistics]] as Aharanov-Bohm effect for a *[[fictitious gauge field]]*

## References

The effect was first predicted by

* W. Ehrenberg, R. E. Siday, *The Refractive Index in Electron Optics and the Principles of Dynamics*,  Proceedings of the Physical Society. Section B, **62** 8 (1949) 1 &lbrack;[doi:10.1088/0370-1301/62/1/303](https://iopscience.iop.org/article/10.1088/0370-1301/62/1/303)&rbrack;

It is named after:

* [[Yakir Aharonov]], [[David Bohm]], *Significance of Electromagnetic Potentials in the Quantum Theory*, Phys. Rev. **115** (1959) 485 &lbrack;[doi:10.1103/PhysRev.115.485](https://doi.org/10.1103/PhysRev.115.485), [pdf](https://journals.aps.org/pr/pdf/10.1103/PhysRev.115.485)&rbrack;


Early discussion with emphasis of the role of [[connection on a bundle|connections]] on [[fiber bundles in physics]] and generalization to non-abelian [[Yang-Mills theory]]:

* [[Tai Tsun Wu]], [[Chen Ning Yang]], *Concept of nonintegrable phase factors and global formulation of gauge fields*, Phys. Rev. D **12** (1975) 3845 &lbrack;[doi:10.1103/PhysRevD.12.3845](https://doi.org/10.1103/PhysRevD.12.3845)&rbrack;

In relation to [[superselection sectors]]:

* [[Claudio Dappiaggi]], [[Giuseppe Ruzzi]], Ezio Vasselli: *Aharonov-Bohm superselection sectors*, Lett Math Phys **110**  (2020) 3243–3278 &lbrack;[doi;10.1007/s11005-020-01335-4](https://doi.org/10.1007/s11005-020-01335-4), [arXiv:, 1912.05297](https://arxiv.org/abs/1912.05297)&rbrack;



See also:

* L. Mangiarotti, [[Gennadi Sardanashvily]], section 6.6 of _Connections in Classical and Quantum Field Theory_, World Scientific, 2000

* [[Mikio Nakahara]], Section 10.5.3 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


* Wikipedia, _[Aharonov-Bohm effect](https://en.wikipedia.org/wiki/Aharonov%E2%80%93Bohm_effect)_
