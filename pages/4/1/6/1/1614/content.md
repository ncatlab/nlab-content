

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


#Contents#
* table of contents
{:toc}

## Idea

A **topological quantum field theory** is a [[quantum field theory]] which 
-- as a [[FQFT|functorial quantum field theory]] -- is a functor on a flavor of the  [[(∞,n)-category of cobordisms]] $Bord_n^S$, where the [[n-morphism]]s are [[cobordism]]s without any non-topological further structure $S$ -- for instance no [[Riemannian metric]] structure -- but possibly some "topological structure", such as  [[Spin structure]] or similar.

For more on the general idea and its development, see [[FQFT]] and [[extended topological quantum field theory]]. 


+-- {: .num_remark }
###### Remark

Often topological _quantum_ field theories are just called _topological field theories_ and accordingly the abbreviation TQFT is reduced to TFT. Strictly speaking this is a misnomer, which is however convenient and very common. It should be noted, however, that TQFTs may have classical counterparts which would better deserve to be called TFTs. But they are not usually.

=--

## Non-topological QFTs

In contrast to topological QFTs, non-topological quantum field theories in the [[FQFT]] description are $n$-functors on $n$-categories $Bord^S_n$ whose morphisms are manifolds with extra $S$-structure, for instance

* $S =$ conformal structure $\to$ [[conformal field theory]]

* $S =$ [[Riemannian manifold|Riemannian structure]] $\to$ "euclidean QFT"

* $S =$ [[pseudo-Riemannian metric|pseudo-Riemannian structure]] $\to$ "relativistic QFT"

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

## Homotopy QFTs

These somehow lie between the previous two types. There is some simple extra structure in the form of a 'characteristic map' from the manifolds and bordisms to a 'background space' $X$. 
In many of the simplest examples, this is taken to be the [[classifying space]] of a group, but this is not the only case that can be considered.  The topic is explored more fully in [[HQFT]]. 

## Related concepts

* [[cohomological field theory]], [[TCFT]]

* [[FQFT]], [[extended topological quantum field theory]]

* [[topological phase of matter]]

* [[topological quantum computation]]



## References
 {#References}


> See also the references at *[[2d TQFT]]*, *[[3d TQFT]]* and *[[4d TQFT]]*.

Survey:

* [[Ralph Cohen]] (notes by Eric Malm), p 20 of: *MATH 283: Topological Field Theories* (2008) &lbrack;[pdf](https://ericmalm.net/ac/projects/math283-w08/math283-w08-n.pdf), [[RCohen-TQFT.pdf:file]]&rbrack;


Discussion of [[action functionals]] for [[topological field theories]] via [[equivariant ordinary differential cohomology]]:

* Joe Davighi, Ben Gripaios, [[Oscar Randal-Williams]], _Differential cohomology and topological actions in physics_ ([arXiv:2011.05768](https://arxiv.org/abs/2011.05768))


### Origin in physics
 {#OriginInPhysics}

The concept originates in the guise of [[cohomological quantum field theory]] motivated from TQFTs appearing in [[string theory]] in

* {#Witten88} [[Edward Witten]], _Topological quantum field theory_, Comm. Math. Phys. Volume 117, Number 3 (1988), 353-386. ([euclid:1104161738](http://projecteuclid.org/euclid.cmp/1104161738))

* {#Witten91} [[Edward Witten]], _Introduction to cohomological field theory_, International Journal of Modern Physics A, Vol. 6,No 6 (1991) 2775-2792 ([[WittenCQFT.pdf:file]])

* {#CordesMooreRamgoolam94} Stefan Cordes, [[Gregory Moore]], Sanjaye Ramgoolam, _Lectures on 2D Yang-Mills Theory, Equivariant Cohomology and Topological Field Theories_, Nucl. Phys. Proc. Suppl.41:184-244,1995 ([arXiv:hep-th/9411210](http://arxiv.org/abs/hep-th/9411210))

and in the discussion of [[Chern-Simons theory]] ("Schwarz-type TQFT") in

* [[Edward Witten]], _Quantum Field Theory and the Jones Polynomial_, Commun. Math. Phys. **121(( (3) (1989) 351-399.  &lbrack;[euclid:cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138), MR0990772&rbrack;

Review:

* Danny Birmingham, [[Matthias Blau]], Mark Rakowski, [[George Thompson]], *Topological field theory*, Physics Reports **209** 4–5 (1991) 129-340 \[<a href="https://doi.org/10.1016/0370-1573(91)90117-5">doi:10.1016/0370-1573(91)90117-5</a>\]

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