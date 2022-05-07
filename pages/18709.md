

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _sphere fiber bundle_ is a [[fiber bundle]] whose [[fibers]] are [[spheres]] $S^n$ of some [[dimension]] $n$.

Often, but not always, this is considered in [[homotopy theory]] or even in [[stable homotopy theory]], hence for [[fibers]] which have the ([[stable homotopy type|stable]]) [[homotopy type]] of a sphere, in which case one speaks of _[[spherical fibrations]]_. See there for more.

## Properties
 {#Properties}

\begin{prop}\label{StableTangentBundleOfUnitSphereBundle}
  The [[stable tangent bundle]] of a [[unit sphere bundle]] $S(\mathcal{V})$ in a [[real vector bundle]] $\mathcal{V} \overset{p}{\longrightarrow} M$ (Example \ref{UnitSphereBundles}) over a [[smooth manifold]] $M$ is [[isomorphism|isomorphic]] to the [[pullback bundle|pullback]]  of the [[direct sum of vector bundles|direct sum]] of the [[stable tangent bundle]] of the base manifold with that vector bundle:

$$
  T^{stab} S(\mathcal{V})
  \;
  \simeq
  \;
  S(p)^\ast
  \big(
    T^{stab} M 
    \oplus_M
    \mathcal{V}
  \big)
  \,.
$$
\end{prop}

(e.g. [Crowley-Escher 03, Fact. 3.1](#CrowleyEscher03), following [Milnor 56, p. 403](#Milnor1956))


## Examples

### Unit sphere bundles

\begin{example}\label{UnitSphereBundles}
A key example of sphere fiber bundles are the _unit sphere bundles_ inside of [[real vector bundles]] that are equipped with [[orthogonal structure]]: the bundles whose [[fibers]] are the [[unit spheres]] in the corresponding fiber of the given [[real vector bundle]].
\end{example}


These appear in the discussion of [[Thom spaces]] and hence of [[Thom spectra]], as well as in the discussion of [[wave front sets]].


## Related concepts

* [[Sullivan model of a spherical fibration]]

## References

With focus on [[3-sphere]]-fiber bundles over the [[4-sphere]] and the construction of [[exotic 7-spheres]]:

* {#Milnor1956} [[John Milnor]], _On manifolds homeomorphic to the 7-sphere_, Annals of Mathematics 64 (2): 399&#8211;405 (1956) ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/exotic.pdf), [doi:10.1142/9789812836878_0001](https://doi.org/10.1142/9789812836878_0001))

* {#CrowleyEscher03} Diarmuid Crowley, Chrstine Escher, _A classification of $S^3$-bundles over $S^4$_, Differential Geometry and its Applications
Volume 18, Issue 3, May 2003, Pages 363-380 (<a href="https://doi.org/10.1016/S0926-2245(03)00012-3">doi:10.1016/S0926-2245(03)00012-3</a>))


[[!redirects sphere fiber bundles]]

[[!redirects sphere bundle]]
[[!redirects sphere bundles]]


[[!redirects unit sphere fiber bundle]]
[[!redirects unit sphere fiber bundles]]


[[!redirects unit sphere bundle]]
[[!redirects unit sphere bundles]]
