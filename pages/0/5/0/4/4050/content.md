<div class="rightHandSide toc">
[[!include monoidal categories - contents]]
</div>

# Categories with duals
* table of contents
{: toc}

## Idea

A _category with duals_ is a [[category]] where [[objects]] and/or [[morphisms]] have [[dual object|duals]].  This exists in several flavours; this list is mostly taken from a recent [`categories` list post](http://article.gmane.org/gmane.science.mathematics.categories/5807/) from [[Peter Selinger]].


## Categories with duals for objects

*  A __[[left autonomous category]]__ is a [[monoidal category]] in which every [[object]] is [[dualisable object|dualisable]] on the left.

*  A __[[right autonomous category]]__ is a [[monoidal category]] in which every [[object]] is [[dualisable object|dualisable]] on the right.

*  An __[[autonomous category]]__, or __[[rigid category]]__ is a monoidal category that is both left and right autonomous. Note that any braided monoidal category is autonomous on both sides if it is autonomous on either side.

*  A __[[pivotal category]]__ is an autonomous category equipped with a [[monoidal natural transformation|monoidal]] [[natural isomorphism]] from the [[identity functor]] to the [[double dual]] functor. A one-sided autonomous category with such an isomorphism is automatically two-sided autonomous. Although each braided autonomous category has an isomorphism from $A$ to $A^{**}$, such a category is not necessarily pivotal because this isomorphism is not in general monoidal. On the other hand, every [[balanced monoidal category|balanced]] autonomous category is pivotal.

*  A __[[spherical category]]__ is a pivotal category where the left and right [[trace]] operations coincide on all objects.

*  A __[[tortile category]]__, or __[[ribbon category]]__, is a [[balanced monoidal category|balanced]] autonomous (therefore pivotal) category in which the [[twist]] on $A^*$ is the dual of the twist on $A$. 

*  A __[[compact closed category]]__ is a [[symmetric monoidal category|symmetric]] tortile category, or equivalently, a symmetric autonomous category.

*  The __$*$-[[star-autonomous category|autonomous categories]]__ do not really belong on this list; being $*$-autonomous is logically independent of being autonomous, and while $*$-autonomous categories have duals, these are not in general duals in the sense of a [[dualisable object]].  However, any compact closed category is $*$-autonomous.


## Categories with duals for morphisms

One might write something about these too, or put them on a separate page.  In the meantime, see the table of contents to the right.


## References

*  Peter Selinger, [`categories` post of 2010-05-15](http://permalink.gmane.org/gmane.science.mathematics.categories/5805);
*  Peter Selinger, _[A survey of graphical languages for monoidal categories](http://arxiv.org/abs/0908.3347)_ 


[[!redirects category with duals]]
[[!redirects categories with duals]]
[[!redirects category with duals for objects]]
[[!redirects categories with duals for objects]]
