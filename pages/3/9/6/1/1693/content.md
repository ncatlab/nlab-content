
# Boolean rigs
* table of contents
{: toc}

## Idea

As a [[Boolean ring]] is a [[ring]] in which multiplication is [[idempotent]], so a Boolean rig is a [[rig]] in which multiplication is idempotent; that is, a rig in which $x^2 = x$ always holds.

While many further properties follow from the idempotence of multiplication in a ring, most of these require subtraction (or at least cancellation of addition), so these will not necessarily hold for a Boolean rig.  As such, it might be proper to add some of them as axioms for a Boolean rig.


## Properties

Even without subtraction, we may define the Boolean join operation $x \vee y \coloneqq x + x y + y$; however, it also seems to have no nice properties without additional axioms.  In a *commutative* Boolean rig, however, we can prove that multiplication distributes over join, meaning that multiplication and join together form another rig structure.  But we cannot prove that this rig is also Boolean, or that join is a [[semilattice]] operation.


## Examples

The main examples are probably [[distributive lattices]].  In this case, the join operation called $\vee$ above will match the original join/addition operation called $+$ above.

Of course, a [[Boolean ring]] is a Boolean rig, since any ring is a rig.  However, since it\'s also a distributive lattice, a Boolean ring is actually a Boolean rig in two different ways.


## References

There seem to be none.  The 'Boolean semirings' in the literature (by which I mean, what Google found for me that wasn\'t cloaked) are something much more complicated than what we\'re looking at here.


[[!redirects Boolean rig]]
[[!redirects Boolean rigs]]

[[!redirects Boolean semiring]]
[[!redirects Boolean semirings]]
