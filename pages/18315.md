
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

In [[category theory]], "left cancellative" is a synonym for *all [[morphism|arrows]] are [[monomorphism|monic]]*. Thus the typical way for left cancellative categories to be constructed to take a category $C$ and then restrict to a class of monomorphisms closed under composition, such as all monomomorphisms, or [[regular monomorphisms]] if the category is [[regular category|regular]], etc. 

In fact every left cancellative $C$ arises this way (in the tautological sense of applying this consideration to $C$ itself): a [[category]] $\mathcal{C}$ being _left cancellative_ means all its _morphisms are monos_. 

Equivalently, for arbitrary morphisms $f,h_0,h_1$ of $\mathcal{C}$, 
if $f\circ h_0=f\circ h_1$, then $h_0=h_1$.

## Examples


Tautological examples: 

 * any (left) [[cancellative monoid]], regared as a category with a single object

 * any [[groupoid]]

 * any [[poset]], or indeed any [[preorder]]   

Non-tautological examples: 
 
 * the category of [[fields]] (with [[ring]] [[homomorphisms]] as the morphisms)

 * the category of nontrivial [[vector spaces]] (over the field of [[real numbers]] or [[complex numbers]]) equipped with positive definite [[inner products]] 



## Related concepts

* [[cancellative monoid]]

* [[right cancellative category]]

* [[cancellative category]]

[[!include oidification - table]]

## References


* M. V. Lawson and A. R. Wallis, A categorical description of Bass-Serre theory ([arXiv:1304.6854v5](https://arxiv.org/abs/1304.6854))


* M. V. Lawson, "Ordered Groupoids and Left Cancellative Categories"
Semigroup Forum, Volume **68**, Issue 3, (2004),  458&#8211;-476 


[[!redirects left-cancellative]]
[[!redirects left-cancellative categories]]
[[!redirects left cancellative categories]]
[[!redirects all morphisms monic]]
[[!redirects all arrows monic]]