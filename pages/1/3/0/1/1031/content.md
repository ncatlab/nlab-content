#Definition#

In a [[category]] with a notion of [[zero morphism]], [[generalized the|the]] **kernel** $ker(f)$ of a [[morphism]] $f : c \to d$ is, if it exists, the [[equalizer]] of $f$ and the zero morphism $0_{c,d}$.  (By a 'notion of zero morphism', we really mean that the category is [[enriched category|enriched]] over [[pointed sets]].)

## As a pullback ##

In a category with a [[zero object]], the kernel can also be described as a [[pullback]]:
$$
  \array{
    ker(f)
    &\to&
    0
    \\
    \downarrow && \downarrow
    \\
    c &\stackrel{f}{\to}& d
  }
  \,.
$$
As $0$ is initial the map $0\to d$ in this diagram is unique.

This definition actually makes sense in any category with an [[initial object]], giving a more general notion.

## As a weighted limit ##

In any category enriched over pointed sets, the kernel of a morphism $f:c\to d$ is the universal morphism $k:a\to c$ such that $f \circ k$ is the basepoint.  It is a [[weighted limit]] in the sense of [[enriched category theory]].  This applies in particular in any (pre)-[[additive category]].

This is a special case of the construction of [[generalized kernels]] in enriched categories.


## In an $(\infty,1)$-category #

The kernel of a morphism in an [[(∞,1)-category]] with $\infty$-categorical [[zero object]] is the [[homotopy pullback]] of the above kind. 

See also [[stable (∞,1)-category]].

# Other meanings #

In some fields, the term 'kernel' refers to an [[equivalence relation]] that category theorists would see as a [[kernel pair]].  This is especially important in fields such as [[monoid]] theory where both notions exist but are not equivalent (while in [[group]] theory they are equivalent).

In [[ring]] theory, even when one assumes that rings have units preserved by ring homomorphisms, the traditional notion of kernel (an [[ideal]]) exists in the category of non-unital rings (and is not itself a unital ring in general).  A purely category-theoretic theory of unital rings can be recovered either by using the kernel pair instead or (to fit better the usual language) moving to a category of [[modules]].

In [[universal algebra]], this may be handled in the framework of [[Malcev variety|Mal?cev varieties]].

[[!redirects kernels]]