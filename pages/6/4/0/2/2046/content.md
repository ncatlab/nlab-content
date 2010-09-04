
# Contents
* automatic table of contents goes here
{:toc}


## Definition

An object $X$ in a category $C$ with a [[zero object]] $0$ is __simple__ if there are precisely two [[quotient objects]] of $X$: $0$ and $X$.  If $C$ is [[abelian category|abelian]], we may use [[subobjects]] in place of quotient objects in the definition, and this is more common; the result is the same.

Note that $0$ itself is *not* simple, as it has only *one* quotient object.  It is [[too simple to be simple]].

In [[constructive mathematics]], we want to phrase the definition as: a quotient object of $X$ is $X$ if and only if it is not $0$.

In an [[abelian category]] $C$, every [[morphism]] between simple objects is either a [[zero morphism]] or an [[isomorphism]]. If $C$ is also [[enriched category|enriched]] in finite-dimensional vector spaces over an [[algebraically closed field]], it follows that $\hom(X, Y)$ has dimension $0$ or $1$.


## Examples

*  In the category [[Vect]] of [[vector spaces]] over some field $k$, the simple objects are precisely the [[line]]s: the $1$-dimensional vector spaces, i.e. $k$ itself, up to [[isomorphism]].

*  A [[simple group]] is a simple of object in [[Grp]].  (Here it is important to use quotient objects instead of subobjects.)

*  For $G$ a [[group]] and $Rep(G)$ its category of [[representations]], the simple objects are the [[irreducible representations]].

*  A [[simple ring]] is *not* a simple object in [[Ring]] (which doesn\'t have a zero object anyway); instead it is a ring $R$ that is a simple in its category of [[bimodules]].

*  A [[simple Lie algebra]] is a simple object in [[LieAlg]] that *also* is not [[abelian Lie algebra|abelian]].  As an abelian Lie algebra is simply a [[vector space]], the only simple object of $Lie Alg$ that is not accepted as a simple Lie algebra is the $1$-dimensional Lie algebra.


## Related entries

* [[semisimple category]]

  * [[fusion category]]

  * [[modular tensor category]]


[[!redirects simple object]]
[[!redirects simple objects]]
[[!redirects simple module]]
[[!redirects simple modules]]
