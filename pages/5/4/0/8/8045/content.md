
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Material set theory
* table of contents
{: toc}

## Overview

__Material set theory__ (also called _membership-based set
theory_) is a style of [[set theory]] with a primitive global membership relation "$\in$" where sets are characterized only by "$\in$". (The terminology 'material', or at least 'materialistic', goes back at least to [Friedman 1997](#Friedman1997).) Material set theory contrasts with *[[structural set theory]]* (cf. *[[material versus structural set theory]]*), as well as with set theories which are neither structural nor material. Material set theories can either be [[unsorted set theories]] or [[two-sorted set theories]]. 

---

There are a number of proposals to formally distinguish between material set theories and structural set theories.  

### Material set theory as set theory whose elements have internal structure

Another proposed difference between material set theory and [[structural set theory]] is that in material set theory, [[elements]] have some notion of "internal structure" and/or [[sets]] are the "internal structure" of some other object in the theory, while in structural set theory, elements do not have internal structure and sets are not the internal structure of other objects. Both could be defined by the membership relation of the theory and distinguished via structure of the membership [[graphs]] of the membership relations, and thus one distinguishes between [[material membership relations]] and [[structural membership relations]]. 

A set theory with a [[homogeneous membership relation]] is a **[[material set theory]]** if it has a material membership relations, and it is a **[[structural set theory]]** if it has a structural membership relation. If the set theory has multiple homogeneous membership relations, the set theory is a **structural set theory** if there exists a structural membership relation, and the set theory is a **material set theory** if every homogeneous membership relation $\in$ is a [[material membership relation]]. 

However, there are multiple distinct proposed definitions of material and structural membership relations. In addition, this proposal only works if the set theory has a [[homogeneous membership relations]], and there exist material set theories which have [[heterogeneous membership relations]], where sets and elements are in fundamentally different sorts. 

### Other

A third proposed difference between material set theory and structural set theory is the difference between the primitives of the two theories. Material set theory takes [[sets]] or [[elements]] to be the primitive concepts, while structural set theory takes [[functions]] or [[relations]] to be the primitive concepts.  

## Related concepts

* [[cumulative hierarchy]]

* [[unsorted set theory]]

* [[two-sorted set theory]]

* [[set-theoretic multiverse]]

* [[material versus structural]]

## References

Relation to [[structural set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

See also

* {#Friedman1997} [[Harvey Friedman]] (1997). [Foundational Completeness](https://cs.nyu.edu/pipermail/fom/1997-November/000143.html). FOM, 1997 November.

[[!redirects material set theory]]
[[!redirects material set theories]]