\tableofcontents

##Idea

A [[polytope]] is traditionally viewed as a generalization of the [[polygon]]: a rank $n$ polytope is constructed by "gluing together" rank $n-1$ polytopes, where the rank 1 polytope is the [[line segment]] with two rank 0 polytopes ([[point | points]]) glued on each end. Then we continue, gluing together line segments along their points to yield polygons, polygons along their edges to yield polyhedra ([[polyhedron | not to be confused with the algebraic topology concept with the same name]]), and so on. However, the details and implementation of this glue can widely vary. The concept of an "abstract polytope" boils down the core features of a polytope's data into an "incidence" [[poset]]. The exact details still often vary from author to author, but this article will cover a mainstream definition of abstract polytopes, but translated into the language of [[category | categories]]; a lot of the definitions become much nicer when we consider posets to simply be [[skeleton | skeletal]] [[(0,1)-category | (0,1)-categories]].

## Terminology

We wish to encode each sub-polytope as an object in our (0,1)-category, where $\operatorname{Hom}(A, B)$ is [[inhabited]] if $A$ is "incident" to $B$, i.e. entirely contained within $B$ in some sense. To that end, firstly, we require our (0,1)-category to have [[initial]] and [[terminal]] objects; the initial object is our "nullitope" which we take to be rank -1 and incident to every element, and the terminal object is our polytope itself, which every element is incident to. Then, we introduce the concept of a *rank*: a [[functor]] $r$ from our (0,1)-category to the (0,1)-category whose objects are ranks $-1, 0, \ldots, n$, where $n$ is the rank of our polytope. (Or [[dimension]], but rank is preferred terminology as lower rank polytopes are often embedded into higher dimensional spaces.) $r$ is required to satisfy the following property:

\begin{definition}
  \label{Definition 2.1} 
  A **ranking** $r: P \rightarrow \mathbb{Z}$ is a functor from a (0,1)-category $P$ to the (0,1)-category of the integers such that for all $a, b \in \operatorname{Obj}(P)$, when the [[interval]] $[a, b]$ is equivalent to the [[interval category]], then so is $[r(a), r(b)]$.
\end{definition}

The concept of an interval is very important for the following definitions as well. The next definition disallows constructions such as two pyramids kissing on a single vertex:

\begin{definition}
  \label{Definition 2.2} 
  A (0,1)-category $P$ with a ranking $r$ is **rank-wise strongly connected** if for all $a, b \in \operatorname{Obj}(P)$ such that $[a, b]$ is inhabited and $[r(a), r(b)]$ consists of at least 4 integers, $[a, b]$ with all initial and terminal objects removed is a [[connected category]].
\end{definition}

Finally, the following property is called the "diamond property" and enforces the idea that every line segment has two points (shares two points with the nullitope), every point and polygon share two line segments, every line segment and polyhedron share two polygons, etc.

\begin{definition}
  \label{Definition 2.3} 
  A (0,1)-category $P$ with a ranking $r$ satisfies the **diamond property** if for all $a, b \in \operatorname{Obj}(P)$ such that $[a, b]$ is inhabited and $[r(a), r(b)]$ consists of exactly 3 integers, $[a, b]$ is equivalent to the (0,1)-category that looks like a diamond, i.e. the product of two interval categories.
\end{definition}

## Definition and Examples

\begin{definition}
  \label{Definition 3.1}
  An **abstract polytope** is a rank-wise strongly connected (0,1)-category with initial and final objects which satisfies the diamond property.
\end{definition}

The [[subobject]] category of a [[set]] with $n+1$ elements is the abstract polytope representing the rank $n$ [[simplex]].

A polygon with 2 sides, i.e. the digon, may be encoded as a rank 2 abstract polytope, but may not be faithfully embedded into [[Euclidean space]]. However, it may be faithfully embedded onto the surface of a sphere.

## References

  * Polytope Wiki contributors. ["Abstract polytope"](https://polytope.miraheze.org/wiki/Abstract_polytope).