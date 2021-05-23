+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The concept of a (left/right) _cancellative category_ is the generalization of the concept of (left/right) [[cancellative monoid]] from [[monoids]] to [[categories]].

## Definition

In [[category theory]], "right cancellative" is a synonym for *all [[morphism|arrows]] are [[epimorphism|epic]]*. Thus the typical way for right cancellative categories to be constructed to take a category $C$ and then restrict to a class of epimorphisms closed under composition, such as all epimomorphisms, or [[extremal epimorphisms]], etc. 

In fact every right cancellative $C$ arises this way (in the tautological sense of applying this consideration to $C$ itself): a [[category]] $\mathcal{C}$ being _right cancellative_ means all its _morphisms are epis_. 

Equivalently, for arbitrary morphisms $f,h_0,h_1$ of $\mathcal{C}$, 
if $h_0 \circ f=h_1\circ f$, then $h_0=h_1$.

## Examples

 * any (right) [[cancellative monoid]], regared as a category with a single object

 * any [[groupoid]]

 * any [[poset]], or indeed any [[preorder]]   

## Related concepts

* [[cancellative monoid]]

* [[left cancellative category]]

* [[cancellative category]]

[[!include oidification - table]]

[[!redirects right-cancellative]]
[[!redirects right-cancellative categories]]
[[!redirects right cancellative categories]]
[[!redirects all morphisms epic]]
[[!redirects all arrows epic]]