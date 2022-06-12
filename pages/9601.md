
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There exists the [[model category]] structure on the [[category]] of [[semi-simplicial sets]] which is [[transferred model structure|transferred]] along the [[right adjoint]] to the [[forgetful functor]] from the [[classical model structure on simplicial sets]] ([van den Berg 13](#vandenBerg)). See [this discussion](https://nforum.ncatlab.org/discussion/4861/model-structure-on-semisimplicial-sets/?Focus=56290#Comment_56290), which seems to conclude that this is [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on simplicial sets]].

There is also a [[weak model category]] structure ([Henry 18](#Henry18)), for which the Quillen equivalence to simplicial sets is proven as [Henry 18, Thm 5.5.6 (iv)](#Henry18).

Also there is the structure of a [[semimodel category]] ([Rooduijn 2018](#Rooduijn2018)) and of a [[fibration category]] on semisimplicial sets ([Sattler 18, Th, 3.18](#Sattler18)) (and [[cofibration category]] on fibrant-cofibrant objects).


## References
 {#References}

As a [[model category]]-structure:

* {#vandenBerg} [[Benno van den Berg]], _A note on semisimplicial sets_, 2013 ([[vandenBerg_SemisimplicialSets.pdf:file]])

As a [[weak model category]]:

* {#Henry18} [[Simon Henry]], Theorem 5.5.6 of: *Weak model categories in classical and constructive mathematics*, Theory and Applications of Categories, Vol. 35, 2020, No. 24, pp 875-958.  ([arXiv:1807.02650](https://arxiv.org/abs/1807.02650), [tac:35-24](http://www.tac.mta.ca/tac/volumes/35/24/35-24abs.html))

As a right [[semimodel category]]:

* {#Rooduijn2018} Jan Rooduijn, *A right semimodel structure on semisimplicial sets*, Amsterdam 2018 ([pdf](https://eprints.illc.uva.nl/id/eprint/1663/1/MoL-2018-34.text.pdf), [mol:4787](https://msclogic.illc.uva.nl/theses/archive/publication/4787/A-right-semimodel-structure-on-semisimplicial-sets))

As a [[fibration category]]:

* {#Sattler18} [[Christian Sattler]], *Constructive homotopy theory of marked semisimplicial sets* ([arXiv:1809.11168](https://arxiv.org/abs/1809.11168))

The above note contains a mistake in Theorem 3.43: semisimplicial sets do not form a [[cofibration category]] as considered there: (cofibration, weak equivalence)-factorizations do not generally exist (cf. the paragraph at the end of Subsection 3.2). Instead, the notion of cofibration category has to be weakened using a notion of pseudofactorizations (similar to the notion of weak model category).

[[!redirects model structure on semisimplicial sets]]

[[!redirects weak model structure on semi-simplicial sets]]
[[!redirects weak model structure on semisimplicial sets]]

[[!redirects semimodel structure on semisimplicial sets]]
[[!redirects semi-model structure on semi-simplicial sets]]

[[!redirects fibration category of semi-simplicial sets]]
[[!redirects fibration category of semisimplicial sets]]
