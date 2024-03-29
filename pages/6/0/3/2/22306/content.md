## Definition

A __complete augmented algebra__ over a [[field]] $k$ is an [[augmented algebra]] $R$ over $k$ equipped with a decreasing [[filtration]] of two-sided [[ideals]]
$$R=F_0 R\supset F_1 R\supset F_2 R \supset \cdots,$$
where $1\in F_0 R$ and $F_p R \cdot F_q R \subset F_{p+q} R$,
and, furthermore,
the map $F_1 R\to F_0 R$ is the [[augmentation ideal]], i.e., the [[kernel]] of the [[augmentation]] map $R\to k$,
the [[associated graded algebra]] of $R$ is generated by its degree $1$ component,
and the [[filtration]] is complete, i.e., the canonical map
$$R\to lim_n F_n R$$
is an [[isomorphism]].

A __morphism of complete augmented algebras__ is a morphism of [[augmented algebras]] that is also a morphism of [[filtered algebras]].

## Examples

The [[forgetful functor]] from complete augmented algebras to [[augmented algebras]]
admits a [[left adjoint functor]], which sends an [[augmented algebra]] $B$
to the complete augmented algebra $\hat B=lim_n B/I^n$,
where $I$ is the [[augmentation ideal]] of $B$.

In particular, for any set $I$, the algebra $k\langle\langle x_i\rangle\rangle_{i\in I}$ of [[noncommutative formal power series]] in variables $x_i$ ($i\in I$)
is a complete augmented algebra, since it is the completion of the algebra
of noncommutative polynomials in the same variables.
Such algebras are precisely the [[projective objects]]
in the category of complete augmented algebras.
(Corollary A.1.9 in [Quillen](#Quillen).)

The [[quotient]] $R/J$ of a complete augmentation algebra $R$ by a closed ideal $J$
such that the [[augmentation map]] vanishes on $J$
is again a complete augmented algebra.

## Properties

Any complete augmented algebra is a [[quotient]] of the algebra of [[noncommutative formal power series]] by a closed [[ideal]].
The quotient map can be chosen to induce an isomorphism of [[associated graded algebras]] in degree 1.
(Corollary A.1.7 in [Quillen](#Quillen).)

A morphism of complete augmented algebras is an [[effective epimorphism]]
if and only if it is surjective,
equivalently, the degree 1 component of its associated graded is surjective.
(Proposition A.1.8 in [Quillen](#Quillen).)

The category of complete augmented algebras admits [[small limits]]
and has a [[projective generator]], namely, $k\langle\langle x\rangle\rangle$.
(Proposition A.1.10 in [Quillen](#Quillen).)

## Constructions

The [[forgetful functor]] from the category of complete augmented algebras
to the [[category of groups]] that sends a complete augmented algebra $R$ to the [[group]] $1+\bar R$, where $\bar R$ denotes the [[augmentation ideal]] of $R$,
admits a [[left adjoint functor]],
which sends a group $G$ to the completion of its [[group algebra]].

The [[forgetful functor]] from the category of complete augmented algebras
to the [[category of Lie algebras]] that sends a complete augmented algebra $R$ to the [[Lie algebra]] $\bar R$ with [[Lie bracket]] $[x,y]=xy-yx$, where $\bar R$ denotes the [[augmentation ideal]] of $R$,
admits a [[left adjoint functor]],
which sends a [[Lie algebra]] $\mathfrak{g}$ to the completion of its [[universal enveloping algebra]].

See (1.12) in [Quillen](#Quillen).

## Monoidal structure

The category of complete augmented algebras admits a [[symmetric monoidal structure]],
given by the completion of the tensor product of the underlying filtered vector spaces.

The [[associated graded]] functor is a [[strong monoidal functor]]
from the category of complete augmented algebras to the category
of graded algebras.

The monoidal product has a universal property:
morphisms $R\otimes R'\to S$ are in a natural bijection
with pairs of morphisms $R\to S$ and $R'\to S$ whose images in $S$ commute.

## Related concepts

* [[augmented algebra]]

* [[complete Hopf algebra]]

* [[Malcev group]]

* [[Malcev completion]]

## References

* {#Quillen} [[Daniel Quillen]], _Rational homotopy theory_, Annals of Mathematics 90:2 (1969), 205.  [doi](http://dx.doi.org/10.2307/1970725).

[[!redirects complete augmented algebras]]