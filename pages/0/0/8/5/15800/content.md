
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
## Idea

In [[cosmology]] and [[particle physics]],  by _baryogenesis_ one refers to the process by which an abundance of [[baryons]] is produced in the early [[observable universe]], leading to the baryonic [[matter]] seen all around. Since in the [[standard model of particle physics]] [[matter]] and [[antimatter]] are _essentially_ always produced symmetrically ("conservation of baryon number"), the topic of baryogenesis is to a large extent the study of how the matter/antimatter symmetry may be [[broken symmetry|broken]].

([Sakharov 67](#Sakharov67)) formulated three conditions jointly necessary for matter/antimatter asymmetry leading to baryogenesis in the early universe, now known as the _Sakharov conditions_

1. violation of baryon number conservation;

1. [[CP problem|C and CP violation]]

1. departure from thermal equilibrium.

Indeed, by a [[quantum anomaly]] in the [[standard model of particle physics]], the _[[axial anomaly]]_ (a [[chiral anomaly]]) (see e.g. [Jackiw 08](#Jackiw08)),  the [[divergence]] of the baryon number [[current]] does not quite vanish but is ([t'Hooft 76](#Hooft76)) in traditional physics notation

$$
  \partial_\mu j_b^\mu 
   = 
  \partial_\mu j_L^\mu
   =
  n_f
  \left(
    \frac{g^2}{32 \pi^2}
    W_{\mu \nu}^\alpha \tilde W^{\alpha \mu \nu}
    -
    \frac{{g'}^2}{32\pi^2} \epsilon_{\mu \nu \rho \sigma} F^{\mu \nu} F^{\rho \sigma}
  \right) 
 \,,
$$

where $F_\nabla$ is the [[field strength]] of the [[electroweak field]] (the [[curvature]] of a $SU(2)$-[[principal connection]] $\nabla$).

(see  e.g. [Dine 90, (4)](#Dine90) [Trodden-Carroll, 4.9.3](#TroddenCarroll), [Shu 08, (7.6)](#Shu08)).

In more intrinsic notation and ignoring numerical constants, the statement is that 

$$
  \mathbf{d} \star j_b = \langle F_\nabla \wedge F_\nabla \rangle
  \,.
$$

Properly interpreted (see at _[Yang-Mills instanton -- from the correct maths to the traditional physics story](Yang-Mills instanton#FromTheMathsToThePhysicsStory)_) this is the _local_ expression for the [[connection on a 3-bundle|3-connection]] on the [[Chern-Simons line 3-bundle]] associated with the gauge field. If the latter is globally nontrivial in that it is in an _[[instanton]]_-sector (has nontrivial [[second Chern class]]), then the [[integral]] of $\langle F\wedge F\rangle$ over closed manifolds is an integer -- the "[[instanton]] number" -- and in conclusion there is baryon generation proportional to this number (physics lingo also: _sphaleron transitions_).

Notice that this would mean that baryons "are" a kind of topological twist, different from, but not entirely unlike to the old idea of _[[On Vortex Atoms]]_. See there at _[Similarlity to concepts of modern particle physics](On+Vortex+Atoms#SimilarityToParticlePhysics)_

That this process was at least one source of baryogenesis in the early universe is plausible but not certain. The process is heavily suppressed by inverse energy/temperature (e.g. [Dine 90, around (9)](#Dine90)) and out of reach of conceivable experiments in the present age of the universe, but plausibly may have occurred in the very early universe -- just as it should be for realistic baryogenesis.


## Exposition
 {#Exposition}

One needs to be careful that the concept of "particle" itself is only well defined on Minkowski spacetime, hence not on cosmological scales. But nevertheless there is a fermion current 3-form $J$, such that its integral 

$$
  Q_\Sigma \coloneqq   \int_\Sigma J \in \mathbb{R}
$$ 

has the interpretation of the total net _charge_ carried by the stuff measured by $J$, hence counts the net  "fermion number" in all of space" as seen by $\Sigma$.

This is familiar from, say, Maxwell's equations, where such a $J$ appears on the right hand side as the electromagnetic source form

$$
  d  \star F = J
  \,.
$$

Now given any such current 3-form, then its de Rham differential $d J$ measures how the charges $Q$ changes as time progresses. Because let $\Sigma_1$ and $\Sigma_2$ be two spatial slices of spacetimes, and $X_4$ a piece of spacetime connecting them, i.e. such that

$$
  \partial X_4 = \Sigma_2 - \Sigma_1
  \,.
$$

Then Stokes's theorem gives that $d J$ is the local change of charge, because:

$$
  \begin{aligned}
    Q_{\Sigma_2} - Q_{\Sigma_1}
    &=
    \int_{\Sigma_2} J - \int_{\Sigma_1} J
    \\
    &=
    \int_{\partial X_4} J
    \\
    & = 
     \int_{X_4} d J
  \end{aligned}
$$

So if $J$ is closed, then total charge is conserved, while if $J$ is not closed, then $d J $ is the local measure for how charge is being "created" or how it disappears.

Now the remarkable fact is that in the standard model of particle physics, $J$ comes out non-closed. It's differetial instead comes out proportial to the 4-form which measures instanton number

$$
  d J \propto \langle F_\nabla \wedge F_\nabla \rangle
  \,.
$$

This is the famous _[[chiral anomaly]]_.

So far this is highlighted in every textbook. But the following further crucial subtlety tends not to be recognized for what it is. 

Namely on cosmological spacetimes that carry [[instantons]], then (as discussed at _[Yang-Mills instanton -- from the correct maths to the traditional physics story](Yang-Mills instanton#FromTheMathsToThePhysicsStory)_) the 4-form $\langle F_\nabla \wedge F_\nabla\rangle$ is not in fact globally exact. The above formulas hold only locally, on a chart of spacetime. But on intersections two such pieces of data need to be glued by a gauge transformation. If we do make the usual simple assumptions (for simplicity of the discussion), then this gauge transformation is that famous "Chern-Simons winding number" $S^3 \to SU(2)$, which they keep handing the physics students without properly explaining it (such as the one who I am reacting to [here](http://physicsoverflow.org/38243/topological-number-integral-theory-boundary-volume-forms)).

As a result, in the presence of instantons, then the integral of $\langle F_{\nabla} \wedge F_{\nabla}\rangle$ may be non-zero on a _closed_ cosmological spacetime.

The usual picture (which you see displayed in many popular accounts) is: imagine a 4d cup $D^4$ (a unit disk thought of as a "cup" cobordism from nothing to $S^3$) where the big bang expands spacetime from nothing. Then glue on something like $S^3 \times LongInterval$ and think of the result as being a simple model for the universe. Then assume some boundary condition saying that far in the future from the big bang the gauge fields $\nabla$ that carry those instantons decay away, hence are [[vanishing at infinity]]. So then for computing the total fermion charge in this universe, we are effectively dealing with its one-point compactification. In the present simple example this is the 4-sphere $S^4$.

So since the four form vanishes "at infinity", we may just as well assume that it is supported on that cup $D^4$ in our model, the neighbourhood of the big bang.

We learn that that:

1. The total net fermion charge in the universe is $\int_{S^4} \langle F_\nabla \wedge F_\nabla\rangle \in \mathbb{Z}$;

1. this fermion number is picked up incrementally increasing from zero (at the origin of our $D^4$-cup, the "big bang singularity) and reaching at "comoving time $t$ \lt 1" the value 

$$
   Q_t
   =
   \int_{D^4_{t}} \langle F_\nabla \wedge F_\nabla\rangle
   = 
   \int_{S^3} J_t  
$$

(where $D^4_t$ is the disk of radius $t \lt 1$).

Then at $t = 1$ (in this paramneterization) the four form goes to zero (and in this fashion eventually extends to a global 4-form on our one-point compactified cosmological spacetime). 

So after the comoving time $t = 1$ there is no net particle creation anymore. Moreover, the net particle number picked up until then is equal to the second Chern class of the cosmological gauge field, hence equal to the number that masure the "knottedness" of the cosmological gauge field (which we here think of as all being concentrated around the big big).

One particle per knottedness of the cosmological gauge field. 



## Related concepts

* [[leptogenesis]]

* [[On Vortex Atoms]]

## References

The original article stating the _Sakharov conditions_ is

* {#Sakharov67} [[Andrei Sakharov]], _Violation of CP invariance, C asymmetry, and baryon asymmetry of the universe_. Journal of Experimental and Theoretical Physics 5: 24&#8211;27. 1967, republished as A. D. Sakharov (1991). _Violation of CP invariance, C asymmetry, and baryon asymmetry of the universe_. Soviet Physics Uspekhi 34 (5): 392&#8211;393. Bibcode:1991SvPhU..34..392S. doi:[10.1070/PU1991v034n05ABEH002497](http://dx.doi.org/10.1070/PU1991v034n05ABEH002497). 1967

The derivation that [[instantons]] lead to baryon number violation is due to

* {#Hooft76} [[Gerard 't Hooft]], _Symmetry Breaking through Bell-Jackiw Anomalies_ Phys. Rev. Lett. 37 (1976) ([pdf](http://www.staff.science.uu.nl/~hooft101/gthpub/symm_br_bell_jackiw.pdf))

* [[Gerard 't Hooft]] _Computation of the quantum effects due to a four-dimensional pseudoparticle_, Phys. Rev. D14:3432-3450 (1976)

A good review of the axial anomaly is in 

* {#Jackiw08} [[Roman Jackiw]], _Axial anomaly_, (2008), Scholarpedia, 3(10):7302. ([web](http://www.scholarpedia.org/article/Axial_anomaly))

and of the resulting [[phenomenology]] of baryon number non-conservation is in

* {#Dine90} [[Michael Dine]], _Baryon number violation at high-energy in the standard model: Fact or fiction?_ Sep 1990 , Review includes ([spire](https://inspirehep.net/record/299206?ln=de), [pdf](http://www.slac.stanford.edu/cgi-wrap/getdoc/ssi90-020.pdf))

* Heidi Kuismanen, section 2 of _Leptogenesis as the origin of matter-antimatter asymmetry in extra dimensionaL and supersymmetric modeLs_ ([[KuismanenBaryogenesis.pdf:file]])

Further review includes

* V.A. Rubakov, [[Mikhail Shaposhnikov]], _Electroweak Baryon Number Non-Conservation in the Early Universe and in High Energy Collisions_, Usp.Fiz.Nauk 166:493-537,1996; Phys.Usp.39:461-502,1996 ([arXiv:hep-ph/9603208](https://arxiv.org/abs/hep-ph/9603208))

* Antonio Riotto, Mark Trodden, _Recent Progress in Baryogenesis_, Ann.Rev.Nucl.Part.Sci.49:35-75,1999 ([arXiv:hep-ph/9901362](http://arxiv.org/abs/hep-ph/9901362))

* Laurent Canetti, Marco Drewes, [[Mikhail Shaposhnikov]], _Matter and Antimatter in the Universe_, New J. Phys. 14 (2012) 095012 ([arXiv:1204.4186](https://arxiv.org/abs/1204.4186))

* Yanagida, _The origin of matter_ ([[YanagidaBaryogenesis.pdf:file]])

* {#TroddenCarroll} Mark Trodden, Sean Carroll, TASI Lectures: Introduction to Cosmology _[4.9 Baryon Number violation](http://ned.ipac.caltech.edu/level5/Sept03/Trodden/Trodden4_9.html)_ 

* {#Shu08} Jing Shu, section 7 of _Connecting LHC Signals with Deep Physics at the TeV Scale and Baryogenesis_ 2008
