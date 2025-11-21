
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Sullivan construction** constructs a ([[rational topological space|rational]]) [[topological space]] from a [[dg-algebra]] (a graded commutative cochain dg-algebra in positive degree).

This is the special case of the construction of [[differential forms on presheaves]] from the definition of polynomial [[differential forms on simplices]].

It is one part of an [[equivalence of categories]] between the [[homotopy category]] of (connected, simply connected) [[dg-algebra]]s and that of ([[simply connected]]) [[rational topological space]]s.
As such it is a central tool in [[rational homotopy theory]]. 



## Definition

Let $\Delta_{Diff} : \Delta \to $ [[Diff]] be the standard smooth [[simplex]]es, and write $\Omega^\bullet_{\mathbb{Q}}(\Delta_{Diff}^n)$ for the [[dg-algebra]] of (polynomial, rational, whatever) [[differential form]]s on $\Delta^n_{Diff}$.

For $A \in dgAlg_{\mathbb{Q}}$ a [[dg-algebra]], consider the [[simplicial set]]

$$
  |A| : [n] \mapsto Hom_{dgAlg^{op}}( \Omega^\bullet(\Delta^n_{Diff}), A)
  \,.
$$

This, or rather its [[geometric realization]] to a [[rational topological space]], is the Sullivan construction.

## Related concepts

* [[Lie integration]]

## References

See the references at [[rational homotopy theory]].