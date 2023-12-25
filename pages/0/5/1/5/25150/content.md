
\tableofcontents

## Idea

The Archimedean property states that every positive element in a [[strictly weakly ordered]] [[cancellative monoid|cancellative]] [[commutative monoid]] is bounded above by a [[natural number]].

So an object satisfying the Archimedean property has no infinite elements. If the [[strict weak order]] is additionally a [[connected relation]] and thus a [[pseudo-order]], every [[infinitesimal]] element is equal to zero.

## Definition

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers.  

Let $(A,\lt, +, 0)$ be a [[strictly ordered]] [[cancellative monoid|cancellative]] [[commutative monoid]]. The positive integers are embedded into the [[function algebra|function monoid]] $A \to A$; there is an injection $inj:\mathbb{N}^+\to (A \to A)$ such that $inj(1) = id_A$ and $inj(s(n)) = inj(n) + id_A$ for all $n:\mathbb{N}^+$.

The __archimedean property__ states that for every $a,b:A$ such that $0 \lt a$ and $0 \lt b$, then there exist $n:\mathbb{N}^+$ such that $a \lt inj(n)(b)$. 

By [[uncurrying]] $inj$ one gets an [[action]] $act: (\mathbb{N}^+\times A) \to A$ such that $act(1,a) = a$ and $act(s(n),a) = act(n,a) + a$ for all $n:\mathbb{N}^+$ and $a:A$. The archimedean property then states that for all $a,b:A$ such that $0 \lt a$ and $0 \lt b$, there exist $n:\mathbb{N}^+$ such that $a \lt act(n,b)$.

## Examples

* [[Archimedean group]] 
* [[Archimedean ordered field]]
* [[Archimedean ordered integral domain]]
* [[Archimedean ordered local ring]]

## References

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Archimedean_property">Archimedean property</a>_

[[!redirects archimedean property]]
[[!redirects Archimedean property]]