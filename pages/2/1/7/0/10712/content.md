
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A fundamental statement in [[stable homotopy theory]]/[[higher algebra]]/[[chromatic homotopy theory]].

## Statement

For any [[ring spectrum]] $E$ the kernel of the canonical [[morphism]]

$$
  \pi_\bullet R \longrightarrow MU_\bullet(R)
$$

to the [[MU]]-homology of $R$ consists of [[nilpotent elements]].

This is due to [[Ethan Devinatz]], [[Mike Hopkins]], and [[Jeff Smith]]. See [Lurie 10, theorem 3](#Lurie10)

## Special cases

The Nishida nilpotence theorem ([Nishida 73](#Nishida73)) is the special case for the [[sphere spectrum]], saying that all positive-degree elements in the [[stable homotopy groups of spheres]] are nilpotent. 

This is indeed a special case. The [[MU]]-homology of the sphere spectrum is the [Lazard ring](https://ncatlab.org/nlab/show/MU#homotopy_groups_cobordism_and_lazard_ring) and hence is torsion-free, whereas all positive-degree elements of the stable homotopy ring are torsion by the [[Serre finiteness theorem]] and therefore 
belong to the aforementioned kernel.

## Consequences

### Relation with $\infty$-fields

The nilpotence theorem implies that every [[∞-field]] is an [[∞-module]] over the [[Morava K-theory]] [[spectrum]] $K(n)$, for some $n$. See at _[[∞-field]]_.

## Related concepts

* [[Serre finiteness theorem]]

* [[thick subcategory theorem]]

## References

* {#Nishida73} [[Goro Nishida]],  (1973), "The nilpotency of elements of the stable homotopy groups of spheres", Journal of the Mathematical Society of Japan 25 (4): 707&#8211;732, doi:10.2969/jmsj/02540707, ISSN 0025-5645, MR 0341485.

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 25 _The Nilpotence lemma_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture25.pdf)) 
 

[[!redirects nilpotence lemma]]

[[!redirects Nishida nilpotence theorem]]
[[!redirects Nishida nilpotence lemma]]
