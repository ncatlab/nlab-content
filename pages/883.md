
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

A __comparison__ on a set $A$ is a (binary) [[relation]] $\sim$ on $A$ such that in every pair of related elements, any other element is related to one of the original elements in the same order as the original pair:
$$\forall (x, y, z: A),\; x \sim z \;\Rightarrow\; x \sim y \;\vee\; y \sim z$$
which generalises from $3$ to any (finite, positive) number of elements.  To include the case where $n = 1$, we must explicitly state that the relation is [[irreflexive relation|irreflexive]].

Comparisons are most often studied in [[constructive mathematics]].  In particular, the relation $\lt$ on the (located Dedekind) [[real numbers]] is a comparison, even though its [[negation]] $\geq$ is not constructively [[total relation|total]].  (Indeed, $\lt$ is a [[linear order]], even though $\geq$ is not constructively a [[total order]].)

A comparison is a [[cartesian monoidal category|cartesian monoidal]] [[semicategory]] [[enriched category|enriched]] on the [[co-Heyting algebra]] $TV^\op$, where $TV$ is the [[Heyting algebra]] of [[truth values]].

[[!redirects comparison]]
[[!redirects comparison relation]]
