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

#Contents#
* table of contents
{:toc}

## Idea

*Kervaire-Milnor groups* are the [[oriented]] [[h-cobordism]] classes of [[homotopy spheres]] with the [[connected sum]] as composition and the reverse [[orientation]] as inversion. It controls the existence of [[smooth structures]] on [[topological manifold|topological]] and [[PL manifold|piecewise linear (PL) manifolds]]. The analogue concept controlling the existence of [[PL manifold|PL structures]] on [[topological manifold|topological]] is the [[Kirby-Siebenmann invariant]].

## Definition

An important property of [[spheres]] is their neutrality with respect to the [[connected sum]] of manifolds. Expanding this [[monoid]] structure with a [[composition]] and a [[neutral element]] to a [[group]] structure requires the restriction on manifolds, for which a connected sum can result in a sphere, hence which intuitively doesn't have holes. This is possible with [[homotopy spheres]], which are closed smooth manifolds with the same [[homotopy type]] as a sphere, with restriction to [[h-cobordism]] classes being useful for application. Inversion is then given by changing their orientation, which results in a group structure.

An alternative definition in five and more dimensions is given by the description of topological, PL and smooth structures. Let $Top_n$ be the [[topological group]] of [[homeomorphisms]], $PL_n$ the [[topological group]] of [[PL homeomorphisms]] and $Diff_n$ be the [[topological group]] of [[diffeomorphisms]] of [[euclidean space]] $\mathbb{R}^n$. There are canonical inclusions $Diff_n\hookrightarrow PL_n\hookrightarrow Top_n$. Taking the [[cartesian product]] with the [[identity]] furthermore gives inclusions $Top_n\hookrightarrow Top_{n+1}$, $PL_n\hookrightarrow PL_{n+1}$ and $Diff_n\hookrightarrow Diff_{n+1}$. An [[inductive limit]] yields topological groups:
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
($Diff$ is [[homotopy equivalent]] to the infinite [[orthogonal group]] $O(\infty)$). There are induced canonical inclusions $Diff\hookrightarrow PL\hookrightarrow Top$. Their [[classifying spaces]] can be now be regarded to study the different structures: For a [[topological manifold]] $X$, its [[tangent bundle]] $TX$ is also a [[topological manifold]], which is classified by a continuous map $X\rightarrow BTop$. Analogous for a PL and a smooth manifold, there are classifying maps $X\rightarrow BPL$ and $X\rightarrow BDiff$, respectively. The canonical inclusions $BDiff\hookrightarrow BPL\hookrightarrow BTop$ show that every smooth is a PL and every PL is a topological structure.

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
All Kervaire-Milnor groups are finite.
\end{proposition}

[[Michel Kervaire]] and [[John Milnor]] already proved this in their original paper for $n\neq 3$ with the remaining case $n=3$ being solved by the proof of the [[Poincaré conjecture]] by [[Grigori Perelman]].

\begin{proposition}
$\Theta_1$, $\Theta_3$, $\Theta_5$ and $\Theta_61$ are the only trivial Kervaire–Milnor groups in odd dimensions.
\end{proposition}

## References

See also:

* Wikipedia, _[Kervaire–Milnor group](https://en.wikipedia.org/wiki/Kervaire–Milnor_group)_

[[!redirects Kervaire-Milnor groups]]
[[!redirects KM group]]
[[!redirects KM groups]]