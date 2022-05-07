## Definition

A __complete Hopf algebra__ is a [[complete augmented algebra]] $A$
equipped with a diagonal map $\Delta\colon A\to A\otimes A$
that is a morphism of [[complete augmented algebras]],
is coassociative and cocommutative
and has the [[augmentation map]] as a counit map.
(See the article [[Hopf algebra]] for a definition of these terms.)

## Examples

The completion of a [[Hopf algebra]] as
an [[augmented algebra]] (see [[complete augmented algebra]] for a construction)
is a complete Hopf algebra.

In particular, the completion of the [[group algebra]] of a [[group]]
and the [[universal enveloping algebra]] of a [[Lie algebra]] is a complete Hopf algebra.

## Properties

The [[monoidal product]] of the underlying [[complete augmented algebras]]
of complete Hopf algebras can be equipped in the obvious way
with a structure of a complete Hopf algebra.
The resulting [[monoidal structure]] $\hat\otimes$ on complete Hopf algebras
is the [[cartesian monoidal structure]],
with the projection maps $A\otimes A'\to A$ and $A\otimes A'\to A'$
induced by the [[augmentation maps]] of $A'$ respectively $A$.

The [[associated graded]] functor sends complete Hopf algebras
to graded [[Hopf algebras]].

## Constructions

The [[forgetful functor]] from the category of complete Hopf algebras
to the [[category of groups]]
sends a complete Hopf algebra $A$ to the [[group]]
$$G(A)=\{x\in 1+\bar A\mid \Delta x=x\hat\otimes x\}$$
of _group-like elements_ in $A$.
Its [[left adjoint functor]] sends a [[group]] to the completion
of its [[group algebra]].
(See Proposition A.2.5 in Quillen \cite{Quillen}.)

In the case $k=\mathbf{Q}$,
the forgetful functor is [[fully faithful]] and its [[essential image]]
comprises precisely [[Malcev groups]].
Thus, the category of rational complete Hopf algebras
is equivalent to the category of [[Malcev groups]].
(Theorem A.3.3 in Quillen \cite{Quillen}.)

The [[monad]] induced by the [[adjunction]] between
groups and complete Hopf algebras
is known as the [[Malcev completion]] of groups.

The [[forgetful functor]] from the category of complete Hopf algebras
to the [[category of Lie algebras]]
sends a complete Hopf algebra $A$ to the [[Lie algebra]]
$$P(A)=\{x\in \bar A\mid \Delta x=x\hat\otimes 1+1\hat\otimes x\}$$
of _primitive elements_ in $A$.
Its [[left adjoint functor]] sends a [[Lie algebra]] to the completion
of its [[universal enveloping algebra]].
(See Proposition A.2.5 in Quillen \cite{Quillen}.)

In the case $k$ has characteristic 0,
the forgetful functor is [[fully faithful]] and its [[essential image]]
comprises precisely [[Malcev Lie algebras]].
Thus, the category of complete Hopf algebras over a [[field]] of characteristic 0
is equivalent to the category of [[Malcev Lie algebras]] over the same [[field]].
(Theorem A.3.3 in Quillen \cite{Quillen}.)

## Properties in the case of zero characteristic

Assume that the [[field]] $k$ has [[characteristic]] 0.

Then the [[exponential]] map
$$\exp\colon P(A)\to G(A)$$
can be defined using [[formal power series]]
for any complete Hopf algebra $A$.

The exponential map is an isomorphism of sets,
both of which have natural filtrations induced from $A$,
which turn them into a complete [[filtered Lie algebra]] and a complete [[filtered group]] respectively.

The exponential map induces an isomorphism of the [[associated graded]] [[Lie algebra]] over [[integers]].
For the filtered [[group]] $G(A)$, the [[Lie bracket]] on its [[associated graded]] [[abelian group]] is given by the [[commutator]].
The [[associated graded]] [[abelian group]] of $G(A)$ is also equipped
with a structure of a $k$-[[module]] transferred from the [[associated graded]]
$k$-[[module]] of $P(A)$ via the exponential isomorphism.


## Related concepts

* [[augmented algebra]]

* [[complete augmented algebra]]

* [[Malcev group]]

* [[Malcev Lie algebra]]

* [[Malcev completion]]

## References

* [[Daniel Quillen]], _Rational homotopy theory_, Annals of Mathematics 90:2 (1969), 205.  [doi](http://dx.doi.org/10.2307/1970725).

[[!redirects complete Hopf algebras]]