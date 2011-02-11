
# Noncommutative associated bundles
* table of contents
{: toc}

## Distinguished from other noncommutative bundles

Here we discuss associating a bundle with fiber $F$ to a [[noncommutative principal bundle]] with structure "group" (e.g. Hopf algebra or generalization). There are also other kinds of [[noncommutative vector bundle]]s (e.g. locally free sheaves on nc spaces; duals of projective modules etc.).


## Affine case

The simplest case of the [[noncommutative principal bundle]] is the case of Hopf-Galois extension. 

* the total and base space are affine, i.e. represented by noncommutative algebras $P$ and $U$. There is a monomorphism of algebras
$U\hookrightarrow P$ (which is viewed as a comorphism of the projection among the spectra)

* $P$ is equipped with a right coaction $P\to P\otimes H$ of a fixed Hopf algebra $H$, which is an algebra map (we say that $P$ is a right $H$-comodule algebra) 

* Hopf-Galois condition is satisfied: $U\hookrightarrow P$ is a $H$-[[Hopf-Galois extension]] (typically required to be faithfully flat).

The space of __global sections of the associated vector bundle__ with  $V$ as a fiber is then simply the [[cotensor product]] with the vector space $P\Box^H V$, for which we need a left $H$-comodule structure $V\to H\otimes V$. This construction however does not give the total space of the associated bundle as a noncommutative space. In commutative algebraic case to get the total algebra we need to replace vector space by the symmetric algebra of the dual, and then do the cotensor product. This can be repeated in the noncommutative case to get some algebra, however this does not reproduce the same space of sections as the cotensor product with the underlying vector space. Instead one can take the tensor algebra of the dual of the vector space as the noncommutative analogue of the symmetric algebra. After taking the cotensor product, one gets much bigger total algebra. However, it does not reproduce the quantum examples. Sometimes one should take some sort of a q-symmetric algebra, like generalizations of quantum Manin plane, what gives a consistent result just in some special cases. 


## Gluing via localizations

One can glue Hopf-Galois extensions along [[noncommutative localization]]s to more global objects. For example, both the total space and the base space can be represented by [[noncommutative scheme]]s. An early example with nonaffine base space is described in Zoran &#352;koda, "Localizations for construction of quantum coset spaces" (most proofs given elsewhere). This is an application of using [[descent in noncommutative algebraic geometry]]. To get to the sheaves of sections of associated bundles, one defines the sections as a cotensor product *locally* on affine pieces and then glues. A simple case is treated in Zoran &#352;koda, "Coherent states for Hopf algebras".


## Literature

### Affine case

* [[S. Majid]], [[T. Brzeziński]], _Quantum group gauge theory on quantum spaces_, Commun. Math. Phys. __157__, 591--638 (1993); Erratum 167, 235 (1995) [MR94g:58015](http://www.ams.org/mathscinet-getitem?mr=1243712), [euclid](http://projecteuclid.org/getRecord?id=euclid.cmp/1104254023)


### Nonaffine case

* Zoran &#352;koda, _Localizations for construction of quantum coset spaces_, Banach Center Publications __61__, 265&#8211;298, Warszawa 2003, [math.QA/0301090](http://arxiv.org/abs/math.QA/0301090)

* Zoran &#352;koda, _Coherent states for Hopf algebras_, Letters in Mathematical Physics __81__, N.1, pp. 1-17, July 2007, [pdf](http://www.irb.hr/korisnici/zskoda/skodacohstates.pdf), (earlier different arXiv version: math.QA/0303357)


[[!redirects noncommutative associated bundle]]
[[!redirects noncommutative associated bundles]]
[[!redirects non-commutative associated bundle]]
[[!redirects non-commutative associated bundles]]
