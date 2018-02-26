
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

A comma double category is a generalization of a [[comma category]] to double categories. Unlike categories, more care is needed in what functors can be used: the comma double category $f/g$ can be constructed when $f : C \to E$ is an [[oplax functor]] $g : D \to E$ is a [[lax functor]] $g : D \to E$.

## Examples ##

1. A monad $T$ in the horizontal bicategory of a double category $C$ is equivalent to a lax functor $T : 1 \to C$ from the terminal double category. In this case we might call $Id_C / T$ the [[slice category|slice double category]].
2. The double category of [[decorated cospans]] is naturally constructed as a comma double category.
3. [[generalized multicategories]] can be constructed using a slice category when the monad $T$ is a [[polynomial monad]]. The slice over $T$ is equivalent to the "horizontal Kleisli category" presented in Crutwell-Shulman. $T$-multicategories are then monads there.
4. [[poset-valued sets]] given by an endofunctor $F$ on $Rel$ and a poset $P$ can be viewed as the comma double category from $F$ to $P$, since a poset is a monad in $Rel$.
