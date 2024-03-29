## Idea

The _derived dg-category_ of a [[dg-category]] is the [[dg-localization]] of the [[dg-category]] of [[dg-modules]] at the class of [[quasi-isomorphisms]]. The result is a [[pretriangulated dg-category]]. However an important caveat is that, even if the original [[dg-category]] is [[pretriangulated dg-category|pretriangulated]], it is strictly contained inside its derived dg-category.

Despite the terminology, the derived dg-category is not quite analogous to the [[derived category]] of an [[abelian category]]. Rather it should be thought of as the analogue of the [[simplicially enriched category]] of [[simplicial presheaves]], hence a presentation of the [[(infinity,1)-category of (infinity,1)-presheaves]].

## Definition

Let $T$ be a [[dg-category]].

+-- {: .num_defn}
###### Definition
The **derived dg-category** of $T$, denoted $D(T)$, is the [[dg-localization]] of the category of [[dg-modules]] over $T$ at the class of objectwise [[quasi-isomorphisms]]:
  $$ D(T) = dg-mod_T[qis^{-1}]. $$
=--

$D(T)$ can also be described as the [[dg-category]] [[dg-category presented by a dg-model category|presented]] by the projective [[dg-model structure on dg-modules]].

## Properties

+-- {: .num_lemma}
###### Lemma
The [[dg-category]] $D(T)$ is [[pretriangulated dg-category|pretriangulated]].
=--

+-- {: .num_lemma}
###### Lemma
There exists a fully faithful functor of [[dg-categories]]
  $$ T \hookrightarrow D(T) $$
called the [[dg-Yoneda embedding]].
=--

## Related concepts

* [[dg-module]]
* [[dg-Yoneda embedding]]
## References

* [[B. Toen]], _The homotopy theory of dg-categories and derived Morita theory_, [arXiv:math/0408337](http://arxiv.org/abs/math/0408337).

[[!redirects derived category of a dg-category]]

[[!redirects derived dg-category]]
[[!redirects derived dg-categories]]