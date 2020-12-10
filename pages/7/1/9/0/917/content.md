
#Contents#
* table of contents
{:toc}

## Definition

A [[function]] $f$ from $A$ to $B$ is __injective__ if $x = y$ whenever $f(x) = f(y)$.  An injective function is also called __one-to-one__ or an __injection__; it is the same as a [[monomorphism]] in [[Set|the category of sets]].

A _[[bijection]]_ is a function that is both injective and [[surjection|surjective]].

In [[constructive mathematics]], a [[strongly extensional function]] between sets equipped with tight [[apartness relation]]s is called __strongly injective__ if $f(x) \ne f(y)$ whenever $x \ne y$ (which implies that the function is injective).  This is the same as a [[regular monomorphism]] in the category of such sets and strongly extensional functions (while any merely injective function, if strongly extensional, is still a monomorphism).  Some authors use 'one-to-one' for an injective function as defined above and reserve 'injective' for the stronger notion.

## In other categories
Since an element $a$ in a set $A$ in the [[category of sets]] is just a [[global element]] $a:1\rightarrow A$, one could define injections in any category $\mathcal{C}$ with a [[terminal object]] $1$:

> A morphism $f:A\rightarrow B$ in $\mathcal{C}$ is an injection if, given any two global elements $x, y:1\rightarrow A$, $x = y$ if $f \circ x = f \circ y$. 

In particular, every [[monomorphism]] in a category with a terminal object is an injection, and every injection from the terminal object is a monomorphism.

+-- {: .query}
Anonymous: Under what conditions are all injections in a category monomorphisms? Obviously injections are monomorphisms in a [[well-pointed]] [[topos]] or [[pretopos]] (those are models of particular types of set theories), but does that remain true in a (pre)topos without well-pointedness, a [[coherent category]] or an [[exact category]]?
=--

### Duals of injections

The categorical [[duality|dual]] of an injection, the coinjection, is a morphism $f:A\rightarrow B$ in a category $\mathcal{C}$ with an [[initial object]] $\emptyset$ such that for morphisms $g,h:B\rightarrow\emptyset$, if $g \circ f = h \circ f$, then $g = h$. 

In particular, every [[epimorphism]] in a category with an initial object is a coinjection, and every coinjection from the initial object is an epimorphism. 

However, every morphism in $\mathcal{C}$ is a coinjection if the initial object is [[strict initial object|strict]], as the identity morphism of the initial object is a coinjection, and for any other morphism $f:A\rightarrow B$ such that $B$ is not the initial object, the statement 'if $g \circ f = h \circ f$, then $g = h$' is vacuously true as there are no morphisms $g,h:B\rightarrow\emptyset$; therefore $f$ is a coinjection. This is true in all [[distributive category|distributive categories]], such as a [[cartesian closed category]], a [[coherent category]], and a [[topos]]. 

If the initial object is a [[zero object]] $0$, every morphism in $\mathcal{C}$ is a coinjection, as an initial object that is a zero object is also a terminal object, and that by the definition of a terminal object, there exist a unique morphism $!:B\rightarrow 0$, and so for any morphisms $g,h:B\rightarrow 0$, $g = h$. As $g = h$ is true regardless of the morphism $f:A\rightarrow B$, every morphism is a coinjection. 

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
