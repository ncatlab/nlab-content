
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Overview

This article is about attempting to identify what makes a [[set theory]] a [[material set theory]] or a [[structural set theory]], and whether certain types of set theories should be considered material set theories, structural set theories, or neither material nor structural. 

We consider only [[simple type theory|simply sorted]] [[set theories]], which all have [[membership relations]]. All [[dependently sorted set theories]] are structural set theories with its membership being a typing judgment rather than a binary relation. 

### Homogeneous and heterogeneous membership relations

One difference between set theories is between the set theories where sets and elements are in two different sorts and the membership relation is a [[heterogeneous membership relation]], and the set theory where sets and elements are in the same sort and the membership relation is a [[homogeneous membership relation]]. 

One proposal is to define [[structural set theory]] to be the former and [[material set theory]] to be the latter. 

Having a homogeneous membership relation is not sufficient for a set theory to be a material set theory, since unsorted set theories such as [[fully formal ETCS]] also have a homogeneous membership relation $\in$, but should be a structural set theory, since it is based in [[category theory]]. (Though see below at the section titled propositional equality of sets for an argument that any set theory like [[fully formal ETCS]] with a homogeneous membership relation has the wrong notion of sameness of sets to be a structural set theory.) 

Nor is having a heterogeneous membership relation sufficient for defining structural set theories. There exist two-sorted presentations of [[pure set]] theories and material set theories with [[urelements]], with separate sorts $Set$ and $Element$ representing all sets and all elements respectively, as well as a global membership relation $\in$ defined as 
$$a:Element, A:Set \vdash a \in A prop$$ 
and functions $\mathrm{asElem}$ and $\mathrm{asSet}$ which [[element reflection|reflect]] a set $A$ over to an element $\mathrm{asElem}(A)$, and for [[pure set]] theory, [[set reflection|reflect]] an element $a$ over to a set $\mathrm{asSet}(a)$. 

As neither having a homogeneous nor heterogeneous membership relation isn't sufficient for defining both material and structural set theories, it isn't necessary for defining either notion, and thus whether a membership relation is homogeneous or heterogeneous is orthogonal to the set theory being material or structural. 

### Primitive and derived membership relations

Another proposed difference between material set theory and structural set theory is that in material set theory, the membership relation is a primitive. However, making the membership relation $\in$ primitive is not sufficient to make a set theory a material set theory, since one could make the membership relation a primitive in [[fully formal ETCS]] as well, and replace the definition with an axiom stating a logical equivalence between the membership relation and what would have been its definition: 

* for every function $f$ and $g$, a relation $f \in g$, 
* axiom: for every function $f$ and $g$, $f \in g$ if and only if $s(f) = 1$, $s(g) = 0$, and $t(f) = t(g)$. 

This is similar to how in [[ZFC]] one could take [[equality]] to be a primitive or a defined concept via the [[axiom of extensionality]]. Thus, having a primitive or a derived membership relation is neither sufficient nor necessary for [[structural set theories]]. 

However, having a primitive membership relation does seem to be a necessary condition for a set theory to be a [[material set theory]]. 

### Elements with "internal structure"

Another proposed difference between material set theory and structural set theory is that in material set theory, [[elements]] have some notion of "internal structure" and/or [[sets]] are the "internal structure" of some other object in the theory, while in structural set theory, elements do not have internal structure and sets are not the internal structure of other objects. Both could be defined by the membership relation of the theory and distinguished via structure of the membership [[graphs]] of the membership relations, and thus one distinguishes between [[material membership relations]] and [[structural membership relations]], as detailed in the article on [[membership relation]]. 

A set theory with a [[homogeneous membership relation]] is a **[[material set theory]]** if it has a material membership relations, and it is a **[[structural set theory]]** if it has a structural membership relation. If the set theory has multiple homogeneous membership relations, the set theory is a **structural set theory** if there exists a structural membership relation, and the set theory is a **material set theory** if every homogeneous membership relation $\in$ is a [[material membership relation]]. 

However, there are multiple distinct proposed definitions of material and structural membership relations. In addition, this proposal only works if the set theory has a [[homogeneous membership relations]], and there exist both structural and material set theories which have [[heterogeneous membership relations]], where sets and elements are in fundamentally different sorts. 

### Primitive sorts: sets/elements vs functions/relations

Another proposed difference between material set theory and structural set theory is the difference between the primitives of the two theories. Material set theory takes [[sets]] or [[elements]] to be the primitive concepts, while structural set theory takes [[functions]] or [[relations]] to be the primitive concepts.  

### Propositional equality of sets

The article on [[structural set theory]] states the following: 

> *Structural set theory* provides a [[foundation of mathematics]] which is free of this "superfluous baggage" attendant on theories such as ZF, in which there is lots of information such as whether or not $3\in 17$ (yes, says von Neumann; no, says Zermelo) which is never used in mathematics. In a structural set theory, the elements (such as $3$) of a set (such as $\mathbb{N}$) *have* no identity apart from their existence as elements of that set, and whatever structure is given to that set by the functions and relations placed upon it. 

There is an argument following the [[principle of equivalence]] that the structural notion of sameness of elements is [[propositional equality]], while the structural notion of sameness of sets is [[bijection]]. From this perspective, [[propositional equality]] of sets is "superfluous baggage" attendant on theories which has propositional equality of sets, and thus that any set theory with propositional equality of sets is not structural. This includes set theories like [[fully formal ETCS]] where sets and elements are in the same sort and the set theory has a [[homogeneous membership relation]]. 

## Related concepts

* [[material set theory]]
* [[structural set theory]]
* [[set theory versus dependent type theory]]

## References

Relation between [[material set theory]] and [[structural set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

[[!redirects material versus structural]]
[[!redirects material versus structural set theories]]