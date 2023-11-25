
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The operations on an [[H-space]] (such as a [[loop space]]) $X$ equip its [[homology]] with the [[mathematical structure|structure]] of  [[ring]]. At least for [[ordinary homology]] this is known as the _[[Pontrjagin ring]]_ $H_*(X)$ of $X$.

## Properties

### Relation to Whitehead product
 {#RelationToWhiteheadProduct}

Under the [[Hurewicz homomorphism]], the [[commutator]] of the Pontrjagin product on homology is the [[Whitehead product]] on [[homotopy groups]] of a [[based loop space]]. 

This is due to [Samelson (1953)](#Samelson53) and for higher Whitehead brackets due to [Arkowitz (1971)](#Arkowitz71). 

In fact, in [[characteristic zero]] the [[Pontrjagin ring]] structure on $\Omega X$ is identified by the [[Hurewicz homomorphism]] with the [[universal enveloping algebra]] (see [there](universal+enveloping+algebra#ForSuperLieAlgebras)) of the [[Whitehead bracket super Lie algebra]] of $X$ &lbrack;[Milnor & Moore (1965) Appendix](#MilnorMoore65); [Whitehead (1978) Thm. X.7.10](#Whitehead78); [Félix, Halperin & Thomas 2000, Thm. 16.13](#FélixHalperinThomas00)&rbrack;. Moreover, in this case the [[underlying]] [[ordinary cohomology]] ([[universal coefficient theorem|hence]] the [[ordinary homology]]) [[vector space]] may be read of from any [[Sullivan model]] of $X$ (by the proposition [here](Sullivan+model+of+loop+space#SullivanModelForBasedLoopSpace))



### Homological group completion

The homological version of 
the _[[group completion theorem]]_ relates the [[Pontrjagin ring]] of a [[topological monoid]] $A$ to that of its [[group completion]] $\Omega B A$.

### Relation to quantum cohomology
 {#RelationToQuantumCohomology}

The homology Pontrjagin product of certain [[compact Lie groups]] is identified with the [[quantum cohomology]] of corresponding [[flag varieties]] (see references [below](#ReferencesOnQuantumCohomologyAsPontrjaginRings)).


## Related concepts

* [[homology of loop spaces]]



## References

### General

The concept and the terminology "Pontryagin-multiplication" is due to

* [[Raoul Bott]], [[Hans Samelson]], *On the Pontryagin product in spaces of paths*, Commentarii Mathematici Helvetici **27** (1953) 320–337 &lbrack;[doi:10.1007/BF02564566](https://doi.org/10.1007/BF02564566)&rbrack;

who name it in honor of the analogous product operation on the homology of [[compact Lie groups]] due to:

* [[Lev Pontrjagin]], *Homologies in compact Lie groups*, Rec. Math. [Mat. Sbornik] N.S. **6**(**48**) 3 (1939) 389–422 &lbrack;[mathnet:5835](http://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=5835&option_lang=eng)&rbrack;

see also:

* [[Hans Samelson]], §3 in: *Beitr&auml;ge Zur Topologie der Gruppen-Mannigfaltigkeiten*, Annals of Mathematics, Second Series, **42** 5 (1941) 1091-1137 &lbrack;[jsotr:1970463](https://www.jstor.org/stable/1970463)&rbrack;

Proof that the [[commutator]] of the Pontrjagin product is the [[Whitehead product]], under the [[Hurewicz homomorphism]]:

* {#Samelson53} [[Hans Samelson]], *A Connection Between the Whitehead and the Pontryagin Product*, American Journal of Mathematics **75** 4 (1953) 744–752  &lbrack;[doi:10.2307/2372549](https://doi.org/10.2307/2372549)&rbrack;

and in [[characteristic zero]]:

* {#MilnorMoore65} [[John Milnor]], [[John Moore]], Appendix (pp. 262) of: _On the structure of Hopf algebras_, Annals of Math. __81__ (1965) 211-264 &lbrack;[doi:10.2307/1970615](https://doi.org/10.2307/1970615), [pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/milnor-moore-ann-math-1965.pdf)&rbrack;

* {#FélixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Thm. 16.13 in: _Rational Homotopy Theory_, Graduate Texts in Mathematics **205** Springer (2000) &lbrack;[doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9)&rbrack;

and for higher Whitehead brackets:

* {#Arkowitz71} [[Martin Arkowitz]], *Whitehead Products as Images of Pontrjagin Products*, Transactions of the American Mathematical Society, **158** 2 (1971) 453-463 &lbrack;[doi:10.2307/1995917](https://doi.org/10.2307/1995917)&rbrack;

Refinement to algebra structure on the [[singular chain complex]] (Adams-Hilton model):

* [[John F. Adams]], [[Peter J. Hilton]], *On the chain algebra of a loop space*, Commentarii Mathematici Helvetici **30** (1956) 305–330 &lbrack;[doi:10.1007/BF02564350](https://doi.org/10.1007/BF02564350)&rbrack;

reviewed and further developed in:

* [[Kathryn Hess]], [[Paul-Eugène Parent]], [[Jonathan Scott]], [[Andrew Tonks]], *A canonical enriched Adams-Hilton model for simplicial sets*, Advances in Mathematics **207** 2 (2006) 847-875 &lbrack;[doi:10.1016/j.aim.2006.01.013](https://doi.org/10.1016/j.aim.2006.01.013), [arXiv:math/0408216](https://arxiv.org/abs/math/0408216)&rbrack;

More on the Pontrjagin rings of the [[classical Lie groups]]:

* [[Ichiro Yokota]], *On the homology of classical Lie groups*, J. Inst. Polytech. Osaka City Univ. Ser. A **8** 2 (1957) 93-120 &lbrack;[euclid:ojm/1353054814](https://projecteuclid.org/journals/osaka-journal-of-mathematics/volume-8/issue-2/On-the-homology-of-classical-Lie-groups/ojm/1353054814.full)&rbrack;

reviewed in:

* [[Inna Zakharevich]], pp. 35 of: *Stable homotopy*, Section 11 of: *[K-theory and characteristic classes](https://pi.math.cornell.edu/~zakh/6530/)*, lecture notes (2017) &lbrack;[pdf](https://pi.math.cornell.edu/~zakh/6530/sec11.pdf), [[Zakharevich-StableHomotopy.pdf:file]]&rbrack;


Further early discussion:

* [[Raoul Bott]], *The space of loops on a Lie group*, Michigan Math. J. **5** 1 (1958) 35-61 &lbrack;[doi:10.1307/mmj/1028998010](https://projecteuclid.org/journals/michigan-mathematical-journal/volume-5/issue-1/The-space-of-loops-on-a-Lie-group/10.1307/mmj/1028998010.full)&rbrack;

  > (for loop spaces of [[Lie groups]])


* [[William Browder]], *Homology and Homotopy of H-Spaces*, Proceedings of the National Academy of Sciences of the United States of America **46** 4 (1960) 543-545 &lbrack;[jstor:70867](https://www.jstor.org/stable/70867)&rbrack;

* [[William Browder]], p. 36 of: *Torsion in H-Spaces*, Annals of Mathematics, Second Series **74** 1 (1961) 24-51  &lbrack;[jstor:1970305](https://www.jstor.org/stable/1970305)&rbrack;

* [[William Browder]], *Homology Rings of Groups*, American Journal of Mathematics **90** 1 (1968) &lbrack;[jstor:2373440](https://www.jstor.org/stable/2373440)&rbrack;




In the context of [[string topology]]:

* [[Moira Chas]], [[Dennis Sullivan]], §3 in: *String Topology* &lbrack;[arXiv:math/9911159](https://arxiv.org/abs/math/9911159)&rbrack;

* [[Ralph L. Cohen]], [[John D. S. Jones]], Jun Yan, pp. 15 of: *The loop homology algebra of spheres and projective spaces*, in *Categorical Decomposition Techniques in Algebraic Topology*, Progress in Mathematics **215**, Birkhäuser (2003) &lbrack;[arXiv:math/0210353](https://arxiv.org/abs/math/0210353), [doi:10.1007/978-3-0348-7863-0_5](https://doi.org/10.1007/978-3-0348-7863-0_5)&rbrack;


* Gwénaël Massuyeau, [[Vladimir Turaev]], *Brackets in the Pontryagin algebras of manifolds*, Mém. Soc. Math. France **154** (2017) &lbrack;[arXiv:1308.5131](https://arxiv.org/abs/1308.5131)&rbrack;



Textbook accounts:


* {#Whitehead78} [[George W. Whitehead]], p. 98 in: *Elements of Homotopy Theory*, Springer (1978) &lbrack;[doi:10.1007/978-1-4612-6318-0](https://link.springer.com/book/10.1007/978-1-4612-6318-0)&rbrack;


* {#Hatcher02} [[Allen Hatcher]], §3.C, pp. 287 in: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

Lecture notes

* [[Tyrone Cutler]], §3 in: *The Bott-Samelson Theorem* (2020) &lbrack;[pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Week%2011%20-%20The%20Bott-Samelson%20Theorem.pdf)&rbrack;

See also

* Wikipedia, _[Pontryagin product](https://en.wikipedia.org/wiki/Pontryagin_product)_

Computation of the Pontryagin products for (loop spaces of) [[flag manifolds]]:

* Jelena Grbic, Svjetlana Terzic, *The integral Pontrjagin homology of the based loop space on a flag manifold*, Osaka J. Math. **47** (2010) 439-460 &lbrack;[arXiv:math/0702113](https://arxiv.org/abs/math/0702113)





[[!include quantum cohomology as Pontrjagin rings -- references]]






[[!redirects Pontrjagin rings]]

[[!redirects Pontryagin ring]]
[[!redirects Pontryagin rings]]
[[!redirects Pontrjagin ring]]
[[!redirects Pontrjagin rings]]

[[!redirects Pontryagin product]]
[[!redirects Pontryagin products]]
[[!redirects Pontrjagin product]]
[[!redirects Pontrjagin products]]

[[!redirects Pontryagin multiplication]]
[[!redirects Pontryagin multiplications]]

[[!redirects Pontryagin-multiplication]]
[[!redirects Pontryagin-multiplications]]

[[!redirects Pontryagin algebra]]
[[!redirects Pontryagin algebras]]
[[!redirects Pontrjagin algebra]]
[[!redirects Pontrjagin algebras]]



[[!redirects Peterson isomorphism]]
[[!redirects Peterson isomorphisms]]

[[!redirects Adams-Hilton model]]
[[!redirects Adams-Hilton models]]


