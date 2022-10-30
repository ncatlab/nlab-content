
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Hopf invariant one_ refers to [[homotopy classes]] of [[continuous functions]] between [[spheres]] of the form

$$
  \phi \;\colon\; S^{2n-1} \longrightarrow S^n
  \,,
$$

hence to elements in the [[homotopy groups of spheres]]

$$
  [\phi] \in \pi_{2n-1}(S^n)
$$

whose [[Hopf invariant]] is equal to one:

$$
  h(\phi) = 1
  \,.
$$



## Properties

### Relation to H-space structure and normed division algebras
 {#RelationToHSpaceStructureAndNormedDivisionAlgebras}

The existence of an element of Hopf invariant one in $\pi_{2n-1}(S^n)$
is equivalent to the existence of an [[H-space]] structure on $S^{n-1}$.

A celebrated theorem due to ([Adams 60](#Adams60), introducing and using the [[Adams spectral sequence]])  states that maps of Hopf invariant one correspond precisely to the the [[Hopf constructions]] on the four [[normed division algebras]] (see also at [[Hurwitz theorem]]): the [[real Hopf fibration]], the [[complex Hopf fibration]], the [[quaternionic Hopf fibration]] and the [[octonionic Hopf fibration]]. 

 <img src="http://ncatlab.org/nlab/files/AdamsHopfInvariantProofFlow.jpg" width="700">

([Adams 60](#Adams60))

## History

> [[stable homotopy theory|Stable homotopy theory]] emerged as a distinct branch of [[algebraic topology]] with [[Frank Adams|Adams]]' introduction of [[Adams spectral sequence|his eponymous spectral sequence]] and his spectacular conceptual use of the notion of stable phenomena in his solution to the Hopf invariant one problem.

> ([Elmendorf-Kriz-May 95](#ElmendorfKrizMay95))

## Related concepts

* [[division algebra and supersymmetry]]

* [[cross product]]

* [[parallelizable manifold|parallelizable]] [[n-sphere]]

[[!include exceptional spinors and division algebras -- table]]

* [[Arf-Kervaire invariant problem]]


## References

The original proof that the only maps of Hopf invariant one are the [[Hopf constructions]] on the four [[normed division algebras]] is due to

* {#Adams60} [[Frank Adams]], _On the non-existence of elements of Hopf invariant one_, Ann. Math., Vol. 72, No. 1,  72 (1): 20&#8211;104, (1960) ([jstor:1970147](http://www.jstor.org/stable/1970147))

and made use of the [[classical Adams spectral sequence]]. 

Review includes

* [[Doug Ravenel]], chapter 1, section 2: _Methods of computing $\pi_\bullet(S^n)$_ in: _[[Complex cobordism and stable homotopy groups of spheres]]_

* {#Rognes12} [[John Rognes]], around lemma 4.14, theorem 4.15 of _The Adams spectral sequence_, 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

* Joseph Victor, Section 2.4 of _Stable Homotopy Groups of Spheres and The Hopf Invariant One Problem_, 2013 ([pdf](http://mathematics.stanford.edu/wp-content/uploads/2013/08/Victor-Honors-Thesis-2013.pdf))

Further comments on the impact of this proof on the development of [[stable homotopy theory]] includes

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland, (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

Another proof that instead uses [[topological K-theory]], [[Adams operations]] and the [[Atiyah-Hirzebruch spectral sequence]] was given in 

* {#AdamsAtiyah66} [[Frank Adams]], [[Michael Atiyah]], _K-theory and the Hopf invariant_, Quart. J. Math. Oxford (2), 17 (1966), 31-38 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/adamatiy.pdf), [doi:10.1093/qmath/17.1.31](https://doi.org/10.1093/qmath/17.1.31))

This is reproduced/reviewed in:

* {#Husemoller66} [[Dale Husemöller]], chapter 15 of _Fibre Bundles_, Graduate Texts in Mathematics 20, Springer New York (1966)

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 12 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))

* {#Hatcher} [[Allen Hatcher]], section 2.3 of _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))


* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 10.6 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* [[Ulrich Pennig]], _[K-theory and the Hopf invariant](http://wwwmath.uni-muenster.de/reine/u/topos/lehre/SS2015/KTheorie-Hopf/Hopf_eng.html)_ 

Review of this K-theoretic approach includes:

* [[Akhil Mathew]], _[K-Theory and the Hopf invariant](https://amathew.wordpress.com/2012/01/08/k-theory-and-the-hopf-invariant/)_

* Ishan Banerjee, _The Hopf invariant one problem_, 2016 ([pdf](http://math.uchicago.edu/~may/REU2016/REUPapers/Banerjee.pdf))


Review using the [[BP]]-[[Adams-Novikov spectral sequence]] includes

* [[Doug Ravenel]], chapter 5, section 2 _[[Complex cobordism and stable homotopy groups of spheres]]_


[[!redirects Hopf invariant 1]]

[[!redirects Hopf invariant one theorem]]

[[!redirects Hopf invariant one problem]]
