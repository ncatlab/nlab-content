
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given two [[vector bundles]] $E_1 \to X_1$ and $E_2 \to X_2$, then their _external tensor product_ $E_1 \boxtimes E_2 \to X_1 \times X_2$ is the [[tensor product of vector bundles]] on the [[product]] [[space]] $X_1 \times X_2$ of the two [[pullback bundles]] to this space, along the canonical [[projection]] maps $pr_i \colon X_1 \times X_2 \to X_i $.

More abstractly, this is the [[external tensor product]] in the [[indexed monoidal category]] of [[vector bundles]] indexed over suitable [[spaces]].

## Definition

Let $X_1$ and $X_2$ be [[topological spaces]] and let $E_1 \to X_1$ and $E_2 \to X_2$ be [[topological vector bundles]]. 

The [[product topological space]] $X_1 \times X_2$ comes with two [[continuous function|continuous]] [[projection]] functions

$$
  X_1 \overset{pr_1}{\longleftarrow} X_1 \times X_2 \overset{pr_2}{\longrightarrow} X_2
  \,.
$$


This gives rise to the [[pullback bundles]] $pr_1^\ast E_1 \to X_1 \times X_2$ and $pr_2^\ast E_2 \to X_1 \times X_2$. 

The _external tensor product_ $E_1 \boxtimes E_2$ is the [[tensor product of vector bundles]] of these pullback bundles:

$$
  E_1 \boxtimes E_2 \coloneqq (pr_1^\ast E_1) \otimes_{X_1 \times X_2} (pr_2^\ast E_2)
$$

which is again naturally a vector bundle over th product space

$$
  E_1 \boxtimes E_2 \longrightarrow X_1 \times X_2
  \,.
$$

## Properties

+-- {: .num_prop #ExternalProductTheoremIntopologicalKTheory}
###### Proposition
**([[external product theorem]] in [[topological K-theory]])**

For $X$ a [[compact Hausdorff space]] then the external tensor product of vector bundles over $X$ and over the [[2-sphere]] $S^2$ is an [[isomorphism]] of [[topological K-theory]] rings:

$$
  K(X) \otimes K(S^2) \overset{\simeq}{\longrightarrow} K(X \times S^2)
  \,.
$$

=--



## Related entries

* [[external direct sum of vector bundles]]

* [[direct sum of vector bundles]], [[inner product on vector bundles]]

* [[fundamental product theorem in topological K-theory]]

## References
 {#References}

The notion of external tensor product of vector bundles originates in discussion of [[topological K-theory]]:

*  {#Atiyah67}  [[Michael Atiyah]], §2.6 in: *K-theory*, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

* [[Raoul Bott]], p. 19 of: *Lectures on $K(X)$*, Benjamin (1969) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/bottk.pdf), [[Bott-KTheory.pdf:file]]&rbrack;

* {#Switzer75} [[Robert Switzer]], Rem. 13.51 in *Algebraic Topology -- Homotopy and Homology*, Grundlehren **212** Springer (1975) &lbrack;[doi:10.1007/978-3-642-61923-6_12](https://doi.org/10.1007/978-3-642-61923-6_12)&rbrack;


* {#Karoubi} [[Max Karoubi]], §4.9 in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften **226**, Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007/978-3-540-79890-3](https://doi.org/10.1007/978-3-540-79890-3)&rbrack;

* {#Wirthmuller12} [[Klaus Wirthmüller]], p. 40 of: *Vector bundles and K-theory* (2012) &lbrack;[[wirthmueller-vector-bundles-and-k-theory.pdf:file]]&rbrack;



It is also briefly mentioned in a context of [[differential geometry]] in: 

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], p. 84 of: *[[Connections, Curvature, and Cohomology]]* Volume 1: _De Rham Cohomology of Manifolds and Vector Bundles_, Academic Press (1973) &lbrack;[ISBN:978-0-12-302701-6](https://www.elsevier.com/books/connections-curvature-and-cohomology-v1/greub/978-0-12-302701-6)&rbrack;


Discussion in the context of the [[K-theory classification of topological phases of matter]]:

* [[Bruno Mera]], *The product of two independent Su-Schrieffer-Heeger chains yields a two-dimensional Chern insulator*, Phys. Rev. B **102** 155150 (2020) &lbrack;[arXiv:2009.02268](https://arxiv.org/abs/2009.02268), [doi:10.1103/PhysRevB.102.155150](https://doi.org/10.1103/PhysRevB.102.155150)&rbrack;


Discussion in the variant of categories of [[quasicoherent sheaves]]  in ([[derived algebraic geometry|derived]]) [[algebraic geometry]]: 

* {#BondalvdBerg03} [[Alexei Bondal]], [[Michel Van den Bergh]], _Generators and representability of functors in commutative and noncommutative geometry_, Mosc. Math. J. **3** 1 (2003) 1-36 &lbrack;[arXiv:math/0204218](https://arxiv.org/abs/math/0204218)&rbrack;

* {#BFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_, J. Amer. Math. Soc. **23** 4 (2010) 909-966 &lbrack;[arXiv:0805.0157](http://arxiv.org/abs/0805.0157)&rbrack;



[[!redirects external tensor products of vector bundles]]
