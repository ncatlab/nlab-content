
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _clutching construction_ is the construction of a $G$-[[principal bundle]] on an [[n-sphere]] from a [[cocycle]] in $G$-[[Cech cohomology]] given by the [[covering]] of the $n$-sphere by two [[hemi-n-spheres]] that overlap a bit at the equator, and one single transition function on that equator $S^{n-1} \to G$.

More generally, if $X$ is a space and $C_+X,C_-X$ are
the two cones forming the [[suspension]] $\Sigma X$,
a map $X\to G$ (called then a *clutching map*)
provides a way to glue the trivial $G$-bundles on
$C_\pm X$ to obtain a $G$-bundle on $\Sigma X$.
To relate this construction with the [[classifying space|classification of $G$-bundles]]
on $\Sigma X$, we can start with a [[pointed topological space|pointed space]] $(X,x)$ and
require that the clutching map sends the basepoint $x$ to the identity $e\in G$.
In this case, the clutching construction is the map
\begin{equation}
  [X,G]_* \cong [\Sigma X,B G]_* \to [\Sigma X,B G] =
  \mathrm{Bun}_G(\Sigma X)
\end{equation}
sending pointed homotopy classes of pointed clutching functions to
$G$-bundles over $\Sigma X$.
By the path-connectedness of $B G$, the map is surjective, but the
map can fail to be injective if $G$ is not connected.
In general, the left hand side carries a trivialization of the fibre over the basepoint.

## Examples

### Basic examples

The [[Möbius strip]] is the result of the single non-trivial clutching construction for [[real vector bundles|real]] [[line bundle]] over the [[circle]].

The real plane bundles on the sphere $S^2$ come from clutching functions $S^1\to O(2)$. The pointed maps are $[S^1,O(2)]_*\cong\pi_1O(2)\cong\mathbb{Z}$ and the passage to the corresponding bundle
\begin{equation}
  \mathbb{Z} \cong [S^1,O(2)]_* \cong [S^2,BO(2)]_* \to [S^2,BO(2)] \cong \mathbb{N}
\end{equation}
identifies $n$ with $-n$.

### In physics

In [[physics]], in [[gauge theory]], the clutching construction plays a central role in the discussion of [[Yang-Mills instantons]], and [[monopoles]] ([[Dirac monopole]]). Here the discussion is usually given in terms of [[gauge fields]] on $n$-dimensional [[Minkowski spacetime]] such that they [[vanishing at infinity|vanish at infinity]]. Equivalently this means that one has [[gauge fields]] on the [[one-point compactification]] of Minkowski spacetime, which is the [[n-sphere]]. The transition function of the clutching construction then appears as the asymptotic [[gauge transformation]].

## Related concepts

* [[QCD instanton]], [[Yang-Mills instanton]]

## Literature

Review:

* [[Dale Husemöller]], chapter 7 of: _Fibre bundles_, Springer (1966, 1975 , 1994) &lbrack;[doi:10.1007/978-1-4757-2261-1](https://doi.org/10.1007/978-1-4757-2261-1), [pdf](https://link.springer.com/content/pdf/10.1007/978-1-4757-4008-0.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/husemoller), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/husemoller.pdf)&rbrack;

* [[Allen Hatcher]], page 22 of: _Vector bundles and K-theory_ ([web](http://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* {#Wirthmuller12} [[Klaus Wirthmüller]], p. 17-28 of: _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])

See also: 

* Wikipedia, _[Clutching construction](http://en.wikipedia.org/wiki/Clutching_construction)_


[[!redirects clutching constructions]]

[[!redirects clutching function]]
[[!redirects clutching functions]]
