
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### Statement

In [Awodey 09](#Awodey09), [Awodey 10](#Awodey10) was first expressed 
the idea that [[dependent type theory]] with intensional [[identity types]] ([[Martin-Löf dependent type theory]]), viewed as [[homotopy type theory]], is in similar relation to the concept of [[(∞,1)-toposes]] as [[extensional type theory]] is to the ordinary concept of [[toposes]] (as discussed at [[relation between type theory and category theory]]).

From [Awodey 09, p. 13](#Awodey09), [Awodey 10, p. 15](#Awodey10):

> The homotopy interpretation of Martin-Löf type theory into Quillen model categories, and the related results on type-theoretic constructions of higher groupoids, are analogous to basic results interpreting extensional type theory and higher-order logic in (1-)toposes, and clearly indicate that the logic of higher toposes, and therewith of higher homotopy theory, is a form of intensional type theory.

A concise statement would be that the [[internal logic of an (∞,1)-topos|internal logic of (∞,1)-toposes]] is [[homotopy type theory]], though there is fine print involved.

Following this suggestion, the weaker form of this idea, ignoring the [[univalence|univalent]] [[type universe]] and relating to the broader class of [[locally Cartesian closed (∞,1)-categories]], was stated more concretely as a conjecture in [Joyal 11](#Joyal11). For more precision see [Kapulkin-Lumsdaine 16, p. 9](#KapulkinLumsdaine16).

Roughly, this is about the following table of correspondences (for more see at [[relation between type theory and category theory]]):

| [[internal logic]]/[[type theory]] | [[higher category theory|higher]] [[category theory]] |
|-----|--------|
| [[type theory]] | [[locally Cartesian closed categories]] |
| [[homotopy type theory]] | [[locally Cartesian closed (∞,1)-categories]] |
| [[homotopy type theory]] with [[univalence|univalent]] [[type universes]] | [[elementary (∞,1)-toposes]] |

Fore more precision see [Kapulkin-Lumsdaine 16, p. 9](#KapulkinLumsdaine16).

### Proof

A [[proof]] of the weaker version of the conjecture, in form of the statement that every [[locally presentable (∞,1)-category|locally presentable]] [[locally Cartesian closed (∞,1)-category]] is presented by a suitable [[type theoretic model category]] which provides [[categorical semantics]] for [[homotopy type theory]], was proven in [Shulman 12, Example 2.16](#Shulman12), following [Cisinski 12](#Cisinski12).

Generalizing this to a proof of the full conjecture required finding "strict" models for the [object classifier](object+classifier#DetailsObjClassf) by strict [[type universes]]. A series of article ([Shulman 12](#Shulman12), [Shulman 13](#Shulman13)) showed that this is possible in an increasing class of special cases. 

A proof of the general case was finally announced in [Shulman 19](#Shulman19).

For more see at _[[homotopytypetheory:model of type theory in an (infinity,1)-topos]]_.



## References

### Statement

The idea is due to 

* {#Awodey09} [[Steve Awodey]], _Homotopy and Type Theory_, grant proposal project description ([pdf](https://ncatlab.org/homotopytypetheory/files/proposal2009.pdf))

* {#Awodey10} [[Steve Awodey]], _Type theory and homotopy_, p. 183-201 in: Dybjer P., Lindström S., Palmgren E., Sundholm G. (eds.),  _Epistemology versus Ontology_, Springer 2012  ([arXiv:1010.1810](http://arxiv.org/abs/1010.1810), [doi:10.1007/978-94-007-4435-6_9](https://doi.org/10.1007/978-94-007-4435-6_9))

A pronounced statement of the weaker version was highlighted in

* {#Joyal11} [[André Joyal]], _Remarks on homotopical logic_ Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))

and stated more precisely in 

* {#KapulkinLumsdaine16} [[Chris Kapulkin]], [[Peter Lumsdaine]], _The homotopy theory of type theories_, Advances in Mathematics Volume 337, 15 October 2018, Pages 1-38 ([arXiv:1610.00037](https://arxiv.org/abs/1610.00037))

### Proof
 {#ReferencesProof}

The proof of the weaker version of Awodey's conjecture (that every [[locally Cartesian closed (∞,1)-category]] has a presentation by a suitable [[type-theoretic model category]] which provides [[categorical semantics]] for [[homotopy type theory]]) is due, independently, to Example 2.16 of 

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))

following

* {#Cisinski12} [[Denis-Charles Cisinski]], [blog comment](http://golem.ph.utexas.edu/category/2012/05/the_mysterious_nature_of_right.html#c041306) (2012)

The proof of the stronger version (including [[univalence|univalent]] [[type universes]] modelling [object classifier](object+classifier#DetailsObjClassf) of [[(∞,1)-toposes]]) was found for the special case of [[(∞,1)-presheaf (∞,1)-toposes]] over [[elegant Reedy categories]] in

* [Shulman 12](#Shulman12)

* {#Shulman13} [[Michael Shulman]], _The univalence axiom for elegant Reedy presheaves_, Homology, Homotopy and Applications Volume 17 (2015) Number 2 ([arXiv:1307.6248](https://arxiv.org/abs/1307.6248), [doi:10.4310/HHA.2015.v17.n2.a6](http://dx.doi.org/10.4310/HHA.2015.v17.n2.a6))

A general proof was announced in

* {#Shulman19} [[Michael Shulman]], slides 5 to 10 of _Semantics of higher modalities_, talk at _[Geometry in Modal HoTT (2019)](http://www.andrew.cmu.edu/user/fwellen/modal-workshop.html)_ ([pdf slides](http://home.sandiego.edu/~shulman/papers/cmu2019b.pdf), [video recording](https://www.youtube.com/watch?v=Wcpi1vVMrCs))

and appeared in

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004)).

[[!redirects Awodey proposal]]

[[!redirects Awodey conjecture]]
[[!redirects Awodey's conjecture]]

[[!redirects Awodey&#39;s conjecture]]
[[!redirects Awodey&#39;s conjecture]]

