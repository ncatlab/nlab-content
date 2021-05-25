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

The concept of a _cancellative category_ is the generalization of the concept of [[cancellative monoid]] from [[monoids]] to [[categories]].

## Definition

In [[category theory]], "cancellative" is a synonym for *all [[morphism|arrows]] are [[monomorphism|monic]] and [[epimorphism|epic]]*. Thus the typical way for cancellative categories to be constructed to take a category $C$ and then restrict to a class of monic and epic morphisms closed under composition, such as all monic and epic morphisms, or [[isomorphisms]], etc. 

In fact every cancellative $C$ arises this way (in the tautological sense of applying this consideration to $C$ itself): a [[category]] $\mathcal{C}$ being _cancellative_ means all its _morphisms are monos and epis_. 

Equivalently, for arbitrary morphisms $f,h_0,h_1$ of $\mathcal{C}$, 
if $h_0 \circ f=h_1\circ f$, then $h_0=h_1$, and 
if $f\circ h_0=f\circ h_1$, then $h_0=h_1$. 

## Examples

 * any [[cancellative monoid]], regarded as a category with a single object

 * any [[groupoid]]

 * any [[poset]], or indeed any [[preorder]]   

## Related concepts

* [[cancellative monoid]]

* [[left cancellative category]], [[right cancellative category]]

[[!include oidification - table]]

[[!redirects cancellative categories]]