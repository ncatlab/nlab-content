
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **comparison** or **cotransitive relation** or **weakly linear relation** on a set $A$ is a (binary) [[relation]] $\sim$ on $A$ such that in every pair of related elements, any other element is related to one of the original elements in the same order as the original pair:
$$\forall (x, y, z: A),\; x \sim z \;\Rightarrow\; x \sim y \;\vee\; y \sim z$$
which generalises from $3$ to any (finite, positive) number of elements.  To include the case where $n = 1$, we must explicitly state that the relation is [[irreflexive relation|irreflexive]].

Alternatively, this is the same condition as 
$$\forall (x, z: A),\; x \sim z \;\Rightarrow\; \forall (y: A),\; x \sim y \;\vee\; y \sim z$$

Comparisons are most often studied in [[constructive mathematics]].  In particular, the relation $\lt$ on the (located Dedekind) [[real numbers]] is an [[irreflexive comparison]], even though its [[negation]] $\geq$ is not constructively [[total relation|total]].  (Indeed, $\lt$ is a [[pseudo-order]], even though $\geq$ is not constructively a [[total order]].)

A comparison is a [[cartesian monoidal category|cartesian monoidal]] [[semicategory]] [[enriched category|enriched]] on the [[co-Heyting algebra]] $TV^\op$, where $TV$ is the [[Heyting algebra]] of [[truth values]].

## Related concepts

* [[pseudo-order]]

* [[total relation]]

## References

For weak linearity of relations as comparison, see section 11.2.1 of: 

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

For cotransitivity of relations as comparison, see section 3.1 of:

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects comparison]]
[[!redirects comparisons]]
[[!redirects comparison relation]]
[[!redirects comparison relations]]

[[!redirects cotransitive]]
[[!redirects cotransitive relation]]
[[!redirects cotransitive relations]]
[[!redirects cotransitivity]]

[[!redirects weakly linear]]
[[!redirects weakly linear relation]]
[[!redirects weakly linear relations]]
[[!redirects weak linearity]]
