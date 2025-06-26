
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A [[connection on a bundle]] $\nabla$ for $\pi : P \to X$ a $G$-[[principal bundle]] encodes data that assigns to each path $\gamma : [0,1] \to X$ a [[homomorphism]]
$$tra_\nabla(\gamma) : P_{\gamma(0)} \to P_{\gamma(1)}$$
between the [[fiber|fibers]] of the bundle, such that this assignment depends well (e.g. smoothly) on the choice of path and is compatible with composition of paths.

This assignment is called the _parallel transport_ of the connection.


### The idea of parallelism

The term "parallel" comes from one of the many equivalent definitions of the notion of [[connection on a bundle]]: the original formulation of [[Ehresmann connection|Ehresmann connections]].

In that formulation, the connection is encoded at each point $p \in P$ in the total space by a decomposition of the [[tangent space]] $T_p P$ as a [[direct sum]] $T_p P \simeq V_p \oplus H_p$ of [[vector space|vector spaces]], such that

* $V_p = \ker \pi_*|_p$ is the [[kernel]] of the projection map that sends vectors in the total space to vectors in base space (this part is fixed by the choice of $p : P \to X$);

* $H_p \subset T_p P$ is a _choice_ of complement, such that this choice varies smoothly over $P$ in an evident sense and is compatible with the $G$-[[action]] on $P$.

The vectors in $V_p$ are called _vertical_ , the vectors in $H_p$ are called _horizontal_ . One may think of this as defining locally in which way the base space sits horizontally in the total space, equivalently as identifying locally a "smoothly varying local trivialization" of $P$.

More precisely, given such a choice of horizontal subspaces, there is for every path $\gamma : [0,1] \to X$ and every choice of lift $\hat \gamma(0) \in P$ of the start point $\gamma(0)$ to the total space of the bundle, a _unique lift_ $\hat \gamma : [0,1] \to P$ of the entire path to the total space:
$$
  \array{
     \hat \gamma(0) &\stackrel{\hat \gamma}{\to}& \hat \gamma(1)
     && \in & P
     \\
     && &&& \downarrow^{\mathrlap{\pi}}
     \\
     \gamma(0) &\stackrel{\gamma}{\to}& \gamma(1) 
     && \in & X
  }
  \,
$$
such that $\hat \gamma$ is everywhere _parallel_ (to $X$) in that all its tangent vectors sit in the horizontal subspaces chosen:
$$
  (\partial_\sigma \hat \gamma)(\sigma) \in H_{\gamma(\sigma)} \subset T_{\gamma(\sigma)} P
  \,.
$$

In other words, this means that given a path $\gamma$ down in $X$, we may _transport_ any point $p \in P_{\gamma(0)}$ above its start point _parallely_ (with respect to the notion of parallelism determined by $\nabla$) along $\gamma$, to find a uniquely determined point $tra_\nabla(\gamma)(p) \in P_{\gamma(1)}$ over the endpoint.

### Holonomic equivalence of curves

**Definition.**
Two curves with the same endpoints are __holonomically equivalent__ if for every principal $G$-bundle with connection, the holonomies along both curves coincide. 

This definition has many variants, depending on which curves are allowed (e.g., smooth, continuously differentiable, continuous, [[rough paths]]).

For continuously differentiable paths we have the following characterization, see Theorem 2.11 in [Bischoff–Lee](#BischoffLee) for an exposition and further references.

**Theorem.**
Suppose $x$ is a continuously differentiable path $[0,1]\to M$ in a smooth manifold $M$ with $x'(0)=0$, $x'(1)=0$.  The following conditions are equivalent.

* The [[holonomy]] of $x$ for every principal $G$-bundle with connection with a [[semi-simple Lie group|semi-simple structure group]] $G$ vanishes.

* There is a $C^1$ endpoint-preserving homotopy of rank at most 1 (a [[thin homotopy]]) that contracts $x$ to a point.

* There is a $C^1$ endpoint-preserving homotopy $h$ that contracts $x$ to a point such that $im h \subset im x$.

* The map $x$ factors through an $\mathbf{R}$-tree $T$, i.e., a metrizable space $T$ such that for every embeddings $a,b\colon[s,t]\to T$ such that $a(s)=b(s)$, $a(t)=b(t)$ we have $im a=im b$.

* There is a Lipschitz function $h\colon[0,1]\to[0,\infty)$ (a __height function__) such that $h(0)=h(1)$ and if $h(s)=h(t)=\inf h|_{[s,t]}, then $x(s)=x(t)$.

* The Chen path signature of $x$ is trivial.

* The path $x$ is word-reduced in the sense of Tlas [Theorem 1](#Tlas).


### The category-theoretic perspective

The parallel transport-assignment of fiber-homomorphisms to paths
$$
  (x \stackrel{\gamma}{\to} y) \mapsto ( P_x \stackrel{tra_\nabla(\gamma)}{\to} y ) 
$$
enjoys the following properties:

* it is invariant under [[thin homotopy]] of paths;

* it is compatible with composition of paths and sends constant paths to identity homomorphisms;

* it sends smooth families of paths to compatible smooth families of homomorphisms.

This may be equivalently but more succinctly be formulated as follows:

We say _diffeological groupoid_ for an [[internal groupoid]] in the category of [[diffeological space|diffeological spaces]]. 

The smooth paths in a smooth manifold $X$ naturally form the diffeological groupoid called the [[path groupoid]] $P_1(X)$.  Objects are points in $X$, morphisms are [[thin homotopy]]-classes of smooth paths which are constant in a neighbourhood of their boundary, composition is concatenation of paths.

For $P \to X$ any $G$-bundle, there is also naturally the diffeological groupoid $At(P)$ -- the [[Atiyah Lie groupoid]]  of $P$. Objects are points in $X$, morphisms are homomorphisms of $G$-[[torsor|torsors]] between the [[fiber|fibers]] over these points.

Then the above properties of parallel transport are equivalent to saying that we have an [[internal functor]]

$$
  tra : P_1(X) \to At(P)
$$

that is the identity on objects. Moreover, this functor _uniquely_ characterizes the [[connection on a bundle|connection]] on $P$ that it comes from. This means that we may identify connections on $P$ with their parallel transport functors. 


But even the bundle $P$ itself is encoded in such functors. If instead of looking at the category of internal groupoids and internal functors, we look at the larger [[2-topos]] of _diffeological stacks_  -- [[stack|stacks]] over [[CartSp]]. 

Then we can take simply the diffeological [[delooping]] groupoid $\mathbf{B}G$, which has a single object and $G$ as its [[hom-set]] and consider morphisms 
$$tra : P_1(X) \to \mathbf{B}G$$
in the 2-topos. These are now given by [[anafunctors]] of internal groupoids, and one finds that they encode a [[Cech cohomology|Cech cocycle]] for a $G$-principal bundle $P$ together with the parallel transport of a connection over it.

This is discussed in more detail at

* [[∞-Chern-Weil theory -- preparatory concepts]].

