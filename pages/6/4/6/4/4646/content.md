
#Contents#
* table of contents
{:toc}

## Idea

A [[connection on a bundle]] $\nabla$ for $\pi : P \to X$ a $G$-[[principal bundle]] encodes data that allows to assigns to each path $\gamma : [0,1] \to X$ [[homomorphism]]s

$$
  tra_\nabla(\gamma) : P_{\gamma(0)} \to P_{\gamma(1)}
$$

between the [[fiber]]s of the bundle, such that this assignment depends well (e.g. smoothly) on the choice of path and is compatible with composition of paths.

This assignment is called the _parallel transport_ of the connection.

The term "parallel" comes from one of the many equivalent definitions of the notion of [[connection on a bundle]]: the original formulation of [[Ehresmann connection]]s.

In that formulation, the connection is encoded at each point $p \in P$ in the total space by a decomposition of the [[tangent space]] $T_p P$ as a [[direct sum]] $T_p P \simeq V_p \oplus H_p$ of [[vector space]]s, such that

* $V_p = \her \pi_*|_p$ is the [[kernel]] of the projection map that sends vectors in the total space to vectors in base space (this part is fixed by the choice of $p : P \to X$);

* $H_p \subset T_p P$ is a _choice_ of complement, such that this choice varies smoothly over $P$ in an evident sense and is compatible with the $G$-[[action]] on $P$.

The vectors in $V_p$ are called _vertical_ , the vectors in $H_p$ are called _horizontal_ . One may think of this as defining locally in which way the base space sits horizontally in the total space, equivalently as identifying locally a "smoothly varying local trivialization" of $P$.

More precisely, given such a choice of horizontal subspaces, there is for every path $\gamma : [0,1] \to X$ and every choice of lift $\hat \gamma(0) \in P$ of the start point $\gamma(0)$ to the total space of the bundle, a _unique lift_ $\hat \gamma : [0,1] \to P$ of the entire path to the total space:

$$
  \array{
     \hat \gamma(0) &\stackrel{hat \gamma}{\to}& \hat \gamma(1)
     && \in P
     \\
     && \downarrow^{\mathrlap{p}}
     \\
     \gamma(0) &\stackrel{\gamma}{\to}& \gamma(1) 
     && \in X
  }
  \,
$$

such that $\hat \gamma$ is everywhere _parallel_ (to $X$) in that all its tangent vectors sit in the horizontal subspaces choses:

$$
  (\partial_\sigma \hat \gamma)(\sigma) \in H_{\gamma(\sigma)} \subset T_{\gamma(\sigma)} P
  \,.
$$

In other words this means that given a path $\gamma$ down in $X$, we may _transport_ any point $p \in P_{\gamma(0)}$ above its start point _parallely_ (with respect to the notion of parallelism determined by $\nabla$) along $\gamma$, to find a uniquely determined point $tra_\nabla(\gamma)(p) \in P_{\gamma(1)}$ over the endpoint.

## Special cases

### Trivial bundle: parallel transport of a 1-form



(...)