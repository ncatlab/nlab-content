

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

A *topological quantum field theory* (TQFT) is a [[quantum field theory]] without dependence on the [[geometry]] (notably not on [[pseudo-Riemannian manifold|pseudo]] [[Riemannian geometry]] or fixed [[embedding of smooth manifolds|embeddings]]) of its [[spacetime]]/[[worldvolume]] [[domains]].

More precisely, in the ([[extended field theory|extended]]) [[FQFT|functorial description of QFTs]], where a [[quantum field theory]] is a ([[(infinity,n)-functor|higher]]) [[functor]] on a ([[(infinity,n)-category of cobordisms|higher]]) [[cobordism category]], a TQFT is such a functor on [[manifolds]] and [[cobordisms]] that carry no geometric structure (but possibly [[tangential structure]], such as [[orientation]] or [[spin structure]], or [[continuous maps]] to some [[classifying space]], cf. *[[HQFT]]*).

(In contrast, a [[conformal field theory]] depends on [[conformal structure]], a [[Euclidean field theory]] depends on [[Riemannian geometry|Riemannian structure]], a [[relativistic field theory]] depends on [[pseudo-Riemannian manifold|pseudo-Riemannian structure]], etc.).

In particular, topological quantum field theories are "[[general covariance|generally covariant]]" in a strong sense ([Witten 1988](#Witten88)), in that they coherently assign [[isomorphism|isomorphic]] ([[equivalence|equivalent]]) [[spaces of states]] to [[diffeomorphism|diffeomorphic]] [[domains]].

Historically, TQFTs first arose as [[theoretical physics|theoretical]] [[model (in theoretical physics)|models]] in the context of [[high energy physics]] and [[string theory]] ([Witten 1988](#Witten88)), prominent original examples being [[2D TQFTs]] of [[topological strings]] and [[3D TQFTs]] of [[Chern-Simons theory]], the latter remaining a pivotal example (also in guises such as the [[Reshetikhin-Turaev construction|Reshetikhin-Turaev]] and the [[Turaev-Viro model]]). 

With the mathematical [[axiom|axiomatization]] of TQFTs both established and tractable ([Atiyah 1989](#Atiyah89), following [Segal 1988](conformal+field+theory#Segal88)'s axiomatization of [[2D CFT]]) --- this in notorious contrast to the situation for general non-topological QFTs --- the topic saw dramatic developments in pure [[mathematics]], where TQFTs (with or without relation to actual [[physics]]) have come to serve as standard mathematical tools in fields of [[low-dimensional topology]] such as [[knot theory]], [[knot homology]], [[quantum topology]] and [[string topology]], also in [[geometric representation theory]], and as a field of study in [[higher category theory]] (cf. the *[[cobordism hypothesis]]*).

More recently, TQFTs find relevance in [[solid state physics]] as models for the behaviour of [[spectral gap|gapped]] [[ground states]] of [[topological order|topologically ordered]] [[quantum materials]]. The [experimental observation](quantum+Hall+effect#ObservationOfAnyonsInFQH) of [[anyon]] [braiding phases](quantum+Hall+effect#BraidingPhase) in [[fractional quantum Hall systems]] may be the first manifestation of TQFT in observational [[physics]] (in this case in the guise of [[abelian Chern-Simons theory]]), and the widely anticipated application of such [[anyon]] [[braiding]] to [[topological quantum computation]] could become the first technological application of TQFT.



## Examples
 {#Examples}

* [[2d TQFT]]

  * [[TCFT]]

  * [[2d Chern-Simons theory]]

* [[3d TQFT]]

  * [[Dijkgraaf-Witten theory]]

  * [[Chern-Simons theory]]

  * [[Reshetikhin-Turaev model]]

  * [[Turaev-Viro model]]

* [[4d TQFT]]

  * [[topological Yang-Mills theory]]

  * [[topologically twisted D=4 super Yang-Mills theory ]]

  * [[4d Chern-Simons theory]]

  * [[Yetter model]]  



## Related concepts

* [[cohomological field theory]], [[TCFT]]

* [[FQFT]], [[extended topological quantum field theory]]

* [[topological phase of matter]]

* [[topological quantum computation]]



## References
 {#References}


> See also the references at *[[2d TQFT]]*, *[[3d TQFT]]* and *[[4d TQFT]]*.

### Survey

* Danny Birmingham, [[Matthias Blau]], Mark Rakowski, [[George Thompson]], *Topological field theory*, Physics Reports **209** 4–5 (1991) 129-340 \[<a href="https://doi.org/10.1016/0370-1573(91)90117-5">doi:10.1016/0370-1573(91)90117-5</a>\]

* [[Romesh K. Kaul]]: *Topological Quantum Field Theories -- A Meeting Ground for Physicists and Mathematicians* &lbrack;[arXiv:hep-th/9907119](https://arxiv.org/abs/hep-th/9907119)&rbrack;

* [[Ralph Cohen]] (notes by [[Eric Malm]]): *MATH 283: Topological Field Theories* (2008) &lbrack;[pdf](https://ericmalm.net/ac/projects/math283-w08/math283-w08-n.pdf), [[RCohen-TQFT.pdf:file]], [web](https://ericmalm.net/ac/projects/math283-w08/)&rbrack;


Discussion of [[action functionals]] for [[topological field theories]] via [[equivariant ordinary differential cohomology]]:

* Joe Davighi, Ben Gripaios, [[Oscar Randal-Williams]], _Differential cohomology and topological actions in physics_ ([arXiv:2011.05768](https://arxiv.org/abs/2011.05768))

Discussion relating to [[differential cohomology]]:

* [[Gregory W. Moore]], [[Vivek Saxena]]: *TASI Lectures On Topological Field Theories And Differential Cohomology*, [TASI 2023](https://sites.google.com/colorado.edu/tasi-2023-wiki/home) lecture notes &lbrack;[arXiv:2510.07408](https://arxiv.org/abs/2510.07408)&rbrack;



### Origin in physics
 {#OriginInPhysics}

The concept originates in the guise of [[cohomological quantum field theory]] motivated from TQFTs appearing in [[string theory]] in

* {#Witten88} [[Edward Witten]]: *Topological quantum field theory*, Comm. Math. Phys. **117** 3 (1988) 353-386 &lbrack;[euclid:1104161738](http://projecteuclid.org/euclid.cmp/1104161738)&rbrack;

* {#Witten91} [[Edward Witten]], _Introduction to cohomological field theory_, International Journal of Modern Physics A, Vol. 6,No 6 (1991) 2775-2792 ([[WittenCQFT.pdf:file]])

* {#CordesMooreRamgoolam94} Stefan Cordes, [[Gregory Moore]], Sanjaye Ramgoolam, _Lectures on 2D Yang-Mills Theory, Equivariant Cohomology and Topological Field Theories_, Nucl. Phys. Proc. Suppl.41:184-244,1995 ([arXiv:hep-th/9411210](http://arxiv.org/abs/hep-th/9411210))

and in the discussion of [[Chern-Simons theory]] ("Schwarz-type TQFT") in

* [[Edward Witten]]: *Quantum Field Theory and the Jones Polynomial*, Commun. Math. Phys. **121** 3 (1989) 351-399.  &lbrack;[euclid:cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138), MR0990772&rbrack;




See also:

* [[Markus Banagl]], *Positive topological quantum field theories*, Quantum Topology **6** 4 (2015) 609-706 &lbrack;[arxiv/1303.4276](http://arxiv.org/abs/1303.4276), [doi:10.4171/qt/71](https://doi.org/10.4171/qt/71)&rbrack;
 

### Global (1-functorial) TQFT

The [[FQFT]]-[[axioms]] for global (i.e. [[functorial field theory|1-functorial]]) TQFTs are due to:

* {#Atiyah89} [[Michael Atiyah]], *Topological quantum field theories*, Publications Mathématiques de l’IHÉS **86** (1989) 175-186 &lbrack;[numdam:PMIHES_1988__68__175_0](http://www.numdam.org/item?id=PMIHES_1988__68__175_0)&rbrack;

Exposition of the conceptual ingredients:

* [[John Baez]], _Quantum Quandaries: a Category-Theoretic Perspective_ ([arXiv:quant-ph/0404040](http://arxiv.org/abs/quant-ph/0404040))

More technical lecture notes:

* [[Daniel Freed]], *Lectures on topological quantum field theory*, in: *Integrable Systems, Quantum Groups, and Quantum Field Theories*, NATO ASI Series **409** (1992) &lbrack;[doi:10.1007/978-94-011-1980-1_5](https://doi.org/10.1007/978-94-011-1980-1_5), [pdf](http://www.ma.utexas.edu/users/dafr/OldTQFTLectures.pdf), [[Freed-TQFTLectures.pdf:file]]&rbrack;

* {#Quinn95} [[Frank Quinn]], *Lectures on axiomatic topological quantum field theory*, in [[Dan Freed]], [[Karen Uhlenbeck]] (eds.) *Geometry and Quantum Field Theory* **1** (1995) &lbrack;[doi:10.1090/pcms/001](https://doi.org/10.1090/pcms/001)&rbrack;


* {#Walker06} [[Kevin Walker]], _TQFTs_, 2006 ([pdf](http://canyon23.net/math/tc.pdf))

* [[Mikhail Khovanov]] (notes by [[You Qi]]), §2 in: *Introduction to categorification*, lecture notes, Columbia University (2010, 2020) &lbrack;[web](https://www.math.columbia.edu/~khovanov/cat2020/), [web](https://you-qi2121.github.io/mypage/categorificationnotes.html), full:[pdf](https://www.dropbox.com/scl/fi/wdesax1c8il6tgwbi20t4/KhovanovYouQi-Categorification.pdf?rlkey=l5cm3khnzu604ijdnl06o89od&dl=0)&rbrack;
  > (with an eye towards [[link homology]])


An introduction specifically to [[2d TQFTs]] is in

* [[Joachim Kock]], _Frobenius algebras and 2D topological quantum field theories_, No. 59 of LMSST, Cambridge University Press, 2003., (full information [here](http://mat.uab.es/~kock/TQFT.html)).

See also the references at _[[HQFT]]_.

Relation to [[cutting and pasting of manifolds|cut-and-paste-ivariants]]:

* [[Carmen Rovi]], Matthew Schoenbauer, *Relating Cut and Paste Invariants and TQFTs*, The Quarterly Journal of Mathematics **73** 2 (2022) 579–607 &lbrack;[arXiv:1803.02939](https://arxiv.org/abs/1803.02939), [doi:10.1093/qmath/haab044](https://doi.org/10.1093/qmath/haab044)&rbrack;

See also:

* {#Torzewska22} [[Fiona Torzewska]], *Topological quantum field theories and homotopy cobordisms* &lbrack;[arXiv:2208.14504](https://arxiv.org/abs/2208.14504)&rbrack;

* [[Fiona Torzewska]], *Topological Quantum Field Theories and Homotopy Cobordisms*, [talk at](CQTS##TorzewskaDec2023) [[CQTS]] (Dec 2023) &lbrack;slides:[[Torzewska-TQFTandHomCob.pdf:file]], video:[YT](https://youtu.be/7rtJ61EPL-M)&rbrack;


### Local ($n$-functorial) TQFT

The local [[FQFT]] formulation (i.e. [[n-functor|n-functorial]]) together with the [[cobordism hypothesis]] was suggested in

*  [[John Baez]], [[James Dolan]], _Higher dimensional algebra and Topological Quantum Field Theory_ J.Math.Phys. 36 (1995) 6073-6105 ([arXiv:q-alg/9503002](http://arxiv.org/abs/q-alg/9503002))

and formalized and proven in

* [[Jacob Lurie]], [[On the Classification of Topological Field Theories]]; _TQFT and the Cobordism Hypothesis_ ([video](http://www.ma.utexas.edu/video/dafr/lurie/), [notes](http://www.ma.utexas.edu/users/plowrey/dev/rtg/notes/perspectives_TQFT_notes.html))

This also shows how [[TCFT]] fits in, which formalizes the original proposal of 2d [[cohomological quantum field theory]].


Lecture notes:

* {#Teleman14} [[Constantin Teleman]], *Five lectures on topological field theory*, in *Geometry and Quantization of Moduli Spaces*, CRM Advanced Courses in Mathematics, Birkhäuser (2016) &lbrack;[doi:10.1007/978-3-319-33578-0_3](https://doi.org/10.1007/978-3-319-33578-0_3), [pdf](http://math.berkeley.edu/~teleman/math/barclect.pdf), [[Teleman-LecturesOnTFT.pdf:file]]&rbrack;

A discussion amplifying the aspects of [[higher category theory]] is in

* [[Anton Kapustin]], _Topological field theory, higher categories, and their applications_, survey for ICM 2010, ([arxiv/1004.2307](http://arxiv.org/abs/1004.2307))

See also

* Mark Feshbach, [[Alexander Voronov]], _A higher category of cobordisms and topological quantum field theory_ &lbrack;[arxiv/1108.3349](http://arxiv.org/abs/1108.3349)&rbrack; 

Indication of local [[quantization]] in the context of [[infinity-Dijkgraaf-Witten theory]] is in

* [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_



[[!redirects topological quantum field theories]]
[[!redirects TQFT]]
[[!redirects TQFTs]]
[[!redirects TFT]]
[[!redirects TFTs]]

[[!redirects topological field theory]]
[[!redirects topological field theories]]