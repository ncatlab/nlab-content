## Definition

If $K$ is a [[bicategory]] and $f \colon a \to a$ is an [[endomorphism]] in $K$, then a (**left**) $f$-**algebra** or $f$-**module** is given by a 1-cell $x \colon b \to a$ together with a 2-cell $\lambda \colon f x \Rightarrow x$.

One can also define right modules/algebras, comodules/coalgebras and bimodules as for [[module over a monad|monads]].

## Examples

If $K$ is $Cat$, an [[algebra for an endofunctor]] $F \colon C \to C$ is the same thing as an $F$-algebra $A \colon \ast \to C$ in the sense above.

Every [[module over a monad]] $(t, \eta, \mu)$ is an algebra over the underlying endomorphism $t$.

An [[algebra for a profunctor]] (q.v.) $H \colon C &#8696; C$ on $X \colon D \to C$ is essentially the same as a $H$-coalgebra $D(1,X) \Rightarrow H \circ D(1,X)$ in $Prof$, the bicategory of categories and [[profunctors]].
