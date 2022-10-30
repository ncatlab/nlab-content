
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

![A pic](http://upload.wikimedia.org/wikipedia/commons/b/b1/Monoid_mult.png)

and the **left and right unit laws**:

![A pic](http://upload.wikimedia.org/wikipedia/commons/1/10/Monoid_unit.png)

Here $\alpha$ is the [[associator]] in $C$, while $\lambda$ and $\rho$ are the left and right [[unitor|unitors]].

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