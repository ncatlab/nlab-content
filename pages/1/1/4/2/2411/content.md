

> this is a sub-entry of [[A Survey of Elliptic Cohomology]], see there for background and context.

**definition**

$d$-dimensional Riemanninan field theories are symmetric monoidal functors $d-RB \to TV$ from $d$-dimensional Riemannian bordisms to [[topological vector space]]s.

A field theory is very similar to a [[representation]] of a group. Only where a representation of a [[group]] $G$ is a functor from the [[delooping]] $\mathbf{B}G = {*}//G$ of $G$ to [[Vect]], an [[FQFT]] is a representation of a more complicated domain category.

**how does [[topology]] enter?**

for $X$ some [[topological space]] there is also a [[symmetric monoidal category]] 

$$
  d-RB(X)
$$

of Riemannian bordisms equipped with a continuous map to $X$.

Notice that $d RB(X)$ does depend covariantly on $X$. This means that Fun^\otimes(d RB(X), TV)$ is contravariant in $X$.

When special structure is around, however, we also have a push-forward of such functors along morphisms.

**Example: push-forward to the point**: for $X$ as above and $X \to {*}$ the unique map to the [[point]] heuristically we want a map

$$
  d RFT(X) \stackrel{p_*}{\to} d RFT(pt)
$$

notice that this push-forward is not an [[adjoint functor]]. Instead, it is a maap that comes from integration over fibers. In particular it will change the degree of [[cohomology theory|cohomology theories]].

heuristically the pushforward

$$
    d RFT(X) \stackrel{p_*}{\to} d RFT(pt)
$$

acts on field theories $E_X$ over $X$ 

$$
  $E_X \mapst E$
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

for instance when $E_X(Y) = \mathbb{C}$ then $E(Y) = \Gamma(Maps(Y,X))$.

