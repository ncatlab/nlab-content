
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *cluster algebra* of rank $n$ is a [[commutative algebra]] equipped with some [[subsets]] of size $n$ called the *clusters*.
Some of these clusters are related by sequences of operations called mutations. A cluster variable is an element of any of the clusters. 

This theory is motivated by the [[total positivity]] phenomena in [[Lie theory]] and existance of good bases of some algebras and their representation spaces, for example canonical and dual canonical bases. 

A [[matrix]] $A$ over the [[field]] of [[real numbers]] is __[[totally positive matrix|totally positive]]__ (resp. __totally nonnegative__) if every [[minor]] (= [[determinant]] of any submatrix) is a [[positive number|positive]] (resp. nonnegative) real number. Total positivity implies a number of remarkable properties; for example all [[eigenvalues]] are distinct and positive. 

[[George Lusztig]] discovered that total positivity is closely related to some phenomena in the theory of [[Lie groups]] and [[quantum groups]]. Later, [[Sergey Fomin]] and [[Andrei Zelevinsky]] studied the canonical bases for [[quantum groups]] and discovered the [[combinatorics]] of simple transformations and defined  associated classical and quantum __cluster algebras__ to such situations.   In particular, Stasheff [[associahedron|associahedra]] are  associated to these cluster algebras. Remarkably, they found an unusual [[algebraic geometry]] related to cluster algebras, possessing new, and at the beginning mysterious, [[Laurent phenomenon]]. Later, the cluster algebras appeared also in the connection to the representations of [[quivers]], tilting theory and the wall crossing phenomenon, with the applications in [[representation theory]] and the study of [[triangulated category|triangulated categories]].

Quantum cluster algebras are noncommutative.


## References

### Cluster algebras

The original articles:

* {#FominZelevinsky02} [[Sergey Fomin]], [[Andrei Zelevinsky]]: *Cluster algebras I: Foundations*, J. Amer. Math. Soc. **15** 2 (2002) 497-529 &lbrack;[math.RT/0104151 ](http://arxiv.org/abs/math/0104151), [doi:10.1090/S0894-0347-01-00385-X](https://doi.org/10.1090/S0894-0347-01-00385-X)&rbrack; 

* {#FominZelevinsky03} [[Sergey Fomin]], [[Andrei Zelevinsky]]: *Cluster algebras II: Finite type classifications*, Invent. Math. **154** 1 (2003) 63-121 &lbrack;[doi:10.1007/s00222-003-0302-y](https://doi.org/10.1007/s00222-003-0302-y), [arXiv:math/0208229](https://arxiv.org/abs/math/0208229)&rbrack;

* {#BerensteinFominZelevinsky05} [[Arkady Berenstein]], [[Sergey Fomin]], [[Andrei Zelevinsky]]: *Cluster algebras III: Upper bounds and double Bruhat cells*, Duke Math. J. **126** 1  (2005) 1-52 &lbrack;[doi:10.1215/S0012-7094-04-12611-9](https://doi.org/10.1215/S0012-7094-04-12611-9), [arXiv:math/0305434](https://arxiv.org/abs/math/0305434)&rbrack;

* {#FominZelevinsky07} [[Sergey Fomin]], [[Andrei Zelevinsky]]: _Cluster algebras IV: Coefficients_, Compos. Math. __143__ (2007) 112-164 &lbrack;[doi:10.1112/S0010437X06002521](http://dx.doi.org/10.1112/S0010437X06002521), [arXiv:math/0602259](https://arxiv.org/abs/math/0602259), [MR2295199](http://www.ams.org/mathscinet-getitem?mr=2295199)&rbrack;

See also: 

* Wikipedia, *[Cluster algebra](https://en.wikipedia.org/wiki/Cluster_algebra)*

* [[Bernhard Keller]], _Cluster algebras, quiver representations and triangulated categories_, [arXiv:0807.1960](http://arXiv.org/abs/0807.1960) [MR2681708](http://www.ams.org/mathscinet-getitem?mr=2681708)

* Lots of links at [Cluster algebras portal](http://www.math.lsa.umich.edu/~fomin/cluster.html) including to the Fomin's [course slides](http://www.math.lsa.umich.edu/~fomin/nordfjordeid.html).

* description and conference info "Cluster Algebras and Lusztig's Semicanonical Basis", Oregon, June 2011, [html](http://pages.uoregon.edu/njp/cluster.html)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, [arXiv:0811.2435](http://arxiv.org/abs/0811.2435)

* [[Yuji Kodama]], Lauren Williams, _KP solitons, total positivity, and cluster algebras_, Proc. Natl. Acad. Sci. 108 (22) 8984--8989 [arxiv/1105.4170](https://arxiv.org/abs/1105.4170) [doi](https://doi.org/10.1073/pnas.1102627108)

* [[Bernard Leclerc]], _Cluster algebras and representation theory_, [arxiv/1009.4552](http://arxiv.org/abs/1009.4552)

* Christof Geiss, [[Bernard Leclerc]], Jan Schr&#246;er, _Preprojective algebras and cluster algebras_, [arxiv/0804.3168](http://arxiv.org/abs/0804.3168); _Kac-Moody groups and cluster algebras_, [arxiv/1001.3545](http://arxiv.org/abs/1001.3545)

* Tomoki Nakanishi, _[[dilogarithm|Dilogarithm]] identities for conformal field theories and cluster algebras: Simply laced case_, Nagoya Math. J. __202__ (2011) 23--43, [MR2804544](http://www.ams.org/mathscinet-getitem?mr=2804544) [doi](https://doi.org/10.1215/00277630-1260432)
* Kentaro Nagao, _Donaldson--Thomas theory and cluster algebras_, Duke Math. J. __162__(7): 1313--1367 [doi](https://doi.org/10.1215/00127094-2142753)

The connections to the exact WKB method a la Voros are studied in 

* Kohei Iwaki, Tomoki Nakanishi, _Exact WKB analysis and cluster algebras_, J. Phys. A 47 (2014) 474009 [arxiv/1401.7094](https://arxiv.org/abs/1401.7094); _Exact WKB analysis and cluster algebras II: simple poles, orbifold points, and generalized cluster algebras_, [arXiv:1409.4641](http://arxiv.org/abs/1409.4641)

Generalized cluster algebras are studied in 

* Leonid Chekhov, Michael Shapiro, _Teichm&#252;ller spaces of Riemann surfaces with orbifold points of arbitrary order and cluster variables_, Int. Math. Res. Notices (2014)  2746-2772 [arxiv/1111.3963](https://arxiv.org/abs/1111.3963) [doi](https://doi.org/10.1093/imrn/rnt016)
* Tomoki Nakanishi, _Structure of seeds in generalized cluster algebras_, [arxiv/1409.5967](https://arxiv.org/abs/1409.5967)

Review:

* Michael Gekhtman, Anton Izosimov, *Integrable systems and cluster algebras*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2403.07287](https://arxiv.org/abs/2403.07287)&rbrack;
 
### Quantum cluster algebras

* [[Arkady Berenstein]], [[Andrei Zelevinsky]], *Quantum cluster algebras*, Advances in Mathematics **195** 2 (2005) 405-455 &lbrack;[doi:10.1016/j.aim.2004.08.003](https://doi.org/10.1016/j.aim.2004.08.003), [math.QA/0404446](http://arxiv.org/abs/math/0404446)&rbrack;

* [[K. R. Goodearl]], [[M. T. Yakimov]], _Quantum cluster algebras and quantum nilpotent algebras_
Proc Natl Acad Sci USA 111(27):9696--9703  (2014) [doi](https://doi.org/10.1073/pnas.1313071111)

* Fan Qin, _Dual canonical bases and quantum cluster algebras_, [arXiv:2003.13674](https://arxiv.org/abs/2003.13674)

> Given any quantum cluster algebra arising from a quantum unipotent subgroup of symmetrizable Kac-Moody type, we verify the quantization conjecture in full generality that the quantum cluster monomials are contained in the dual canonical basis after rescaling. 

* Christof Geiss, [[Bernard Leclerc]], Jan Schr&#246;er, _Cluster structures on quantum coordinate rings_, Selecta Math. __19__ (2013), 337--397 [arxiv/1104.0531](https://arxiv.org/abs/1104.0531)

* Yoshiyuki Kimura, _Quantum unipotent subgroup and dual canonical basis_, Kyoto J. Math. 52(2): 277--331 (2012) [doi](https://doi.org/10.1215/21562261-1550976) 

category: algebra

[[!redirects cluster algebras]]
[[!redirects cluster transformation]]
[[!redirects cluster transformations]]

[[!redirects quantum cluster algebra]]
[[!redirects quantum cluster algebras]]


