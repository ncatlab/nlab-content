
\tableofcontents

## Idea

*[[polytope|Polytopes]]* are traditionally viewed as a generalization of [[polygons]]: a rank $n$ polytope is constructed by "gluing together" rank $n-1$ polytopes, where the rank 1 polytope is the [[line segment]] with two rank 0 polytopes ([[point|points]]) glued on each end. Then we continue, gluing together line segments along their end-points to yield *polygons*, polygons along their [[edges]] to yield *polyhedra* (not to be confused with the concept in [[algebraic topology]] of the
[[polyhedron|same name]]), and so on. 

However, the details and implementation of this glueing process can widely vary. The concept of "abstract polytopes" is meant to capture the core features of polytope data into an "incidence" [[poset]]. The exact details still often vary from author to author, but this article will cover a mainstream definition of abstract polytopes, translated into the language of [[category theory]]; a lot of the definitions become much nicer when we consider [[posets]] to simply be [[skeleton|skeletal]] [[(0,1)-categories]].

## Terminology

We wish to encode each sub-polytope as an [[object]] in our [[(0,1)-category]], where the [[hom-set]] $\operatorname{Hom}(A, B)$ is [[inhabited]] if $A$ is "incident" to $B$, i.e. entirely contained within $B$ in some sense. To that end, firstly, we require our (0,1)-category to have [[initial object|initial]] and [[terminal objects]]; the initial object is our "nullitope" which we take to be rank -1 and incident to every element, and the terminal object is our polytope itself, which every element is incident to. Then, we introduce the concept of a *rank*: a [[functor]] $r$ from our (0,1)-category to the (0,1)-category whose objects are ranks $-1, 0, \ldots, n$. (Also called *[[dimensions]]*, but *rank* is preferred terminology as lower rank polytopes are often embedded into higher dimensional spaces.) Here $r$ is required to satisfy the following property:

\begin{definition}
  \label{Ranking} 
  A **ranking** $r \colon P \rightarrow \mathbb{Z}$ is a [[functor]] from a [[(0,1)-category]] $P$ to the (0,1)-category of the [[integers]] such that for all $a, b \in \operatorname{Obj}(P)$, when the [[interval]] $[a, b]$ is equivalent to the [[interval category]], then so is $[r(a), r(b)]$.
\end{definition}

The concept of an interval is very important for the following definitions as well. The next definition disallows constructions such as two pyramids kissing on a single vertex:

\begin{definition}
  \label{RankwiseStronglyConnected} 
  A (0,1)-category $P$ with a ranking $r$ (Def. \ref{Ranking}) is **rank-wise strongly connected** if for all $a, b \in \operatorname{Obj}(P)$ such that $[a, b]$ is inhabited and $[r(a), r(b)]$ consists of at least 4 integers, $[a, b]$ with all initial and terminal objects removed is a [[connected category]].
\end{definition}

Finally, the following property, called the "diamond property", enforces the idea that every line segment has two end-points (shares two points with the nullitope), every point and polygon share two line segments, every line segment and polyhedron share two polygons, etc.

\begin{definition}
  \label{DiamondProperty} 
  A (0,1)-category $P$ with a ranking $r$ satisfies the **diamond property** if for all $a, b \in \operatorname{Obj}(P)$ such that $[a, b]$ is inhabited and $[r(a), r(b)]$ consists of exactly 3 integers, $[a, b]$ is equivalent to the (0,1)-category that looks like a diamond, i.e. the [[product category|product]] of two interval categories.
\end{definition}

## Definition and Examples

\begin{definition}
  \label{AbstractPolytope}
  An **abstract polytope** is a rank-wise strongly connected [[(0,1)-category]] (Def. \ref{RankwiseStronglyConnected}) with [[initial object|initial]] and [[terminal objects]] which satisfies the diamond property (Def. \ref{DiamondProperty}).
\end{definition}

The [[subobject]] category of a [[set]] with $n+1$ elements is the abstract polytope representing the rank $n$ [[simplex]].

A polygon with 2 sides, i.e. the digon, may be encoded as a rank 2 abstract polytope, but may not be faithfully embedded into [[Euclidean space]]. However, it may be faithfully embedded onto the surface of a sphere.

## References

  * Polytope Wiki: *[Abstract polytope](https://polytope.miraheze.org/wiki/Abstract_polytope)*

[[!redirects abstract polytopes]]


