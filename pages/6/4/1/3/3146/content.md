
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _curvature_ of a [[connection on a bundle]] measures how the connection is _locally_ non-trivial.

In as far as the notion of connection on a bundle is generalized by the notion of a cocycle in [[differential cohomology]], curvature is essentially the [[Chern character]].

In as far as cocycles in differential cohomology represent [[gauge field]]s in [[physics]], the curvature is the [[field strength]] of these gauge fields.

The term _curvature_ may be motivated from the special case of curvature of [[Levi-Civita connection]]s on a [[tangent bundle]] $T X$ of a [[Riemannian manifold]] $X$: here the connection manifestly encodes how the metric space $X$ is "bent" and the curvature of the connection is a measure for this. It generalizes the notion of [[Gaussian curvature]] of surfaces.

After the conception of [[gauge theory]], the term _curvature_ was firmly established in its generalization from this special case the case of connections on all kinds of bundles and [[principal infinity-bundle|higher bundles]].


## On trivial bundles

On a trivial bundle (and in particular locally, on every locally trivial bundle) a [[connection on a bundle|connection]] is given by [[differential form]] data. We describe the curvatures of these:

* A connection on a trivial [[line bundle]] on a [[space]] $X$ is just a [[differential forms|1-form]] 

  $$
    A \in \Omega^1(X)
    \,.
  $$ 

  The curvature in this case is the 2-form $F = d A$.

*  A connection on a trivial $G$-[[principal bundle]] for $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ is a $\mathfrak{g}$-valued 1-form (see [[groupoid of Lie-algebra valued forms]])
 
   $$
     A \in \Omega^1(X) \otimes \mathfrak{g}
     \,.
   $$

   Its curvature is the Lie-algebra valued 2-form

   $$
     F_A = d A + [A \wedge A]
     \,,
   $$

   where $[-,-]$ is the Lie bracket in $\mathfrak{g}$.

* According to the discussion at [[schreiber:theory of differential nonabelian cohomology]], a connection on a trivial [[principal ∞-bundle]] is given by a collection of [[schreiber:∞-Lie algebroid valued differential forms]]. The notion of curvature in this general context is discussed at [[schreiber:curvature of ∞-Lie algebroid valued differential forms]].