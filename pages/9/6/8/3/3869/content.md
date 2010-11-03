<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
</div>

If $T$ is a [[2-monad]] on a [[2-category]] $K$, then a **pseudoalgebra** for $T$ is a 2-dimensional version of an [[algebra over a monad]] which satisfies the laws only up to coherent isomorphism.

## Definition

A pseudo $T$-algebra is the same as a [[lax algebra for a 2-monad|lax algebra]] whose constraint 2-cells are invertible.

## Examples

...

## Normalization

A pseudoalgebra is said to be **normal** or **normalized** if its unit constraint isomorphism is an identity.

While making a pseudoalgebra strict is quite difficult, usually making it normal is quite easy, and many pseudoalgebras arising naturally are normal.  For instance, for the strict 2-monad $T$ whose strict algebras are strict monoidal categories and whose pseudoalgebras are unbiased non-strict monoidal categories, the unit constraint says that the "1-ary tensor product" $\otimes(x)$ is isomorphic to $x$ itself.  Clearly in most cases it is most sensible to *define* the 1-ary tensor product to *be* $x$, so that the pseudoalgebra is normal.

This situation is fairly general: if $T$ is a strict 2-monad for which the components of the unit $\eta_X \colon X\to T X$ are [[isocofibrations]], then any pseudoalgebra structure can be modified to a normalized one on the same underlying object.


## Coherence theorems

One way to state a coherence theorem is to say that every pseudoalgebra for a given 2-monad is equivalent to a strict one, perhaps in a structured way.  See [coherence theorems](/nlab/show/coherence+theorem#2monads).


[[!redirects pseudoalgebra for a 2-monad]]
[[!redirects pseudoalgebras for a 2-monad]]
[[!redirects pseudoalgebras for 2-monads]]
[[!redirects algebra for a 2-monad]]
[[!redirects algebras for a 2-monad]]
[[!redirects algebras for 2-monads]]
[[!redirects pseudoalgebra]]
[[!redirects pseudoalgebras]]
