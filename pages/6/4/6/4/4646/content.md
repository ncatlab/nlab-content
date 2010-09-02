
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
     \hat \gamma(0) &\stackrel{\hat \gamma}{\to}& \hat \gamma(1)
     && \in & P
     \\
     && &&& \downarrow^{\mathrlap{p}}
     \\
     \gamma(0) &\stackrel{\gamma}{\to}& \gamma(1) 
     && \in & X
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

Of $P \to X$ is a _trivial bundle_ in that $P = X \times G$, then a connection on this is equivalently encoded in a [[Lie-algebra valued 1-form]]

$$
  A \in \Omega^1(X, \mathcal{g})
$$


on $X$.

In terms of this, parallel transport is a solution to a [[differential equation]].

For $\gamma : [0,1] \to X$ we have the pull-back 1-form $\gamma^* A \in \Omega^1([0,1])$. For $f \in C^\infty([0,1], G)$ a smooth function with values in the [[Lie group]] $G$, consider the differential equation

$$
  d f + \rho(f)_*(\gamma^*A) = 0
  \,,
$$

where $d f : T [0,1] \to T G$ is the differential of $f$ and where $\rho : G \times G \to G$ is the left [[action]] of $G$ on itself (i.e. just the multiplication on $G$) and $r(f)_* : T G \to T G$ its differential and using the defining identification $\mathfrak{g} \simeq T_e G$ we take $r(f)_*(A)$ to be the composite $T [0,1] \stackrel{\gamma^* A}{\to} \mathfrak{g} \hookrightarrow T G \stackrel{r(f)_*}{\to} T G$.

If $G$ is a [[matrix Lie group]] such as the [[orthogonal group]] $O(n)$ or the [[unitary group]] $U(n)$, then also its Lie algebra identifies with matrices, and we may write this simply as

$$
  d f + \gamma^*(A) \cdot f  = 0
  \,,
$$

where the dot is matrix multiplication.

By general results on [[differential equations]], this type of equation has a unique solution for each choice of value of $f(0)$.

**Definition** The parallel transport of $A \in \Omega^1(X,\mathfrak{g})$ along a path $\gamma : [0,1] \to X$ which we write

$$
  tra_A(\gamma) := P \exp(\int_{[0,1]} \gamma^* A) \in G
$$

is the value $f(1) \in G$ for the unique solution of the equation $d f  + \rho(f)_*(A) = 0$ with initial value $f(0) = e$ (the neutral element in $G$).


The notation here is motivated from the special case where $G = \mathbb{R}$ is the group of [[real number]]s. In that case the [[Lie algebra]] $\mathfrak{g} \simeq \mathbb{R}$ is abelian, the differential equation above is simply

$$
  d f = \gamma^*(A) \wedge f
$$

for a real valued function $f \in C^\infty([0,1])$, and the unique solution to that with $f(0) = e = 0$ is literally the exponential of the integral of $A$:

$$
  tra_A(\gamma) = \exp(\int_{[0,1]} \gamma^* A)
  \,.
$$

In the case of general nonabelian $\mathfrak{g}$ this simple exponential formula gives the wrong result. One can see that a slightly better approximation to the correct result is given by

$$
  \exp(\int_{[0,1/2]} \gamma^* A) \cdot \exp(\int_{[1/2,1]} \gamma^* A)
$$

and an even a bit more better approximation by

$$
  \exp(\int_{[0,1/3]} \gamma^* A) \cdot \exp(\int_{[1/3,2/3]} \gamma^* A)
   \cdot \exp(\int_{[2/3,1]} \gamma^* A)
$$

and so on, with the correct result being the limit of this sequence -- if one defines it carefully -- as we integrate piecewise over ever smaller pieces of the path.

This is called a **path-ordered integral**. The "P" in the above formula is short for "path ordering". Possibly this notation originates in [[physics]] where the above is known as the [[Dyson formula]]. 


