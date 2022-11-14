
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
theory_) is a style of [[set theory]] that contrasts with [[structural set theory]]. (The terminology 'material', or at least 'materialistic', goes back at least to [Friedman 1997](#Friedman1997).) In contrast to structural set theory, the elements in material set theory have internal structure and/or the sets in material set theory are internal structure. Material set theories can either be [[unsorted set theories]] or [[two-sorted set theories]]. 

### Unsorted material set theories

Both unsorted material set theories like [[ZFC]] and [[ZFA]] and unsorted structural set theories like [[fully formal ETCS]] have a global membership relation on the theory (and fully formal ETCS has multiple global membership relations). This means that merely having a global membership relation is not sufficient for an unsorted set theory to be a material set theory. 

In order to define what a material set theory, we need to define what it it means for elements, however defined, to have internal structure, and for sets, however defined, to be an internal structure of some other object, via the structure of the membership [[graphs]] of the global membership relations on the theory. An element $e$ **has internal structure** if there exists an object $a$ such that $a \in e$, and an set $S$ **is an internal structure** if there exists an object $a$ such that $S \in a$. 

$$\mathrm{hasInternalStructure}(e) \coloneqq \mathrm{isElement}(e) \wedge \exists a.a \in e$$
$$\mathrm{isInternalStructure}(S) \coloneqq \mathrm{isSet}(S) \wedge \exists a.S \in a$$

If an unsorted set theory only has one membership relation, then an unsorted set theory is a **material set theory** if there exists an element $e$ which has internal structure or a set $S$ which is an internal structure, and an unsorted set theory is a **[[structural set theory]]** if for all elements $e$, $e$ does not have internal structure, and for all sets $S$, $S$ is not an internal structure. 

$$\mathrm{isMaterial} \coloneqq \exists a.(\mathrm{hasInternalStructure}(a) \vee \mathrm{isInternalStructure}(a))$$

$$\mathrm{isStructural} \coloneqq \forall a.(\neg\mathrm{hasInternalStructure}(a) \wedge \neg\mathrm{isInternalStructure}(a))$$

If an unsorted set theory has multiple membership relations, the unsorted set theory is a **structural set theory** if there exists a membership relation $\in$ for which for all elements $e$, $e$ does not have internal structure, and for all sets $S$, $S$ is not an internal structure. An unsorted set theory is a **material set theory** if for all membership relations $\in$, there exists an element $e$ which has internal structure or a set $S$ which is an internal structure. 

Thus, a theory like [[ZFC]] is a material set theory because sets and elements are the same, and thus all elements have internal structure and all sets are internal structure. The same is true of any theory of [[pure sets]], such as [[New Foundations]]. In a theory with non-set [[urelements]] such as [[ZFA]], every object in the theory is an element, and while urelements do not have internal structure, there exist other elements which do have internal structure, namely those elements which are sets. 

In contrast, [[fully formal ETCS]] is not a material set theory, since there exists a global membership relation where every element does not have internal structure and every set is not internal structure, namely the predicate $\mathrm{isSet}$ defined as 
$$\mathrm{isSet}(a) \coloneqq s(b) = 0$$
and the relation $\in$ defined by 
$$a \in b \coloneqq s(a) = 1 \wedge \mathrm{isSet}(a) \wedge t(a) = t(b)$$
where the constant primitive $1$ is the identity morphism of the terminal object and the constant primitive $0$ is the identity morphism of the initial object. 

#### Alternate definition

The above definition states that in an unsorted structural set theory, [[Quine atoms]] cannot exist. An alternative definition allows for Quine atoms to exist in an unsorted structural set theory. In unsorted structural set theories, each connected component of the membership graph is either an edgeless vertex, a rooted [[tree]] whose children are all leaves, or possibly a vertex with a single loop:

* the edgeless vertex represents the [[empty set]], as well as any non-set non-element objects in the set theory 

* the root of the rooted tree represents a set with more than one element, as well as the [[singleton]] in presentations of unsorted structural set theories where the singleton is different from the element in the singleton. The children leaves of the root represent the elements of the set. 

* the vertex with a single loop represents a [[Quine atom]] with respect to the membership relation $\in$, which occur in some definitions of sets in structural set theories, such as defining sets as [[identity functions]] or as functions with [[singleton]] [[codomain]], where the [[singleton]] is always a [[Quine atom]]. 

Unsorted material set theories are then those unsorted set theories whose membership graphs have more complex structure than those of unsorted structural set theories. 

### Two-sorted material set theories

In two-sorted material set theories, there are separate sorts $Set$ and $Element$ representing all sets and all elements respectively, as well as a global membership relation $\in$ defined as 
$$a:Element, A:Set \vdash a \in A prop$$ 

Sets are not literally elements in two-sorted material set theories. Instead, there are functions $\mathrm{asElem}$ and $\mathrm{asSet}$ which [[element reflection|reflect]] a set $A$ over to an element $\mathrm{asElem}(A)$, and for [[pure set]] theory, [[set reflection|reflect]] an element $a$ over to a set $\mathrm{asSet}(a)$. 

## Related concepts

* [[cumulative hierarchy]]

* [[unsorted set theory]]

* [[two-sorted set theory]]

* [[set-theoretic multiverse]]

## References

Relation to [[structural set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

See also

* {#Friedman1997} [[Harvey Friedman]] (1997). [Foundational Completeness](https://cs.nyu.edu/pipermail/fom/1997-November/000143.html). FOM, 1997 November.

[[!redirects material set theory]]
[[!redirects material set theories]]