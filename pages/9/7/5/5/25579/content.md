
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The term *representation stability* &lbrack;[Church & Farb (2013)](#ChuchFarb13)&rbrack; refers to the phenomenon that for various [[sequences]] of [[group representations]] which arise in [[topology]] --- notably for  ([[symmetric group representations]] on) ([[cohomology groups|co]])[[homology groups]] of  ordered [[configuration spaces of points]] and other [[moduli spaces]] --- certain aspects, such as the multiplicities of [[irrep|irreducible]] sub-representations, eventually stabilize. 

Specifically for the case of the [[ordinary homology]] of [[configuration spaces of points]] the phenomenon of representation stability is a refinement of the older notion of *[homological stabilization](configuration+space+of+points#HomologyAndStabilization)*:
Namely, where homological stabilization applies to *un*-ordered configurations of points, and says that the [[ordinary homology]] of these spaces eventually stabilizes (i.e. no longer increases) as the number of points grows, the same is far from true, at face value, for the *ordered* configuration spaces, the rank of whose homology groups instead increases strictly monotonically with the number of points. But the homology of unordered configuration spaces is still equipped with an [[group action|action]] of the [[symmetric group]] $Sym(n)$ on the given number of points, and the statement of *representation stability* is that *as [[representation theory of the symmetric group|symmetric group representations]]* the homology still does stabilize, notably in that the number and multiplicity of [[irreducible representations]] stabilizes. 

In particular, the homology of the un-ordered configuration spaces is canonically included into that of ordered configuration spaces as the summand of the [[trivial representation]], and in this way representation stability does subsume and generalize the phenomenon of [homological stabilization](configuration+space+of+points#HomologyAndStabilization).

Moreover, it turns out that the general phenomenon and the details of representation stability for ordered [[configuration spaces of points]] is abstractly all governed by the fact that, as one looks at all numbers of points at once, their homology forms an *[[FI-representation]]* namely a [[functor]] from the [[category]] [[FinSetInj|$FinSet_{inj}$]] of [[finite sets]] with (just) [[injections]] between them.


## References

The observation originates with:

* {#ChurchFarb13} [[Thomas Church]], [[Benson Farb]], *Representation theory and homological stability*, Advances in Mathematics
**245** (2013) 250-314 &lbrack;[doi:10.1016/j.aim.2013.06.016](https://doi.org/10.1016/j.aim.2013.06.016)&rbrack;

Lecture notes:

* [[Steven V Sam]], *Representation stability*, lecture notes (2017) &lbrack;[pdf](https://mathweb.ucsd.edu/~ssam/old/17F-847/notes.pdf)&rbrack;

Introduction and review:

* [[Benson Farb]], *Representation Stability* &lbrack;[arXiv:1404.4065](https://arxiv.org/abs/1404.4065)&rbrack;

* [[Jenny Wilson]], *A brief introduction to representation stability*, Oberwolfach Workshop (Jan 2018) &lbrack;[pdf](https://dept.math.lsa.umich.edu/~jchw/OberwolfachTalk-IntroductionToRepStability.pdf), [[Wilson-RepresentationStability.pdf:file]]&rbrack;

* [[Jennifer C. H. Wilson]], *Representation stability and the braid groups*, talk at *[ICERM -- Braids](https://icerm.brown.edu/programs/sp-s22/)* (Feb 2022) &lbrack;[pdf](https://app.icerm.brown.edu/assets/362/3661/3661_3250_021720221430_Slides.pdf)&rbrack;

* {#Wilson23} [[Jenny Wilson]], *Stability patterns for braid groups and configuration spaces*, [talk at](Center+for+Quantum+and+Topological+Systems#WilsonApr2023) [[CQTS]] (Apr 2023) &lbrack;[web](Center+for+Quantum+and+Topological+Systems#WilsonApr2023), slides:[[Wilson-CQTS-Apr-2023.pdf:file]], video:[YT](https://www.youtube.com/watch?v=uO2CFY7h5lo)&rbrack;

* [[Rita Jimenez Rolland]], [[Jennifer C. H. Wilson]], *Stability properties of moduli spaces*, Notices of the AMS [**69** 4](https://www.ams.org/notices/202204/202204FullIssue.pdf) (April 2022) &lbrack;[arXiv:2201.04096](https://arxiv.org/abs/2201.04096), [pdf](https://www.ams.org/journals/notices/202204/rnoti-p522.pdf), [web](https://www.ams.org/journals/notices/202204/noti2452/noti2452.html)&rbrack;

Expressing the [[rational cohomology]] of [[ordered configuration spaces of points]] via [[factorization homology]] and [[Ran spaces]], and relation to higher representation stability:

* [[Quoc P. Ho]], _Higher representation stability for ordered configuration spaces and twisted commutative factorization algebras_ &lbrack;[arXiv:2004.00252](https://arxiv.org/abs/2004.00252)&rbrack;

In view of [[FI-representation]]-theory:

* [[Trevor Hyde]], *$FI$-Modules and Representation Stability* (2016) &lbrack;[pdf](https://math.uchicago.edu/~tghyde/Hyde%20--%20FI-modules%20and%20representation%20stability.pdf)&rbrack;

* [[Nir Gadish]], *Categories of FI type: a unified approach to generalizing representation stability and character polynomials*, Journal of Algebra **480** (2017) 450-486 &lbrack;[arXiv:1608.02664](https://arxiv.org/abs/1608.02664), [doi:10.1016/j.jalgebra.2017.03.010](https://doi.org/10.1016/j.jalgebra.2017.03.010)&rbrack;

* [[Joe Moeller]], *Extensions of representation stable categories* &lbrack;[arXiv:2209.03879](https://arxiv.org/abs/2209.03879)&rbrack;


See also:

* [[Christin Bibby]], [[Nir Gadish]], *A generating function approach to new representation stability phenomena in orbit configuration spaces*, Trans. Amer. Math. Soc. Ser. B **10** (2023) 241-287 &lbrack;[ams:S2330-0000-2023-00130-3](https://www.ams.org/journals/btran/2023-10-09/S2330-0000-2023-00130-3), [arXiv:1911.02125](https://arxiv.org/abs/1911.02125)&rbrack;



