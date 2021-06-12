

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
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

The [[equivariant cohomology|equivariant]] [[generalized cohomology theory]] which is [[Brown representability theorem|represented]] by the [[equivariant sphere spectrum]] may also be called _equivariant stable cohomotopy_, as it is the [[equivariant stable homotopy theory]] version of [[stable cohomotopy]], hence of [[cohomotopy]]. This is to be thought of as the first order [[Goodwillie-Taylor tower|Goodwillie approximation]] of plain ("unstable") [[equivariant cohomotopy]].

Just as the plain [[sphere spectrum]] is a distinguished object of plain [[stable homotopy theory]], so the [[equivariant sphere spectrum]] is distinguished in [[equivariant stable homotopy theory]] and hence so is equivariant stable cohomotopy theory.

## Properties

### As equivariant algebraic K-theory over $\mathbb{F}_1$
 {#AsAlgebraicKTheoryOverTheFieldWithOneElement}

The following is known as the _Barratt-Priddy-Quillen theorem_:

+-- {: .num_prop #StableCohomotopyIsKTheoryOfFinSet}
###### Proposition
**([[stable cohomotopy]] is K-theory of [[FinSet]])**

Let $\mathcal{C} = $ [[FinSet]] be a [[skeleton]] of the category of [[finite sets]], regarded as a [[permutative category]]. Then the [[K-theory of a permutative category|K-theory of this permutative category]] 

$$
  K(FinSet) \;\simeq\; \mathbb{S}
$$

is represented by the [[sphere spectrum]], hence is stable cohomotopy.

=--

This is due to [Barratt-Priddy 72](#BarrattPriddy72) reproved in [Segal 74, Prop. 3.5](#Segal74). See also [Priddy 73](#Priddy73), [Glasman 13](#Glasman13).

+-- {: .num_remark #StableCohomotopyIsAlgebraicKTheoryOverFieldWithOneElement}
###### Remark
**([[stable cohomotopy]] as [[algebraic K-theory]] over the [[field with one element]])**

Notice that for $F$ a [[field]], the [[K-theory of a permutative category]] of its [[category of modules]] $F Mod$ is its [[algebraic K-theory]] $K F$ (see [this example](K-theory+of+a+permutative+category#OrdinaryAlgebraicKTheoryFromPermutativeCategoryOfProjectiveModules))

$$
  K F \;\simeq\; K(F Mod)
  \,.
$$ 

Now ([[pointed sets|pointed]]) [[finite sets]] may be regarded as the modules over the "[[field with one element]]" $\mathbb{F}_1$ (see [there](field+with+one+element#Modules)):

$$
  \mathbb{F}_1 Mod
  \;=\;
  FinSet^{\ast/}
$$

If this is understood, example \ref{StableCohomotopyIsKTheoryOfFinSet} says that [[stable cohomotopy]] is the algebraic K-theory of the [[field with one element]]:

$$
  \mathbb{S} \;\simeq\; K \mathbb{F}_1
  \,.
$$

=--

This perspective is highlighted for instance in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06), [Mahanta 17](#Mahanta17), [Dundas-Goodwillie-McCarthy 13, II 1.2](#DundasGoodwillieMcCarthy13), [Morava](#MoravaSomeBackground), [Connes-Consani 16](#ConnesConsani16)).



The perspective that the [[K-theory]] $K \mathbb{F}_1$ over $\mathbb{F}_1$ should be [[stable Cohomotopy]] has been highlighted in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06), [Mahanta 17](#Mahanta17), [Dundas-Goodwillie-McCarthy 13, II 1.2](#DundasGoodwillieMcCarthy13), [Morava](#MoravaSomeBackground), [Connes-Consani 16](#ConnesConsani16)). Generalized to [[equivariant stable homotopy theory]], the statement that [[equivariant K-theory]] $ K_G \mathbb{F}_1$ over $\mathbb{F}_1$ should be [[equivariant stable Cohomotopy]] is discussed in [Chu-Lorscheid-Santhanam 10, 5.3](#ChuLorscheidSanthanam10).

[[!include Segal completion -- table]]


## Examples

### Equivariant stable $\pi_3^{\mathbb{S}}$

See at _[quaternionic Hopf fibration --  Class in equivariant stable homotopy theory](quaternionic+Hopf+fibration#ClassInEquivariantStableHomotopyTheory)_


### Of the point: The Burnside ring

+-- {: .num_prop #BurnsideRingIsEquivariantStableCohomotopyOfPoint}
###### Proposition
**([[Burnside ring is equivariant stable cohomotopy of the point]])**

Let $G$ be a [[finite group]], then its [[Burnside ring]] $A(G)$ is [[isomorphism|isomorphic]] to the [[equivariant stable cohomotopy]] [[cohomology ring]] $\mathbb{S}_G(\ast)$ of the [[point]] in degree 0. 

$$
  A(G) \overset{\simeq}{\longrightarrow} \mathbb{S}_G(\ast)
  \,.
$$

=--

This is due to [Segal 71](#Segal71), a detailed proof is given by [tom Dieck 79, theorem 8.5.1](#tomDieck79). See also [Lück 05, theorem 1.13](#Lueck05), [tom Dieck-Petrie 78](#tomDieckPetrie78).

[[!include Segal completion -- table]]


More explicitly, this means that the Burnside ring of a group $G$ is isomorphic to the [[colimit]]

$$
  A(G) \simeq \underset{\longrightarrow}{\lim}_V [S^V,S^V]_G
$$

over $G$-[[representations]] in a complete [[G-universe]], of $G$-[[homotopy classes]] of $G$-equivariant based [[continuous functions]] from the [[representation sphere]] $S^V$ to itself ([Greenlees-May 95, p. 8](#GreenleesMay95)).



## Related concepts

[[!include flavours of cohomotopy -- table]]


* [[Burnside ring]]

* [[Segal conjecture]], [[Sullivan conjecture]]

## References

### Relation to Burnside ring

Relation to [[Burnside ring]]:

* {#Segal71} [[Graeme Segal]], _Equivariant stable homotopy theory_, In Actes du Congr&egrave;s International des Math &eacute;maticiens (Nice, 1970), Tome 2 , pages 59–63. Gauthier-Villars, Paris, 1971 ([[SegalEquivariantStableHomotopyTheory.pdf:file]])

* {#tomDieckPetrie78} [[Tammo tom Dieck]], T. Petrie,  _Geometric modules over the Burnside ring_, Invent. Math. 47 (1978) 273-287 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/tomDieck-geometric.pdf))

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Springer 1979

* {#tomDieck87} [[Tammo tom Dieck]], Section II.8 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))


### Relation to Segal-Carlsson completion theorem

Relation to [[Segal-Carlsson completion theorem]]:

* Czes Kosniowski, _Equivariant cohomology and Stable Cohomotopy_, Math. Ann. 210, 83-104 (1974) ([doi:10.1007/BF01360033](https://doi.org/10.1007/BF01360033) [pdf](https://link.springer.com/content/pdf/10.1007/BF01360033.pdf))

* Erkki Laitinen, _On the Burnside ring and stable cohomotopy of a finite group_,  Mathematica Scandinavica Vol. 44, No. 1 (August 30, 1979), pp. 37-72 ([jstor:24491306](https://www.jstor.org/stable/24491306), [[Laitinen79.pdf:file]])  

* [[Gunnar Carlsson]], _Equivariant Stable Homotopy and Segal's Burnside Ring Conjecture_,  Annals of Mathematics Second Series, Vol. 120, No. 2 (Sep., 1984), pp. 189-224 ([jstor:2006940](https://www.jstor.org/stable/2006940), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/carlsson.pdf))

* {#Lueck05} [[Wolfgang Lück]], _The Burnside Ring and Equivariant Stable Cohomotopy for Infinite Groups_, Pure Appl. Math. Q.  1 (2005), no. 3, Special Issue: In memory of Armand Borel. Part 2, 479--541 ([arXiv:math/0504051](https://arxiv.org/abs/math/0504051))

* Noe Barcenas, _Nonlinearity, Proper Actions and Equivariant Stable Cohomotopy_ ([arXiv:1302.1712](https://arxiv.org/abs/1302.1712))

A lift of [[Seiberg-Witten invariants]] to classes in [[circle group]]-equivariant stable cohomotopy is discussed in

* Stefan Bauer, Mikio Furuta _A stable cohomotopy refinement of Seiberg-Witten invariants: I_ ([arXiv:math/0204340](http://arxiv.org/abs/math/0204340))

* Stefan Bauer, _A stable cohomotopy refinement of Seiberg-Witten invariants: II_ ([arXiv:math/0204267](http://arxiv.org/abs/math/0204267))

* Christian Okonek, Andrei Teleman, _Cohomotopy Invariants and the Universal Cohomotopy Invariant Jump Formula_, J. Math. Sci. Univ. Tokyo 15 (2008), 325-409 ([pdf](http://www.matmor.unam.mx/~barcenas/nonlinearity.pdf))

### As equivariant K-theory over the field with one element

The identification of stable cohomotopy with the [[K-theory of a permutative category|K-theory of the permutative category]] of [[finite set]] is due to 

* {#BarrattPriddy72} [[Michael Barratt]], [[Stewart Priddy]], _On the homology of non-connected monoids and their associated groups_, Commentarii Mathematici Helvetici, December 1972, Volume 47, Issue 1, pp 1–14 ([doi:10.1007/BF02566785](https://doi.org/10.1007/BF02566785))

* {#Segal74} [[Graeme Segal]], _Categories and cohomology theories_, Topology vol 13, pp.  293-312,  1974  ([pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))

see also

* {#Priddy73} [[Stewart Priddy]], _Transfer, symmetric groups, and stable homotopy theory_, in _Higher K-Theories_, Springer, Berlin, Heidelberg, 1973. 244-255 ([pdf](https://link.springer.com/content/pdf/10.1007/BFb0067060.pdf))

* {#Glasman13} [[Saul Glasman]], _The multiplicative Barratt-Priddy-Quillen theorem and beyond_, talk 2013 ([pdf](http://math.mit.edu/~sglasman/bpq-beamer.pdf))

The resulting interpretation of stable cohomotopy as [[algebraic K-theory]] over the [[field with one element]] is amplified in the following texts:

* {#DundasGoodwillieMcCarthy13} [[Bjørn Dundas]], [[Thomas Goodwillie]], [[Randy McCarthy]], chapter II, section 1.2 of  _The local structure of algebraic K-theory_, Springer 2013 ([pdf](http://math.mit.edu/~nrozen/juvitop/dundas.pdf))

* {#Deitmar06} [[Anton Deitmar]], _Remarks on zeta functions and K-theory over $\mathbb{F}_1$_ ([arXiv:math/0605429](https://arxiv.org/abs/math/0605429))

* {#Guillot06} [[Pierre Guillot]], _Adams operations in cohomotopy_ ([arXiv:0612327](https://arxiv.org/abs/math/0612327))

* {#Mahanta17} [[Snigdhayan Mahanta]], _G-theory of $\mathbb{F}_1$-algebras I: the equivariant Nishida problem_, J. Homotopy Relat. Struct. 12 (4), 901-930, 2017 ([arXiv:1110.6001](https://arxiv.org/abs/1110.6001))

* {#ChuLorscheidSanthanam10} Chenghao Chu, [[Oliver Lorscheid]], Rekha Santhanam, _Sheaves and K-theory for $\mathbb{F}_1$-schemes_, Advances in Mathematics, Volume 229, Issue 4, 1 March 2012, Pages 2239-2286 ([arxiv:1010.2896](https://arxiv.org/abs/1010.2896))


see also

* {#MoravaSomeBackground} [[Jack Morava]], _Some background on Manin's theorem $K(\mathbb{F}_1) \sim \mathbb{S}$_ ([pdf](http://www.alainconnes.org/docs/Morava.pdf), [[MoravaSomeBackground.pdf:file]])

* {#ConnesConsani16} [[Alain Connes]], [[Caterina Consani]], _Absolute algebra and Segal's Gamma sets_, Journal of Number Theory 162 (2016): 518-551 ([arXiv:1502.05585](https://arxiv.org/abs/1502.05585))

* {#Berman18} [[John D. Berman]], p. 92 of: _Categorified algebra and equivariant homotopy theory_, PhD thesis 2018  ([arXiv:1805.08745](https://arxiv.org/abs/1805.08745))


### Relation to equivariant cobordism theory

Proof that [[equivariant framed bordism homology theory]] is [[Brown representability theorem|co-represented]] by the [[equivariant sphere spectrum]]:

* Czes Kosniowski, _Equivariant Stable Homotopy and Framed Bordism_, Transactions of the American Mathematical Society
Vol. 219 (1976), pp. 225-234 ([jstor:1997591](https://www.jstor.org/stable/1997591))


### In M-brane charge quantization

Discussion for [[M-brane]] physics:

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

  ([[equivariant rational homotopy theory|rational]]  [[equivariant cohomotopy]])

* {#SatiSchreiber19} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))

  (implying [[RR-field tadpole cancellation]])

[[!redirects equivariant stable Cohomotopy]]

[[!redirects equivariant stable cohomotopy theory]]
[[!redirects equivariant stable cohomotopy theories]]

[[!redirects equivariant stable Cohomotopy theory]]
[[!redirects equivariant stable Cohomotopy theories]]


[[!redirects stable equivariant cohomotopy]]
[[!redirects stable equivariant Cohomotopy]]


