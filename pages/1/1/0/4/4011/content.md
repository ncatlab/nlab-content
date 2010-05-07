## Introduction ##

This page is part of the collections of pages relating to the [[differential topology of mapping spaces]].  Here, we consider the linear situation.  That is, we consider mapping spaces of the form $C^\infty(N, E)$ where $N$ is a sequentially compact [[Frölicher space]] and $E$ is a [[convenient vector space]].  The reason for studying these is that such spaces are the model spaces for the more general mapping spaces.

The properties that we need to prove for these spaces are, essentially, inheritance properties.  These are:

1. $C^\infty(N,E)$ is a [[convenient vector space]].
2. If $U \subseteq E$ is a $0$-neighbourhood then $C^\infty(N,U)$ is a $0$-neighbourhood.
3. If $\phi \colon U \to V$ is a diffeomorphism of open subsets of $E$ then $C^\infty(N,\phi)$ is a diffeomorphism $C^\infty(N,U) \to C^\infty(N,V)$.

These properties are what is needed to propogate the manifold structure of the target to the mapping space.

## Structure ##

Let $E$ be a [[convenient vector space]] and let $N$ be a [[Frölicher space]] whose [[curvaceous topology]] is [[sequentially compact]].  As a convenient vector space is a special Fr&#246;licher space, and the category of Fr&#246;licher spaces is [[cartiesian closed]], the mapping space $C^\infty(N,E)$ is again a Fr&#246;licher space and is characterised by the fact that smooth maps $X \to C^\infty(N,E)$ correspond to smooth maps $X \times N \to E$ in the obvious way.
In particular, the smooth curves in $C^\infty(N,E)$ correspond to the smooth maps $\mathbb{R} \times N \to E$.

## Open Sets ##

The key property on the source is that it be [[sequentially compact]] (with the curvaceous topology).  The reason for this is to do with relating open sets in the target to open sets in the mapping space.

+-- {: .num_prop #PropLin}
###### Proposition ######
Let $N = (N, C_N, F_N)$ be a [[Frölicher space]] whose [[curvaceous topology]] is [[sequentially compact]].  Let $E$ be a [[convenient vector space]].  Let $U$ be a $0$-neighbourhood in $E$ in the $c^\infty$-topology.  Then the set

$$
C^\infty(N,U) \coloneqq \{f \colon N \to E : f(N) \subseteq U\}
$$

is a $0$-neighbourhood of $C^\infty(N,E)$ in the $c^\infty$-topology.
=--

+-- {: .proof}
###### Proof ######
The Fr&#246;licher space structure on $C^\infty(N,E)$ is such that  smooth maps $X \to C^\infty(N,E)$ correspond to smooth maps $X \times N \to E$.  Therefore, a smooth curve $c \colon \mathbb{R} \to C^\infty(N,E)$ corresponds to a smooth map $\hat{c} \colon \mathbb{R} \times N \to E$.

The $c^\infty$-topology is the [[curvaceous topology]].  In this topology, a set is open if its preimage under all smooth curves is open.  So to determine whether or not $C^\infty(N,U)$ is a $0$-neighbourhood, we need to examine $c^{-1}(C^\infty(N,U))$.  This is the set

$$
\{t \in \mathbb{R} : c(t)(N) \subseteq U\} = \{t \in \mathbb{R} : \hat{c}(t,x) \in U \forall x \in N\}
$$

Now $\hat{c} \colon \mathbb{R} \times N \to E$ is smooth and so $\hat{c}^{-1}(U)$ is open in $\mathbb{R} \times N$.  The relationship between $\hat{c}^{-1}(U)$ and $c^{-1}(C^\infty(N,U))$ is that $t \in c^{-1}(C^\infty(N,U))$ if and only if $\{t\} \times N \subseteq \hat{c}^{-1}(U)$.

Now we apply the sequential compactness of $N$ to deduce that as $\hat{c}^{-1}(U)$ is open, it contains a subset of the form $(-\epsilon,\epsilon) \times N$ for some $\epsilon \gt 0$.  Then $(-\epsilon,\epsilon) \subseteq c^{-1}(C^\infty(N,U))$ and so $c^{-1}(C^\infty(N,U))$ is a neighbourhood of $0$.

Thus as $c$ was a generic smooth curve, $C^\infty(N,U)$ is a $0$-neighbourhood in $C^\infty(N,E)$.
=--

This result can fail if $N$ is not sequentially compact, as shown by the simplest example: $N = E = \mathbb{R}$.  For this example, the topologies involved are all the "standard" ones.  In particular, the $0$-neighbourhoods in $C^\infty(\mathbb{R},\mathbb{R})$ are defined by uniform convergence on compact subsets of $\mathbb{R}$.  Hence the set $\{f \colon \mathbb{R} \to \mathbb{R} : \abs{f(t)} \lt 1\}$ is not a $0$-neighbourhood.

## Linear Structure ##



## Diffeomorphisms ##

