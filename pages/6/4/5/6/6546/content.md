
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ a [[space]] equipped with a $G$-[[connection on a bundle]] $\nabla$ (for some [[Lie group]] $G$) and for $x \in X$ any point, the [[parallel transport]] of $\nabla$ assigns to each [[curve]] $\Gamma : S^1 \to X$ in $X$ starting and ending at $x$ an element $ hol_\nabla(\gamma) \in  G$: the [[holonomy]] of $\nabla$ along that curve.

The **holonomy group** of $\nabla$ at $x$ is the subgroup of $G$ on these elements.

If $\nabla$ is the [[Levi-Civita connection]] on a [[Riemannian manifold]] and the holonomy group is a proper subgroup $H$ of the [[special orthogonal group]], one says that $(X,g)$ is a manifold of _[[special holonomy]]_ .

## Classification of holonomy groups of affine connections

Any [[closed Lie subgroup]] of $GL(V)$ occurs as the holonomy
group of some [[affine connection]] (with [[torsion]], in general).
See Hano–Ozeki \cite{HanoOzeki}.

Holonomy groups of locally symmetric connections can be classified using [[Élie Cartan]]'s [[classification of symmetric spaces]].

For [[Levi-Civita connections]], holonomy groups were classified by [[Marcel Berger]] \cite{Berger}.

The case of torsion-free [[affine connections]] that are not locally symmetric
and are not [[Levi-Civita connections]] was treated
by Merkulov and Schwachhöfer \cite{MerkulovSchwachhofer}.
A complete list of exotic holonomy groups (for the metric and nonmetric cases)
can be found in \cite{MerkulovSchwachhofer2}.

## Related concepts

* [[connection on a bundle]]

  * [[connection on a 2-bundle]], [[connection on an infinity-bundle]]

* [[parallel transport]], [[higher parallel transport]]

* [[holonomy]]

  * **holonomy group**

  * [[special holonomy]]

## References

* {#HanoOzeki} J. Hano, H. Ozeki, _On the holonomy groups of linear connections_, Nagoya Math. J. 10, 97-100 (1956).  [doi](https://doi.org/10.1017/S0027763000000106).

* {#Berger} [[Marcel Berger]], Sur les groupes d'holonomie homogènes de variétés à connexion affine et des variétés riemanniennes.  Bulletin de la Soci&#233;t&#233; math&#233;matique de France 79:null (1955), 279-330.  [doi](http://dx.doi.org/10.24033/bsmf.1464).

* {#MerkulovSchwachhofer} [[Sergei Merkulov]], Lorenz Schwachhöfer.  Classification of Irreducible Holonomies of Torsion-Free Affine Connections.  Annals of Mathematics 150:1 (1999), 77–149.  [doi](http://dx.doi.org/10.2307/121098).

* {#MerkulovSchwachhofer2} [[Sergei Merkulov]], Lorenz Schwachhöfer.  Addendum to Classification of Irreducible Holonomies of Torsion-Free Affine Connections.  Annals of Mathematics 150:3 (1999), 1177–1179.  [doi](http://dx.doi.org/10.2307/121067).

[[!redirects holonomy groups]]