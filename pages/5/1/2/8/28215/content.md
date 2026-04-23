+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


\tableofcontents

## Idea

*Kervaire-Milnor groups* are the [[oriented]] [[h-cobordism]] [[equivalence classes|classes]] of [[homotopy spheres]] with the [[connected sum]] as [[group]] [[binary operation|operation]] and the reverse [[orientation]] as inversion. It controls the existence of [[smooth structures]] on [[topological manifolds]] and [[PL manifold|piecewise linear (PL) manifolds]]. The analogue concept controlling the existence of [[PL manifold|PL structures]] on [[topological manifold|topological]] is the *[[Kirby-Siebenmann invariant]]*.

## Definition

An important property of [[spheres]] is their neutrality with respect to the [[connected sum]] of [[manifolds]]. Expanding this [[monoid]] structure with a [[composition]] and a [[neutral element]] to a [[group]] [[structure]] requires the restriction on manifolds, for which a connected sum can result in a sphere, hence which intuitively doesn't have holes. This is possible with [[homotopy spheres]], which are [[closed manifold|closed]] [[smooth manifolds]] with the same [[homotopy type]] as a sphere, with restriction to [[h-cobordism]] classes being useful for application. Inversion is then given by changing their [[orientation]], which results in a group structure.

An alternative definition in five and more dimensions is given by the description of topological, PL and smooth structures. Let $Top_n\coloneqq C^0(\mathbb{R}^n,\mathbb{R}^n)$ be the [[topological group]] of [[homeomorphisms]] ([[homeomorphism group]]), $PL_n$ the [[topological group]] of [[PL homeomorphisms]] and $Diff_n\coloneqq C^\infty(\mathbb{R}^n,\mathbb{R}^n)$ be the [[topological group]] of [[diffeomorphisms]] ([[diffeomorphism group]]) of [[Euclidean space]] $\mathbb{R}^n$. There are canonical inclusions $Diff_n\hookrightarrow PL_n\hookrightarrow Top_n$. Taking the [[cartesian product]] with the [[identity]] furthermore gives inclusions $Top_n\hookrightarrow Top_{n+1}$, $PL_n\hookrightarrow PL_{n+1}$ and $Diff_n\hookrightarrow Diff_{n+1}$. An [[inductive limit]] yields [[topological groups]]:
$$
Top
\coloneqq\lim_{n\rightarrow\infty}Top_n;
$$
$$
PL
\coloneqq\lim_{n\rightarrow\infty}PL_n;
$$
$$
Diff
\coloneqq\lim_{n\rightarrow\infty}Diff_n.
$$
([[diffeomorphism group|$Diff$]] is [[homotopy equivalent]] to the infinite [[orthogonal group]] $O(\infty)$). There are induced canonical inclusions $Diff\hookrightarrow PL\hookrightarrow Top$. Their [[classifying spaces]] can be now be regarded to study the different structures: For a [[topological manifold]] $X$, its [[tangent bundle]] $TX$ is also a [[topological manifold]], which is classified by a continuous map $X\rightarrow BTop$. Analogous for a PL and a smooth manifold, there are classifying maps $X\rightarrow BPL$ and $X\rightarrow BDiff$, respectively. The canonical inclusions $BDiff\hookrightarrow BPL\hookrightarrow BTop$ show that every smooth is a PL and every PL is a topological structure.

The Kervaire–Milnor groups are then alternatively given by the [[homotopy groups]] of the [[quotient groups]] $PL/Diff$ and $Top/Diff$:
$$
\Theta_n
\cong\pi_n\left(PL/Diff\right)
\cong\pi_n\left(Top/Diff\right)
$$
for $n\geq 5$. (The [[quotient group]] $PL/Top$ is an [[Eilenberg-MacLane space]] $K(\mathbb{Z}_2,3)$ and its single non-trivial [[homotopy group]] leads to the [[Kirby-Siebenmann invariant]].)

## Examples

* $\Theta_1\cong\Theta_2\cong\Theta_3\cong\Theta_4\cong\Theta_5\cong\Theta_6\cong 1$

* $\Theta_7\cong\mathbb{Z}_{28}$

* $\Theta_8\cong\mathbb{Z}_2$

* $\Theta_9\cong\mathbb{Z}_2^2$

* $\Theta_{10}\cong\mathbb{Z}_6$

* $\Theta_{11}\cong\mathbb{Z}_{992}$

* $\Theta_{14}\cong\mathbb{Z}_2$

* $\Theta_{16}\cong\mathbb{Z}_2$

* $\Theta_{61}\cong 1$

## Properties

\begin{proposition}
All Kervaire-Milnor groups are [[finite group|finite]].
\end{proposition}
This was shown for $n\neq 3$ by [Kervaire & Milnor 1963](#KervaireMilnor1963), with the remaining case $n=3$ being solved by the proof of the [[Poincaré conjecture]] by [Perelman 2002](Poincaré+conjecture#Perelman02), [03a](Poincaré+conjecture#Perelman03a), [03b](Poincaré+conjecture#Perelman03b).

\begin{proposition}
$\Theta_1$, $\Theta_3$, $\Theta_5$ and $\Theta_61$ are the only trivial Kervaire–Milnor groups in odd dimensions.
\end{proposition}

## References

Named after the original discussion in:

* {#KervaireMilnor1963} [[Michel A. Kervaire]], [[John W. Milnor]]: *Groups of Homotopy Spheres I*, Annals of Mathematics **77** 3 (1963) &lbrack;[doi:10.2307/1970128](https://doi.org/10.2307/1970128), [jstor:1970128](https://www.jstor.org/stable/1970128),  [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/kervmiln.pdf)&rbrack;

Further descriptions:

* {#FreedUhlenbeck91} [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#Lück01} [[Wolfgang Lück]], _A Basic Introduction to Surgery Theory_ (2001) &lbrack;[pdf](https://math.uchicago.edu/~shmuel/tom-readings/Luck%20Surgery%20book.pdf)&rbrack;

* {#WangXu17} [[Guozhen Wang]], [[Zhouli Xu]], _The triviality of the 61-stem in the stable homotopy groups of spheres_, Annals of Mathematics **186**, No. 2, 2017, pp. 501–580 &lbrack;[arXiv:1601.02184](https://arxiv.org/abs/1601.02184) [10.4007/annals.2017.186.2.3](https://annals.math.princeton.edu/2017/186-2/p03)&rbrack;

See also:

* Wikipedia: _[Kervaire–Milnor group](https://en.wikipedia.org/wiki/Kervaire–Milnor_group)_

[[!redirects Kervaire-Milnor groups]]
[[!redirects KM group]]
[[!redirects KM groups]]