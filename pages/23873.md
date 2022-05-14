
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

Given a [[category]] $C$ and objects $a, b \in Ob(A)$, a pair of [[morphisms]] $f, g \in Mor(a, b)$ are **jointly monic** if for every object $c:Ob(A)$ and pair of morphisms $h, k \in Mor(c, a)$, $f \circ h = f \circ k$ and $g \circ h = g \circ k$ imply that $h = k$. 

In a [[well-pointed category]] $C$, given objects $a, b \in Ob(A)$, a pair of [[morphisms]] $f, g \in Mor(a, b)$ are **jointly injective** if for every [[global element]] $h, k \in Mor(1, a)$, $f \circ h = f \circ k$ and $g \circ h = g \circ k$ imply that $h = k$. 

## In tablular allegories

In every [[tabular allegory]], a relation $R$ could be factored into jointly monic [[map in a dagger 2-poset|maps]] $f$ and $g$ such that $f^\dagger \circ g = R$. 

## See also

* [[monomorphism]]

* [[internal relation]]

* [[regular category]]

* [[tabular allegory]]

* [[bicategory of relations]]

* [[Rel]]

* [[SEAR]]

* [[ETCR]]

* [[digraph]]

* [[loop digraph object]]

* [[toddtrimble:Theory of units and tabulations in allegories]]

[[!redirects jointly monic]]
[[!redirects jointly injective]]

## References 

* [[Peter Freyd]], [[Andre Scedrov]]:

  **Categories, Allegories** 

  Mathematical Library Vol 39, North-Holland (1990). 

  [ISBN 978-0-444-70368-2](https://www.elsevier.com/books/categories-allegories/freyd/978-0-444-70368-2)