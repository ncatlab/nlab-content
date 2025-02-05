# Lax algebras for a $2$-monad
* table of contents
{: toc}

## Idea

If $T$ is a [[2-monad]] on a [[2-category]] $\mathcal{K}$, then in addition to strict (if $T$ and $\mathcal{K}$ are strict) $T$-[[algebra for a monad|algebras]], which satisfy their laws strictly, and [[pseudoalgebra for a 2-monad|pseudo]] $T$-algebras, which satisfy laws up to isomorphism, one can consider also *lax* and *colax* algebras, which satisfy laws only up to a transformation in one direction or the other.


## Definition

If $T$ is a 2-monad on $\mathcal{K}$, a **lax $T$-algebra** in $\mathcal{K}$ consists of an object $A$, a morphism $T A \overset{a}{\to} A$, and (not necessarily invertible) 2-cells
$$\array{T^2A & \overset{T a}{\to} & T A\\
  ^m\downarrow & \Downarrow & \downarrow^a\\
  T A& \underset{a}{\to} & A}$$
and
$$\array{ A & & \overset{id}{\to} & & A\\
  & _i \searrow & \Downarrow & \nearrow_a \\
  & & T A}$$
satisfying suitable axioms.  (Here $m$ is the multiplication of $T$ and $i$ is the unit.)

Of course, in a **colax $T$-algebra** (also called an **oplax $T$-algebra**) the transformations go the other way.  The official way to remember which is lax and which is colax is that a lax $T$-algebra structure on $A$ is a [[lax morphism|lax M-morphism]] $T \to \langle A,A\rangle$, where $M$ is the 2-monad on the 2-category $[\mathcal{K},\mathcal{K}]$ of (some) endofunctors of $\mathcal{K}$ whose algebras are 2-monads, and $\langle A,A\rangle$ is the [[codensity monad]] of $A$, i.e. the right [[Kan extension]] of $1\overset{A}{\to} \mathcal{K}$ along itself.

If the transformations are invertible, then $A$ is a [[pseudoalgebra for a 2-monad|pseudo-algebra]].


## Related pages

* [[pseudoalgebra for a 2-monad]]

* [[lax monoidal category]]


[[!redirects lax algebra for a 2-monad]]
[[!redirects lax algebras for a 2-monad]]
[[!redirects lax algebras for 2-monads]]
[[!redirects lax algebra]]
[[!redirects lax algebras]]

[[!redirects colax algebra for a 2-monad]]
[[!redirects colax algebras for a 2-monad]]
[[!redirects colax algebras for 2-monads]]
[[!redirects colax algebra]]
[[!redirects colax algebras]]

[[!redirects oplax algebra for a 2-monad]]
[[!redirects oplax algebras for a 2-monad]]
[[!redirects oplax algebras for 2-monads]]
[[!redirects oplax algebra]]
[[!redirects oplax algebras]]
