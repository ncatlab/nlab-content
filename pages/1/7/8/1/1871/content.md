
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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
 {#Idea}

Yang--Mills theory is a [[gauge theory]] on a given 4-[[dimensional]] ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian manifold|Riemannian]] [[manifold]] $X$ whose field is the [[Yang–Mills field]] -- a cocycle $\nabla \in \mathbf{H}(X,\bar \mathbf{B}U(n))$ in differential [[nonabelian cohomology]] represented by a [[vector bundle]] [[connection on a bundle|with connection]] -- and whose [[action functional]] is 

$$
  \nabla \mapsto
  \frac{1}{g^2 }\int_X tr(F_\nabla \wedge \star F_\nabla)  \;+\; i \theta \int_X tr(F_\nabla \wedge F_\nabla)
$$

for 

* $F_\nabla$ the [[field strength]], locally the [[curvature]] $\mathfrak{u}(n)$-[[Lie algebra valued differential form]] on $X$ ( with $\mathfrak{u}(n)$ the [[Lie algebra]] of the [[unitary group]] $U(n)$);

* $\star$ the [[Hodge star]] operator of the metric  $g$;

* $\frac{1}{g^2}$ the _Yang-Mills [[coupling constant]]_ and $\theta$ the _[[theta angle]]_, some [[real numbers]] (see at _[[S-duality]]_).

(See [this example](A+first+idea+of+quantum+field+theory#YangMillsLagrangian) at _[[A first idea of quantum field theory]]_.) 

## Properties

### Classification of solutions

* [[Narasimhan-Seshadri theorem]]

* [[Donaldson-Uhlenbeck-Yau theorem]]

### Quantization

Despite its fundamental role in the [[standard model of particle physics]], various details of the [[quantization]] of Yang-Mills theory are still open. See at _[[quantization of Yang-Mills theory]]_.


## Applications

All gauge fields in the [[standard model of particle physics]] as well as in [[GUT]] models are Yang--Mills fields.

The matter fields in the standard model are spinors charged under the Yang-Mills field. See

* [[spinors in Yang-Mills theory]]

## History
 {#History}

From [Jaffe-Witten](#JaffeWitten):

> By the 1950s, when Yang&#8211;Mills theory was discovered, it was already known that the [[quantum field theory|quantum version]] of [[electromagnetism|Maxwell theory]] -- known as [[quantum electrodynamics|Quantum Electrodynamics]] or QED -- gives an extremely accurate account of [[electromagnetic fields]] and [[Lorentz force|forces]]. In fact, QED improved the accuracy for certain earlier quantum theory predictions by several orders of magnitude, as well as predicting new splittings of energy levels. 

> So it was natural to inquire whether [[non-abelian group|non-abelian]] [[gauge theory]] described other [[forces]] in [[observable universe|nature]], notably the [[weak nuclear force|weak force]] (responsible among other things for certain forms of radioactivity) and the [[strong nuclear force|strong or nuclear force]] (responsible among other things for the binding of [[protons]] and [[neutrons]] into nuclei). The massless nature of [[classical field theory|classical]] Yang&#8211;Mills waves was a serious obstacle to applying Yang&#8211;Mills theory to the other forces, for the [[weak nuclear force|weak]] and [[strong nuclear force|nuclear forces]] are short range and many of the particles are massive. Hence these phenomena did not appear to be associated with long-range fields describing massless particles.

> In the 1960s and 1970s, physicists overcame these obstacles to the physical interpretation of non-abelian gauge theory. In the case of the weak force, this was accomplished by the Glashow&#8211;Salam&#8211;Weinberg [[electroweak theory]]  with gauge group $H = $ [[special unitary group|SU(2)]] $\times$ [[circle group|U(1)]]. By elaborating the theory with an additional "[[Higgs field]]", one avoided the massless nature of [[classical field theory|classical]] Yang&#8211;Mills waves. The [[Higgs field]] transforms in a two-dimensional [[representation]] of $H$; its non-zero and approximately constant value in the [[vacuum state]] reduces the [[structure group]] from $H$ to a $U(1)$ [[subgroup]] ([[diagonal|diagonally]] embedded in $SU(2) \times U(1)$. This [[theory (physics)|theory]] describes both the [[electromagnetism|electromagnetic]] and [[weak nuclear force|weak forces]], in a more or less unified way; because of the reduction of the structure group to $U(1)$, the long-range fields are those of [[electromagnetism]] only, in accord with what we see in [[observable universe|nature]]. 

> The solution to the problem of massless Yang&#8211;Mills fields for the [[strong nuclear force|strong interactions]] has a completely different nature.  That solution did not come from adding fields to Yang&#8211;Mills theory, but by discovering a remarkable property of the quantum Yang&#8211;Mills theory itself, that is, of the quantum theory whose [[classical field theory|classical]] [[Lagrangian density|Lagrangian]] has been given $[$above$]$. This property is called "[[asymptotic freedom]]". Roughly this means that at short distances the field displays [[quantum physics|quantum]] behavior very similar to its classical behavior; yet at long distances the [[classical field theory|classical theory]] is no longer a good guide to the quantum behavior of the [[field (physics)|field]].

> [[asymptotic freedom|Asymptotic freedom]], together with other experimental and theoretical discoveries made in the 1960s and 1970s, made it possible to describe the [[strong nuclear force|nuclear force]] by a [[non-abelian group|non-abelian]] [[gauge theory]] in which the [[gauge group]] is $G = $ [[special unitary group|SU(3)]]. The additional [[field (physics)|fields]] describe, at the [[classical field theory|classical level]], "[[quarks]]," which are [[spinor|spin 1/2 objects]] somewhat analogous to the [[electron]], but transforming in the [[fundamental representation]] of $SU(3)$.  The non-abelian gauge theory of the strong force is called [[quantum chromodynamics|Quantum Chromodynamics]] (QCD).

> The use of [[QCD]] to describe the [[strong nuclear force|strong force]] was motivated by a whole series of experimental and theoretical discoveries made in the 1960s and 1970s, involving the [[symmetries]] and high-energy behavior of the strong interactions. But [[classical field theory|classical]] [[non-abelian group|non-abelian]] [[gauge theory]] is very different from the [[observable universe|observed world]] of [[strong nuclear force|strong interactions]]; for [[QCD]] to describe the strong force successfully, it must have at the quantum level the following three properties, each of which is dramatically different from the behavior of the classical theory:

> (1) It must have a "[[mass gap]];" namely there must be some constant $\Delta \gt 0$ such that every excitation of the [[vacuum]] has [[energy]] at least $\Delta$.

> (2) It must have "[[quark]] [[confinement]]," that is, even though the theory is described in terms of elementary [[field (physics)|fields]], such as the quark fields, that transform non-trivially under [[special unitary group|SU(3)]], the physical particle states -- such as the [[proton]], [[neutron]], and [[pion]] --are [[special unitary group|SU(3)]]-[[invariant]].

> (3) It must have "[[chiral symmetry breaking]]," which means that the vacuum is potentially invariant (in the [[limit of a sequence|limit]], that the quark-bare masses vanish) only under a certain [[subgroup]] of the full [[symmetry group]] that [[action|acts]] on the [[quark]] [[field (physics)|fields]].

> The first point is necessary to explain why the [[strong nuclear force|nuclear force]] is strong but short-ranged; the second is needed to explain why we never see individual [[quarks]]; and the third is needed to account for the "[[current algebra]]" theory of soft [[pions]] that was developed in the 1960s.

> Both [[experiment]] -- since [[QCD]] has numerous successes in confrontation with experiment -- and [[lattice gauge theory|computer simulations]], carried out since the late 1970s, have given strong encouragement that QCD does have the properties cited above. These properties can be seen, to some extent, in theoretical calculations carried out in a variety of highly oversimplified models (like strongly coupled [[lattice gauge theory]]).  But they are not fully understood theoretically; there does not exist a convincing, whether or not mathematically complete, theoretical computation demonstrating any of the three properties in QCD, as opposed to a severely simplified truncation of it.

This is the problem of [[non-perturbative quantum field theory|non-perturbative]] [[quantization of Yang-Mills theory]]. See there for more.


## Related concepts

* [[D=5 Yang-Mills theory]]

* [[massive Yang-Mills theory]]

* [[self-dual Yang-Mills theory]]

* [[super Yang-Mills theory]]

* [[minimal coupling]]

* [['t Hooft double line notation]]

* [[Einstein-Yang-Mills theory]]

  * [[Einstein-Maxwell theory]]

  * [[Einstein-Yang-Mills-Dirac theory]]

  * [[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]]

* [[Yang-Mills equation]]

* [[standard model of particle physics]]

  * [[electromagnetism]]

  * [[spinors in Yang-Mills theory]]

  * [[QED]], [[QCD]], 

  * [[electroweak field]]


* [[Yang monopole]], [['t Hooft-Polyakov monopole]]

* [[S-duality]], [[Montonen-Olive duality]]

  * [[electric-magnetic duality]]

  * [[geometric Langlands duality]]

* [[Chern-Simons theory]]

* [[Yang-Mills instanton]]

  * [[confinement]]

* [[asymptotic freedom]]

## References

### General

Yang-Mills theory is named after the article

* [[Chen Ning Yang]], [[Robert Mills]], _Conservation of Isotopic Spin and Isotopic Gauge Invariance_. Physical Review 96 (1): 191&#8211; 195. (1954) ([web](http://prola.aps.org/abstract/PR/v96/i1/p191_1))

which was the first to generalize the principle of [[electromagnetism]] to a [[non-abelian group|non-abalian]] [[gauge group]]. This became accepted as formulation of [[QCD]] and [[weak interactions]] (only) after [[spontaneous symmetry breaking]] (the [[Higgs mechanism]]) was understood in the 1960s.

Modern reviews of the basics:
 
* {#JaffeWitten} [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_  ([pdf](http://www.arthurjaffe.com/Assets/pdf/QuantumYangMillsWebRevised.pdf))

* [[Simon Donaldson]], _Yang-Mills theory and geometry_ (2005) [pdf](http://www2.imperial.ac.uk/~skdona/YMILLS.PDF)

* [[José Figueroa-O'Farrill]], _[Gauge theory](http://empg.maths.ed.ac.uk/Activities/GT/index.html)_

* {#Uhlenbeck12} [[Karen Uhlenbeck]], notes by [[Laura Fredrickson]], _Equations of Gauge Theory_, lecture at Temple University, 2012 ([pdf](https://web.stanford.edu/~ljfred4/Attachments/TempleLectures.pdf), [[UhlenbeckGaugeTheory.pdf:file]])

* {#Donaldson06} [[Simon Donaldson]], _Gauge Theory: Mathematical Applications_, Encyclopedia of Mathematical Physics, Academic Press, Pages 468-481, 2006  ([doi:10.1016/B0-12-512666-2/00075-4](https://doi.org/10.1016/B0-12-512666-2/00075-4), [author pdf](http://wwwf.imperial.ac.uk/~skdona/EMP.PDF), [[DonaldsonGaugeTheory.pdf:file]])

* [[Mikio Nakahara]], Section 10.5.4 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)

* [[Gerd Rudolph]], [[Matthias Schmidt]], Chapters 7-9 of: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))

See also the references at _[[QCD]]_, _[[gauge theory]]_, _[[Yang-Mills monopole]]_, _[[Yang-Mills instanton]]_ and at _[[super Yang-Mills theory]]_.

Classical discussion of YM-theory over [[Riemann surfaces]] (which is closely related to [[Chern-Simons theory]], see also at _[[moduli space of flat connections]]_) is in 

* {#AtiyahBott83} [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences
Vol. 308, No. 1505 (Mar. 17, 1983), pp. 523-615 ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))

which is reviewed in the lecture notes

* [[Jonathan Evans]] _Aspects of Yang-Mills theory_, ([web](http://www.homepages.ucl.ac.uk/~ucahjde/yangmills.htm))

For the relation to [[instanton Floer homology]] see also

* [[Simon Donaldson]], _Floer homology groups in Yang-Mills theory_ Cambridge University Press (2002) ([pdf](http://catdir.loc.gov/catdir/samples/cam031/2001035888.pdf))

For the relation to [[Tamagawa numbers]] see

* Aravind Asok, Brent Doran, Frances Kirwan, _Yang-Mills theory and Tamagawa numbers_ ([arXiv:0801.4733](http://arxiv.org/abs/arXiv:0801.4733))


### Classical solutions

Wu and Yang (1968) found a static solution to the sourceless $SU(2)$ [[Yang-Mills equations]]. Recent references include

* J. A. O. Marinho, O. Oliveira, B. V. Carlson, T. Frederico, _Revisiting the Wu-Yang Monopole: classical solutions and conformal invariance_ 

	
There is an old review, 

* Alfred Actor, _Classical solutions of $SU(2)$ Yang&#8212;Mills theories_, Rev. Mod. Phys. 51, 461&#8211;525 (1979), 

that provides some of the known solutions of $SU(2)$ gauge theory in [[Minkowski spacetime|Minkowski]] ([[monopoles]], plane waves, etc) and [[Euclidean space]] ([[instantons]] and their cousins). For general [[gauge groups]] one can get solutions by embedding $SU(2)$'s. 

For [[Yang-Mills instantons]] the most general solution is known, first worked out by

* [[Michael Atiyah]], [[Nigel Hitchin]], [[Vladimir Drinfeld]], [[Yuri Manin]], _Construction of instantons_, Physics Letters 65 A, 3, 185--187 (1978) [pdf](http://www.new.ox.ac.uk/system/files/ADHM.pdf)

for the [[classical groups]] [[special unitary group|SU]], [[special orthogonal group|SO]] , [[symplectic group|Sp]], and then by 

* C. Bernard, N. Christ, A. Guth, E. Weinberg, _Pseudoparticle Parameters for Arbitrary Gauge Groups_, Phys. Rev. __D16__, 2977 (1977)  

for [[exceptional Lie groups]]. The latest twist on the [[Yang-Mills instanton]] story is the construction of solutions with non-trivial [[holonomy]]: 

* Thomas C. Kraan, Pierre van Baal, _Periodic instantons with nontrivial holonomy_, Nucl.Phys. B533 (1998) 627-659, [hep-th/9805168](http://arxiv.org/abs/hep-th/9805168)

There is a nice set of lecture notes 

* David Tong, _TASI Lectures on Solitons_ ([hep-th/0509216](http://arxiv.org/abs/hep-th/0509216)), 

on topological solutions with different co-dimension (instantons, monopoles, vortices, domain walls). Note, however, that except for instantons these solutions typically require extra scalars and broken U(1)'s, as one  may find in [[super Yang-Mills theories]].

Some of the material used here has been taken from 

* [TP.SE](http://theoreticalphysics.stackexchange.com/), _[Which exact solutions of the classical Yang-Mills equations are known?](http://theoreticalphysics.stackexchange.com/questions/317/which-exact-solutions-of-the-classical-yang-mills-equations-are-known)_ 

Another model featuring Yang-Mills fields has been proposed by Curci and Ferrari, see [[Curci-Ferrari model]].

See also

* DispersiveWiki, _[Yang-Mills equations](http://wiki.math.toronto.edu/DispersiveWiki/index.php/Yang-Mills_equations)_

[[!redirects Yang-Mills theories]]

[[!redirects Yang--Mills theory]]
[[!redirects Yang–Mills theory]]
[[!redirects Yang-Mills action]]
[[!redirects Yang-Mills action functional]]




