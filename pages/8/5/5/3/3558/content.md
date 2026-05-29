
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A *complete Heyting algebra* is a [[Heyting algebra]] which is also a [[complete lattice]]; that is, it is a [[poset]] with arbitrary [[limits]] and [[colimits]], that is also [[cartesian closed]].

## Properties

### Relation to frames

By the [[adjoint functor theorem]], one can demonstrate that every [[frame]] is a complete Heyting algebra, and vice versa, so far as the underlying [[poset]] goes.  

However, [[morphisms]] of frames needn't preserve [[exponential objects]] or infinitary [[meets]], as would most naturally be required of morphisms of complete Heyting algebras.  Also, when considering *[[large category|large]]* lattices which are only *small*-[[complete category|complete]], then frames and complete Heyting algebras are different objects. This becomes important in [[predicative mathematics|predicative]] [[constructive mathematics]], where frames are not provably [[small category|small]], but only [[large category|large]], [[locally small category|locally small]], and [[small category|small]]-complete, and so one can't show that every frame is a complete Heyting algebra. 

However, it is still the case in predicative constructive mathematics that any [[frame]] with a [[small set|small]] [[base]] satisfies the [[adjoint functor theorem]] and is a complete Heyting algebra, since having a small base is the posetal verison of the [[solution set condition]]. Thus, the [[initial object|initial]] [[frame]] is a complete Heyting algebra, since its base is given by the [[boolean domain]], which is always small. 

## Related concepts

* [[sigma-complete Heyting algebra]]

* [[frame]]

## References

For that [[frames]] are not [[complete Heyting algebras]] in [[predicative mathematics|predicative]] [[constructive mathematics]], see: 

* [[Ayberk Tosun]], *Constructive and Predicative Locale Theory in Univalent Foundations* ([arXiv:2603.01308](https://arxiv.org/abs/2603.01308))

See also at *[[Heyting algebra]]*.

[[!redirects complete Heyting algebra]]
[[!redirects complete Heyting algebras]]
