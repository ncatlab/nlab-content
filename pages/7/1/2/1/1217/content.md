{:myundef: .un_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

[[Kuo Tsai Chen]] described several categories of [[generalized smooth space|generalised smooth spaces]] in his works (see also at _[[diffeological space]]_).
Four are reproduced below.

His initial motivation appears to be extending the theory of [[differential forms]] from finite-dimensional [[manifolds]] to [[path spaces]].

+-- {: myundef}
###### 1973

By a convex $n$-region (or, simply a _convex_ region), we mean a closed convex region in $\mathbb{R}^n$.  A convex $0$-region consists of a single point.

_Definition._ A differentiable space $X$ is a [[Hausdorff space]] equipped with a family of maps called plots which satisfy the following conditions:

1. Every plot is a continuous map of the type $\phi: U \to X$, where $U$ is a convex region.

2. If $U'$ is also a convex region (not necessarily of the same dimension as $U$) and if $\theta: U' \to U$ is a $C^\infty$-map, then $\phi\theta$ is also a plot.

3. Each map $\{0\} \to X$ is a plot.
=--

+-- {: myundef}
###### 1975

By a convex region we mean a closed convex set in $\mathbb{R}^n$ for some finite $n$.

__Definition.__  A predifferentiable space $X$ is a topological space equipped with a family of maps called plots which satisfy the following conditions:

1. Every plot is a continuous map of the type $\phi: U \to X$, where $U$ is a convex region.

2. If $U'$ is also a convex region (not necessarily of the same dimension as $U$) and if $\theta: U' \to U$ is a $C^\infty$-map, then $\phi\theta$ is also a plot.

3. Each map $\{0\} \to X$ is a plot.

__Remark.__ in [1973], a predifferentiable space is called a "differentiable space".
We propose to amend the definition of a differentiable space by adding the following condition:

4. Let $\phi: U\to X$ be a continuous map and let $\{\theta_i: U_i \to U\}$ be a family of $C^\infty$-maps, $U$, $U_i$ being convex regions, such that a function $f$ on $U$ is $C^\infty$ if and only if each $f\circ \theta_i$ is $C^\infty$ on $U_i$.
If each $\phi \circ \theta_i$ is a plot of $X$, then $\phi$ itself is a plot of $X$.
=--

+-- {: myundef}
###### 1977

  The symbols $U$, $U'$, $U_i$, ... will denote convex sets.
  All convex sets will be finite dimensional.
  They will serve as models, i.e. sets whose differentiable structure is known.

...

__Definition 1.2.1__ A differentiable space $M$ is a set equipped with a family of set maps called plots, which satisfy the following conditions:

1. Every plot is a map of the type $U\to M$, where $\dim U$ can be arbitrary.

2. If $\phi: U \to M$ is a plot and if $\theta: U' \to U$ is a $C^\infty$-map, then $\phi \circ \theta$ is a plot.

3. Every constant map from a convex set to $M$ is a plot.

4. Let $\phi: U\to M$ be a set map.
  If $\{U_i\}$ is an open covering of $U$ and if each restriction $\phi | U_i$ is a plot, then $\phi$ is itself a plot.
=--

##  Remarks 

* In 1986, Chen gave a definition equivalent to the last.
* It seems clear from the context that in the 1975 paper Chen was first recalling the definition from the 1973 paper.  However, his recollection was not completely accurate as the underlying object was now a [[topological space]] rather than a [[Hausdorff space]].
* The forcing condition on the maps in the 1975 paper is actually stronger than that in the 1977 paper.
* The final structure is of [[sheaf|sheaves]] on a [[site]].  This is the definition used in, for example, Baez and Hoffnung [0807.1704].

## Related notions

* [[diffeological space]]

## References 

* [Iterated integrals of differential forms and loop space homology](http://www.ams.org/mathscinet-getitem?mr=380859), 1973
* [Iterated integrals, fundamental groups and covering spaces](http://www.ams.org/mathscinet-getitem?mr=0377960), 1975
* [Iterated path integrals](http://www.ams.org/mathscinet-getitem?mr=0454968), 1975
* [On differentiable spaces](http://www.ams.org/mathscinet-getitem?mr=842915), 1986
* [Convenient Categories of Smooth Spaces](http://arxiv.org/abs/0807.1704v1), 0807.1704

[[!redirects Chen spaces]]