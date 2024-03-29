
#Contents#
* table of contents
{:toc}

## Idea

Serre's intersection formula is a refinement of the [[intersection theory]] statement of [[Bézout's theorem]]. By replacing the plain [[tensor product]] of [[structure sheaves]] of intersecting subvarieties with the [[derived functor|derived]] tensor product -- the [[Tor]] -- it holds also when the subvarieties do not intersect transversally.

This may be understood as a first step towards formulating [[intersection theory]] properly in [[derived algebraic geometry]].

## Statement

Given a [[regular scheme]] $X$ and subschemes $Y,Z$ with defining ideal sheaves $\mathcal{I},\mathcal{J}$, respectively, the intersection multiplicity $m(x,Y,Z)$ at a generic point $x$ of (an irreducible component of) the intersection $Y\cap Z$ is given by the Serre intersection (or multiplicity) formula in terms of torsion groups:

$$
m(x,Y,Z) = \sum_{i\geq 0} (-1)^i length_{\mathcal{O}_{X,x}} Tor_i^{\mathcal{O}_{X,x}}
(\mathcal{O}_{X,x}/\mathcal{I}_x,\mathcal{O}_{X,x}/\mathcal{J}_x)
$$

The formula can be interpreted by the [[Hochschild homology]], or within the [[derived category of coherent sheaves]] on $X$. It has been one of the motivating results for the development of [[derived algebraic geometry]].

## References

* MathOverflow: [serre-intersection-formula-and-derived-algebraic-geometry](http://mathoverflow.net/questions/12236/serre-intersection-formula-and-derived-algebraic-geometry)

[[!redirects Serre multiplicity formula]]

[[!redirects Serre's intersection formula]]