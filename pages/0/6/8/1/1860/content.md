<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The path [[∞-groupoid]] $\Pi(X)$ of a [[generalized smooth space]] $X$ is a smooth version of the [[fundamental ∞-groupoid]] of $X$. Its [[coskeleton|truncations]] to lower categorical degree yield

* [[path groupoids]]

* [[path n-groupoids]].

## Definition 

One way to define a path [[∞-groupoid]] in terms of [[Kan complexes]] is to let 

$$
  \Delta_{SmoothSp} : \Delta \to SmoothSp
$$

be the canonical [[simplicial object|cosimplicial object]] in [[smooth spaces]] that sends the abstract $n$-[[simplex]] $\Delta[n]$ to the standard smooth $n$-simplex $\Delta^n \subset \mathbb{R}^n$.

As every cosimplicial object with values in a category with colimits this induces a notion of [[nerve and realization]].  The smooth [[nerve]] operation

$$
  N : SmoothSp \to SmoothSp^{\Delta^{op}}
$$

with values in [[smooth ∞-stacks]] given by

$$
 N(X) : U \mapsto SmoothSp(U \times \Delta^\bullet_{SmoothSp}, X)
  \,,
$$

where on the right we have a [[simplicial object]] in the category of [[smooth spaces]] regarded as a [[model structure on simplicial presheaves|model for]] a [[smooth ∞-stack]].

Notice that the [[Kan complex]] valued sheaf presented by this is given for instance by the simplicial sheaf

$$
 N(X) : U \mapsto Ex^\infty SmoothSp(U \times \Delta^\bullet_{SmoothSp}, X)
  \,,
$$

which can be thought of as having in degree $k$ _piecewise smooth_ $k$-dimensional paths.


## Connections 

Functors out of the [[path groupoid]] and [[path n-groupoid]] represent [[connection on a bundle|connections]] and higher connectios. Discussion of this for the path $\infty$-groupoid is [[schreiber:Differential Nonabelian Cohomology|here]].


## References 

A more detailed account is at 

* [[schreiber:path ∞-groupoid]]


[[!redirects  path infinity-groupoids]]
[[!redirects  path ∞-groupoid]]
[[!redirects  path ∞-groupoids]]