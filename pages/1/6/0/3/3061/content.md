

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

##Idea

The **Atiyah Lie algebroid** associated to a $G$-[[principal bundle]] $P$ over $X$ is a [[Lie algebroid]] structure on the [[vector bundle]] $T P/ G$, the [[quotient]] of the [[tangent bundle]] of the total space $P$ by the canonical induced $G$-[[action]].

The [[Lie groupoid]] that the Atiyah Lie algebroid [[Lie integration|integrates to]] is the _[[Atiyah Lie groupoid]]_. See there for more background and discussion.

## Definition

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and let $P \to X$ be a $G$-[[principal bundle]]:

the **Atiyah Lie algebroid sequence** of $P$ is a sequence of [[Lie algebroid]]s

$$
  ad(P) \to at(P) \to T X
  \,,
$$

where 

* $ad(P) = P \times_G \mathfrak{g}$ is the [[adjoint bundle]] of Lie algebras, associated via the [[adjoint action]] of $G$ on its Lie algebra;

* $at(P) := (T P)/G$ is the **Atiyah Lie algebroid**

* $T X$ is the [[tangent Lie algebroid]] of $X$.

The [[Lie bracket]] on the sections of $at(P)$ is that inherited from the tangent Lie algebroid of $P$.

## Relation to connections

A splitting $\nabla_{flat} : T X \to at(P)$ of the Atiyah Lie algebroid sequence in the category of [[Lie algebroid]]s is precisely a flat [[connection on a bundle|connection on]] $P$.

To get non-flat connections in the literature one often sees discussed splittings of the Atiyah Lie algebroid sequence in the category just of [[vector bundle]]s. In that case one finds the curvature of the connection precisely as the [[obstruction]] to having a splitting even in Lie algebroids.

One can describe non-flat connections without leaving the context of Lie algebroids by passing to higher Lie algebroids, namely $L_\infty$-[[L-infinity-algebroid|algebroids]], in terms of an [[horizontal categorification]] of [[nonabelian Lie algebra cohomology]]:

## Atiyah class

The $Ext^1$-cohomology class corresponding to the Atiyah exact sequence (usually in a version for vector bundles/coherent sheaves) is the __Atiyah class__. 

## Related concepts

* [[Courant Lie 2-algebroid]]

## References

* [[Michael Atiyah]], _Complex analytic connections in fibre bundles_, Trans. Amer. Math. Soc. 85 (1957), 181--207, [doi](http://dx.doi.org/10.2307/1992969),[MR0086359](http://www.ams.org/mathscinet-getitem?mr=0086359) 
* Pietro Tortella, _Representations of Atiyah algebroids and logarithmic connections_, [arxiv/1505.04763](http://arxiv.org/abs/1505.04763)

A discussion with an emphasis on the relation to [[connection on a 2-bundle|2-connections]] and [[Lie 2-algebras]] is on the first pages of

* {#Stevenson06} [[Danny Stevenson]], *Lie 2-algebras and the geometry of gerbes*, Unni Namboodiri Lectures 2006 &lbrack;[pdf](http://math.ucr.edu/home/baez/namboodiri/stevenson_maclane.pdf), [[Stevenson-Lie2AlgebrasAndGerbes.pdf:file]]&rbrack;

For Atiyah classes see:
	
* [[Luc Illusie]], _Complexe cotangent et d&#233;formations_ (vol. 1) IV.2.3

* [MO:atiyah-class-for-non-locally-free-sheaf](http://mathoverflow.net/questions/56405/atiyah-class-for-non-locally-free-sheaf)

* [[M. Kapranov]], _Rozansky&#8211;Witten invariants via Atiyah classes_, Compositio Math. 115 (1999), 71&#8211;113.

* [[Ugo Bruzzo]], Igor Mencattini, [[Vladimir Rubtsov]], 
 _Nonabelian holomorphic Lie algebroid extensions_, Intern. J. Math. 26, No. 05, 1550040 (2015) [doi](https://doi.org/10.1142/S0129167X15500408) [arXiv:1305.2377](https://arxiv.org/abs/1305.2377)

* Zhuo Chen, Mathieu Sti&#233;non, Ping Xu, _From Atiyah classes to homotopy Leibniz algebras_, [arXiv/1204.1075](http://arxiv.org/abs/1204.1075); _A Hopf algebra associated to a Lie pair_, [arxiv/1409.6803](http://arxiv.org/abs/1409.6803)

* R. A. Mehta, M. Sti&#233;non, P. Xu, _The Atiyah class of a dg-vector bundle_, [arxiv/1502.03119](http://arxiv.org/abs/1502.03119)

* [[Nikita Markarian]], _The Atiyah class, Hochschild cohomology and the Riemann-Roch theorem_, J. Lond. Math. Soc. (2) 79 (2009), no. 1, 129--143 [doi](https://doi.org/10.1112/jlms/jdn064)

* F. Bottacin, _Atiyah classes for Lie algebroids_, [pdf](http://www.math.unipd.it/~bottacin/papers/liealgebroids.pdf)

* Ajay C. Ramadoss, _The big Chern classes and the Chern character_, Internat. J. Math. 19 (2008), no. 6, 699--746.

* [[Zhuo Chen]], [[Mathieu Stiénon]], [[Ping Xu]], _From Atiyah classes to homotopy Leibniz algebras_, Commun. Math. Phys. __341__ (2016) 309-349 &lbrack;[arXiv:1204.1075](https://arxiv.org/abs/1204.1075), [doi:10.1007/s00220-015-2494-6](https://doi.org/10.1007/s00220-015-2494-6)&rbrack;

* Stack Project 92.19 ([tag/09DF](https://stacks.math.columbia.edu/tag/09DF)) The Atiyah class of a sheaf of modules

[[!redirects Atiyah Lie algebroids]]
[[!redirects Atiyah algebroid]]
[[!redirects Atiyah algebroids]]
[[!redirects Atiyah class]]
[[!redirects Atiyah sequence]]