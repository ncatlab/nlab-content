
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Fukaya category_ (named after [Fukaya 1993](#Fukaya93)) of a [[symplectic manifold]] $X$ is an [[A-∞ category]] having [[Lagrangian submanifolds]] of $X$ as objects. 

When two Lagrangian submanifolds $L_1$ and $L_2$ of $X$ meet
[[transversal maps|transversally]], their [[hom-space]] in the Fukaya category is roughly defined as the [[vector space]] [[linear span|spanned]] by the intersection points $x\in L_1\cap L_2$. 

One of the main difficulties in giving a rigorous
definition of the Fukaya category in general relies precisely in the problem of correctly defining the hom-spaces for nontransversal intersections. As one could expect, the same difficulty carries on to the definition of the multilinear operations in the Fukaya category: when
Lagrangians $L_1, L_2,\dots,L_{k+1}$ intersect transversally one has a clear geometric intuition of the multiplication
$$
  m_k 
    \,\colon\, 
  Hom(L_1,L_2)\otimes\cdots\otimes Hom(L_k,L_{k+1})
    \longrightarrow
  Hom(L_1,L_{k+1})
$$
in terms of counting pseudo-holomorphic disks into $X$ whose boundaries lie on the given Lagrangian submanifolds, but when intersections are nontransverse, the definition of $m_k$ becomes more elusive.

When defined, the Fukaya category is an [[A-infinity category|$A_\infty$-category]] which consitutes one side of the [[duality in string theory|duality]] of [[homological mirror symmetry]].

## In string theory

### A-Model topological string

In [[string theory]], the Fukaya category of a [[symplectic manifold]] $X$ represents the category of [[D-branes]] in the [[A-model]] -- the [[A-branes]] -- with [[target space]] $X$. For [[Landau-Ginzburg models]], the category of [[A-branes]] is described by [[Fukaya-Seidel categories]].

The assignment that sends a [[symplectic manifold]] to its Fukaya category extends to a [[functor]] on a variant of the [[symplectic category]] with [[Lagrangian correspondences]] as morphisms. This is supposed to be the [[FQFT]] incarnation of [[Donaldson theory]]. See at _[[Lagrangian correspondences and category-valued TFT]]_ for more on this and see at _[[homological mirror symmetry]]_.

### Yukawa couplings in intersecting D-brane models

In [[intersecting D-brane models]] Yukawa couplings are encoded by [[worldsheet instantons]] of open strings stretching between the [[brane intersection|intersecting]] [[D-branes]] (see [Marchesano 03, Section 7.5](#Marchesano03)). Mathematically this is encoded by  [[derived hom-spaces]] in a [[Fukaya category]] (see [Marchesano 03, Section 7.5](#Marchesano03)).


\begin{center}
<img src="https://ncatlab.org/nlab/files/YukawaFukaya.jpg" width="600">
\end{center}

> table grabbed from [Marchesano 03](#Marchesano03)


## Related concepts

* [[Weinstein symplectic category]]

* [[intersecting D-brane model]], [[Yukawa coupling]]


## References

Fukaya categories are named after:

* {#Fukaya93} [[Kenji Fukaya]], *Morse homotopy, $A_\infty$-category, and Floer homologies*, Proceedings of GARC Workshop on Geometry and Topology '93 (Seoul, 1993) &lbrack;[[Fukaya-MorseHomotopy.pdf:file]]&rbrack;

Monographs:

* [[Kenji Fukaya]], [[Yong-Geun Oh]], Hiroshi Ohta, Karo Ono, _Lagrangian intersection Floer theory - anomaly and obstruction_, Studies in Advanced Mathematocs **46**, AMS (2009)  &lbrack;[ISBN:978-0-8218-5253-8](https://bookstore.ams.org/amsip-46/)&rbrack;

* [[Paul Seidel]], *Fukaya categories and Picard-Lefschetz theory*, EMS (2008) &lbrack;[doi:10.4171/063](https://doi.org/10.4171/063)&rbrack;

Introduction:

* [[Denis Auroux]], *A beginner's introduction to Fukaya categories*, lectures at *Summer School on Contact and Symplectic Topology*,  Universit&#233; de Nantes (June 2011) &lbrack;[arXiv:1301.7056](https://arxiv.org/abs/1301.7056)&rbrack;

and with an eye towards [[mirror symmetry]]:

* Felipe Espreafico G. Ramos, *Mirror Symmetry and Fukaya Categories* (2020) &lbrack;[pdf](https://mathi.uni-heidelberg.de/~framos/Fukaya.pdf), [[Ramos-MirrorSymmetry.pdf:file]]&rbrack;

On the relation to [[Lagrangian cobordism]]:

* {#NadlerTannaka11} [[David Nadler]], [[Hiro Tannaka]], _A stable infinity-category of Lagrangian cobordisms_ ([arXiv:1109.4835](http://arxiv.org/abs/1109.4835))
  

Relation to [[Yukawa couplings]] in [[intersecting D-brane models]]:

* {#Marchesano03} [[Fernando Marchesano]], section 7.5 of _Intersecting D-brane Models_ &lbrack;[arXiv:hep-th/0307252](https://arxiv.org/abs/hep-th/0307252)&rbrack;

Towards a [[higher category theory|higher]] generalization:

* James Pascaleff, Nicolò Sibilla. *Speculations on higher Fukaya categories* (2025). ([arXiv:2503.20906](https://arxiv.org/abs/2503.20906)).

[[!redirects Fukaya categories]]
