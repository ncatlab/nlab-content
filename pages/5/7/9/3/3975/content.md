#Contents#
* automatic table of contents goes here
{:toc}


## Idea

Just as a [[functor]] is a [[morphism]] between [[categories]], so a _closed functor_ is a morphism between [[closed categories]].  Like [[monoidal functors]], closed functors come in varying levels of strictness and strength.


## Definition

A __strict closed functor__ is a [[functor]] $F : C \to D$ between [[closed categories]] that preserves all the structure on the nose.  In particular, it must preserve the [[internal homs]] and the unit object:

$$ F(I_C) = I_D ,$$

$$ F([X,Y]) = [F(X),F(Y)].$$

but it should also preserve all of the additional structure transformations.

More commonly occurring in nature are functors that preserve the closed structure merely up to a transformation, which may perhaps be invertible.  Just as [[lax monoidal functors]] are often called simply "monoidal functors," the "lax" sort of closed functor for which the transformation is not invertible are often called simply *closed functors*, the ones where it is invertible being called *strong*.

To be precise: a **(lax) closed functor** between closed categories $C$ and $D$ is a functor $F\colon C\to D$ together with:

* A transformation $\hat{F}\colon F([X,Y]_C) \to [F(X),F(Y)]_D$, natural in $X$ and $Y$.

* A morphism $F^0\colon I_D \to F(I_C)$.

which satisfy the following axioms.

* The following diagram commutes for any $X$.
  $$\array{F(I_C) & \overset{F(j)}{\to} & F([X,X])\\
  ^{F^0}\uparrow && \downarrow^{\hat{F}}\\
  I_D & \underset{j}{\to} & [F(X),F(X)]}$$

* The following diagram commutes for any $X$.
  $$\array{F([I,X]) & \overset{\hat{F}}{\to} & [F(I),F(X)]\\
  ^{F(j)}\downarrow && \downarrow^{[F^0 ,1]}\\
  F(X) & \underset{j}{\to} & [I,F(X)]}$$

* The following diagram commutes for any $X,Y,Z$.
  $$\array{F([Y,Z]) & \overset{F(L)}{\to} & F([[X,Y],[X,Z]]) & \overset{\hat{F}}{\to} & [F([X,Y]),F([X,Z])]\\
  ^{\hat{F}}\downarrow &&&& \downarrow^{[1,\hat{F}]}\\
  [F(Y),F(Z)] & \underset{L}{\to} & [[F(X),F(Y)],[F(X),F(Z)]] & \underset{[\hat{F},1]}{\to} & [F([X,Y]),[F(X),F(Z)]]}$$

A **strong closed functor** is a closed functor such that $\hat{F}$ and $F^0$ are isomorphisms.

Together with [[closed natural transformations]], closed categories and closed functors form a [[2-category]].

## Examples

* Suppose that $C$ and $D$ are [[closed monoidal categories]].  Then any [[lax monoidal functor]] $F\colon C\to D$ gives rise to a lax closed functor by defining $F^0$ to be the unit constraint of $F$, and $\hat{F}\colon F([X,Y]) \to [F(X),F(Y)]$ to be the [[adjunct]] under the [[internal-hom]] adjunction of the composite
  $$ F([X,Y]) \otimes F(X) \to F([X,Y] \otimes X) \to F(Y). $$
  Conversely, from a lax closed functor between closed monoidal categories we can recover a lax monoidal functor, with multiplication constraint $F(X)\otimes F(Y) \to F(X\otimes Y)$ being adjunct to the composite
  $$ F(X) \to F([Y,X\otimes Y]) \to [F(Y), F(X\otimes Y)]$$
  where the map $X\to [Y,X\otimes Y]$ is adjunct to the identity of $X\otimes Y$.  In this way, lax monoidal and lax closed functors between closed monoidal categories are in bijective correspondence.  Note, however, that for such a functor to be *strong monoidal* or *strong closed* are generally independent conditions.

* The same idea works more generally for closed unital [[multicategories]], since arbitrary "multifunctors" between multicategories correspond to lax monoidal functors.

* However, there does not seem to be a natural notion of "colax" functor between closed categories.  One could, of course, simply ask for transformations in the other direction, but such things do not seem to arise much in practice, and would not correspond to colax monoidal functors in the same way.

## References

* Samuel Eilenberg and Max Kelly, _Closed categories._ Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).


[[!redirects closed functor]]
[[!redirects closed functors]]
