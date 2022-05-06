
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Generalizing the classical notion of [[monoid]], one can define a _monoid_ (or _monoid object_) in any [[monoidal category]] $(C,\otimes,I)$.
Classical monoids are of course just monoids in [[Set]] with the [[cartesian product]].

By the [[microcosm principle]], in order to define monoid objects in $C$, $C$ itself must be a "categorified monoid" in some way.  The natural requirement is that it be a [[monoidal category]].  In fact, it suffices if $C$ is a [[multicategory]].  Contrast this with a [[group object]], which can only be defined in a [[cartesian monoidal category]] (or a [[cartesian multicategory]]).

## Definition

Namely, a **monoid in $C$** is an object $M$ equipped with a multiplication $\mu: M \otimes M \to M$ and a unit $\eta: I \to M$ satisfying the **associative law**:

$$
\array{
  & (M \otimes M) \otimes M
    & \stackrel{\alpha}{\longrightarrow}
  & M \otimes (M \otimes M)
    & \stackrel{\mu}{\longrightarrow}
  & M \otimes M
  \\
  & {}_{\mu}\searrow
    &&
    && \swarrow_{\mu}
  &
  \\
  &&
  M \otimes M
    & \stackrel{\mu}{\longrightarrow}
  M
  &&
}
$$

and the **left and right unit laws**:

$$
\array{
  & I \otimes M
  & \stackrel{\eta \otimes 1}{\longrightarrow}
  & M \otimes M
  & \stackrel{1 \otimes \eta}{\longleftarrow}
  & M \otimes I
  \\
  &
  & {}_{\lambda}\searrow
  & {}_{\mu}\downarrow
  & \swarrow_{\rho}
  &
  \\
  &
  &
  & M
  &
  &
}
$$

Here $\alpha$ is the [[associator]] in $C$, while $\lambda$ and $\rho$ are the left and right [[unitor|unitors]].

## Morphism of monoids

The analogue of a monoid homomorphism, called a morphism of monoids, is a morphism, $\f: M \to M'$  between two monoid objects, satisfying the equations;


$f \circ \mu = \mu' \circ (f \otimes f)$

$f \circ \eta = \eta'$

corresponding to the commutative diagrams;

$$
\array{
  & M \otimes M
  & \stackrel{f \otimes f}{\longrightarrow}
  & M' \otimes M'
  \\
  & {}_{\mu}\downarrow
  &
  & \downarrow_{\mu'}
  \\
  & M
  & \stackrel{f}{\longrightarrow}
  & M'
}
$$

$$
\array{
  & I
  & \stackrel{\eta}{\longrightarrow}
  & M
  \\
  &
  & {}_{\eta'}\searrow
  & \downarrow_{f}
  \\
  &
  &
  & M'
}
$$

## As categories with one object

Just as the category of regular [[monoid|monoids]] is equivalent to the category of locally small (i.e. Set-enriched) categories with one object, the category of monoids in $C$ (with the obvious morphisms) is equivalent to the category of $C$-[[enriched category|enriched categories]] with one object.

## Examples

A monoid in a [[category of modules]] is an [[associative unital algebra]].
A monoid in a [[endofunctor|category of endofunctors]] where tensor product is defined by composition, is a [[monad]].

## Related concepts

* [[monoid]]
* [[commutative monoid in a symmetric monoidal category]]
* [[module over a monoid]]
* [[category of monoids]]
* [[monoid in a monoidal (infinity,1)-category]]

## References

Categorical properties of [[monoid objects]] in [[monoidal categories]] are spelled out in sections 1.2 and 1.3 of

* Florian Marty, _Des Ouverts Zariski et des Morphismes Lisses en G&#233;om&#233;trie Relative_, Ph.D. Thesis, 2009, [web](http://thesesups.ups-tlse.fr/540/)

A summary is in section 4.1 of

* [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_, [arXiv:1410.1716](http://arxiv.org/abs/1410.1716).

See also [MO/180673](http://mathoverflow.net/questions/180673/category-of-modules-over-commutative-monoid-in-symmetric-monoidal-category).

[[!redirects monoids in a monoidal category]]
[[!redirects monoids in monoidal categories]]

[[!redirects monoid object in a monoidal category]]
[[!redirects monoid objects in a monoidal category]]
[[!redirects monoid objects in monoidal categories]]


[[!redirects monoid object]]
[[!redirects monoid objects]]
[[!redirects internal monoid]]
[[!redirects internal monoids]]

[[!redirects algebra object]]
[[!redirects algebra objects]]

