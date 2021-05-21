
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
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
    & \stackrel{1 \otimes \mu}{\longrightarrow}
  & M \otimes M
  \\
  & {}_{\mu \otimes 1}\searrow
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


## Properties

### Preservation by lax monoidal functors

Monoid structure is preserved by [[lax monoidal functor]]s. Comonoid structure by [[oplax monoidal functor]]s. See there for more.

### Category of monoids

For special properties of categories of monoids, see [[category of monoids]].


## Examples

* A monoid object in [[Ab]] (with the usual tensor product of $\mathbb{Z}$-modules as the tensor product) is a [[ring]].
 A monoid object in the category of vector spaces over a field $k$ (with the usual tensor product of vector spaces) is an [[algebra]] over $k$.
* A monoid in a [[category of modules]] is an [[associative unital algebra]].
* A monoid object in [[Top]] (with cartesian product as the tensor product) is a [[topological monoid]].
* A monoid object in [[Ho(Top)]] is an [[H-monoid]].
* A monoid object in the category of monoids (with cartesian product as the tensor product) is a [[commutative monoid]].  This is a version of the [[Eckmann-Hilton argument]].
* A monoid object in the category of complete join-[[semilattice]]s (with its tensor product that represents maps preserving joins in each variable separately) is a unital [[quantale]].
* Given any monoidal category $C$, a monoid in the monoidal category $C^{op}$ is called a [[comonoid]] in $C$.
* In a [[cocartesian monoidal category]], every object is a monoid object in a unique way.
* For any category $C$, the [[endofunctor]] category $C^C$ has a monoidal structure induced by composition of endofunctors, and a monoid object in $C^C$ is a [[monad]] on $C$.

These are examples of monoids internal to monoidal categories.  More generally, given any [[bicategory]] $B$ and a chosen object $a$, the [[hom-category]] $B(a,a)$ has the structure of a monoidal category.  So, the concept of monoid makes sense in any [[bicategory]] $B$: we define a **monoid in $B$** to be a monoid in $B(a,a)$ for some object $a \in B$.  This often called a [[monad]] in $B$.  The reason is that a monad in [[Cat]] is the same as monad on a category.

A monoid in a bicategory $B$ may also be described as the [[hom-object]] of a $B$-[[enriched category]] with a single object. 


## Related concepts

* [[monoid]]
* [[commutative monoid in a symmetric monoidal category]]
* [[module over a monoid]]
* [[category of monoids]]
* [[monoid in a monoidal (infinity,1)-category]]

## References


* [[Saunders MacLane]], Section III.6 in: _[[Categories for the Working Mathematician]]_, Springer (1971) 

* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], p. 7 in: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))


* Florian Marty, Dections 1.2, 1.3 in: _Des Ouverts Zariski et des Morphismes Lisses en G&#233;om&#233;trie Relative_, Ph.D. Thesis, 2009 ([web](http://thesesups.ups-tlse.fr/540/))

* [[Martin Brandenburg]], Section 4.1 of: _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](http://arxiv.org/abs/1410.1716))

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

