
#Contents#
* table of contents
{:toc}

## Definition

A [[function]] $f$ from $A$ to $B$ is __injective__ if $x = y$ whenever $f(x) = f(y)$.  An injective function is also called __one-to-one__ or an __injection__; it is the same as a [[monomorphism]] in [[Set|the category of sets]].

A _[[bijection]]_ is a function that is both injective and [[surjection|surjective]].

In [[constructive mathematics]], a [[strongly extensional function]] between sets equipped with tight [[apartness relation]]s is called __strongly injective__ if $f(x) \ne f(y)$ whenever $x \ne y$ (which implies that the function is injective).  This is the same as a [[regular monomorphism]] in the category of such sets and strongly extensional functions (while any merely injective function, if strongly extensional, is still a monomorphism).  Some authors use 'one-to-one' for an injective function as defined above and reserve 'injective' for the stronger notion.

## In other categories
Since an element $a$ in a set $A$ in the [[category of sets]] is just a [[global element]] $a:1\rightarrow A$, one could define injections in any category $\mathcal{C}$ with a [[terminal object]] $1$:

+-- {: .num_defn}
###### Definition
A morphism $f:A\rightarrow B$ in $\mathcal{C}$ is an __injection__ or a __one-to-one morphism__ if, given any two global elements $x, y:1\rightarrow A$, $x = y$ if $f \circ x = f \circ y$. 
=--

+-- {: .num_remark} 
###### Remark 
The term __injective morphism__ is already used in category theory in a different context to mean a morphism with a [[right lifting property]]. 
=--

+-- {: .num_prop}
###### Proposition
In a category $\mathcal{C}$ with a [[terminal object]] $1$, every [[monomorphism]] is an injection. 
=--

This follows from the definition of a monomorphism. 

+-- {: .num_prop}
###### Proposition
In a category $\mathcal{C}$ with a [[terminal object]] $1$, every global element $e:1\rightarrow A$ is an injection. 
=--

+-- {: .proof}
###### Proof
By definition of [[terminal object]] $1$, the unique global element $i:1\rightarrow 1$ is the identity morphism of the terminal object. Thus for every global element $e:1\rightarrow A$, for any two global elements $x, y:1\rightarrow 1$, $x = y$ is always true, making $e:1\rightarrow A$ an injection. 
=--

If the category has a [[strict initial object]] $\emptyset$, then every morphism $f:\emptyset\rightarrow B$ is vacuously an injection, since there are no global elements $x:1\rightarrow\emptyset$. 

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

[[!redirects injectivity]]



