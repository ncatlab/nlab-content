
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

What is called _Rozansky-Witten theory_ ([Rozansky-Witten 96](#RozanskyWitten96)) is a [[topological twist]] of [[D=3 N=4 super Yang-Mills theory]], or else the assignment of  [[TQFT|topological invariant]] [[quantum observables]] which such a [[perturbative quantum field theory]] assigns to a given [[3-manifold]] $\Sigma^3$, or more generally to a [[Wilson loop]] [[knot]] inside a [[3-manifold]] -- the _[[Rozansky-Witten invariants]]_.

The key result of [Rozansky-Witten 96](#RozanskyWitten96) is that, after [[gauge fixing]] and some subtle [[field (physics)|field]] identifications, the [[Feynman rules]] of RW-[[topological twist|twisted]] [[D=3 N=4 super Yang-Mills theory]] are those of [[perturbative quantization of 3d Chern-Simons theory|perturbative]] [[Chern-Simons theory]], in that the only relevant [[propagator]] is the [[Chern-Simons propagator]] and the only relevant [[Feynman diagrams]] are trivalent, _except_ that the [[Lie algebra weight system|Lie algebra weights]] assigned by [[Chern-Simons theory]] to a [[Feynman diagram|Feynman]]-[[Jacobi diagram]], are replaced by other [[weight systems]], now called _[[Rozansky-Witten weight systems]]_.

Precisely: Recalling that [[perturbative quantization of 3d Chern-Simons theory|perturbative Chern-Simons]] [[Wilson loop observables]] are given by evaluating [[Lie algebra weight systems]] on the [[Jacobi diagram]]-valued [[universal Vassiliev invariant]]

<center>
<img src="https://ncatlab.org/nlab/files/TheGrandStoryOfVassilievKnotInvariantsIII.jpg" width="800">
</center>

we have that [[Wilson loop]] [[Rozansky-Witten invariants]] ([Rozansky-Witten 96 (2.26)](#RozanskyWitten96)) are given by evaluating [[Rozansky-Witten invariants]] on the [[Jacobi diagram]]-valued [[universal Vassiliev invariant]] 

<center>
<img src="https://ncatlab.org/nlab/files/TheGrandStoryOfRozanskyWittenKnotInvariantsIII.jpg" width="800">
</center>


> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

These [[Rozansky-Witten weight systems]] depend only on the [[hyperkähler manifold]] $\mathcal{M}^{4n}$ which is the (classical) [[Coulomb branch]] of the RW-[[topological twist|twisted]] [[D=3 N=4 super Yang-Mills theory]], and in fact they are independent of the [[Riemannian geometry]] of $\mathcal{M}^{4n}$ and depend only on the underlying [[holomorphic symplectic manifold]] ([Kapranov 99](#Kapranov99)). Generally, they are defined for $\mathcal{M}^{4n}$ any [[hyperkähler manifold]] which is either asymptotically flat ([[ALE spaces]]) or [[compact topological space]] ([[compact hyperkähler manifolds]]).

Via the equivalent reformulation by [Kapranov 99](#Kapranov99) one finds ([Roberts-Willerton 10](#RobertsWillerton10)) that the [[Rozansky-Witten invariants]] are structurally [[Lie algebra weight systems]] themselves, but [[Lie algebra object|internal]] to the [[derived category of coherent sheaves]] of $\mathcal{M}^{4n}$ and composed with an [[integration]] over $\mathcal{M}^{4n}$ which makes the resulting [[Dolbeault cohomology]]-valued weights become [[ground field]]-valued.

\linebreak

[Konsevich 97](#Konsevich97) gives a formulation of [[Rozansky-Witten invariants]] via [[characteristic classes]] of [[foliations]] and [[Gelfand-Fuks cohomology]]. He devised a formal construction, again depending on a trivalent graph of a cohomology class of the Lie algebra of formal (in the sense of formal power series) [[Hamiltonian vector fields]] on any arbitrary finite-dimensional symplectic vector space. Characteristic classes of foliations may induce examples where this construction applies; one of the examples yields Rozansky-Witten . 

## Properties

### As KK-compactification of M5-brane worldvolume

Rozansky-Witten theory may be identified with [[topological twist|topologically twisted]] [[KK-compactification]] of the [[D=6 N=(2,0) SCFT]] on the [[M5-brane]] ([Gukov-Putrov-Vafa 17, Sections 3.2 and 4.2](#GukovPutrovVafa17))

## Examples

### Rozanzky-Witten Wilson loop of unknot is $\hat A$-genus

+-- {: .num_prop #RozanskyWittenWilsonLoopOfUnknotIsSquareRootOfAHat}
###### Proposition
**([[Rozansky-Witten Wilson loop of unknot is A-hat genus|Rozansky-Witten Wilson loop of unknot is square root of A-hat genus]])**

For $\mathcal{M}^{4n}$ a [[hyperkähler manifold]] (or just a [[holomorphic symplectic manifold]]) the [[Rozansky-Witten invariant]] [[Wilson loop observable]] associated with the [[unknot]] in the [[3-sphere]] is the [[square root]] $\sqrt{{\widehat A}(\mathcal{M}^{4n})}$ of the [[A-hat genus]] of $\mathcal{M}^{4n}$.

=--

This is [Roberts-Willerton 10, Lemma 8.6](Rozansky-Witten+Wilson+loop+of+unknot+is+A-hat+genus#RobertsWillerton10), using the [[Wheels theorem]] and the [[Hitchin-Sawon theorem]].


## Related concepts

* [[Casson invariant]]

* [[Seiberg-Witten invariant]]

## References


Original articles:

* {#RozanskyWitten96} [[Lev Rozansky]], [[Edward Witten]], _Hyper-K&#228;hler geometry and invariants of 3-manifolds_, Selecta Math., New Ser. __3__ (1997), 401&#8211;458 ([arXiv:hep-th/9612216](https://arxiv.org/abs/hep-th/9612216), [doi:10.1007/s000290050016](https://doi.org/10.1007/s000290050016), [MR98m:57041](http://www.ams.org/mathscinet-getitem?mr=98m:57041))

* {#Konsevich97} [[Maxim Kontsevich]], _Rozansky&#8211;Witten invariants via formal geometry_, Compositio Mathematica 115: 115&#8211;127, 1999, [doi](http://dx.doi.org/10.1023/A:1000619911308), [arXiv:dg-ga/9704009](http://arxiv.org/abs/dg-ga/9704009), [MR2000h:57057](http://www.ams.org/mathscinet-getitem?mr=2000h:57057) 

* {#Kapranov99} [[Mikhail Kapranov]], _Rozansky&#8211;Witten invariants via Atiyah classes_,  Compositio Math.  __115__ (1999), no. 1, 71--113 ([MR2000h:57056](http://www.ams.org/mathscinet-getitem?mr=2000h:57056), [doi](http://dx.doi.org/10.1023/A:1000664527238), [alg-geom/9704009](http://arxiv.org/abs/alg-geom/9704009))

* [[Justin Roberts]], [[Justin Sawon]], _Generalisations of Rozansky-Witten invariants_, Geom. Topol. Monogr. 4 (2002) 263-279 ([arXiv:math/0112210](https://arxiv.org/abs/math/0112210))

Unified description of [[Rozansky-Witten weight systems]] as [[Lie algebra weight systems]] for [[Lie algebra objects]] in the [[derived category of quasi-coherent sheaves]], and unified [[Wheels theorem]]:

* {#RobertsWillerton10} [[Justin Roberts]], [[Simon Willerton]], _On the Rozansky-Witten weight systems_, Algebr. Geom. Topol. 10 (2010) 1455-1519 ([arXiv:math/0602653](https://arxiv.org/abs/math/0602653))


Review:

* [[Justin Sawon]], _Rozansky-Witten invariants of hyperkähler manifold_, Cambridge 2000 ([arXiv:math/0404360](https://arxiv.org/abs/math/0404360))

* {#Roberts01} [[Justin Roberts]], _Rozansky-Witten theory_ ([arXiv:math/0112209](https://arxiv.org/abs/math/0112209))



Further relation to [[Chern-Simons theory]]:

* [[Anton Kapustin]], [[Natalia Saulina]], _Chern-Simons-Rozansky-Witten topological field theory_, Nucl. Phys. B823 (2009) 403-427 ([arXiv:0904.1447](https://arxiv.org/abs/0904.1447), [spire:817599/](http://inspirehep.net/record/817599/))

* Jian Qiu, Maxim Zabzine, _Odd Chern-Simons theory, Lie algebra cohomology and characteristic classes_, Commun. Math. Phys. 300:789-833, 2010
 ([arxiv/0912.1243](http://arxiv.org/abs/0912.1243))

As [[topological twist|topologically twisted]] [[KK-compactification]] of the [[D=6 N=(2,0) SCFT]] on the [[M5-brane]] (see [[D=3 N=4 super Yang-Mills theory]] and [[3d-3d correspondence]]):

* {#GukovPutrovVafa17}  [[Sergei Gukov]], Pavel Putrov, [[Cumrun Vafa]], Sections 3.2 and 3.4 of: _Fivebranes and 3-manifold homology_, J. High Energ. Phys. (2017) 2017: 71 ([arXiv:1602.05302](https://arxiv.org/abs/1602.05302))

* Cyril Closset, Heeyeon Kim, Section 6.1 of: _Comments on twisted indices in 3d supersymmetric gauge theories_, JHEP 08 (2016) 059 ([arXiv:1605.06531](https://arxiv.org/abs/1605.06531))

Discussion of [[Rozansky-Witten theory]] as a [[boundary field theory]]:

* [[Anton Kapustin]], [[Lev Rozansky]], [[Natalia Saulina]], 
_Three-dimensional topological field theory and symplectic algebraic geometry I_ ([arXiv:0810.5415](https://arxiv.org/abs/0810.5415))


Relation to [[equivariant cohomology]]:

* [[Sergei Gukov]], Po-Shen Hsin, Hiraku Nakajima, Sunghyuk Park, Du Pei, Nikita Sopenko, _Rozansky-Witten geometry of Coulomb branches and logarithmic knot invariants_ ([arXiv:2005.05347](https://arxiv.org/abs/2005.05347))

* Jian Qiu, _Rozansky-Witten theory, Localised then Tilted_ ([arXiv:2011.05375](https://arxiv.org/abs/2011.05375))











[[!redirects Rozansky-Witten class]]
[[!redirects Rozansky-Witten invariant]]
[[!redirects Rozansky-Witten invariants]]
[[!redirects Rozansky-Witten theories]]