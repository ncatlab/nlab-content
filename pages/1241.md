
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

### General idea

The [[standard model of particle physics]] asserts that the fundamental quantum [[field (physics)|physical fields]] and [[particles]] are modeled as [[sections]] of and [[connection on a bundle|connections]] on a [[vector bundle]] that is [[associated bundle|associated]] to a $G$-[[principal bundle]], where the [[Lie group]] $G$ -- called the [[gauge group]] -- is  the [[product]] of ([[special unitary group|special]]) [[unitary groups]] $G = SU(3) \times SU(2) \times U(1)$ (or rather a [[quotient]] of this by the [[cyclic group]] $Z/6$, see [there](standard+model+of+particle+physics#GaugeGroup)) and where the [[representation]] of $G$ used to form the [[associated bundle|associated]] [[vector bundle]] looks fairly ad hoc on first sight.

A **grand unified theory** ("GUT" for short) in this context is an attempt to realize the standard model as sitting inside a conceptually simpler [[model (in particle physics)|model]], in particular one for which the [[gauge group]] is a bigger but _simpler_ group $\hat{G}$, preferably a _[[simple Lie group]]_ in the technical sense, which contains $G$ as a [[subgroup]]. Such a grand unified theory would be [[phenomenology|phenomenologically]] viable if a process of [[spontaneous symmetry breaking]] at some high [[energy]] scale -- the "GUT scale" -- would reduce the model back to the [[standard model of particle physics]] without adding spurious extra effects that would not be in agreement with existing observations in [[experiment]].

The terminology "grand unified" here refers to the fact that such a single simple group $\hat{G}$ would unify the fundamental [[forces]] of [[electromagnetism]], the [[weak nuclear force]] and the [[strong nuclear force]] in a way that generalizes the way in which the [[electroweak field]] already unifies the [[weak nuclear force]] and [[electromagnetism]], and electromagnetism already unifies, as the word says, electricity and magnetism.


Since no GUT model has been fully validated yet (but see for instance [Fong-Meloni 14](#FongMeloni14)), GUTs are [[model (physics)|models]] "beyond the [[standard model of particle physics|standard model]]". Often quantum physics "beyond the standard model" is expected to also say something sensible about [[quantum gravity]] and hence unify not just the three gauge forces but also the fourth known fundamental force, which is [[gravity]]. Models that aim to do all of this would then "unify" the entire content of the [[standard model of particle physics]] plus the [[standard model of cosmology]], hence "everything that is known about fundamental physics" to date. Therefore such theories are then sometimes called a _[[theory of everything]]_. 

(Here it is important to remember the context, both "grand unified" and "of everything" refers to aspects of presently available models of fundamental physics, and not to deeper philosophical questions of [[ontology]].)


### The $SU(5)$-GUT
  {#IdeaofSU5GUT}

The argument for the hypothesis of "grand unification" is fairly compelling if one asks for _[[simple objects|simple algebraic structures]]_ in the technical sense ([[simple Lie groups]] and their [[irreducible representations]]): 

The _exact_ gauge group of the [[standard model of particle physics]] is really a [[quotient group]] 

$$
  G_{SM}
  \;=\; 
  \big( U(1) \times SU(2) \times SU(3) \big) / \mathbb{Z}_6
  \,,
$$

where the [[cyclic group]] $\mathbb{Z}_6$ [[free action|acts freely]], hence exhibiting a subtle global twist in the gauge structure. This seemingly ad hoc group turns out to be [[isomorphism|isomorphic]] to the [[subgroup]]

$$
  \underset{
    \simeq \big( U(1) \times SU(2) \times SU(3) \big) / \mathbb{Z}_6  }{
  \underbrace{
    S \big( U(2) \times U(3)\big)
  }}
  \;\subset\;
  SU(5)
$$

of [[special unitary group|SU(5)]] (see [Baez-Huerta 09, p. 33-36](#BaezHuerta09)). The latter happens to be a [[simple Lie group]], thus exhibiting the exact standard model Lie group as being "simply" a "(2+3)-breaking" of a [[simple Lie group]].

Moreover, the [[gauge group]]-[[representation]] $V_{SM}$ that captures one [[generation of fundamental particles]] of the [[standard model of particle physics]], which looks fairly ad hoc as a representation of $G_{SM}$ (e.g. [Baez-Huerta 09, table 1](#BaezHuerta09)), but as a representation of $SU(5)$ it is simply 

$$
  V_{SM} \simeq \Lambda \mathbb{C}^5
$$ 

(see [Baez-Huerta 09, p. 36-41](#BaezHuerta09)).


### The $Spin(10)$-GUT (known as "$SO(10)$")

There is a further inclusion $SU(5) \hookrightarrow Spin(10)$ into the [[spin group]] in 10 (Euclidean) dimensions (still a [[simple Lie group]]), and one [[generation of fundamental particles]] regarded as an $SU(5)$-[[representation]] $\Lambda \mathbb{C}^5$ as [above](#IdeaofSU5GUT) extends to a [[spin representation]] (see [Baez-Huerta 09, theorem 2](#BaezHuerta09)). This has the aesthetically pleasing effect that under this identification the 1-generation rep $V_{SM}$ is now identified as

$$
  V_{SM} \;\simeq\; \mathbf{16} \oplus \overline{\mathbf{16}}
$$

namely as the [[direct sum]] of [[generalized the|the]] two (complex) [[irreducible representations]] of $Spin(10)$, together being the [[Dirac representation]] of $Spin(10)$.

Again, this means that under the embedding of the gauge group $G_{SM}$ all the way into the [[simple Lie group]] $Spin(10)$, its ingredients become _simpler_, not just in a naive sense, but in the technical mathematical sense of _[[simple objects|simple algebraic objects]]_.

### Exceptional series GUTs

This way, the most studied choices of GUT-groups $G$ are [[special unitary group|SU(5)]], [[spin group|Spin(10)]] (in the physics literature often referred to as [[special orthogonal group|SO(10)]]) and [[E6]] (review includes [Witten 86, sections 1 and 2](#Witten86)). 

It so happens that, mathematically, the sequence [[special unitary groups|SU(5)]], [[spin group|Spin(10)]], [[E6]] naturally continues (each step by consecutively adding a node to the [[Dynkin diagrams]]) with the [[exceptional Lie groups]] [[E7]], [[E8]] that naturally appear in [[heterotic string theory|heterotic]] [[string phenomenology]] (exposition is in [Witten 02a](#Witten02a)) and conjecturally further via the [[U-duality]] [[Kac-Moody groups]] [[E9]], [[E10]], [[E11]] that are being argued to underly [[M-theory]]. In the context of [[F-theory]] model building, also properties of the observes [[Yukawa couplings]] may point to exceptional GUT groups ([Zoccarato 14, slide 11](#Zoccarato14), [Vafa 15, slide 11](#Vafa15)).

## Properties

### Relation to proton decay
  {#RelationToProtonDecay}

Many GUT models imply that the [[proton]] -- which in the [[standard model of particle physics]] is a stable [[bound state]] (of [[quarks]]) -- is in fact unstable, albeit with an extremely long mean liftetime, and hence may decay (e.g. [KM 14](#KM14)). [[experiment|Experimental]] searches for such _[[proton decay]]_ (see there for more) put strong bounds on this effect and hence heavily constrain or rule out many [[GUT]] [[model (physics)|models]].

Recently it was claimed that there are in fact realistic [[GUT]] [[model (physics)|models]] that do not imply any [[proton decay]] ([Mütter-Ratz-Vaudrvange 16](#MuetterRatzVaudrvange16), [Fornal-Grinstein 17](#FornalGrinstein17)).

### Relation to neutrino masses

The high energy scale required by a [[seesaw mechanism]] to produce the experimentally observer [[neutrino]] masses happens to be about the conventional GUT scale, for review see for instance ([Mohapatra 06](#Mohapatra06)).

### Relation to leptoquarks
 {#RelationToLeptoquarks}

Genrically GUT-theories predict existence of [[leptoquarks]] ([Murayama-Yanagida 92](#MurayamaYanagida92)) possibly related to the apparently observed [[flavour anomalies]] ([BDFKFS 18](#BDFKFS18))


### Occurrence in string phenomenology
 {#InStringPhenomenology}

Discussion of [[string phenomenology]] of [[intersecting D-brane models]] [[KK-compactification|KK-compactified]] with non-geometric [[fibers]] such that the would-be string [[sigma-models]] with these [[target spaces]] are in fact [[Gepner models]] (in the sense of _[Spectral Standard Model and String Compactifications](https://www.physicsforums.com/insights/spectral-standard-model-string-compactifications/)_) is in ([Dijkstra-Huiszoon-Schellekens 04a](#DijkstraHuiszoonSchellekens04a), [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b)):


<center>
<img src="https://ncatlab.org/nlab/files/SchellekensSuperGepnerModelScanII.jpg" width="600">
</center>

>  A plot of [[standard model of particle physics|standard model]]-like [[coupling constants]] in a computer scan of [[Gepner model]]-[[KK-compactification]] of [[intersecting D-brane models]] according to [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b). 

>  The blue dot indicates the couplings in $SU(5)$-[[GUT]] theory. The faint lines are NOT drawn by hand, but reflect increased density of Gepner models as seen by the computer scan.


## Related concepts

* [[theory of everything]]

* [[gauge coupling unification]]

* [[supersymmetry]]

## References 
 {#References}

Original articles include

* {#GeorgiGlashow74} [[Howard Georgi]], [[Sheldon Glashow]], _Unity of All Elementary-Particle Forces_, Phys. Rev. Lett. 32, 438, 1974 ([doi:10.1103/PhysRevLett.32.438](https://doi.org/10.1103/PhysRevLett.32.438))


An original article with an eye towards [[supergravity]] unification is

* [[Murray Gell-Mann]], [[Pierre Ramond]], Richard Slansky, _Complex Spinors and Unified Theories_, Supergravity, [[Peter van Nieuwenhuizen]] and D.Z. Freedman, eds, North Holland Publishing Co, 1979, reprinted as [arXiv:1306.4669](http://arxiv.org/abs/1306.4669)

A textbook account is in

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 1.2 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012


Survey of arguments for the hypothesis of grand unification includes

* [[Michael Peskin]], _Beyond the Standard Model_ ([arXiv:hep-ph/9705479](http://arxiv.org/abs/hep-ph/9705479))

* [[Jogesh Pati]], _Discovery of Proton Decay: A Must for Theory, a Challenge for Experiment_ ([arXiv:hep-ph/0005095](http://arxiv.org/abs/hep-ph/0005095))



* {#Witten02a} [[Edward Witten]], _Quest For Unification_, Heinrich Hertz lecture at [SUSY 2002](http://www.desy.de/susy02/) at DESY, Hamburg ([arXiv:hep-ph/0207124](http://arxiv.org/abs/hep-ph/0207124))
 

Introduction to GUTs aimed more at mathematicians include

* {#Witten86} [[Edward Witten]], section 1 and 2 of _Physics and geometry_, Proceedings of the international congress of mathematicians, 1986 ([pdf](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0267.0306.ocr.pdf)) 

* {#BaezHuerta09} [[John Baez]], [[John Huerta]], _The Algebra of Grand Unified Theories_, Bull.Am.Math.Soc.47:483-552,2010 ([arXiv:0904.1556](http://arxiv.org/abs/0904.1556))

Discussion of comparison of GUTs to [[experiment]] and [[phenomenology]] includes

for non-superymmetric [[model (physics)|models]]:

* L. Lavoura and Lincoln Wolfenstein, _Resuscitation of minimal $SO(10)$ grand unification_, Phys. Rev. D 48, 264 ([doi:10.1103/PhysRevD.48.264](https://doi.org/10.1103/PhysRevD.48.264))

* Guido Altarelli, Davide Meloni, _A non Supersymmetric SO(10) Grand Unified Model for All the Physics below $M_{GUT}$_ ([arXiv:1305.1001](https://arxiv.org/abs/1305.1001))

* Alexander Dueck, Werner Rodejohann, _Fits to $SO(10)$ Grand Unified Models_ ([arXiv:1306.4468](http://arxiv.org/abs/1306.4468))

* {#FongMeloni14} Chee Sheng Fong, Davide Meloni, Aurora Meroni, Enrico Nardi, _Leptogenesis in $SO(10)$_ ([arXiv:1412.4776](http://arxiv.org/abs/1412.4776))


for [[supersymmetry|supersymmetric]] [[model (physics)|models]]:

* Archana Anandakrishnan, B. Charles Bryant, Stuart Raby, _LHC Phenomenology of $SO(10)$ Models with Yukawa Unification II_ ([arXiv:1404.5628](http://arxiv.org/abs/1404.5628))

* Ila Garg, _New minimal supersymmetric $SO(10)$ GUT phenomenology and its cosmological implications_ ([arXiv:1506.05204](http://arxiv.org/abs/1506.05204))

Introductory overview to GUTs in [[string theory]] is in 

* {#Nilles11} [[Hans-Peter Nilles]], _Strings, Exceptional Groups and Grand Unification_, talk at _[Planck 2011](https://indico.cern.ch/event/112851/)_ ([pdf](http://www.th.physik.uni-bonn.de/nilles/db/HPtalks/114planck.pdf), [[Nilles11GUT.pdf:file]])

Computer scan of [[Gepner model]]-compactifications in relation to GUT-models is in 

* {#DijkstraHuiszoonSchellekens04a} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Chiral Supersymmetric Standard Model Spectra from Orientifolds of Gepner Models_, Phys.Lett. B609 (2005) 408-417 ([arXiv:hep-th/0403196](https://arxiv.org/abs/hep-th/0403196))

* {#DijkstraHuiszoonSchellekens04b} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Supersymmetric Standard Model Spectra from RCFT orientifolds_, Nucl.Phys.B710:3-57,2005 ([arXiv:hep-th/0411129](https://arxiv.org/abs/hep-th/0411129))


Realization of GUTs in the context of [[M-theory on G2-manifolds]] and possible resolution of the [[doublet-triplet splitting problem]] is discussed in

* {#Witten02b} [[Edward Witten]], _Deconstruction, $G_2$ Holonomy, and Doublet-Triplet Splitting_, ([arXiv:hep-ph/0201018](http://arxiv.org/abs/hep-ph/0201018))

* [[Bobby Acharya]], Krzysztof Bozek, Miguel Crispim Romao, Stephen F. King, Chakrit Pongkitivanichkul, _$SO(10)$ Grand Unification in M theory on a $G_2$ manifold_ ([arXiv:1502.01727](http://arxiv.org/abs/1502.01727))

Discussion of GUTs in [[F-theory]] includes

* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_ ([arxiv:0802.3391](http://arxiv.org/abs/0802.3391)), _II: Experimental Predictions_ ([arxiv:0806.0102](http://arxiv.org/abs/0806.0102))


* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_, JHEP 0901:058,2009 ([arXiv:0802.3391](http://arxiv.org/abs/0802.3391))


* {#Zoccarato14} Gianluca Zoccarato, _Yukawa couplings at the point
of $E_8$ in F-theory_, 2014 ([pdf](http://stringpheno2014.ictp.it/parallels/tuesday/F-theory(B)/zoccarato.pdf))

* {#Vafa15} [[Cumrun Vafa]], _Reflections on F-theory_, 2015 (<a href="http://f-theory15.mpp.mpg.de/talks/Vafa.pdf">pdf</a>)

Discussion of experimental bounds on [[proton decay]] in GUTs includes

* {#KM14} Helena Kole&#353;ov&#225;, [[Michal Malinský]], _Proton lifetime in the minimal $SO(10)$ GUT and its implications for the LHC_, Phys. Rev. D 90, 115001 (2014) ([arXiv:1409.4961](http://arxiv.org/abs/1409.4961))

Claim that [[proton decay]] may be entirely avoided:

* {#MuetterRatzVaudrvange16} Andreas Mütter, Michael Ratz, Patrick K.S. Vaudrevange, _Grand Unification without Proton Decay_ ([arXiv:1606.02303](https://arxiv.org/abs/1606.02303))

  (claims that many [[string theory]] and [[supergravity]] models have this property)

* {#FornalGrinstein17} Bartosz Fornal, Benjamin Grinstein, _$SU(5)$ Unification without Proton Decay_, Physics Review Letters ([arXiv:1706.08535](https://arxiv.org/abs/1706.08535))

Relation to [[leptoquarks]] and [[flavour anomalies]]:

* {#MurayamaYanagida92} H. Murayama, T. Yanagida, _A viable $SU(5)$ GUT with light leptoquark bosons_, Mod.Phys.Lett. A7 (1992) 147-152 ([arXiv:315898](inspirehep.net/record/315898), [doi:10.1142/S0217732392000070](https://doi.org/10.1142/S0217732392000070))

* {#BDFKFS18} Damir Bečirević, Ilja Doršner, Svjetlana Fajfer, Nejc Košnik, Darius A. Faroughy, Olcyr Sumensari, _Scalar leptoquarks from GUT to accommodate the $B$-physics anomalies_, Phys. Rev. D 98, 055003 (2018) ([arXiv:1806.05689](https://arxiv.org/abs/1806.05689))


[[!redirects GUTs]]
[[!redirects grand unified theory]]
[[!redirects grand unified theories]]

[[!redirects grand unified field theory]]
[[!redirects grand unified field theories]]


[[!redirects Grand Unified Theory]]

[[!redirects grand unification]]
[[!redirects grand unifications]]