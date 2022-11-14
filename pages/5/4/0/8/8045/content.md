
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
theory_) is a style of [[set theory]] that contrasts with [[structural set theory]]. (The terminology 'material', or at least 'materialistic', goes back at least to [Friedman 1997](#Friedman1997).) Material set theories can either be [[unsorted set theories]] or [[two-sorted set theories]]. 

There are a number of proposals to formally distinguish between material set theories and structural set theories.  

### Material set theories as set theories with a homogeneous membership relation

One proposed difference between material set theory and structural set theory is that material set theories have a global membership relation. 

From one point of view, this is not sufficient for a set theory to be a material set theory, since unsorted set theories such as [[fully formal ETCS]] also have a global membership relation and should be a structural set theory, since it is based in [[category theory]]. Making the global membership relation primitive is not enough either, since one could make the global membership relation a primitive in fully formal ETCS as well, and replace the definition with an axiom stating a logical equivalence between the global membership relation and what would have been its definition: 

* for every function $f$ and $g$, a relation $f \in g$, 
* axiom: for every function $f$ and $g$, $f \in g$ if and only if $s(f) = 1$, $s(g) = 0$, and $t(f) = t(g)$. 

This is similar to how in [[ZFC]] one could take [[equality]] to be a primitive or a defined concept via the [[axiom of extensionality]]. 

However, the article on [[structural set theory]] states the following: 

> *Structural set theory* provides a [[foundation of mathematics]] which is free of this "superfluous baggage" attendant on theories such as ZF, in which there is lots of information such as whether or not $3\in 17$ (yes, says von Neumann; no, says Zermelo) which is never used in mathematics. In a structural set theory, the elements (such as $3$) of a set (such as $\mathbb{N}$) *have* no identity apart from their existence as elements of that set, and whatever structure is given to that set by the functions and relations placed upon it.  

In any set theory with a [[homogeneous membership relation]], such as [[fully formal ETCS]], there is such information such as whether or not $3 \in 17$, or $1 \in 1$, since sets and elements are in the same sort and thus can be compared for membership. In fact, depending on the definition of [[set]] in [[fully formal ETCS]], the [[identity morphism]] of a [[singleton]] could be a [[Quine atom]] with respect to the defined membership relation $\in$, since it represents both a set and an element; this is the "superfluous baggage" from which structural set theory should be free of. From this point of view, any set theory with a [[homogeneous membership relation]] is *not* a structural set theory, and thus a material set theory. 

Finally, there is an argument following the [[principle of equivalence]] that sets and elements should be in fundamentally different sorts in [[structural set theory]], since the structural notion of sameness of elements is equality, while the structural notion of sameness of sets is [[bijection]]. Since in any set theory where sets and elements are in the same sort, sets can be compared for equality, any such set theory is not a structural set theory. 

### Material set theory as set theory whose elements have internal structure

Another proposed difference between material set theory and structural set theory is that in material set theory, [[elements]] have some notion of "internal structure" and/or [[sets]] are the "internal structure" of some other object in the theory, while in structural set theory, elements do not have internal structure and sets are not the internal structure of other objects. Both could be defined by the membership relation of the theory and distinguished via structure of the membership [[graphs]] of the membership relations, and thus one distinguishes between [[material membership relations]] and [[structural membership relations]]. 

A set theory with a [[homogeneous membership relation]] is a **[[material set theory]]** if it has a material membership relations, and it is a **[[structural set theory]]** if it has a structural membership relation. If the set theory has multiple homogeneous membership relations, the set theory is a **structural set theory** if there exists a structural membership relation, and the set theory is a **material set theory** if every homogeneous membership relation $\in$ is a [[material membership relation]]. 

However, there are multiple distinct proposed definitions of material and structural membership relations. In addition, this proposal only works if the set theory has a [[homogeneous membership relations]], and there exist material set theories which have [[heterogeneous membership relations]], where sets and elements are in fundamentally different sorts. 

### Other

A third proposed difference between material set theory and structural set theory is the difference between the primitives of the two theories. Material set theory takes [[sets]] or [[elements]] to be the primitive concepts, while structural set theory takes [[functions]] or [[relations]] to be the primitive concepts.  

## Two-sorted material set theories

In two-sorted material set theories, there are separate sorts $Set$ and $Element$ representing all sets and all elements respectively, as well as a global membership relation $\in$ defined as 
$$a:Element, A:Set \vdash a \in A prop$$ 

Sets are not literally elements in two-sorted material set theories. Instead, there are functions $\mathrm{asElem}$ and $\mathrm{asSet}$ which [[element reflection|reflect]] a set $A$ over to an element $\mathrm{asElem}(A)$, and for [[pure set]] theory, [[set reflection|reflect]] an element $a$ over to a set $\mathrm{asSet}(a)$. 

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