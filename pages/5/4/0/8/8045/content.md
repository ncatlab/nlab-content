
# Material set theory
* table of contents
{: toc}

## Overview

__Material set theory__ (also called _membership-based set
theory_) is a style of [[set theory]] that contrasts with [[structural set theory]]. (The terminology 'material', or at least 'materialistic', goes back at least to [Friedman 1997](#Friedman1997).) While both material set theories like [[ZFC]] and [[ZFA]] and unsorted structural set theories like [[fully formal ETCS]] have a global membership relation on the theory (and fully formal ETCS has multiple global membership relations), the resulting membership [[graphs]] have drastically different structure. 

In particular, in unsorted structural set theories, each connected component of the membership graph is either an edgeless vertex, a rooted [[tree]] whose children are all leaves, or possibly a vertex with a single loop:

* the edgeless vertex represents the [[empty set]], as well as any non-set non-element objects in the set theory 

* the root of the rooted tree represents a set with more than one element, as well as the [[singleton]] in presentations of unsorted structural set theories where the singleton is different from the element in the singleton. The children leaves of the root represent the elements of the set. 

* the vertex with a single loop represents the singleton in some presentations of unsorted structural set theories where the [[singleton]] and the single element of the singleton are the same object, and is thus a [[Quine atom]] with respect to the membership relation $\in$. 

Material set theories are then those set theories whose membership graphs have more complex structure than those of unsorted structural set theories. Frequently in material set theory one takes everything to be a [[pure set]], including the elements of sets themselves. Therefore, any two sets may be meaningfully compared to ask if they are [[equal]] or if one is a member of the other. As a slight variation (still material set theory), one may also accept ur-elements (or atoms) as elements. 

The material/structural distinction in set theories is distinct from the unsorted/two-sorted/dependently-sorted distinction in set theories. There exist two-sorted material set theories with atoms, and unsorted structural set theories. 

## Related concepts

* [[cumulative hierarchy]]

* [[unsorted set theory]]

* [[set-theoretic multiverse]]

## References

Relation to [[structural set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

See also

* {#Friedman1997} [[Harvey Friedman]] (1997). [Foundational Completeness](https://cs.nyu.edu/pipermail/fom/1997-November/000143.html). FOM, 1997 November.

[[!redirects material set theory]]
[[!redirects material set theories]]

