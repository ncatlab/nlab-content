<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A _homotopical category_ is a construction used in [[homotopy theory]], related to but more flexible than a [[model category]].


#Definition#

A _homotopical category_ is a [[category with weak equivalences]] where on top of the 2-out-of-3-property the morphisms satisfy the 

**2-out-of-6-property**: 

If morphisms $h \circ g$ and $g \circ f$ are weak equivalences, then so are $f$, $g$, $h$ and $h \circ g \circ f$.

#Remarks#

* The 2-out-of-6-property implies the [[category with weak equivalences|2-out-of-3]]-property.

* A functor $F : C \to D$ between homotopical categories which preserves weak equivalences is a [[homotopical functor]].

# Simplicial localization #

Every homotopical category $C$ "presents" or "models" an [[(infinity,1)-category]] $L C$, a [[simplicially enriched category]] called the [[simplicial localization]] of $C$, which is in some sense the universal solution to inverting the weak equivalence up to [[higher category theory|higher categorical]] morphisms.


#Related concepts#

* [[category of fibrant objects]]

* [[cofibration category]]

* [[Waldhausen category]]

* [[model category]]

* category with a [[calculus of fractions]]

#References#

This definition is in paragraph 33 of

* William G. Dwyer, Philip S. Hirschhorn, Daniel M. Kan, and Jeffrey H. Smith. _Homotopy Limit Functors on Model Categories and Homotopical Categories_, volume 113 of Mathematical Surveys and Monographs.