
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 
 {#Idea}


An ordinary [[spectral triple]] is, as discussed there, the abstract algebraic data characterizing [[supersymmetric quantum mechanics]] on a [[worldline]] and thereby spectrally encoding an effective (possibly [[non-commutative geometry|non-commutative]], hence "[[non-geometric background|non-geometric]]") [[target space]] [[geometry]]. 
Ordinary [[Riemannian geometry]] with [[spin structure]] is the special case of this where the [[Hilbert space]] in the spectral triple is that of [[square integrable function|square integrable]] [[sections]] of the [[spinor bundle]] on a [[spin structure|spin]] [[Riemannian manifold]] and the operator $D$ acting on that is the standard [[Dirac operator]], hence the "supercharge" of the worldline supersymmetry of the [[spinning particle]].

In generalization of this, a "2-spectral triple" should be the analogous algebraic data that encodes the [[worldsheet]] theory of a [[superstring]] propagating on a [[target space]] geometry which is a generalization of [[Riemannian geometry]] with ([[twisted string structure|twisted]]) [[string structure]].

Of course such data is just that of a [[2d superconformal field theory]], realized locally by,  for instance, a [[vertex operator algebra]] or by a [[conformal net]] of [[local net of observables|local observables]]. But for emphasis it may be useful to speak of such data as constituting a "2-spectral triple", for emphasizing more the important and intricate relation to the concept of [[spectral triples]], which in much of the literature seems to be unduly ignored.

| [[quantum system]]    | [[supercharge]] | formalization | algebra | 
|----------------------|---------|------------------------|-----|
| quantum [[spinning particle]] | [[Dirac operator]] | [[spectral triple]]    | [[operator algebra]]
| quantum [[spinning string]] |  [[Dirac-Ramond operator]] | [[2d SCFT]] | [[vertex operator algebra]] |

That the 0-mode sector of a [[2d SCFT]] -- hence the quantum point [[particle]] limit of a quantum [[superstring]] dynamics -- yields a [[spectral triple]] was maybe first highlighted in ([Fr&#246;hlich-Gaw&#281;dzki 93](#FroehlichGawedzki93)) by way of a series of concrete examples, such as the [[WZW model]]. 

Here the role of the [[Dirac operator]] of the spectral triple is played by the [[Dirac-Ramond operator]] of the [[superstring]], hence the operator whose [[index]] (in the [[large volume limit]]) is the [[Witten genus]]. 

That hence the superstring quantum theory should be regarded as a kind of higher spectral triple was maybe first suggested in ([Chamseddine 97](#Chamseddine97)), together with arguments that the associated [[spectral action]] indeed reproduces the [[action functional]] of the string's [[target space]] [[effective quantum field theory|effective]] [[supergravity]] theory. An exposition of this perspective is in ([Fr&#246;hlich-Grandjean-Recknagel 97, section 7.2](#FroehlichGrandjeanRecknagel97)).

From [Fröhlich 92, p. 11](non-perturbative+quantum+field+theory#Froehlich92):

> I still have hopes, perhaps romantic ones, that [[string theory]], or something inspired by it, will come back to life again. I believe it is interesting to attempt to formulate string theory in an "invariant" way, quite like it is useful to formulate geometry in a coordinate-independent way. One might, for example, start with a family $\mathcal{F}$, of [[von Neumann algebra factor|hyperfinite type $III_1$ von Neumann algebras]] -- to be a little technical -- [[conformal net|indexed by]] intervals of the circle with non-empty complement (or of the super-circle). It may pay to formulate the starting point using the language of [[sheaves]]. $[...]$ This structure determines a [[braided monoidal category|braided monoidal]] [[C*-category]] with unit, ...; briefly, a quantum theory. From a combination of such [[tensor categories]] (left and right movers) one would attempt to reconstruct (symmetries of) _physical space-time_. String amplitudes would correspond to [[morphisms|arrows]] ([[intertwiners]]) of the [[tensor category]]. $[...]$ it would provide a general way of thinking about string theory that does not presuppose knowing the target space-time of the theory.

Later it was shown more formally ([Roggenkamp-Wendland 03](#RoggenkampWendland03)), reviewed in ([Roggenkamp-Wendland 08](#RoggenkampWendland08)), that there is a precise algebraically formalization of taking the "point particle limit" of a quantum string, by sending its [[vertex operator algebra]] to a spectral triple obtained by suitably retaining only [[worldsheet]] 0-modes.

In ([Soibelman 11](#Soibelman11)) this was used as a means to systematically study the large volume limit of [[effective quantum field theory|effective]] string [[spacetimes]] (and hence aspects of the [[landscape of string theory vacua]]) by studying the spectral geometries (i.e. the Connes-style noncommutative geometries) of the spectral triples arising from the string's point particle limit this way.

Now, since there is information lost in passing from a stringy "2-spectral triple" (a [[2d SCFT]]) to its underlying point particle [[spectral triple]], not all spectral triples are to be expected to have a lift to a 2-spectral triple (possibly corresponding to a [[UV-completion]] of the corresponding target space [[effective field theories]]).

In view of this, it is noteworthy that the spectral triple of the [[Connes-Lott-Chamseddine model]] shares a few key properties with the 2d SCFTs considered in [[string phenomenology]]:

The [[Connes-Lott-Chamseddine model]] is an encoding in a spectral triple of the [[standard model of particle physics]] coupled to [[gravity]] realized as a kind of spectral [[Kaluza-Klein compactification]] on a non-commutative fiber space down to ordinary 4d [[Minkowski spacetime]] (or possibly its [[Wick rotation|Wick rotated]] Euclidean version). In order for this to work out, it turns out that the compactified non-commutative fiber space needs to have [[KO-dimension]] equal to $6$. (Here the fiber space is classically just a ("non-commutative") point, but it appears as the singular collapsing limit of a space of finite dimension. This actual dimension is the [[KO-dimension]].)

Hence the claim of the [[Connes-Lott-Chamseddine model]] is that if the [[standard model of particle physics]] is encoded as a singular limit of a [[Kaluza-Klein compactification]] modeled via a [[spectral triple]] then the [[dimensions]] of the [[KK-compactification]] are

$$
  4 + 6 \;\;\; (mod\;8)
$$

with 4-dimensional base space and 6-dimensional fiber space, to a total of a 10-dimensional [[spacetime]] at high energy (after uncompactification of the fiber). 

This, of course, is precisely the dimensionality of the target spacetime of [[perturbative string theory vacua]] for the critical [[superstring]]. 

This point was highlighted in [Connes 06, p. 8](#Connes06):

> {#Connes06OnRelationToStringVacua} When one looks at the table (7.2) of Appendix 7 giving the [[KO-dimension]] of the finite space $[$ i.e. the [[noncommutative geometry|noncommutative]] [[KK-compactification]]-[[fiber]] $F$ $]$ one then finds that its [[KO-dimension]] is now equal to 6 [[modulo]] 8 (!). As a result we see that the [[KO-dimension]] of the [[Cartesian product|product space]] $M \times F$ $[$ i.e. of 4d [[spacetime]] $M$ with the [[noncommutative geometry|noncommutative]] [[KK-compactification]]-[[fiber]] $F$$]$ is in fact equal to $10  \sim 2$ [[modulo]] 8. Of course the above 10 is very reminiscent of string theory, in which the finite space $F$ might bea good candidate for an "[[effective field theory|effective]]" [[KK-compactification|compactification]] at least for low energies. But 10 is also 2 [[modulo]] 8 which might be related to the observations of [Lauscher-Reuter 06](#LauscherReuter06) about [[gravity]].


Algebraically, this arises from the fact that the [[BRST complex]] for the [[superstring]] [[worldsheet]] theory is consistent (has BRST differential squaring to 0) precisely if the corresponding [[2d SCFT]] has conformal [[central charge]] 15, and each spacetime dimension contributes $1 \tfrac{1}{2}$ to this central charge (a contribution of 1 from each bosonic direction, and another $\tfrac{1}{2}$ for the corresponding fermionic contribution).






## Examples

### Flop transition

There is at least evidence that there is a continuous path in the space of 2-spectral triples that starts and ends at a point describing the ordinary geometry of a complex 3-dimensional [[Calabi-Yau space]] but passes in between through a 2-spectral triple/2d SCFT (a [[Gepner model]]) which is not the $\sigma$-model of an ordinary geometry, hence which describes "noncommutative 2-geometry" (to borrow that terminology from the situation of ordinary spectral triples). This is called the [[flop transition]] (alluding to the fact that the geometries at the start and end of this path have different [[topology]]). This was further expanded on and used for the mathematical study of the [[large volume limit]] of [[string theory]] [[vacua]] in ([Soibelman 11](#Soibelman11)).

## Related concepts

* [[spectral triple]]

* [[spectral action]]

* [[D-brane geometry]]

* [[automorphism of a 2-spectral triple]]

* [[swampland]]

## References
  {#References}

An early observation that the 0-mode sector of a [[2d SCFT]] is a [[spectral triple]], demonstrated in a series of concrete examples, is

* {#FroehlichGawedzki93} [[Jürg Fröhlich]], [[Krzysztof Gawędzki]], _Conformal Field Theory and Geometry of Strings_,  extended lecture notes for lecture given at the Mathematical Quantum Theory Conference, Vancouver, Canada, August 4-8 ([arXiv:hep-th/9310187](http://arxiv.org/abs/hep-th/9310187))

The suggestion to understand, conversely, the [[string theory|string]]'s [[worldvolume]] [[2d SCFT]] as a higher spectral triple is due to

*  {#Chamseddine97} [[Ali Chamseddine]], _An Effective Superstring Spectral Action_, Phys.Rev. D56 (1997) 3555-3567 ([arXiv:hep-th/9705153](http://arxiv.org/abs/hep-th/9705153)),

which claims to show that the corresponding [[spectral action]] reproduces the correct effective background action known in [[string theory]]. A more expository account of this perspective is in

* {#FroehlichGrandjeanRecknagel97} [[Jürg Fröhlich]], Oliver Grandjean, [[Andreas Recknagel]], section 7 of _Supersymmetric quantum theory, non-commutative geometry, and gravitation_,  Lecture Notes Les Houches (1995) ([arXiv:hep-th/9706132](http://arxiv.org/abs/hep-th/9706132)).


A more formal derivation of how ordinary [[spectral triples]] arise as point particle limits of [[vertex operator algebra]]s for [[2d SCFTs]] then appears in

* {#RoggenkampWendland03} [[Daniel Roggenkamp]], [[Katrin Wendland]], _Limits and Degenerations of Unitary Conformal Field Theories_, Commun.Math.Phys. 251 (2004) 589-643 ([arXiv:hep-th/0308143](http://arxiv.org/abs/hep-th/0308143))

summarized in

* {#RoggenkampWendland08} [[Daniel Roggenkamp]], [[Katrin Wendland]], _Decoding the geometry of conformal field theories_, Proceedings of the 7th International Workshop "Lie Theory and Its Applications in Physics", Varna, Bulgaria ([arXiv:0803.0657](http://arxiv.org/abs/0803.0657))

A brief indication of some ideas of [[Yan Soibelman]] and [[Maxim Kontsevich]] on this matter is at

* [[Urs Schreiber]],  [_Spectral triples and graph field theory_](http://golem.ph.utexas.edu/category/2007/06/had_the_pleasure_of_talking.html)

Further development of this and application to the study of the [[large volume limit]] of [[superstring]] [[vacua]] is in

* {#Soibelman11} [[Yan Soibelman]], _Collapsing CFTs, spaces with non-negative Ricci curvature and nc-geometry_ ([pdf](http://www.math.ksu.edu/~soibel/nc-riem-3.pdf)), in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String 
Theory]]_, Proceedings of Symposia in Pure Mathematics, AMS (2001)

based on 

* [[Maxim Kontsevich]], [[Yan Soibelman]], section 2 of _Homological mirror symmetry and torus fibrations_, Proceedings of KIAS Annual International Conference on Symplectic Geometry and Mirror Symmetry ([arXiv:math/0011041](http://arxiv.org/abs/math/0011041), [spire](http://inspirehep.net/record/536540/))

(discussing aspects of [[homological mirror symmetry]]).

Analogous detailed discussion based not on the [[vertex operator algebra]] description of local [[CFT]] but on the [[AQFT]] description via [[conformal nets]] is in

* {#CHKL09} [[Sebastiano Carpi]], Robin Hillier, [[Yasuyuki Kawahigashi]], [[Roberto Longo]], _Spectral triples and the super-Virasoro algebra_, Commun.Math.Phys.295:71-97 (2010) ([arXiv:0811.4128](http://arxiv.org/abs/0811.4128))

where [[2d SCFTs]] are related essentially to [[local nets]] of [[spectral triples]].

Exposition of these results is in 

* [[Urs Schreiber]], _[Spectral Standard Model and String Compactifications](https://www.physicsforums.com/insights/spectral-standard-model-string-compactifications/)_, PhysicsForums--Insights (2016)

See also the references at [[geometric model for elliptic cohomology]].

That the [[Connes-Lott models]] could be [[effective field theory]]-limits of [[perturbative string theory vacua]] is also mentioned in 

* {#Connes06} [[Alain Connes]],  p. 8 of _Noncommutative Geometry and the standard model with neutrino mixing_, JHEP0611:081,2006 ([arXiv:hep-th/0608226](http://arxiv.org/abs/hep-th/0608226))





[[!redirects 2-spectral triples]]