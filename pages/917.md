
#Contents#
* table of contents
{:toc}

## Definition

A [[function]] $f$ from $A$ to $B$ is __injective__ if $x = y$ whenever $f(x) = f(y)$.  An injective function is also called __one-to-one__ or an __injection__; it is the same as a [[monomorphism]] in [[Set|the category of sets]].

A _[[bijection]]_ is a function that is both injective and [[surjection|surjective]].

In [[constructive mathematics]], a [[strongly extensional function]] between sets equipped with tight [[apartness relation]]s is called __strongly injective__ if $f(x) \ne f(y)$ whenever $x \ne y$ (which implies that the function is injective).  This is the same as a [[regular monomorphism]] in the category of such sets and strongly extensional functions (while any merely injective function, if strongly extensional, is still a monomorphism).  Some authors use 'one-to-one' for an injective function as defined above and reserve 'injective' for the stronger notion.

## In abstract categories
Since an element $a$ in a set $A$ in the [[category of sets]] is just a [[global element]] $a:1\rightarrow A$, one could define injections in any abstract category $\mathcal{C}$ with a [[terminal object]] $1$:

> A morphism $f:A\rightarrow B$ in $\mathcal{C}$ is an injection if, given any two global elements $x, y:1\rightarrow A$, $x = y$ if $f \circ x = f \circ y$. 

Every [[monomorphism]] is an injection as defined above in a category $\mathcal{C}$ with a terminal object $1$, since it is a morphism $f:A\rightarrow B$ such that given any set $C$ and two parallel morphisms $x, y:C\rightarrow A$, $x = y$ if $f \circ x = f \circ y$. The special case $C = 1$ yields an injection.

Every global element $e:1\rightarrow A$ is an injection, since the unique global element $i:1\rightarrow 1$ is the identity morphism of the terminal object. Every injection $e:1\rightarrow A$ is a monomorphism, since it is a global element, and for any object $B$ in the category, the morphism $i:B\rightarrow 1$ is unique by the definition of a terminal object, thus making $e:1\rightarrow A$ a monomorphism.

If the category has a [[strict initial object]] $\emptyset$, then every morphism $f:\emptyset\rightarrow B$ is vacuously an injection, since there are no global elements $x:1\rightarrow\emptyset$. In addition, every morphism $f:\emptyset\rightarrow B$ is vacuously a monomorphism, since for any set $B$ not the strict initial object, there are no global elements $x:B\rightarrow\emptyset$. This is the case in a [[distributive category]]. 

If the category has a binary disjoint coproducts $+$, then every morphism $f:1 + 1\rightarrow B$ for a set $B$ is an injection, since the coprojections of the coproduct $1 + 1$, $x, y:1\rightarrow 1 + 1$ are two distinct global elements by definition of a disjoint coproduct, which implies that $x = y$ if $f \circ x = f \circ y$ and that $f$ is a injection. 

This implies that in any category with a binary disjoint coproduct and a [[strict initial object]], every function $f$ from a finite coproduct of the terminal object to a set $B$ is an injection. 

+-- {: .query}
Anonymous: Under what conditions are all injections in a category monomorphisms? Obviously injections are monomorphisms in a [[well-pointed]] [[topos]] or [[pretopos]] (those are models of particular types of set theories), but does that remain true in a (pre)topos without well-pointedness, a [[coherent category]] or an [[exact category]]?

Anonymous: There is [this stackexchange post](https://math.stackexchange.com/questions/53405/conditions-for-monic-iff-injective), but the answers only refer to concrete categories with a [[forgetful functor]] to Set and a [[free functor]] from Set, rather than arbitrary abstract categories. 
=-- 

## Related concepts

* [[surjection]]

* [[monomorphism]]

* [[embedding]]

* [[monomorphism in an (infinity,1)-category]]

[[!redirects injective function]]
[[!redirects strongly injective function]]
[[!redirects injective functions]]
[[!redirects strongly injective functions]]
[[!redirects injections]]
[[!redirects one-to-one function]]
[[!redirects one-to-one functions]]
[[!redirects injective]]

[[!redirects injective map]]
[[!redirects injective maps]]

[[!redirects inclusion]]
[[!redirects inclusions]]
