
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

In particular, every [[monomorphism]] in a category with a terminal object is an injection. 

The term '[[injective morphism]]' is already being used for morphisms satisfying a [[right lifting property]], so isn't used here. 

### Duals of injections

The categorical [[duality|dual]] of an injection, the coinjection, is a morphism $f:A\rightarrow B$ in a category $\mathcal{C}$ with an [[initial object]] $\emptyset$ such that for morphisms $g,h:B\rightarrow\emptyset$, if $g \circ f = h \circ f$, then $g = h$. 

In particular, every [[epimorphism]] in a category with an initial object is a coinjection. 

If the initial object $\emptyset$ is a [[zero object]], then every morphism in $\mathcal{C}$ is a coinjection. If $\emptyset$ is [[strict initial object|strict]], such as in a [[distributive category]], then the identity morphism on $\emptyset$ is a coinjection, and every other morphism in $\mathcal{C}$ is vacuously a coinjection. 

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
