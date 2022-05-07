
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

### General

The construction of [[algebraic K-theory]] $K(R)$, originally defined for [[rings]] $R$, generalizes to [[A-∞ ring|$A_\infty$]]-[[ring spectra]]. 
When $R$ happens to be a [[connective spectrum|connective]] [[E-infinity ring|$E_\infty$]]-[[ring spectrum]], then also the [[Brown representability theorem|representing spectrum]] $K(R)$ of its algebraic K-theory is a [[connective spectrum|connective]] [[E-infinity ring|$E_\infty$]]-[[ring spectrum]]
([Schwänzl & Vogt 1994, Thm. 1](#SchwaenzlVogt94), [EKMM 1997, Thm. 6.1](#EKMM97)) so that this construction may then be iterated to yield _iterated algebraic K-theories_ $K(K(R))$, $K(K(K(R)))$, etc.


The [[red-shift conjecture]] says that this iteration plays a special role in [[chromatic homotopy theory]].

### On topological K-theory

The construction of iterated algebraic K-theory has received particular attention for the case that $R = $ [[ku]] is the [[connective spectrum|connective]] [[ring spectrum]] [[Brown representability theorem|representing]] [[complex vector bundle|complex]] [[topological K-theory]].

Here the first iterated stage $K(ku)$ is related to [[BDR 2-vector bundles]] essentially like [[ku]] is related to ordinary [[complex vector bundles]].

The tower $K^{2r}(ku)$ of higher iterated algebraic K-theories of topological K-theory has been shown to accommodate a generalization of the [[Fourier-Mukai transform|Fourier-Mukai]]-type transform on [[twisted K-theory]] that is given by [[topological T-duality]], generalizing it to [[spherical T-duality]] ([Lind-Sati-Westerland 16](#LindSatiWesterland16)).

## Properties

### Red-shift conjecture

## References

### Algebraic K-theory of ring spectra

On the [[algebraic K-theory]] of ([[connective spectrum|connective]]) [[ring spectra]]:

* {#SchwaenzlVogt94} [[Roland Schwänzl]], [[Rainer Vogt]], *Basic Constructions in the K-Theory of Homotopy Ring Spaces*, Transactions of the American Mathematical Society, Vol. 341, No. 2 (Feb., 1994), pp. 549-584 ([jstor:2154572](https://www.jstor.org/stable/2154572), [doi:10.2307/2154572](https://doi.org/10.2307/2154572))


* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], chapter VI of _[[Rings, modules and algebras in stable homotopy theory]]_, AMS Mathematical Surveys and Monographs Volume 47 (1997) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))

* {#BlumbergGepnerTabuada10} [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], Section 9.5 of: _A universal characterization of higher algebraic K-theory_, Geom. Topol. 17 (2013) 733-838 ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282), [doi:10.2140/gt.2013.17.733](http://dx.doi.org/10.2140/gt.2013.17.733))

* [[Jacob Lurie]], _Algebraic K-Theory of Ring Spectra_, Lecture 19 of _[Algebraic K-Theory and Manifold Topology](https://www.math.ias.edu/~lurie/281.html)_, 2014 ([pdf](http://people.math.harvard.edu/~lurie/281notes/Lecture19-Rings.pdf))

The  algebraic K-theory of specifically of [[suspension spectra]] of [[loop spaces]] (Waldhausen's _[[A-theory]]_) is originally due to

* [[Friedhelm Waldhausen]], _Algebraic K-theory of spaces_, In: A. Ranicki N.,  Levitt, F. Quinn (eds.), Algebraic and Geometric Topology, Lecture Notes in Mathematics, vol 1126. Springer, Berlin, Heidelberg (1985) ([doi:10.1007/BFb0074449](https://doi.org/10.1007/BFb0074449))


On the [[algebraic K-theory]] $K(R)$ of a [[ring spectrum]] $R$ as the [[Grothendieck group]] of [[(∞,1)-module bundles]] over $R$: 

* [[John Lind]], _Bundles of spectra and algebraic K-theory_, Pacific J. Math. 285 (2016) 427-452 ([arXiv:1304.5676](https://arxiv.org/abs/1304.5676), [doi:10.2140/pjm.2016.285.427](https://doi.org/10.2140/pjm.2016.285.427))


### Algebraic K-theory of topological K-theory

On the first [[algebraic K-theory]] $K(ku)$ of [[connective spectrum|connective]] [[topological K-theory]]:

* [[Christian Ausoni]], _On the algebraic K-theory of the complex K-theory spectrum_, Inventiones mathematicae volume 180, pages 611–668 (2010) ([arXiv:0902.2334](http://arxiv.org/abs/0902.2334), [doi:10.1007/s00222-010-0239-x](https://doi.org/10.1007/s00222-010-0239-x))

* [[Christian Ausoni]], [[John Rognes]], _Algebraic K-theory of topological K-theory_, Acta Math. Volume 188, Number 1 (2002), 1-39 ([euclid:acta/1485891473](https://projecteuclid.org/euclid.acta/1485891473))

* [[Christian Ausoni]], [[John Rognes]], _Rational algebraic K-theory of topological K-theory_, Geom. Topol. 16 (2012) 2037-2065 ([arXiv:0708.2160](https://arxiv.org/abs/0708.2160), [doi:10.2140/gt.2012.16.2037](http://dx.doi.org/10.2140/gt.2012.16.2037))


Interpretation of $K(ku)$ as the [[K-theory]] of [[BDR 2-vector bundles]]:

* [[Nils Baas]], [[Bjørn Ian Dundas]], [[John Rognes]], _Two-vector bundles and forms of elliptic cohomology_, London Math. Soc. Lecture Note Ser., 308, Cambridge Univ. Press, Cambridge, 2004 ([arXiv:math/0306027](https://arxiv.org/abs/math/0306027),  [doi:10.1017/CBO9780511526398.005](https://doi.org/10.1017/CBO9780511526398.005))

* [[Nils Baas]], [[Bjørn Ian Dundas]], [[Birgit Richter]], [[John Rognes]], _Stable bundles over rig categories_, Journal of Topology, Volume 4, Issue 3, September 2011, Pages 623–640 ([arXiv:0909.1742](https://arxiv.org/abs/0909.1742), [doi:10.1112/jtopol/jtr016](https://doi.org/10.1112/jtopol/jtr016))

### Algebraic K-theory of algebraic K-theory

On the [[algebraic K-theory]] of algebraic K-theory of [[finite fields]] $K(K(\mathbb{F}))$:

* Gabe Angelini-Knoll, _Detecting the $\beta$-family in iterated algebraic K-theory of finite fields_, Wayne State University 2017 ([arXiv:1810.10088](https://arxiv.org/abs/1810.10088), [oa_dissertations:1778](https://digitalcommons.wayne.edu/oa_dissertations/1778))

### Higher iterated algebraic K-theory of topological K-theory

Discussion of higher and of [[twisted cohomology|twisted]] iterated K-theory on $ku$, and realization of the [[spherical T-duality]] on twisted $K^{2r}(ku)$:

* {#LindSatiWesterland16}  [[John Lind]], [[Hisham Sati]], [[Craig Westerland]], _A higher categorical analogue of topological T-duality for sphere bundles_, Annals of K-Theory, Vol. 5 (2020), No. 1, 1–42 ([arXiv:1601.06285](http://arxiv.org/abs/1601.06285), [doi:doi:10.2140/akt.2020.5.1](https://msp.org/akt/2020/5-1/p01.xhtml))


[[!redirects iterated algebraic K-theories]]

[[!redirects iterated K-theory]]
[[!redirects iterated K-theories]]


