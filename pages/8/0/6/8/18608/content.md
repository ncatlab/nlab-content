
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The _Yang-Mills Mass Gap problem_ is an open conceptual problem in the [[quantization of Yang-Mills theory]] (cf. general *[[spectral gaps]]* of [[quantum systems]]), closely related to what in the [[phenomenology]] of [[quantum chromodynamics]] is called the _[[confinement]]_ of [[quarks]], hence the existence of [[hadron|hadronic]], in particular [[baryon|baryonic]] [[matter]] at ordinary (non-excessive) [[temperatures]].

The [[Lagrangian]] for [[Yang-Mills theory]] coupled to [[fermion fields]] (such as for [[QCD]]) makes manifest (only) the existence of [[mass]]-less [[quarks]] and [[gluons]]. Indeed, at very high [[temperature]] [[QCD]] is thought to exhibit a [[quark-gluon plasma]] well described by these degrees of freedoms.

But at comparatively smaller [[temperature]] it is observed in [[experiment]] as well as in [[lattice QCD]] [[computer experiment]] that [[QCD]] exhibits _[[confinement]]_, meaning that the low energy states of the theory are not free massless quarks and gluons anymore, but that these form [[bound states]] in the form of [[hadrons]] (including, notably, [[protons]] and [[neutrons]], and hence all the ordinary [[baryon|baryonic]] [[matter]] of the [[observable universe]]). 

The existence of massive [[hadron]]-[[bound states]] in low-energy [[QCD]] is thus well-established [[phenomenology|phenomenologically]], but it is as yet lacking a conceptual theoretical explanation.

The _mass gap problem_ is the problem in [[mathematical physics]] to demonstrate theoretically (i.e. not just by [[lattice QCD|computer simulation]]) the existence of this mass gap/[[confinement]]-phenomenon in [[QCD]] and in [[Yang-Mills theory]] coupled to [[fermion fields]] in general.

This issue is well and widely known in the [[particle physics]]-community, see for instance [Kutschke 96, Section 3.1](#Kutschke96), [INFN 15](#INFN15). It gained more attention among the [[mathematics]]/[[mathematical physics]]-community when the [Clay Mathematics Institute](http://www.claymath.org/) declared the problem to be one in a list of "[Millennium Problems](http://www.claymath.org/millennium-problems)", see [Jaffe-Witten 2000](#JaffeWitten00), [Douglas 04](#Douglas04).

In contrast to the other Millennium problems, the Yang-Mills mass gap problem is more wide-ranging, since the issue is not primarily to perform a complicated deduction in an otherwise well-understood theoretical framework, but to establish such a theoretical backdrop in the first place:

Namely [[confinement|confined]] [[QCD]] is "strongly coupled", meaning that common methods of [[perturbative quantum field theory]] do not apply: What is needed to even state the mass gap problem with precision is first a formulation of [[Yang-Mills theory]] as a [[non-perturbative quantum field theory]] -- which is generally a wide open problem for interacting field theories in $D = 4$ [[spacetime]] [[dimensions]]. 

While there exist several models for the [[quantum hadrodynamics]] in [[confinement|confined]] [[QCD]] ([[chiral perturbation theory]], [[Skyrmions]], ...) these are more or less *ad hoc* phenomenological models not actually derived from a "microscopic" theory like [[Yang-Mills theory]] and hence tend to assume the mass gap more than explaining it.

A more fundamental approach to [[confinement|confined]] [[QCD]]/[[Yang-Mills theory|YM]] is *[[holographic QCD]]*, where notably the [[Skyrmion|Skyrme]] model with its predicted [[baryon]] [[masses]] appears as an emergent effect. 


## Related pages

* [[spectral gap]]

* [[confinement]]

* [[mass term]]

* [[gapped Hamiltonian]]


## References

### The mass gap problem
 {#ReferencesMassGapProblem}

Survey and problem description in [[mathematics]]/[[mathematical physics]]:

* [Clay Mathematics Institute](http://www.claymath.org/), _[Yang-Mills & The Mass Gap](https://www.claymath.org/millennium/yang-mills-the-maths-gap)_

* {#JaffeWitten00} [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_ (2000) &lbrack;[pdf](https://www.claymath.org/wp-content/uploads/2022/06/yangmills.pdf), [pdf](https://www.arthurjaffe.com/Assets/pdf/QuantumYangMillsWebRevised.pdf), [[JaffeWitten-QuantumYangMills.pdf:file]]&rbrack;

* {#Atiyah2000} [[Michael Atiyah]], *The millennium problems II*, talk at *[CMI Millennium Event at Collège de France](https://www.msri.org/realvideo/ln/hosted/cmi/2000/cmiparis/index-tate.html)* (24-25 May 2000) &lbrack;[web](https://www.claymath.org/lectures/the-millennium-prize-problems-ii/), [YT](https://youtu.be/trxjCOmg8GY), discussion of Yang-Mills&MassGap starting at: [29:40](https://youtu.be/trxjCOmg8GY?t=1764)&rbrack;

> [40:20](https://youtu.be/trxjCOmg8GY?t=2420) What is the future of this problem &lbrack;Yang-Mills & mass-gap&rbrack; in physics, what could happen?

> [40:24](https://youtu.be/trxjCOmg8GY?t=2424) This is now my personal guess or, if you like, hints &lbrack;or&rbrack; suggestions.

> [40:30](https://youtu.be/trxjCOmg8GY?t=2430) You can try a direct analytical assault. If you are a young man and brave and you have a long way into the future, you can just get out your hammer and chisel and crack away.

> [40:47](https://youtu.be/trxjCOmg8GY?t=2447) Or you might think that you want something different.

> [40:50](https://youtu.be/trxjCOmg8GY?t=2450) You might find to get a better understanding of the formal structure of [[quantum field theory]] of this Yang-Mills type. 

> [40:58](https://youtu.be/trxjCOmg8GY?t=2458) These Yang-Mills theories have very elaborate mathematical formal structure, which incorporate very mysterious [[duality in physics|dualities]] of various kinds and also a thing called *[[supersymmetry]]*, and many of the applications in mathematics incorporate all these.

> [41:51](https://youtu.be/trxjCOmg8GY?t=2475) So here there is a very elaborate structure, and it is just possible that if we get a better understanding of that structure then that might have given us a better way of trying to lay the foundations.

> [41:25](https://youtu.be/trxjCOmg8GY?t=2485) For example, a problem that can be described in two different ways, by duality, two dual pictures might look quite different, one of them might be practical and the other one might be intractable.

> [41:35](https://youtu.be/trxjCOmg8GY?t=2495) They are certainly not at all unreasonable to think this might be a way starting to understand better these formal operators[?], the formal operators here is very sophisticated.

> [41:47](https://youtu.be/trxjCOmg8GY?t=2507) You could of course sit back and wait, await development in string theory.

> [41:54](https://youtu.be/trxjCOmg8GY?t=2514) String theory and the latest things that follow string theory, called *[[M-theory]]* and every other new theory, develop [at] an enormous rate.

> [42:00](https://youtu.be/trxjCOmg8GY?t=2520) The theoretical physics community here is tremendously active, there are very beautiful things happening every week, new results come out, many of them will have mathematical overtones.

> [42:10](https://youtu.be/trxjCOmg8GY?t=2530) And it could be that if we wait a few years there'll be such a totally new  picture emerging from string theory that we'll get a better idea how to go about attacking the problem, so that's not an unreasonable expectation.

> [42:21](https://youtu.be/trxjCOmg8GY?t=2541) You see, trying to lay the foundations for physics is like an architect trying to lay the foundations for a building that's rapidly going up.

> [42:30](https://youtu.be/trxjCOmg8GY?t=2550) I mean, which do you do first, it's not quite clear: You want to see the design or you want to lay the foundations. Maybe you want the design first.

> [42:39](https://youtu.be/trxjCOmg8GY?t=2559) Then, of course, you might also sit back and say: Well, quantum electrodynamics was very hard, because we didn't incorporate extra things like proton and neutrons, we only worried about electrons. Maybe even that isn't enough perhaps we should have incorporated gravity, then we'll have all the forces under control and perhaps at that stage the fundamental theory will be even easier.

> [43:00](https://youtu.be/trxjCOmg8GY?t=2580) People in string theory aim here and this is the ultimate theory, and perhaps the ultimate theory will be easier than the transitional theories. But who knows.

> [43:09](https://youtu.be/trxjCOmg8GY?t=2589) The big challenge [for] mathematics and the physicists of the 21st century is to really make progress along this program by whatever method they can. Good luck to you.


Early report on the progress (essentially none):

* {#Douglas04} [[Michael Douglas]], _Report on the Status of the Yang-Mills Millennium Prize Problem_ (2004) &lbrack;[[Douglas-StatusOfYMMillenniumProb.pdf:file]]&rbrack;

Further comments:

* [[Ludvig Faddeev]]: _Mass in Quantum Yang-Mills Theory (Comment on a Clay Millennium Problem)_, in: *Perspectives in Analysis*, Mathematical Physics Studies **27**, Springer (2005) 63-72 &lbrack;[doi:10.1007/3-540-30434-7_6](https://doi.org/10.1007/3-540-30434-7_6), [arXiv:0911.1013](https://arxiv.org/abs/0911.1013)&rbrack;
  
  also: Bull Braz Math Soc, New Series **33** 2 (2005) 201-212 &lbrack;[pdf](http://emis.impa.br/EMIS/journals/em/docs/boletim/vol332/v33-2-a4-2002.pdf)&rbrack;

* [[David Gross]]: *Millennium Prize Problem: Yang Mills Theory*, talk at *Kavli Institute for Theoretical Physics* (Jan 2018) &lbrack;video:[YT](https://youtu.be/vMiY7zlBOFI)&rbrack;

* Lorenzo Sadun: *Yang-Mills existence and mass gap*, talk at *2001 University of Texas Lectures on the Millennium Problems* &lbrack;video:[YT](https://youtu.be/6sDJWSjEE8Y)&rbrack;

Notes reviewing more technical details of the problem:

* Jay Yablon, _The Origins of QCD Confinement in Yang-Mills Gauge Theory_, January 2008 ([pdf](http://jayryablon.files.wordpress.com/2008/01/qcd-confinement-handout-10.pdf))

Problem description in terms of [[probability theory|probabilistic]] [[lattice gauge theory]]:

* [[Sourav Chatterjee]], _Yang-Mills for probabilists_, in: _Probability and Analysis in Interacting Physical Systems_, PROMS **283**, Springer (2019) &lbrack;[arXiv:1803.01950](https://arxiv.org/abs/1803.01950), [doi:10.1007/978-3-030-15338-0](https://link.springer.com/book/10.1007/978-3-030-15338-0)&rbrack;

* [[Sourav Chatterjee]]: *Yang-Mills Existence and Mass Gap*, talk at: *[Millennium Prize Problems Lecture Series](https://cmsa.fas.harvard.edu/millennium/)*, Center of Mathematical Science and Applications, Harvard (15 Oct 2025) &lbrack;[webpage](https://cmsa.fas.harvard.edu/event/clay_101425/)&rbrack;


See also

* Wikipedia, _[Mass gap](https://en.wikipedia.org/wiki/Mass_gap)_.

* Wikipedia, _[Yang-Mills existence and the mass gap](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills_existence_and_mass_gap)_



### In the nuclear physics literature
{#ExplicitMentioningInPhysicsLiterature} 

In the [[nuclear physics]]/[[QCD]]-literature the mass gap problem is (and has long been) known as the _[confinement problem](confinement#OpenProblemConfinementReferences)_.
Explicit mentioning of the CMI's "mass gap" Millennium Problem in [[nuclear physics]]/[[phenomenology|phenomenological]] discussion of [[confinement]] includes the following:

* [[Igor Klebanov]], Oyvind Tafjord, "Can we quantitatively understand quark and gluon confinement in Quantum Chromodynamics and the existence of a mass gap?", 10th of *[10 Physics Problems for the Next Millennium](http://theory.caltech.edu/~preskill/millennium.html)* selected at [Strings 2000](https://inspirehep.net/conferences/972466)

* [[Yakov Shnir]], Section 9.1. of: *Magnetic Monopoles*, Springer 2005 ([ISBN:978-3-540-29082-7](https://www.springer.com/gp/book/9783540252771))

* [[Koji Hashimoto]], pp. 126 of: _D-Brane -- Superstrings and New Perspective of Our World_, Springer (2012) &lbrack;[doi:10.1007/978-3-642-23574-0](https://link.springer.com/book/10.1007%2F978-3-642-23574-0), [spire:1188897](http://inspirehep.net/record/1188897)&rbrack;

* [Barnaföldi & Gogokhia (2019), p. 2](#BarnafoldiGogokhia19)

* [Roberts & Schmidt (2020), p. 2](#RobertsSchmidt20)

* [Roberts (2021), footn. 2](#Roberts21)

* [Roberts (2022), p. 2](#Roberts22)



[[!include open problem of confinement -- references]]



### Approaches

#### Computer lattice QFT

Of course various partial approaches exist, notably computer-[[experiment]] in [[lattice QCD]]. (Such computer-checks of the mass-gap problem are analogous to computer checks of the [[Riemann hypothesis]], see [there](Riemann+hypothesis#ReferencesComputerChecks))
High-accuracy computation of [[hadron]]-[[masses]] in [[lattice QCD]]-simulations are reported here:

* S. Durr, Z. Fodor, J. Frison, C. Hoelbling, R. Hoffmann, S.D. Katz, S. Krieg, T. Kurth, L. Lellouch, T. Lippert, K.K. Szabo, G. Vulvert,

  _Ab-initio Determination of Light Hadron Masses_,

  Science 322:1224-1227,2008 ([arXiv:0906.3599](https://arxiv.org/abs/0906.3599))


* Zoltan Fodor, Christian Hoelbling, section V of _Light Hadron Masses from Lattice QCD_, Rev. Mod. Phys. 84, 449, ([arXiv:1203.4789](https://arxiv.org/abs/1203.4789))

* S. Aoki et. al. _Review of lattice results concerning low-energy particle physics_ ([arXiv:1607.00299](https://arxiv.org/abs/1607.00299))


\linebreak

* Yonggoo Heo, C. Kobdaj, M.F.M. Lutz, _Constraints from a large-$N_c$ analysis on meson-baryon interactions at chiral order $Q^3$_, Phys. Rev. D 100, 094035 (2019) ([arXiv:1908.11816](https://arxiv.org/abs/1908.11816))

> Still after many decades of vigorous studies the outstanding challenge of modern physics is to establish a rigorous link of QCD to low-energy hadron physics as it is observed in the many experimental cross section measurements. 

#### Rigorous lattice QFT

But there is also an approach via rigorous analytic [[lattice gauge theory]]:

* {#Chatterjee20} [[Sourav Chatterjee]], _A probabilistic mechanism for quark confinement_, Comm. Math. Phys. 2021 ([arXiv:2006.16229](https://arxiv.org/abs/2006.16229))


(...)

### In solid state physics

Discussion in [[solid state physics]]:

* Alessandra N. Braga, Wagner P. Pires, Jeferson Danilo L. Silva, Danilo T. Alves, Van Sérgio Alves, *Renormalization of the band gap in 2D materials near an interface between two dielectrics* &lbrack;[arXiv:2306.04759](https://arxiv.org/abs/2306.04759)&rbrack;

[[!redirects Yang-Mills mass gap problem]]

[[!redirects mass gap]]
[[!redirects mass gaps]]

[[!redirects mass gap problem]]
[[!redirects mass gap problems]]




