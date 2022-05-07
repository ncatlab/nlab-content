
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Khovanov homology_ is a [[knot invariant]] that is a [[categorification]] of the [[Jones polynomial]]. 

## Interpretation in QFT

Khovanov homology has long been expected to appear as the [[observable]]s in a 4-dimensional [[TQFT]] in higher analogy of how the [[Jones polynomial]] arises as a observables in 3-dimensional [[Chern-Simons theory]]. For instance for $\Sigma : K \to K'$ a [[cobordism]] between two [[knot]]s there is a natural morphism

$$
  \Phi_\Sigma : \mathcal{K}(K) \to \mathcal{K}(K')
$$

between the Khovanov homologies associated to the two knots.


In ([Witten11](#Witten11)) it is argued, following indications in ([Gukov-Schwarz-Vafa 05](#GukovSchwarzVafa04)) that this 4d TQFT is related to the worldvolume theory of the image in [[string theory|type IIA string theory]] of D3-[[brane]]s ending on NS5-[[brane]]s in a type IIB background of the form $\mathbb{R}^9 \times S^1$ with the circle transverse to both kinds of branes, under one [[S-duality]] and one [[T-duality]] operation

$$
  (D3-NS5) 
    \stackrel{S}{\mapsto}
  (D3-D5)
    \stackrel{T}{\mapsto}
  (D4-D6)
  \,.
$$

To go from the [[Jones polynomial]] to [[Khovanov homology]], we interpret the circle as Euclidean time. The [[path integral]] with the circle is the [[partition function]] (Witten index), $Tr_{\mathcal{H}}(-1)^F e^{-\beta H}$, of a 5D theory. Khovanov homology is $\mathcal{H}$ itself, rather than the index. 

See ([Witten11, p. 14](http://arxiv.org/PS_cache/arxiv/pdf/1101/1101.3216v1.pdf#page=14)).

Earlier indication for this had come from the observation [Witten92](#Witten92) that Chern-Simons theory is the effective background theory for the [[A-model]] 2d [[TCFT]] (see <a href="http://ncatlab.org/nlab/show/TCFT#ActionFunctionals">TCFT -- Worldsheet and effective background theories</a> for details).


## Related concepts

* [[categorification in representation theory]]

[[!include table of branes]]

## References

Original sources include

* [[Louis Crane]], [[Igor Frenkel]], _Four-dimensional topological quantum field theory, Hopf categories, and the canonical bases_, J. Math. Phys. __35__ (1994) 5136-5154, [hep-th/9405183](http://arxiv.org/abs/hep-th/9405183)

* [[Igor Frenkel]], [[Mikhail Khovanov]], _Canonical bases in tensor products and graphical calculus for $U_q(\mathfrak{sl}_2)$_, Duke Math. J. __87__ (1997) 409-480, [MR99a:17019](http://www.ams.org/mathscinet-getitem?mr=1446615), [doi](http://dx.doi.org/10.1215/S0012-7094-97-08715-9)

* [[Joseph Bernstein]], [[Igor Frenkel]], [[Mikhail Khovanov]], _A categorification of the Temperley-Lieb algebra and Schur quotients of $U(\mathfrak{sl}-2)$ by projective and Zuckerman functors, Selecta. Math. __5__ (1999) 199-241, [MR2000i:17009](http://www.ams.org/mathscinet-getitem?mr=1714141), [doi](http://dx.doi.org/10.1007/s000290050047)

* [[Igor Frenkel]], [[Mikhail Khovanov]], [[Catharina Stroppel]], _A categorification of finite-dimensional irreducible representations of quantum $\mathfrak{sl}_2$ and their tensor products_, Selecta Math. (N.S.) __12__ (2006), no. 3-4, 379&#8211;431, [MR2008a:17014](http://www.ams.org/mathscinet-getitem?mr=2305608), [doi](http://dx.doi.org/10.1007/s00029-007-0031-y)

* M Khovanov, _A categorification of the Jones polynomial_, Duke Math. J. __101__ (2000) 359&#8211;426 MR1740682 (2002j:57025)
* M Khovanov, _A functor-valued invariant of tangles_, Algebr. Geom. Topol. __2__ (2002) 665&#8211;741 MR1928174 (2004d:57016)

* M Khovanov, _Patterns in knot cohomology. I_, Experiment. Math. __12__ (2003) 365&#8211;374 
* M Khovanov, An invariant of tangle cobordisms, Trans. Amer. Math. Soc. __358__ (2006), no. 1, 315&#8211;327, arXiv:math.QA/0207264, [MR2006g:57046](http://www.ams.org/mathscinet/search/publdoc.html?pg1=MR&s1=2171235&loc=fromreflist), [doi](http://dx.doi.org/10.1090/S0002-9947-05-03665-2)
* Rapha&#235;l Rouquier, _Khovanov-Rozansky homology and 2-braid groups_, [arxiv/1203.5065](http://arxiv.org/abs/1203.5065)
 
* [[Carlo Collari]],  _The Functoriality of Khovanov Homology and the Monodromy of Knots_, 2013 ([pdf](https://core.ac.uk/download/pdf/19204099.pdf), [[CollariKhovanovHomology.pdf:file]])



An expository reviews are

* [[Dror Bar-Natan]], _On Khovanov's categorification of the Jones polynomial_, Alg. Geom. Topology __2__ (2002) 337-370, [arXiv:math.GT/0201043](http://arxiv.org/abs/math/0201043)
{#Bar-Natan}
* Paul Turner, _Five Lectures on Khovanov Homology_, [math.GT/0606464](http://arxiv.org/abs/math/0606464)

A proposal for a 4-dimensional [[quantum field theory]] whose [[observable]]s are given by Khovanov homology is discussed in

* {#Witten11} [[Edward Witten]], _Fivebranes and Knots_, Quantum Topology, Volume 3, Issue 1, 2012, pp. 1-137 ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216), [doi:10.4171/QT/26](https://www.ems-ph.org/journals/show_abstract.php?issn=1663-487X&vol=3&iss=1&rank=1))


based on

* [[Sergei Gukov]], [[Albert Schwarz]], [[Cumrun Vafa]], _Khovanov-Rozansky homology and topologicals strings_ , Lett. Math. Phys. __74__ (2005) 53-74, [arXiv:hep-th/0412243](http://arxiv.org/abs/hep-th/0412243), [MR2007a:57014](http://www.ams.org/mathscinet-getitem?mr=2193547), [doi](http://www.ams.org/leavingmsn?url=http://dx.doi.org/10.1007/s11005-005-0008-8) 
{#GukovSchwarzVafa04}

and earlier hints in

* [[Edward Witten]], _Chern-Simons gauge theory as a string theory_, The Floer memorial volume, 637&#8211;678, Progr. Math. __133__, Birkh&#228;user 1995, [arXiv/hep-th/9207094](http://arxiv.org/abs/hep-th/9207094), [MR97j:57052](http://www.ams.org/mathscinet-getitem?mr=1362846)
{#Wittem92}

Lecture notes on this and its relation to the [[Jones polynomial]] are in

* [[Edward Witten]], _A New Look At The Jones Polynomial of a Knot_, Clay Conference, Oxford, October 1, 2013 ([[WittenOnJonesPolynomial2013.pdf:file]])

* [[Edward Witten]], _Khovanov Homology And Gauge Theory_, Clay Conference, Oxford, October 1, 2013 ([[WittenOnKhovanovHomology2013.pdf:file]])


See also 

* [[Edward Witten]], _Khovanov homology and gauge theory_, [arxiv/1108.3103](http://arxiv.org/abs/1108.3103)

* [[Edward Witten]], _Fivebranes and Knots_ ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216)) 
 {#Witten11}

Related $n$Caf&eacute; discussions: [categorification in Glasgow](http://golem.ph.utexas.edu/category/2008/11/categorification_in_glasgow.html), [Kamnitzer on categorifying tangles](http://golem.ph.utexas.edu/category/2009/04/kamnitzer_on_categorifying_tan.html), [link homology in Paris](http://golem.ph.utexas.edu/category/2009/02/link_homology_in_paris.html), [4d QFT and Khovanov homology](http://golem.ph.utexas.edu/category/2011/02/4d_qft_for_khovanov_homology.html)

Parts of the above remarks on the QFT interpretation makes use of comments provided  by [[Jacques Distler]] in <a href="http://golem.ph.utexas.edu/category/2011/02/4d_qft_for_khovanov_homology.html#comments">this blog discussion</a>.

* [[Dror Bar-Natan]], _Khovanov's homology for tangles and cobordisms_, 
Geom. Topol. __9__ (2005), 1443&#8211;1499, [MR2006g:57017](http://www.ams.org/mathscinet-getitem?mr=2174270)

See also

* David Clark, [[Scott Morrison]], [[Kevin Walker]], _Fixing the functoriality of Khovanov homology_ ([arXiv:math/0701339](http://arxiv.org/abs/math/0701339) [pdf slides](http://canyon23.net/math/talks/Kh%20200704.pdf))