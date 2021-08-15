
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
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

In [[quantum field theory]] with chiral [[fermions]] ([[spinor fields]]) $\psi$ with _chiral version of the [[Dirac current]]_ $J = i \bar \Psi \Gamma \Psi$, a _chiral anomaly_ is a non-[[conserved current|conservation]] of this current

$$
  div J = Anomaly
  \,.
$$

(See at _[[Ward identity]]_.)

In the [[standard model of particle physics]] this happens and plays a role for [[pion]] decay and for [[baryogenesis]]. Here the current is the [[baryon current]] and the anomaly term is the Pontryagin 4-form $Anomaly = \langle F_\nabla \wedge F_\nabla\rangle$ of the [[gauge field]] $\nabla$, hence the [[curvature]] 4-form of the corresponding [[Chern-Simons line 3-bundle]].

If there are [[instantons]], i.e. if the [[gauge field]] [[principal connection]] $\nabla$ has a nontrivial underlying [[principal bundle]], then also the [[Chern-Simons line 3-bundle]] is topologically nontrivial the anomaly term $\langle F_\nabla \wedge F_\nabla\rangle$ is a non-exact integral form, hence the above equation is to be read as the _local_ expression identifying $\star j$ with the local [[3-connection]] on the CS 3-bundle.

## Properties

### Relation between Chiral anomaly, Skyrme model, Baryon current and WZ-term

The "topological"-part $B_{top}$ of the [[baryon]] [[current]] (the piece that is not generally [[conserved current|conserved]], reflecting the [[chiral anomaly]]), is the [[Wess-Zumino-Witten term]] of the [[exponentiated pion field]]:

\[
  \label{ExponentiatedPionField}
  e^{i \vec \pi/f_\pi}
  \;\colon\;
  \mathbb{R}^{0,1} \times (\mathbb{R}^3)^{cpt}
  \;=\;
  \mathbb{R}^{0,1} \times S^3
  \longrightarrow
  S^3 
  \simeq
  SU(2)
\]


$$
  \begin{aligned}
  B_{top}
  & \coloneqq \;
  Tr
  \big( 
    ( e^{-i \vec \pi/f_\pi} d e^{i \vec \pi/f_\pi} )
    \wedge
    ( e^{-i \vec \pi/f_\pi} d e^{i \vec \pi/f_\pi} )
    \wedge
    ( e^{-i \vec \pi/f_\pi} d e^{i \vec \pi/f_\pi} )
  \big)
  \\
  & =\;
  \big\langle
    (e^{i \vec \pi/f_\pi})^\ast(\theta)
    \wedge
    (e^{i \vec \pi/f_\pi})^\ast(\theta)
    \wedge
    (e^{i \vec \pi/f_\pi})^\ast(\theta)
  \big\rangle
  \;\;\in\;
  \Omega^3(\mathbb{R}^{3,1})
  \end{aligned}
$$

Here the expression in the first line uses the fact that [[SU(2)]] is a [[matrix group]], while the second line exporesses the same via [[pullback of differential forms|pullback]] of the [[Maurer-Cartan form]] $\theta$ from the group manifold.


The [[homotopy class]] of the [[exponentiated pion field]] (eq:ExponentiatedPionField), as a [[continuous function]], is an element of the ([[cohomotopy|co-]])[[homotopy group of spheres]] $\pi_3(S^3) \simeq \pi^3(S^3) \simeq \mathbb{Z}$, is the [[Skyrmion]]-number, or, in fact, the [[baryon]]-number, encoded in the [knotted stucture](On+Vortex+Atoms#RanadaTrueba01) of the pion field.

\linebreak

See also [physics.stackexchange.com/a/306242/5603](https://physics.stackexchange.com/a/306242/5603)

## Related concepts

* [[chiral perturbation theory]]

## References

### General

The orginal observation is due to

* [[Stephen Adler]]. _Axial-Vector Vertex in Spinor Electrodynamics_, Physical Review 177 (5): 2426. (1969)

* [[John Bell]], [[Roman Jackiw]], _A PCAC puzzle: $\pi^0 \to \gamma \gamma$ in the &#963;-model". Il Nuovo Cimento A 60: 47. (1969)

A detailed mathematical derivation is in

* [[Luis Alvarez-Gaumé]], [[Paul Ginsparg]], section 3 of: _The structure of gauge and gravitational anomalies_ , Ann. Phys. 161 (1985) 423. ([spire](http://inspirehep.net/record/202565/?ln=en))

Detailed argument for the [[theta vacuum]] ([[Yang-Mills instanton]] vacuum) from chiral symmetry breaking is offered in 

* [[Curtis Callan]], R.F. Dashen, [[David Gross]], _The Structure of the Gauge Theory Vacuum_, Phys.Lett. 63B (1976) 334-340 ([spire](http://inspirehep.net/record/3673?ln=en))

* G. Morchio, [[Franco Strocchi]], _Chiral symmetry breaking and theta vacuum structure in QCD_, Annals Phys.324:2236-2254, 2009 ([arXiv:0907.2522](https://arxiv.org/abs/0907.2522))

Textbook account:

* [[Robert E. Marshak]], Chapter 7 of: *Conceptual Foundations of Modern Particle Physics*, World Scientific 1993 ([doi:10.1142/1767](https://doi.org/10.1142/1767))

Further review:

* [[Raphael Flauger]], _Anomalies and the Atiyah-Singer Index Theorem_ ([pdf](http://www.ma.utexas.edu/~dafr/Index/Flauger.pdf))

* [[Jeffrey Harvey]], section 1 and 3.6 of _TASI 2003 Lectures on Anomalies_ ([arXiv:hep-th/0509097](http://arxiv.org/abs/hep-th/0509097))

* B.L.Ioffe, _Axial anomaly: the modern status_, Int. J. Mod. Phys. A21:6249-6266,2006 ([arXiv:hep-ph/0611026](http://arxiv.org/abs/hep-ph/0611026))

* {#Jackiw08} [[Roman Jackiw]], _Axial anomaly_, (2008), Scholarpedia, 3(10):7302. ([web](http://www.scholarpedia.org/article/Axial_anomaly))

* Wikipedia, _[Chiral anomaly](http://en.wikipedia.org/wiki/Chiral_anomaly)_

Discussion in the rigorous context of [[causal perturbation theory]]/[[perturbative AQFT]] is (for $m \gt 0$) in 

* {#Scharf95} [[Günter Scharf]], section 5.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

and (for $m = 0$) in

* {#Duetsch92} [[Michael Dütsch]], F. Krahe, [[Günter Scharf]], _Axial Anomalies in Massless Finite QED_, N. Cimento A 105 (3) (1992), 399–422. 

and reviewed in the context the [[master Ward identity]] in

* [[Michael Dütsch]], around p. 331 in _[[From classical field theory
to perturbative quantum field theory]]_, 2018


Application to [[baryogenesis]] is due to

* {#Hooft76} [[Gerard 't Hooft]], _Symmetry Breaking through Bell-Jackiw Anomalies_ Phys. Rev. Lett. 37 (1976) ([pdf](http://www.staff.science.uu.nl/~hooft101/gthpub/symm_br_bell_jackiw.pdf))


* [[Gerard 't Hooft]], _Computation of the quantum effects due to a four-dimensional pseudoparticle_, Phys. Rev. D14:3432-3450 (1976).





[[!include WZW term of QCD chiral perturbation theory -- references]]





[[!redirects chiral anomalies]]


[[!redirects axial anomaly]]
[[!redirects axial anomalies]]

