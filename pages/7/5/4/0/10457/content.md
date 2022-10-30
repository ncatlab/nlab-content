

> The following surveys how basic [[theorems]] about the standard foundation of [[quantum mechanics]] imply an accurate [[geometry|geometric]] incarnation of the "[[phase space]] in [[quantum mechanics]]" by an [[order theory|order-theoretic structure]] that combines with an [[algebra|algebraic]] structure to a [[ringed topos]], the "[[Bohr topos]]". While the notion of [[Bohr topos]] has been _motivated_ by the [[Kochen-Specker theorem]], the point here is to highlight that taking into account further theorems about the standard foundations of [[quantum mechanics]], the notion effectively follows automatically and provides an accurate and useful description of the geometry of "quantum phase space" also in [[quantum field theory]] formulated in the style of [[AQFT]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## The quantum phase space as a Jordan-geometry given by a ringed topos
  {#QuantumPhaseSpaceAsJordanGeometry}



Back when [[quantum mechanics]] was discovered in the first half of the 20th century, it was eventually formalized as [[mathematical physics]] and eventually the traditional modern formulation emerged, where, in [[AQFT]] perspective, [[quantum observables]] are represented by suitable [[operators]] on a [[Hilbert space]] and more generally by elements of a [[C*-algebra]] [[algebra of observables|of observables]], and where [[quantum states]] are certain (namely positive and normalized) linear functionals on these [[C*-algebra|C*]]-[[algebras of observables]].

But one may still ask if the [[axioms]] in the definition of _[[C*-algebra]]_ accurately capture the intended [[physics]]. This or similar questions were discussed back in the middle of the 20th century, when these notions were still in flux. Specifically in the 1930s [[Pascual Jordan]] argued ([Jordan 32](#Jordan32)) that the [[associative algebra]] structure on the observables is more structure than supported by the physics of states and observation, that instead only the underlying structure of what is now called the _[[Jordan algebra]]_ should matter.

Much later in 1978 this idea was formally validated by the [[Alfsen-Shultz theorem]] ([Alfsen-Shultz 78](#AlfsenShultz78)). This states that the [[space of quantum states]] for given [[quantum observables]] depends indeed only on the underlying [[Jordan algebra]] structure. This is not too surprising: the definition of a [[state on an operator algebra]] does not even mention the [[associative algebra]] structure but mentions only the [[positive operator|positivity]] structure, which is what the [[Jordan algebra]] captures.


Despite these insights, [[Jordan algebras]] found and find only marginal attention in [[mathematical physics]]. In a [review from 2004](#ASReview04) of the book of Alfsen and Shultz it says that back then Jordan algebras were hoped to shed light on conceptual problems of genuine [[quantum field theory]], but that these hopes never materialized. However, more recent developments change this picture a bit, we come to that below.

Much more recently in 2010, the [[Harding-Döring-Hamhalter theorem]] sheds a new light on the role of [[Jordan algebra]] structure. This theorem states mild conditions under which a [[Jordan algebra]] structure on [[quantum observables]] is equivalently encoded in the [[poset of commutative subalgebras]] of the full [[C*-algebra]].

These commutative subalgebras themselves are of course of old fame in quantum mechanics, they are the "[[classical contexts]]" given by tuples of [[quantum observables]] that all commute with each other and hence which can all be [[measurement|measured]] simultaneously without the [[uncertainty principle]] interfering. These [[classical contexts]] played a crucial role in the discussion of the foundation of quantum mechanics in the first half of the 20th century: back then people argued that for $A$ and $B$ two [[quantum observables]] which do not commute with each other it is unclear what it means physically to form their sum $A + B$ or their product $A B$, hence that a [[quantum state]] should be demanded to be a linear (and positive normed) [[functional]] on all [[poset of commutative subalgebras|commutative subalgebras]], but not necessarily on the whole non-commutative algebra. Such a notion of "quantum state on all [[classical contexts]]" was called a _[[quasi-state]]_.

The issue of whether quasi-states are a more accurate description of quantum [[measurement]] was settled in 1957 by [[Gleason's theorem]] ([Gleason 57](#Gleason57)), which says that given a  [[Hilbert space]] of [[dimension]] greater than 2, then the [[quasi-states]] are automatically [[quantum states]] also on the full non-commutative [[algebra of observables]]. Typically this is viewed as making the notion of [[quasi-state]] obsolete, but since that is a formally weaker notion the opposite attitude makes sense: what is traditionally taken as the definition of [[quantum state]] is more accurately thought of as being a [[quasi-state]], hence something that is intrinsically related not to a non-commutative algebra of observables, but to the "[[classical contexts]]" of its [[poset of commutative subalgebras]].

Indeed, by combining the [[Alfsen-Shultz theorem]] with the [[Harding-Döring-Hamhalter theorem]], we have (under the pertinent mild assumptions) that two algebras of observables have the same [[space of quantum states]] already when they have the same [[poset of commutative subalgebras]]. Notice that where [[Gleason's theorem]] only involves the commutative subalgebras themselves, this Jordan-Alfsen-Shultz-Harding-D&#246;ring-Hamhalter theorem crucially involves their [[order]] of inclusions, hence the actual [[poset]] structure of their inclusions. 



Therefore there is an intrinsic [[order theory|order theoretic]] aspect in the standard foundations of [[quantum mechanics]]. But it is not _just_ order theory, for it is the [[poset]] structure of inclusions alone that matters in the Jordan-Alfsen-Shultz-Harding-D&#246;ring-Hamhalter theorem, but that poset structure together with the actual [[commutative C*-algebra]] structure of each [[classical context]]. 


There is an elegant way to combine these two aspects: a system of [[commutative ring|commutative algebras]] together with the [[order]] of their inclusions is equivalently a single [[algebra object]] [[internalization|internal to]] the [[sheaf topos]] over the [[poset]]. With some basics of [[topos theory]] in hand this is a trivial statement, but in view of the above it is worthwhile to make explicit: the Jordan-Alfsen-Shultz-Harding-D&#246;ring-Hamhalter theorem ([Harding-D&#246;ring 10](#HardingDoering10), [Hamhalter 11](#Hamhalter11)) says that the collection of [[quantum observables]] in [[quantum mechanics]] is accurately formalized by a single [[commutative C*-algebra]] [[internalization|internal]] to a [[sheaf topos]] over a [[poset]].

It has been argued that this serves as a formalization of the views on [[quantum mechanics]] that in the middle of the 20th century [[Niels Bohr]] expressed in extensive but informal writing (see [Scheibe 73](#Scheibe73)): he said roughly that whatever [[quantum mechanics]] is, it must be expressible and must be expressed through classical contexts. In honor of this intuition, the above [[toposes]] deserve to be called _[[Bohr toposes]]_, following the term "Bohrification" in ([Heunen-Landsman-Spitters 09](#HeunenLandsmanSpitters09)).

In fact, a [[Bohr topos]] is fairly trivial as far as [[toposes]] go, since, by the above, it is just a reflection -- precisely: the "[[localic reflection]]" -- of a purely [[order theory|order theoretic structure]]. But the key is that passing to the topos over the [[poset]] provides a home for the context-wise [[commutative C*-algebra]] structure which makes the [[Bohr topos]] have the additional structure of a _[[ringed topos]]_. This is the additional [[algebra|algebraic]] datum on top of the purely  [[order theory|order theoretic]] datum in the [[Jordan algebra]] structure of [[quantum observables]].

Ringed toposes have of course a long tradition in [[geometry]] (most famously in [[algebraic geometry]]). By [[Grothendieck]]'s foundational work, laid out in the [thesis](#Hakim72) of [[Monique Hakim]], ringed toposes form a general foundation for structured [[geometry]]. More recently this was further strengthened and refined by [[Jacob Lurie]] by the notion of [[structured (infinity,1)-topos|higher ringed toposes]], which we will see appear in [[quantum field theory]] below. In as far as the [[quantum observables]] in [[quantum mechanics]] are supposed to be the [[Isbell duality|dual]] of the _[[phase space]]_, it is therefore natural to have this "quantum phase space" be realized as a [[ringed topos]]. 

Notice that this is a different geometric interpretation of "quantum phase space" than the traditional idea that quantum phase space is an object in [[non-commutative geometry]]! Here by the Jordan-Alfsen-Shultz-Harding-D&#246;ring-Hamhalter theorem we see that it is not actually accurate to say that quantum phase space is dually given by a non-commutative [[C*-algebra]], as in fact it is given dually just by a [[Jordan algebra]]. The [[ringed topos|ringed]] [[Bohr topos]] provides a natural [[geometry|geometric]] interpretation of this, one might call it "Jordan geometry".

This geometric nature of the Bohr topos becomes more manifest as we consider its [[opposite category]]. By [[Gelfand duality]] this carries not an internal [[commutative C*-algebra]] but its [[Gelfand spectrum]]: an actual internal [[topological space]]. This internal topological space has been called the _[[spectral presheaf]]_ ([Butterfield-Hamilton-Isham 98](#ButterfieldHamiltonIsham98)).

While here we find this [[spectral presheaf]] as an accurate dual description of the space of [[quantum observables]] in [[quantum mechanics]] based on the Jordan-Alfsen-Shultz-Harding-D&#246;ring-Hamhalter theorem, interest in the spectral presheaf originally came from the observation that it provides a clear geometric formulation of yet another theorem about the foundations of [[quantum mechanics]], namely of the _[[Kochen-Specker theorem]]_ ([Kochen-Specker 67](#KochenSpecker67)). 

This again amplifies the role of the "classical contexts" of commutative subalgebras: one may ask if there is a [[hidden variable]] description of [[quantum mechanics]] that allows to assign actual values to all [[quantum observables]] such that in all [[classical contexts]] this assignment behaves as an actual [[classical observable]] in that it provies a (star-)[[homomorphism]] of [[associative algebras]] from the [[commutative C*-algebra]] of the classical context to the real numbers. The [[Kochen-Specker theorem]] rules out such a [[hidden variable theory]] by stating that when the [[algebra of observables]] is that of [[bounded operators]] on a [[Hilbert space]] of [[dimension]] greater than 2, then such a "hidden variable" assignment cannot exist.

In ([Butterfield-Isham 98](#IshamButterfield98) it was observed, that this statement has a natural geometric interpretation in the [[Bohr topos]]: it simply says that the [[spectral presheaf]], hence the "Jordan-algebraic geometry" incarnation of quantum phase space, has no [[global element]]. This statement in turn is a characterization of how the quantum phase space is "exotic" as far as [[spaces]] go. It behaves like a non-trivial space, and yet there is no way to map a point into it as a whole, maps of points into it exist only locally. 

In summary, the [[Bohr topos]] incarnation of the Jordan-Alfsen-Shultz-Harding-D&#246;ring-Hamhalter characterization of quantum observables not only accurately captures the nature of quantum observables, but also makes other subtle nature of [[quantum mechanics]] becomes more explicitly evident than in other formulations.

To see how one can get more out of the [[Bohr topos]] incarnation of the quantum phase space, it serves to pass from plain [[quantum mechanics]] to the more general context of [[quantum field theory]]. Here the original [[Haag-Kastler axioms]] of [[AQFT]] demand that to a region of [[spacetime]] is to be assigned the [[quantum observables]] as a [[C*-algebra]]/[[von Neumann algebra]]. But by the above discussion it is rather only the underlying [[Jordan algebra]] structure that matters, hence the [[Bohr topos]]. In light of this a [[local net of observables]] in [[AQFT]] is naturally regarded as a [[presheaf]] of [[ringed toposes]] on [[spacetime]], assigning the respective [[Bohr topos]] of local observables to each local region of spacetime.

Such "Bohrification of local nets of observables" were analyzed in ([Nuiten 12](#Nuiten12)). There it was found that the natural structure of the transition functions of local nets of Bohr toposes of observables by [[geometric morphisms]] automatically capture the [[causal locality]] condition of [[local quantum field theory]]. This is now called "Nuiten's lemma" in ([Wolters-Halvorson 13](#WoltersHalvorson13)). Moreover, ([Nuiten 12](#Nuiten12)) shows that a natural [[descent]] condition on spacetime nets of [[Bohr toposes]] is equivalent to _[strong locality](local+net#StrongLocality)_ of the [[quantum field theory]], something slightly weaker than _[Einstein causality](local+net#EinsteinLocality)_, which implies it. Since, by the above, the [[Bohr topos]] is the geometric incarnation of the [[Jordan algebra]] structure on [[quantum observables]], one might see this as a reply to the alleged lack of implications (in [the AS review, 04](#ASReview04)) fo [[Pascual Jordan]]'s ideas from the 1930s to quantum field theory.

Be that as it may, notice that generally local systems of [[ringed toposes]] are to be expected to naturally encode [[quantum field theory]] on general grounds: the modern [[AQFT]]-style formulation of [[classical field theory]]/[[prequantum field theory]] via [[factorization algebras]] or similar assigns to subsets of [[spacetime]] the [[derived critical locus]] of local [[field (physics)|fields]] extremizing the given [[local action functional]], hence the [[derived geometry|derived space]] of solutions to the [[Euler-Lagrange equations]] of motion: the [[covariant phase space]] (pre-quantum). In [[physics]] this [[derived critical locus]] is modeled explicitly as a [[BV-BRST formalism|BV-complex]], but when realized in the full technical beauty of [[derived geometry]] it is in fact a [[structured (infinity,1)-topos|higher ringed topos]], as explained by [[Jacob Lurie]]. In view of this incarnation of [[classical field theory]] in [[AQFT]]-perspective as a net of [[structured (infinity,1)-topos|higher ringed topos]], it seems rather natural that under [[quantization]] it remains a net of ringed toposes, sending ringed toposes incarnating classical [[covariant phase spaces]] to ringed toposes incarnating their quantized version as quantum phase spaces.

## Relation to the traditional non-commutative geometry
 {#RelationToTheNonCommutativePhaseSpace}

In the above we highlighted that by [the fundamental theorems](#ListOfTheoremsInvoked) on the foundations of [[quantum mechanics]] -- going back to insights of [[Pascual Jordan]] way back in 1930 and formally affirmed by more recent results by Alfsen-Shultz and Harding-D&#246;ring -- it follows that, accurately speaking, quantum phase space is not really an object in [[noncommutative geometry]], but rather in a kind of _non-associative_ "Jordan geometry" which is naturally captured by the [[ringed topos|ringed]] [[Bohr topos]] over the [[poset of commutative subalgebras]].

This observation indeed puts doubt on the long and widely held believe that the quantum phase space is an object in [[noncommutative geometry]], a believe that in fact motivated much of the development of [[noncommutative geometry]] in the first place.

But that this is not really true was "well known" all along: it is pointed out for instance in the foundational text ([Bates-Weinstein 97](#BatesWeinstein97)) on [[geometric quantization]]. On page 80 there is highlighted how given a classical [[phase space]] represented by a [[Poisson manifold]] $(X, \{-,-\})$, hence of a [[manifold]] that carries 

1. a commutative algebra of classical observables 

1. equipped with a compatible non-commutative [[Lie bracket]] $\{-,-\}$ (the [[Poisson bracket]])

the [[quantization]] of this data is to be thought of as applying to these two items separately: 

1. a non-associative but commutative [[Jordan algebra]] structure of quantum observables is the [[deformation quantization]] of the commutative algebra structure of classical observables;


1. a non-commutative [[Lie bracket]] structure is the deformation quantization of the Poisson bracket

and that if the quantization of both items is given by a single [[C*-algebra]] structure, then the non-associative commutative Jordan algebra structure is the one induced by the anticommutator

$$
  A \circ B = \tfrac{1}{2}(A B + B A)
$$

while the non-commutative algebra structure is that given by the commutator

$$
  [A,B] = \tfrac{1}{2}(A B - B A)
$$

See also at _[Jordan algebra -- Origin in quantum physics](Jordan+algebra#OriginInQuantumPhysics)_.

To understand that this makes good sense notice that this decomposition is that into [[kinematics]] and [[dynamics]] of [[quantum mechanics]]:

1. [[kinematics]] --- the construction of the [[quantum observables]] and of the [[space of quantum states]] alone indeed does _not_ involve the associative product of the [[C*-algebra]];

1. [[dynamics]]  ---  the commutator [[Lie bracket]] structure is used to impose quantum [[Hamiltonian flows]] $\exp([A,-])$, hence (time) propagation along the [[trajectories]] generated by the observables $A$.

But then observe in addition that when we pass from [[quantum mechanics]] to [[quantum field theory]] axiomatized as [[AQFT]], then in fact time propagation is no longer implemented by [[inner automorphisms]] of the form $\exp([A,-])$. Indeed it is impossible for any realistic [[physical system]] with infinitely many degrees of freedom (such as a [[field (physics)|field]]) to have time evolution given by an [[inner automorphism]]. That this does work for [[quantum mechanics]] is really an artifact of the degenerate case of finitely many degrees of freedom considered there.

Instead, in [[AQFT]] the [[spacetime]]-evolution of the quantum fields is all encoded in the transition functions of the [[local net of observables]]. By the [above](#QuantumPhaseSpaceAsJordanGeometry) discussion, this is however accurately speaking not actually a net of [[C*-algebras]], but a net of [[Jordan algebra]], hence a net of [[Bohr toposes]]. This way the need for the non-commutative algebraic structure disappears and only the non-associative commutative [[Jordan algebra]] structure remains.

In this context it may be noteworthy to recall what is a well-kept secret: despite much work on [[AQFT]] with the traditional [[Haag-Kastler axioms]] that demand to assign [[C*-algebras]] to regions of spacetime, there is to date not a single non-[[free field theory|free field]] example in [[spacetime]] [[dimension]] greater than 3 of these axioms. (There are plenty of interesting example in dimension 2, though, see at _[[conformal net]]_ and pointers given there.)

On the other hand, more recently the variant of the [[AQFT]] axioms known as _[[factorization algebras]]_ has been shown to admit plenty of interesting examples of [[quantum field theory]]. Comparison of the axioms is not straightforward and should be taken with a grain of salt, but it is maybe noteworthy that a [[factorization algebra]] is indeed a net that assigns to a region of spacetime _not_ an algebra structure. The algebra structure there is instead all encoded into the way that spacetime regions are included into each other.



## List of theorems invoked
 {#ListOfTheoremsInvoked}

For reference, the following lists that theorems about the standard foundations of quantum mechanics that are being referred to [above](QuantumPhaseSpaceAsJordanGeometry):

* [[Gleason's theorem]]

* [[Alfsen-Shultz theorem]]

* [[Harding-Döring-Hamhalter theorem]]

* [[Kochen-Specker theorem]]

* [[Nuiten's lemma]]


## References

*  [[Pascual Jordan]], &#220;ber eine Klasse nichtassociativer
hyperkomplexer Algebren, _Nachr. Ges. Wiss. G&#246;ttingen
(1932), 569--575.
 {#Jordan32}

* [[Pascual Jordan]], [[John von Neumann]] and [[Eugene Wigner]], On an algebraic generalization of the quantum mechanical formalism, _Ann. Math._ **35** (1934), 29--64.
 {#JordanvNeumannWigner34}

* A.M. Gleason, _Measures on the closed subspaces of a Hilbert space_, Journal of Mathematics and Mechanics,  Indiana Univ. Math. J. 6 No. 4 (1957), 885&#8211;893 ([web](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050))
  {#Gleason57}

* [[Simon Kochen]], [[Ernst Specker]], _The problem of hidden variables in quantum mechanics_ , Journal of Mathematics and Mechanics 17, 59&#8211;87 (1967), ([pdf](http://www.iumj.indiana.edu/IUMJ/FTDLOAD/1968/17/17004/pdf))
  {#KochenSpecker67}


* [[Monique Hakim]], _Topos annel&#233;s et sch&#233;mas relatifs_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 64, Springer, Berlin, New York (1972). 
  {#Hakim72}

* Erhard Scheibe, _The logical analysis of quantum mechanics_ . Oxford: Pergamon Press, 1973.
 {#Scheibe73}

* [[Erik Alfsen]], [[Frederic Shultz]], _A Gelfand Neumark theorem for Jordan algebras_, Advances in Math., 28 (1978), 11-56.
  {#AlfsenShultz78}

* [[Erik Alfsen]], H. Hanche-Olsen, [[Frederic Shultz]], _State spaces of $C^\ast$-algebras_, Acta Math., 144 (1980), 267-305.
  {#AlfsenHOShultz80}

* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_  American Mathematical Society in the Berkeley Mathematics Lecture Notes series, 1997 ([pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf))
  {#BatesWeinstein97}

* [[Jeremy Butterfield]], [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem: I. Quantum States as Generalized Valuations_ ([arXiv:quant-ph/9803055](http://arxiv.org/abs/quant-ph/9803055))
  {#IshamButterfield98}

* [[Jeremy Butterfield]], John Hamilton, [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem_, _I. quantum states as generalized valuations_, Internat. J. Theoret. Phys. 37(11):2669--2733, 1998, [MR2000c:81027](http://www.ams.org/mathscinet-getitem?mr=1669557), [doi](http://dx.doi.org/10.1023/A:1026680806775); _II. conceptual aspects and classical analogues_ Int. J. of Theor. Phys. 38(3):827--859, 1999, [MR2000f:81012](http://www.ams.org/mathscinet-getitem?mr=1697983), [doi](http://dx.doi.org/10.1023/A:1026652817988); _III. Von Neumann algebras as the base category_, Int. J. of Theor. Phys. 39(6):1413--1436, 2000, [arXiv:quant-ph/9911020](http://arxiv.org/abs/quant-ph/9911020), [MR2001k:81016](http://www.ams.org/mathscinet-getitem?mr=1788498),[doi](http://dx.doi.org/10.1023/A:1003667607842); _IV. Interval valuations_, Internat. J. Theoret. Phys. __41__ (2002), no. 4, 613&#8211;639, [MR2003g:81009](http://www.ams.org/mathscinet-getitem?mr=1902067), [doi](http://dx.doi.org/10.1023/A:1015276209768)    
  {#ButterfieldHamiltonIsham98}

* review of Alfsen-Shultz, 2004 ([pdf](http://www.ams.org/journals/bull/2004-41-04/S0273-0979-04-01019-5/S0273-0979-04-01019-5.pdf))
 {#ASReview04}

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _Bohrification of operator algebras and quantum logic_, in _Deep Beauty_ Cambridge University Press (2009) ([arXiv:0909.3468](http://arxiv.org/abs/0909.3468), [arXiv:0905.2275](http://arxiv.org/abs/0905.2275))
  {#HeunenLandsmanSpitters09}

* [[John Harding]], [[Andreas Döring]], _Abelian subalgebras and the Jordan structure of a von Neumann algebra_ ([arXiv:1009.4945](http://arxiv.org/abs/1009.4945))
 {#HardingDoering10}


* [[Jan Hamhalter]], _Isomorphisms of ordered structures of abelian $C^\ast$-subalgebras of $C^\ast$-algebras_, J. Math. Anal. Appl. 383 (2011) 391&#8211;399 ([journal](dx.doi.org/10.1016/j.jmaa.2011.05.035))
 {#Hamhalter11}


* [[Joost Nuiten]], _[[schreiber:bachelor thesis Nuiten|Bohrification of local nets of observables]]_, [Proceedings of QPL 2011](http://qpl.science.ru.nl/) [EPTCS 95](http://rvg.web.cse.unsw.edu.au/eptcs/content.cgi?QPL2011), 2012, pp. 211-218 ([arXiv:1109.1397](http://arxiv.org/abs/1109.1397))
  {#Nuiten12}

* Sander Wolters, [[Hans Halvorson]], _Independence Conditions for Nets of Local Algebras as Sheaf Conditions_ ([arXiv.1309.5639](http://arxiv.org/abs/1309.5639))
  {#WoltersHalvorson13}