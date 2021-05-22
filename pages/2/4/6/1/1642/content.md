
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A semigroup is like a [[monoid]] where there might not be an [[identity element]].  

The term "semigroup" is standard, but _semi-monoid_ would be more systematic.

## Definition

A __semigroup__ is, equivalently,

*  a [[set]] equipped with an [[associativity|associative]] binary operation.  

*  an associative [[magma]];

*  the [[hom-set]] of a [[semicategory]] with a single object.


## Properties

Some semigroups happen to be [[monoid]]s; even then, a semigroup [[homomorphism]] might not be a monoid homomorphism (because it might not preserve the identity element).  Nevertheless, semigroup [[isomorphisms]] must be monoid isomorphisms.  Thus, the identity element of a monoid forms a [[property-like structure]] on the underlying semigroup.

This should be contrasted with the phenomenon that a semigroup homomorphism between two semigroups that happens to be [[group]]s does, in fact, happen to be a group homomorphism, since in this special case one can show a semigroup homomorphism must preserve the identity and inverses.

As a monoid is a [[category]] with one object, so a semigroup is a [[semicategory]] with one object.

Any [[small category]] $\mathcal{C}$ can be thought of as a semigroup by defining $S = \text{Mor}(\mathcal{C})\cup \{0\}$ and taking $f*g = f \circ g$ for any composable morphisms $f, g$, and $f*g = 0$ otherwise. Then the semigroup $(S, *)$ fully describes $\mathcal{C}$. This type of semigroup is a [[weakly reductive semigroup]].

Generalizing this, any [[category]] can be thought of as a semigroup which isn't necessarily defined on a set.


## Attitudes toward semigroups 

Some mathematicians consider semigroups to be a case of [[centipede mathematics]].  [[category theory|Category theorists]] sometimes look with scorn on semigroups, because unlike a monoid, a semigroup is not an example of a [[category]].    

However, a semigroup can be promoted to a monoid by adjoining a new element and decreeing it to be the identity.  This gives a [[fully faithful functor]] from the category of semigroups to the category of monoids.  So, a semigroup can actually be seen as a monoid with extra property.

+-- {: .un_example}
###### Exercise  

Describe this property. 
=--

On the other hand, analysts run across semigroups often in the wild, and don\'t always want to add formal identities just to turn them into monoids.

Another variant with strong links with category theory is that of [[inverse semigroups]], which [[Charles Ehresmann]] showed were closely related to [[ordered groupoid]]s. Inverse semigroups naturally occur when considering partial symmetries of an object.

## Examples

* The natural numbers with a binary operation $(-) +_n (-):\mathbb{N}\times\mathbb{N}\to\mathbb{N}$ inductively defined as $0 +_n 0 = n$, $S(x) +_n y = S(x +_n y)$, and $x +_n S(y) = S(x +_n y)$ for all $x,y:\mathbb{N}$ is a commutative semigroup for all $n:\mathbb{N}$. 

## Internalization 

We can [[internalization|internalize]] the concept of semigroup in any [[monoidal category]] (or even [[multicategory]]) $V$ to get a __semigroup object__ in $V$.

## Related topics

*  There is a strong connection between semigroups and finite automata; see e.g. [[Krohn-Rhodes theory]].

* [[inverse semigroups]]

* [[associative quasigroup]]

* [[cancellative semigroup]]

* [[weakly reductive semigroup]]

* [[semiring]]

* [[semi-category]], [[semi-simplicial set]], [[semi-Segal space]]

* [[rectangular band]]

## References

Semicategories and semigroups are mentioned for instance in section 2 in

* W. Dale Garraway, _Sheaves for an involutive quantaloid_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 4 (2005), p. 243-274  ([numdam](http://www.numdam.org/item?id=CTGDC_2005__46_4_243_0))


[[!redirects semigroup]]
[[!redirects semigroups]]
[[!redirects semigroup object]]
[[!redirects semigroup objects]]

[[!redirects semi-group]]
[[!redirects semi-groups]]
[[!redirects semi-monoid]]
[[!redirects semi-monoids]]
[[!redirects semimonoid]]
[[!redirects semimonoids]]

