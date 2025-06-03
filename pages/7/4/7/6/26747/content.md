
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

All [[dependent type theories]] satisfy a meta-theoretic version of [[parametricity]] traditionally called *external parametricity*. 

**Parametric dependent type theory** is [[dependent type theory]] with an explicit notion of [[parametricity]] inside of the theory itself called **explicit parametricity**, in the same way that some dependent type theories have [[explicit substitution]]. A dependent type theory without explicit parametricity is called **non-parametric**. 

Parametric dependent type theories are distinguished by the kind of explicit parametricity that they have: 

* **External parametricity**, which applies to types and terms in the empty context. 

* **Internal parametricity**, which applies to types and terms in all contexts. 

Explicit external parametricity is not the same as meta-theoretic external parametricity in that the parametricity is partially internalized in the theory itself. The use of the bare *external parametricity* for explicit external parametricity originates from [[Narya]]'s [documentation](#NaryaDocs). 

**Note:** *In the rest of this article, we shall follow the terminology of the Narya documentation and use* external parametricity *for explicit external parametricity. To disambiguate, we shall use* meta-theoretic parametricity *for the traditional meta-theoretic notion of external parametricity.* 

The various forms of explicit parametricity differ to whether it is a conservative extension of non-parametric dependent type theory. 

* External parametricity is a [[conservative extension]] over non-parametric dependent type theory and is thus fully consistent with all classical axioms. 

* Internal parametricity is not a conservative extension; it contradicts many classical axioms such as the [[axiom of choice]] and [[excluded middle]].  

In addition, external parametricity has [[categorical semantics]] in any $(\infty,1)$-topos of [[semi-cubical objects]] in a base $(\infty,1)$-topos, while internal parametricity has [[categorical semantics]] in any $(\infty,1)$-topos of [[cubical objects]] in a base $(\infty,1)$-topos (see [Kolomatskaia & Shulman 2023](#KS23), [Narya Docs](#NaryaDocs)). 

There are also versions of explicit parametricity called **modal parametricity**, which are [[modal type theories]] with a discrete mode and a non-discrete mode, where parametricity can only be applied in the non-discrete mode and where the discrete mode is consistent with all classical axioms: 

* In external modal parametricity the parametricity in the non-discrete mode can only be applied to types and terms in contexts that are guarded by a context lock for the [[modal operator]] representing the discrete coreflection of a type. 

* In internal modal parametricity the parametricity in the non-discrete mode can be applied to types and terms in all contexts. 

These modal type theories attempt to formalize, in addition to the [[internal logic]] of a $(\infty,1)$-topos of cubical or semi-cubical objects, also the internal logic of the base $(\infty,1)$-topos and its [[adjoint functors]] with the [[(infinity,1)-sheaf (infinity,1)-topos|$(\infty,1)$-sheaf $(\infty,1)$-topos]]. 

Examples of such modal parametric type theories include the [[displayed type theory]] by [Kolomatskaia & Shulman 2023](#KS23) with external modal parametricity and the [[cohesive type theory]] by [Aberlé 2024](#Aberle24) with internal modal parametricity. 

## Related concepts

* [[parametric polymorphism]]

* [[dependent type theory]]

  * [[cubical type theory]]

  * [[simplicial type theory]]

  * [[modal type theory]]

  * [[cohesive type theory]]

  * [[observational type theory]]

  * [[higher observational type theory]]

  * [[displayed type theory]]

* [[bridge type]]

## References

* {#BJP10} [[Jean-Philippe Bernardy]], [[Patrik Jansson]], and [[Ross Paterson]]. 2010. *Parametricity and dependent types.* In Proceeding of the 15th ACM SIGPLAN international conference on Functional programming, ICFP 2010, Baltimore, Maryland, USA, September 27-29, 2010, Paul Hudak and Stephanie Weirich (Eds.). ACM, 345–356. &lbrack;[doi:10.1145/1863543.1863592](https://doi.org/10.1145/1863543.1863592)&rbrack;

* {#BM12} [[Jean-Philippe Bernardy]] and [[Guilhem Moulin]]. 2012. *A Computational Interpretation of Parametricity.* In Proceedings of the 27th Annual IEEE Symposium on Logic in Computer Science, LICS 2012, Dubrovnik, Croatia, June 25-28, 2012. IEEE Computer Society, 135–144. &lbrack;[doi:10.1109/LICS.2012.25](https://doi.org/10.1109/LICS.2012.25)&rbrack;

* {#AGJ14} [[Robert Atkey]], [[Neil Ghani]] and Patricia Johann, _A Relationally Parametric Model of Dependent Type Theory_, In Proceedings of the 41st ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (POPL 2014). 2014. ([web](http://bentnib.org/dtt-parametricity.html))

* {#BCM15} [[Jean-Philippe Bernardy]], [[Thierry Coquand]], and [[Guilhem Moulin]]. 2015. *A Presheaf Model of Parametric Type Theory.* In The 31st Conference on the Mathematical Foundations of Programming Semantics, MFPS 2015, Nijmegen, The Netherlands, June 22-25, 2015 (Electronic Notes in Theoretical Computer Science, Vol. 319), Dan R. Ghica (Ed.). Elsevier, 67–82. &lbrack;[doi:10.1016/j.entcs.2015.12.006](https://doi.org/10.1016/j.entcs.2015.12.006)&rbrack;

* {#BELS16} [[Auke Bart Booij]], [[Martín Hötzel Escardó]], [[Peter LeFanu Lumsdaine]], and [[Michael Shulman]]. 2016. *Parametricity, Automorphisms of the Universe, and Excluded Middle.* In 22nd International Conference on Types for Proofs and Programs, TYPES 2016, May 23-26, 2016, Novi Sad, Serbia (LIPIcs, Vol. 97), Silvia Ghilezan, Herman Geuvers, and Jelena Ivetic (Eds.). Schloss Dagstuhl - Leibniz-Zentrum für Informatik, 7:1–7:14. &lbrack;[doi:10.4230/LIPICS.TYPES.2016.7](https://doi.org/10.4230/LIPICS.TYPES.2016.7)&rbrack;

* {#Moulin16} [[Guilhem Moulin]]. *Internalizing parametricity.* PhD thesis, Chalmers University, 2016. &lbrack;[pdf](https://publications.lib.chalmers.se/records/fulltext/235758/235758.pdf)&rbrack;

* {#Cavallo21} [[Evan Cavallo]]. 2021. *Higher Inductive Types and Internal Parametricity for Cubical Type Theory.* Ph. D. Dissertation. Carnegie Mellon University, USA. &lbrack;[doi:10.1184/r1/14555691](https://doi.org/10.1184/r1/14555691)&rbrack;

* {#CH21} [[Evan Cavallo]] and [[Robert Harper]]. 2021. *Internal Parametricity for Cubical Type Theory.* Log. Methods Comput. Sci. 17, 4 (2021). &lbrack;<a href="https://doi.org/10.46298/lmcs-17(4:5)2021">doi:10.46298/lmcs-17(4:5)2021</a>, [arXiv:2005.11290](https://arxiv.org/abs/2005.11290)&rbrack;

* {#ACKS24} [[Thorsten Altenkirch]], [[Yorgo Chamoun]], [[Ambrus Kaposi]], [[Michael Shulman]], *Internal parametricity, without an interval*, Proceedings of the ACM on Programming Languages (POPL) **8** (2024) 2340-2369 &lbrack;[arXiv:2307.06448](https://arxiv.org/abs/2307.06448), [doi:10.1145/3632920](https://doi.org/10.1145/3632920)&rbrack;

* {#MND24} [[Antoine Van Muylder]], [[Andreas Nuyts]], and [[Dominique Devriese]]. 2024. *Internal and Observational Parametricity for Cubical Agda.* In Proceedings of the ACM on Programming LanguagesVolume 8Issue POPLArticle No.: 8pp 209–240. &lbrack;[doi:10.1145/3632850](https://dl.acm.org/doi/10.1145/3632850)&rbrack;

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#NaryaDocs} *Parametric Observational Type Theory*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/parametric-observational-type-theory.html)) 

A proof assistant implementing an observational [[parametric type theory]] with both internal and external parametricity of variable [[arity]]:

* [Narya](https://github.com/mikeshulman/narya)

[[!redirects parametric type theory]]
[[!redirects parametric type theories]]

[[!redirects parametric dependent type theory]]
[[!redirects parametric dependent type theories]]

[[!redirects non-parametric type theory]]
[[!redirects non-parametric type theories]]

[[!redirects non-parametric dependent type theory]]
[[!redirects non-parametric dependent type theories]]

[[!redirects modal parametricity]]

[[!redirects modal parametric type theory]]
[[!redirects modal parametric type theories]]

[[!redirects modal parametric dependent type theory]]
[[!redirects modal parametric dependent type theories]]

[[!redirects parametric modal type theory]]
[[!redirects parametric modal type theories]]

[[!redirects parametric modal dependent type theory]]
[[!redirects parametric modal dependent type theories]]

[[!redirects explicit parametricity]]

[[!redirects external parametricity]]
[[!redirects internal parametricity]]

[[!redirects modal external parametricity]]
[[!redirects external modal parametricity]]
[[!redirects modal internal parametricity]]
[[!redirects internal modal parametricity]]

[[!redirects explicit external parametricity]]
[[!redirects explicit internal parametricity]]

[[!redirects explicit modal parametricity]]

[[!redirects explicit modal external parametricity]]
[[!redirects explicit external modal parametricity]]
[[!redirects explicit modal internal parametricity]]
[[!redirects explicit internal modal parametricity]]

[[!redirects explicit parametric polymorphism]]
[[!redirects external parametric polymorphism]]
[[!redirects internal parametric polymorphism]]
[[!redirects modal parametric polymorphism]]
