
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For [[N=2 D=4 super Yang-Mills theory]] the [[moduli space]] of [[vacuum expectation values]] (VEVs) of the theory is meant to locally be a [[Cartesian product]] of spaces of

1. [[moduli]] of the [[vector multiplet]] (the [[gauge field]] sector) 

   this is called the *Coulomb branch*

1. moduli of the [[hypermultiplet]] (the scalar matter field sector)

   this is called the *[[Higgs branch]]*.

These are thought to be [[duality in physics|dual]] to each other under a version of [[mirror symmetry]]. This is largely the topic of [[Seiberg-Witten theory]]. 


Definitions of the Coulomb and Higgs branches have been extended to [[N=4 D=3 super Yang-Mills theory]].

## Definition

### D=4

### D=3

Given $G$ a complex reductive group and $M$ a complex [[symplectic representation]] of the form $M=N \bigoplus N^*$, the Coulomb branch is defined as the spectrum of the ring given by equivariant Borel-Moore homology $H_\bullet^{G_\mathcal{O}} ( \mathcal{R} )$ with convolution product. $\mathcal{R}$ is a space of triples of a $G$ principle bundle over the formal disk $\mathcal{P}$, a trivialization over the punctured formal disk $\phi$ and a section $s$ of $\mathcal{P} \times_G N$ with the restriction that $\phi (s)$ extends over the puncture.

By including $\mathbb{C}^*$ equivariance as well, this gives a non-commutative deformation. This gives a Poisson structure at the classical level.

#### Examples

* If $N=0$, this gives the Bezrukavnikov-Finkelberg-Mirkovic (BFM) space for the Langlands dual $^L G$.

## Related concepts

* [[symplectic duality]]

* [[fractional D-brane]], [[McKay correspondence]]


## References

### General

The terminology "Coulomb branch" and "[[Higgs branch]]" first appears in:

* {#SeibergWitten94} [[Nathan Seiberg]], [[Edward Witten]], _Monopoles, duality and chiral symmetry breaking in $N=2$ supersymmetric QCD_, Nucl.Phys. __B431__ (1994) 484--550 ([doi](https://doi.org/10.1016/0550-3213%2894%2990214-3) [arXiv:hep-th/9408099](https://arxiv.org/abs/hep-th/9408099))

The definition is summarized (specifically for [[super QCD]]) in [Assel-Cremoni 17, Section 2.1](#AsselCremoni17).

Relation to [[integrable systems]]:

* [[Ron Donagi]], [[Edward Witten]]: *Supersymmetric Yang-Mills Systems And Integrable Systems*, Nucl. Phys. B **460** (1996) 299-334 &lbrack;[arXiv:hep-th/9510101](https://arxiv.org/abs/hep-th/9510101), <a href="https://doi.org/10.1016/0550-3213(95)00609-5">doi:10.1016/0550-3213(95)00609-5</a>&rbrack;


Quick exposition of the basic idea includes

* {#Albertsson03} Cecilia Albertsson, around p. 31 of _Superconformal D-branes and moduli spaces_ ([arXiv:hep-th/0305188](https://arxiv.org/abs/hep-th/0305188))

Mathematical discussion in the case of [[D=3 N=4 super Yang-Mills theory]]:

* [[Hiraku Nakajima]], _Introduction to a provisional mathematical definition of Coulomb branches of 3-dimensional $\mathcal{N} = 4$ gauge theories_ ([arXiv:1706.05154](http://arxiv.org/abs/1706.05154))

* [[Hiraku Nakajima]], _Towards a mathematical definition of Coulomb branches of 3-dimensional $\mathcal{N} = 4$ gauge theories, I_ ([arXiv:1503.03676](https://arxiv.org/abs/1503.03676))

* [[Alexander Braverman]], [[Michael Finkelberg]], [[Hiraku Nakajima]], _Towards a mathematical definition of Coulomb branches of 3-dimensional $\mathcal{N} = 4$ gauge theories, II_, Adv. Theor. Math. Phys. __22__ (2018) 1071-1147 ([arXiv:1601.03586](http://arxiv.org/abs/1601.03586))

* [[Alexander Braverman]], [[Michael Finkelberg]], [[Hiraku Nakajima]], *Coulomb branches of 3d $\mathcal{N}=4$ quiver gauge theories and slices in the affine Grassmannian* (with appendices by Alexander Braverman, Michael Finkelberg, Joel Kamnitzer, Ryosuke Kodera, Hiraku Nakajima, Ben Webster, and Alex Weekes), Advances in Theoretical and Mathematical Physics __23__:1 (2019) ([arXiv:1604.03625](https://arxiv.org/abs/1604.03625))
  > (relation to the [[moduli space of Yang-Mills monopoles]])

* [[Ben Webster]], _Koszul duality between Higgs and Coulomb categories $\mathcal{O}$_, ([arXiv:1611.06541](https://arxiv.org/abs/1611.06541))

* Spencer Tamagni: *Coulomb Branches in 3d $\mathcal{N} = 4$ Revisited* &lbrack;[arXiv:2412.17904](https://arxiv.org/abs/2412.17904)&rbrack;


See also:

* [[Constantin Teleman]], _The role of Coulomb branches in 2D gauge theory_, ([arXiv:1801.10124](https://arxiv.org/abs/1801.10124))

* Justin Hilburn, Joel Kamnitzer, Alex Weekes, _BFN Springer Theory_, Commun. Math. Phys. __402__ (2023) 765--832 (2023) ([doi](https://doi.org/10.1007/s00220-023-04735-4) [arXiv:2004.14998](https://arxiv.org/abs/2004.14998))

* Zijun Zhou, *Virtual Coulomb branch and vertex function* ([arXiv:2107.06135](https://arxiv.org/abs/2107.06135))


On [[mirror symmetry]] between [[Higgs branches]]/[[Coulomb branches]] of [[D=3 N=4 super Yang-Mills theory]] (with emphasis of [[Hilbert schemes of points]]):

* [[Jan de Boer]], [[Kentaro Hori]], [[Hirosi Ooguri]], [[Yaron Oz]], _Mirror symmetry in three-dimensional gauge theories, quivers and D-branes_, Nucl. Phys. __B493__:101--147, 1997 ([arXiv:hep-th/9611063](https://arxiv.org/abs/hep-th/9611063))

* [[Alexander Braverman]], [[Michael Finkelberg]], [[Hiraku Nakajima]], _Line bundles over Coulomb branches_ ([arXiv:1805.11826](https://arxiv.org/abs/1805.11826))


### Singularities

Discussion of Coulomb branch [[singularities]]:

* [[Mathew Bullimore]], [[Tudor Dimofte]], [[Davide Gaiotto]], _The Coulomb branch of 3d $\mathcal{N}=4$ theories_, Commun. Math. Phys. (2017) 354: 671 ([arXiv:1503.04817](https://arxiv.org/abs/1503.04817))

  (relation to [[Nahm's equations]])

* {#AsselCremoni17} [[Benjamin Assel]], [[Stefano Cremonesi]], _The infrared physics of bad theories_, SciPost Phys. 3, 024 (2017) ([arXiv:1707.03403](https://arxiv.org/abs/1707.03403))


[[!redirects Coulomb branches]]

