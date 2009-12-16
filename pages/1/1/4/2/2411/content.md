
> this is a sub-entry of [[A Survey of Elliptic Cohomology]], see there for background and context.

**definition**

$d$-dimensional Riemanninan field theories are symmetric monoidal functors $RCob_d \to TopVect$ from $d$-dimensional Riemannian bordisms to [[topological vector space]]s.

A field theory is very similar to a [[representation]] of a group. Only where a representation of a [[group]] $G$ is a functor from the [[delooping]] $\mathbf{B}G = {*}//G$ of $G$ to [[Vect]], an [[FQFT]] is a representation of a more complicated domain category.

**how does [[topology]] enter?**

for $X$ some [[topological space]] there is also a [[symmetric monoidal category]] 

$$
  RCob_d(X)
$$

of Riemannian bordisms equipped with a continuous map to $X$.

Notice that $d RRCob_d(X)$ does depend covariantly on $X$. This means that $Fun^\otimes(RCob_d(X), TopVect)$ is contravariant in $X$.

When special structure is around, however, we also have a push-forward of such functors along morphisms.

**Example: push-forward to the point**: for $X$ as above and $X \to {*}$ the unique map to the [[point]] heuristically we want a map

$$
  d RFT(X) \stackrel{p_*}{\to} d RFT(pt)
$$

notice that this push-forward is not an [[adjoint functor]]. Instead, it is a map that comes from integration over fibers. In particular it will change the degree of [[cohomology theory|cohomology theories]].

heuristically the pushforward

$$
    d RFT(X) \stackrel{p_*}{\to} d RFT(pt)
$$

acts on field theories $E_X$ over $X$ 

$$
  E_X \mapsto E
$$

by the assignment

$$
  E(Y^{d-1}) \mapsto 
  \Gamma\left(
  \array{
     E_X(Y)
     \\
     \downarrow
     \\
     Maps(Y,X)
  }
  regarded as a vector bundle
  \right)
$$

for instance when $E_X(Y) = \mathbb{C}$ then $E(Y) = \Gamma(Maps(Y,X);\mathbb{C})$. This is clearly reminiscent of the pushforward of a sheaf along a continuous functions and suggests that $d RFT(X)$ should be looked at as a sheaf on $X$. It is however not so, since if $X=X_1\cup X_2$ then an object $Y$ in $RCob_d(X)$ (i.e., a $(d-1)$-dimensional closed manifold with a map to $X$) cannot in general be reconstructed from $RCob_d(X_1)$ and $RCob_d(X_2)$. On the other hand, such a reconstruction is possible if one allows objects in $RCob_d(X_i)$ to have $(d-2)$-dimensional boundaries. This point of view leads to [[extended topological quantum field theory]].

