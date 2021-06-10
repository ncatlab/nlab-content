

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A **Heyting category** (called a **[[logos]]** in [Freyd-Scedrov](#FreydScedrov)) is a [[coherent category]] in which each [[base change]] functor $f^*:Sub(Y)\to Sub(X)$ has a _[[right adjoint]]_ $\forall_f$ (the _[[universal quantifier]]_, in addition to the [[left adjoint]] [[existential quantifier]] that exists in any [[regular category]]).  

It follows that each [[poset of subobjects]] $Sub(X)$ is a [[Heyting algebra]] and the base-change functors $f^*$ are Heyting algebra homomorphisms. The Heyting implication can be defined as follows: if $A$ and $B$ are subobjects of $X$, then we can define $(A\Rightarrow B) \in Sub(X)$ as $\forall_i(A\cap B) \hookrightarrow X$, where $i\colon A\hookrightarrow X$ is the subobject inclusion and we take $A \cap B\in Sub(A)$.  Any Heyting category has an [[internal logic]] which is full ([[type theory|typed]]) [[first order logic|first-order]] [[intuitionistic logic]]. The extra right adjoint $\forall_f$ provided by the above axiom gives the [[universal quantifier]] in this logic.

A **Heyting functor** is a [[coherent functor]] between Heyting categories which additionally preserves the right adjoints $\forall_f$.  Such functors also preserve the [[internal logic|internal interpretation]] of [[first-order logic]].

## Examples

Any [[topos]], and in fact any [[well-powered category|well-powered]] [[infinitary coherent category]], is a Heyting category.  Any [[Boolean category]] is also a Heyting category.

## Related concepts

* [[Boolean category]]

* [[De Morgan category]]

* [[Heyting pretopos]]

* [[elementary topos]]

* [[Heyting algebra]]

## References

* [[Peter Freyd]], Andre Scedrov, _[[Categories, Allegories]]_
 {#FreydScedrov}

[[!redirects Heyting functor]]
[[!redirects Heyting categories]]
[[!redirects Heyting functors]]

