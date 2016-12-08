# Located subspaces

* table of contents
{: toc}

## Idea

Help!  What is the idea?

## Definition

### In metric spaces

Given a [[metric space]] $X$, a [[subspace]] $S$ of $X$, and a [[point]] $x$ of $X$, we commonly define the __distance__ from $x$ to $S$ (or from $S$ to $x$) as an [[infimum]]:
$$ d(x,S) \coloneqq \inf_{y \in S} d(x,y) .$$
In [[constructive mathematics]], this infimum is generally an [[upper real number]], even if (as is usual) we require the distances $d(x,y)$ to always be a [[located real number]].

The subspace $S$ is __located__ (or __metrically located__ to be specific) if, for each point $x$, $d(x,S)$ is located.  (Although we are defining located subspaces in terms of located real numbers, this is backwards historically; the term was first used, by [[Jan Brouwer]], to refer to subsets.)

### In uniform spaces

If $X$ is a [[uniform space]], [Bridges et. al.](#BridgesAL) define a subspace $S$ to be **almost located** if for any entourage $U$, there is an entourage $V$ such that $\neg V[S] \cup U[S] = X$.  In other words, every point $x\in X$ is either within $U$ of some point of $S$ or not within $V$ of any point of $S$.

Since this seems the most natural notion of locatedness for uniform spaces, one might naturally also call such a subspace **uniformly located**.  However, note that even if $X$ is a metric space, metric locatedness is strictly stronger than uniform locatedness; Bridges et. al. give an example showing that metric locatedness is not a uniform invariant (while uniform locatedness is of course).

### In topological spaces

??

## Examples

### Singletons

Any singleton subset of a metric space, or more generally any finite subset, is metrically located, since we can take the minimum of any finite set.  A singleton subset of a uniform space is uniformly located if and only if the uniform space is [[regular space|regular]].

### Covert subsets

+-- {: .un_theorem}
###### Theorem
Suppose $X$ is a [[uniformly regular space|uniformly regular]] uniform space and that (the underlying set of) $S\subseteq X$ is a [[covert set]].  Then $S$ is uniformly located in $X$.
=--
+-- {: .proof}
###### Proof
Since $X$ is uniformly regular, for any entourage $U$ there is an entourage $V$ such that $\neg V \cup U = X\times X$.  In particular, for any $x\in X$, for any $y\in S$, we have either $(x,y)\in U$ or $(x,y)\notin V$.  By covertness of $S$, it follows that either $(x,y)\in U$ for some $y\in S$, or $(x,y)\notin V$ for all $y\in S$, which is to say that $x\in \neg V[S] \cup U[S]$.
=--

### Compact subspaces

+-- {: .un_theorem}
###### Theorem
Suppose $X$ is a [[uniformly regular space|uniformly regular]] uniform space and that $S\subseteq X$ is [[compact space|compact]] in its induced topology.  Then $S$ is uniformly located in $X$.
=--
+-- {: .proof}
###### Proof
Given any entourage $U$, let $V$ and $W$ be entourages such that $\neg V \cup U = X\times X$ (by uniform regularity) and $W\circ W\circ W \subseteq V$.  Let $G$ be the interior of $\neg W$.  Then $\neg V \subseteq G$, since if $(x,y)\notin V$ then $W[x] \times W[y]$ is a neighborhood of $(x,y)$ contained in $\neg W$ (for if $x \approx_W w \approx_W z \approx_W y$ then $(x,y)\in V$, which is not the case, hence $(w,z)\notin W$).  Thus, $G\cup U = X\times X$.

Let $i: X\times S \to X\times X$ be the inclusion and $\pi : X\times S \to X$ the projection.  Then $i^* G \cup i^* U = X\times S$.  Since $X$ is uniformly regular, it is regular.  Thus $S$ is compact regular, and hence locally compact, so the locale product $X\times S$ is spatial.  Therefore $\pi$ is both an [[open map]] and a [[proper map]] of [[locales]].  We then have $i^* G \cup \pi^* \pi_! i^* U = X\times S$, hence $\pi_*(i^* G \cup \pi^* \pi_! i^* U) = X$, and so by properness $\pi_* i^* G \cup \pi_! i^* U = X$ as well.  In other words, for every $x\in X$ either $(x,y)\in G$ for all $y\in S$, or there exists a $y\in S$ such that $(x,y)\in U$.  Since $G\subseteq \neg W$, it follows that $S$ is almost located.
=--
 


## References

* [[Douglas Bridges]], Hajime Ishihara, Ray Mines, [[Fred Richman]], Peter Schuster, and Lumini&#355;a V&#238;&#355;&#259;.  *Almost locatedness in uniform spaces*, Czechoslovak Mathematical Journal , Vol. 57 (2007), No. 1, 1&#8211;12, [web](http://dml.cz/dmlcz/128150)
 {#BridgesAL}

[[!redirects located set]]
[[!redirects located sets]]
[[!redirects located subset]]
[[!redirects located subsets]]
[[!redirects located subspace]]
[[!redirects located subspaces]]
[[!redirects metrically located set]]
[[!redirects metrically located sets]]
[[!redirects metrically located subset]]
[[!redirects metrically located subsets]]
[[!redirects metrically located subspace]]
[[!redirects metrically located subspaces]]
[[!redirects uniformly located set]]
[[!redirects uniformly located sets]]
[[!redirects uniformly located subset]]
[[!redirects uniformly located subsets]]
[[!redirects uniformly located subspace]]
[[!redirects uniformly located subspaces]]
[[!redirects topologically located set]]
[[!redirects topologically located sets]]
[[!redirects topologically located subset]]
[[!redirects topologically located subsets]]
[[!redirects topologically located subspace]]
[[!redirects topologically located subspaces]]
[[!redirects almost located set]]
[[!redirects almost located sets]]
[[!redirects almost located subset]]
[[!redirects almost located subsets]]
[[!redirects almost located subspace]]
[[!redirects almost located subspaces]]
