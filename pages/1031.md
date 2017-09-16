#Definition#

In a [[category]] with [[zero object]] [[generalized the|the]] **kernel** $ker(f)$ of a [[morphism]] $f : c \to d$ is, if it exists, the [[equalizer]] of $f$ and the [[zero morphism]] from $c$ to $d$.

This is the same as the [[pullback]] of the [[zero object]] along $f$:

$$
  \array{
    ker(f)
    &\to&
    0
    \\
    \downarrow && \downarrow
    \\
    c &\to& d
  }
  \,.
$$

More generally, in a category [[enriched category|enriched]] over [[pointed set]]s (with [[smash product]]), the kernel of a morphism $f:c\to d$ is the universal morphism $k:a\to c$ such that $f k$ is the basepoint.  It is a [[weighted limit]] in the sense of enriched category theory.  This applies in particular in any [[additive category]].


# Kernel in $\infty$-categories #

Accordingly, the kernel of a morphism in an [[infinity-category]] with $\infty$-categorical [[zero object]] is the [[homotopy pullback]] of the above kind. 

See also [[stable (infinity,1)-category]].
