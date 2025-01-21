
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

It is a member of the family of Khovanov-Rozansky link homology theories which categorify the [[HOMFLY-PT polynomial]] and some of its one-variable specializations. 

## Interpretation in QFT

Khovanov homology has long been expected to appear as the [[quantum observables]] in [[D=4 TQFT]] in higher analogy of how the [[Jones polynomial]] arises as a [[quantum observable]] in 3-dimensional [[Chern-Simons theory|Chern-Simons]] [[D=3 TQFT]]. For instance for $\Sigma \colon K \to K'$ a [[knot cobordism]] between two [[knots]] there is a natural morphism

$$
  \Phi_\Sigma \colon \mathcal{K}(K) \to \mathcal{K}(K')
$$

between the Khovanov homologies associated to the two knots.


[Witten 2011](#Witten11) argued, following indications in [Gukov, Schwarz & Vafa 2005](#GukovSchwarzVafa04), that this [[4d TQFT]] is related to the worldvolume theory of the image in [[type IIB string theory]] of [[D3-branes]] [[brane intersection|ending]] on [[NS5-branes]] in a [[type II supergravity]] [[background field|background]] of the form $\mathbb{R}^9 \times S^1$ with the circle transverse to both kinds of branes, under one [[S-duality]] and one [[T-duality]] operation

$$
  (D3-NS5) 
    \stackrel{S}{\mapsto}
  (D3-D5)
    \stackrel{T}{\mapsto}
  (D4-D6)
  \,.
$$

To go from the [[Jones polynomial]] to [[Khovanov homology]], one interprets the circle as Euclidean time. The [[path integral]] with the circle is the [[partition function]] (Witten index), $Tr_{\mathcal{H}}(-1)^F e^{-\beta H}$, of a 5D theory. Khovanov homology is $\mathcal{H}$ itself, rather than the index. 

(See [Witten 2011, p. 14](http://arxiv.org/PS_cache/arxiv/pdf/1101/1101.3216v1.pdf#page=14)).

Earlier indication for this had come from the observation [Witten92](#Witten92) that Chern-Simons theory is the effective background theory for the [[A-model]] 2d [[TCFT]] (see <a href="http://ncatlab.org/nlab/show/TCFT#ActionFunctionals">TCFT -- Worldsheet and effective background theories</a> for details).


## Related concepts

* [[link cobordism]]

* [[categorification in representation theory]]



## References

### General

Exposition:

* {#Lobb24} Andrew Lobb: *A feeling for Khovanov homology*, Notices of the AMS **71** 5 (2024) &lbrack;[doi:10.1090/noti2928](https://doi.org/10.1090/noti2928), [pdf](https://www.ams.org/notices/202405/rnoti-p621.pdf), [pdf](https://www.maths.dur.ac.uk/users/andrew.lobb/notices.pdf), full issue:[pdf](https://www.ams.org/notices/202405/202405FullIssue.pdf)&rbrack;

Original articles:

* [[Louis Crane]], [[Igor Frenkel]], _Four-dimensional topological quantum field theory, Hopf categories, and the canonical bases_, J. Math. Phys. __35__ (1994) 5136-5154, [hep-th/9405183](http://arxiv.org/abs/hep-th/9405183)

* [[Igor Frenkel]], [[Mikhail Khovanov]], _Canonical bases in tensor products and graphical calculus for $U_q(\mathfrak{sl}_2)$_, Duke Math. J. __87__ (1997) 409-480, [MR99a:17019](http://www.ams.org/mathscinet-getitem?mr=1446615), [doi](http://dx.doi.org/10.1215/S0012-7094-97-08715-9)

* [[Joseph Bernstein]], [[Igor Frenkel]], [[Mikhail Khovanov]], _A categorification of the Temperley-Lieb algebra and Schur quotients of $U(\mathfrak{sl}-2)$ by projective and Zuckerman functors, Selecta. Math. __5__ (1999) 199-241, [MR2000i:17009](http://www.ams.org/mathscinet-getitem?mr=1714141), [doi](http://dx.doi.org/10.1007/s000290050047)

* [[Igor Frenkel]], [[Mikhail Khovanov]], [[Catharina Stroppel]], _A categorification of finite-dimensional irreducible representations of quantum $\mathfrak{sl}_2$ and their tensor products_, Selecta Math. (N.S.) __12__ (2006), no. 3-4, 379&#8211;431, [MR2008a:17014](http://www.ams.org/mathscinet-getitem?mr=2305608), [doi](http://dx.doi.org/10.1007/s00029-007-0031-y)

* [[Mikhail Khovanov]], *A categorification of the Jones polynomial*, Duke Math. J. __101__ (2000) 359-426 &lbrack;[arXiv:math/9908171](https://arxiv.org/abs/math/9908171), [doi:10.1215/S0012-7094-00-10131-7](https://projecteuclid.org/journals/duke-mathematical-journal/volume-101/issue-3/A-categorification-of-the-Jones-polynomial/10.1215/S0012-7094-00-10131-7.full), MR1740682 (2002j:57025)&rbrack;

* [[Mikhail Khovanov]], _A functor-valued invariant of tangles_, Algebr. Geom. Topol. __2__ (2002) 665-741 MR1928174 (2004d:57016)

* [[Mikhail Khovanov]], _Patterns in knot cohomology. I_, Experiment. Math. __12__ (2003) 365&#8211;374 

* {#Jacobsson04} Magnus Jacobsson: *An invariant of link cobordisms from Khovanov homology*, Algebr. Geom. Topol. **4** (2004) 1211-1251 &lbrack;[arXiv:math/0206303](https://arxiv.org/abs/math/0206303), [doi:10.2140/agt.2004.4.1211](https://doi.org/10.2140/agt.2004.4.1211)&rbrack;


* [[Mikhail Khovanov]], An invariant of tangle cobordisms, Trans. Amer. Math. Soc. __358__ (2006), no. 1, 315&#8211;327, arXiv:math.QA/0207264, [MR2006g:57046](http://www.ams.org/mathscinet/search/publdoc.html?pg1=MR&s1=2171235&loc=fromreflist), [doi](http://dx.doi.org/10.1090/S0002-9947-05-03665-2)


* Rapha&#235;l Rouquier, _Khovanov-Rozansky homology and 2-braid groups_, [arxiv/1203.5065](http://arxiv.org/abs/1203.5065)
 
* [[Carlo Collari]],  _The Functoriality of Khovanov Homology and the Monodromy of Knots_ (2013) &lbrack;[pdf](https://core.ac.uk/download/pdf/19204099.pdf), [[CollariKhovanovHomology.pdf:file]]&rbrack;


Review and lecture notes:

* {#Bar-Natan} [[Dror Bar-Natan]], _On Khovanov's categorification of the Jones polynomial_, Alg. Geom. Topology __2__ (2002) 337-370 &lbrack;[arXiv:math.GT/0201043](http://arxiv.org/abs/math/0201043)&rbrack;


* [[Mikhail Khovanov]] (notes by [[You Qi]]), *Introduction to categorification*, lecture notes, Columbia University (2010, 2020) &lbrack;[web](https://www.math.columbia.edu/~khovanov/cat2020/), [web](https://you-qi2121.github.io/mypage/categorificationnotes.html), full:[pdf](https://www.dropbox.com/scl/fi/wdesax1c8il6tgwbi20t4/KhovanovYouQi-Categorification.pdf?rlkey=l5cm3khnzu604ijdnl06o89od&dl=0)&rbrack;


* Paul Turner, _Five Lectures on Khovanov Homology_, &lbrack;[math.GT/0606464](http://arxiv.org/abs/math/0606464)&rbrack;

* [[Mikhail Khovanov]], Robert Lipshitz, _Categorical lifting of the Jones polynomial: a survey_, Bulletin (New Series) of the American Mathematical Society (2022) &lbrack;[doi:10.1090/bull/1772](https://doi.org/10.1090/bull/1772)&rbrack;


* [[Dror Bar-Natan]], _Khovanov's homology for tangles and cobordisms_,  Geom. Topol. __9__ (2005), 1443&#8211;1499, [MR2006g:57017](http://www.ams.org/mathscinet-getitem?mr=2174270)

See also

* David Clark, [[Scott Morrison]], [[Kevin Walker]], _Fixing the functoriality of Khovanov homology_ ([arXiv:math/0701339](http://arxiv.org/abs/math/0701339) [pdf slides](http://canyon23.net/math/talks/Kh%20200704.pdf))

Discussion via a [[cobordism category]] of "foams":

* {#Khovanov04} [[Mikhail Khovanov]], *$sl(3)$ link homology*, Algebr. Geom. Topol. **4** (2004) 1045-1081 &lbrack;[arXiv:math/0304375](https://arxiv.org/abs/math/0304375), [doi:10.2140/agt.2004.4.1045](https://doi.org/10.2140/agt.2004.4.1045)&rbrack;

* [[Marco Mackaay]], [[Pedro Vaz]], *The universal $sl_3$-link homology*, Algebr. Geom. Topol. **7** (2007) 1135-1169 &lbrack;[doi:10.2140/agt.2007.7.1135](https://doi.org/10.2140/agt.2007.7.1135)&rbrack;

* [[Marco Mackaay]], [[Pedro Vaz]], *The foam and the matrix factorization $sl_3$ link homologies are equivalent*, Algebr. Geom. Topol. **8** (2008) 309-342 &lbrack;[arXiv:0710.0771](https://arxiv.org/abs/0710.0771), [doi:10.2140/agt.2008.8.309](https://doi.org/10.2140/agt.2008.8.309)&rbrack;

* [[Marco Mackaay]], [[Pedro Vaz]], *The diagrammatic Soergel category and $sl(N)$-foams, for $N \gt 3$ &lbrack;[arXiv:0911.2485](https://arxiv.org/abs/0911.2485)&rbrack;


* [[Mikhail Khovanov]], [[Louis-Hadrien Robert]], *Foam evaluation and Kronheimer--Mrowka theories*, Advances in Mathematics **376**  (2021) 107433 &lbrack;[arXiv:1808.09662](https://arxiv.org/abs/1808.09662), [doi:10.1016/j.aim.2020.107433](https://doi.org/10.1016/j.aim.2020.107433)&rbrack;

* [[Mikhail Khovanov]], [[Louis-Hadrien Robert]], *Conical $SL(3)$ foams*, Journal of Combinatorial Algebra **6** 1/2 (2022) 79-108 &lbrack;[arXiv:2011.11077](https://arxiv.org/abs/2011.11077), [doi:10.4171/jca/61](https://doi.org/10.4171/jca/61)&rbrack;

Reviewed in:

* [[Mikhail Khovanov]], *Universal construction, foams and link homology*, lecture series at *[QFT and Cobordism](https://nyuad.nyu.edu/en/events/2023/march/quantum-field-theories-and-cobordisms.html)*, [[CQTS]] (Mar 2023) &lbrack;[web](Center+for+Quantum+and+Topological+Systems#KhovanovMar2023), video 1:[YT](https://www.youtube.com/watch?v=Urh1NNcbCcc), 2:[YT](https://www.youtube.com/watch?v=SPBcAAmGT88)&rbrack;


A proposal to incorporate the geometry of knots to Khovanov homology is in

* Li Shen, Jian Liu, Guo-Wei Wei. *Evolutionary Khovanov homology* (2024). ([arXiv:2406.02821](https://arxiv.org/abs/2406.02821)).

See also:

* Khaled Qazaqzeh, [[Nafaa Chbili]], *On Khovanov Homology of Quasi-Alternating Links*,  Mediterr. J. Math. **19** 104 (2022) &lbrack;[arXiv:2009.08624](https://arxiv.org/abs/2009.08624), [doi:10.1007/s00009-022-02006-5](https://doi.org/10.1007/s00009-022-02006-5)&rbrack;

* [[Nafaa Chbili]], *Quasi-alternating links, Examples and obstructions*, talk at *[QFT and Cobordism](https://nyuad.nyu.edu/en/events/2023/march/quantum-field-theories-and-cobordisms.html)*, [[CQTS]] (Mar 2023) &lbrack;[web](Center+for+Quantum+and+Topological+Systems#ChbiliMar2023)&rbrack;



[[!include knot invariants via topological strings and 5-branes -- references]]


Related $n$Caf&eacute; discussions: [categorification in Glasgow](http://golem.ph.utexas.edu/category/2008/11/categorification_in_glasgow.html), [Kamnitzer on categorifying tangles](http://golem.ph.utexas.edu/category/2009/04/kamnitzer_on_categorifying_tan.html), [link homology in Paris](http://golem.ph.utexas.edu/category/2009/02/link_homology_in_paris.html), [4d QFT and Khovanov homology](http://golem.ph.utexas.edu/category/2011/02/4d_qft_for_khovanov_homology.html)

Parts of the above remarks on the QFT interpretation makes use of comments provided  by [[Jacques Distler]] in <a href="http://golem.ph.utexas.edu/category/2011/02/4d_qft_for_khovanov_homology.html#comments">this blog discussion</a>.

More on relation to [[topological quantum field theory]]:

* [[Nitu Kitchloo]], *Symmetry Breaking and Link Homologies I* &lbrack;[arXiv:1910.07443](https://arxiv.org/abs/1910.07443)&rbrack;

* [[Nitu Kitchloo]], *Symmetry Breaking and Link Homologies II* &lbrack;[arXiv:1910.07444](https://arxiv.org/abs/1910.07444)&rbrack;

* [[Nitu Kitchloo]], *Symmetry Breaking and Link Homologies III* &lbrack;[arXiv:1910.07516](https://arxiv.org/abs/1910.07516)&rbrack;

* [[Catharina Stroppel]], *Categorification: tangle invariants and TQFTs* &lbrack;[arXiv:2207.05139](https://arxiv.org/abs/2207.05139)&rbrack;

Relation to [[gauge theory]]:

* [[Nitu Kitchloo]], *Symmetry breaking and homotopy types for link homologies*, talk at *[QFT and Cobordism](https://nyuad.nyu.edu/en/events/2023/march/quantum-field-theories-and-cobordisms.html)*, [[CQTS]] (Mar 2023) &lbrack;[web](Center+for+Quantum+and+Topological+Systems#KitchlooMar2023), video:[YT](https://www.youtube.com/watch?v=StRyIjpER9I)&rbrack;




[[!redirects Khovanov homologies]]

[[!redirects knot homology]]
[[!redirects knot homologoes]]

[[!redirects link homology]]
[[!redirects link homologies]]

[[!redirects Khovanov-Rozansky link homology]]
[[!redirects Khovanov-Rozansky homology]]



