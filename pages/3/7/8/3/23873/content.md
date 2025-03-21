
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

Given a [[category]] $C$ and objects $a, b \in Ob(C)$, a pair of [[morphisms]] $f, g \in C(a, b)$ is **jointly monic** if for every object $c: Ob(C)$ and pair of morphisms $h, k \in C(c, a)$, $f \circ h = f \circ k$ and $g \circ h = g \circ k$ imply that $h = k$.

In a [[well-pointed category]] $C$, given objects $a, b \in Ob(C)$, a pair of [[morphisms]] $f, g \in C(a, b)$ is **jointly injective** if for every [[global element]] $h, k \in C(1, a)$, $f \circ h = f \circ k$ and $g \circ h = g \circ k$ imply that $h = k$.

More generally, we can consider a **jointly monic family of morphisms**, where we indexed over a set $I$. When $I$ is a [[singleton set]], this reduces to a [[monomorphism]], and when $I$ is a two-element set, this reduces to a jointly monic pair. (And similarly for joint injectivity.)

## In tablular allegories

In every [[tabular allegory]], a relation $R$ could be factored into jointly monic [[map in a dagger 2-poset|maps]] $f$ and $g$ such that $f^\dagger \circ g = R$.

## Examples

* Taking $C = Set$, and ${ F_i : X \to Y }_{i \in I}$ to be a family of [[functors]], joint monicity of $(F_i)_{x, x'} : X(x, x') \to Y(F_i x, F_i x')$ is the notion of **joint faithfulness** (which specialises to the notion of [[faithful functor]] when $I$ is a singleton).

## See also

* [[monomorphism]]

* [[faithful functor]]

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

## References 

* [[Peter Freyd]], [[Andre Scedrov]], *Categories, Allegories*, Mathematical Library Vol 39, North-Holland (1990). [ISBN 978-0-444-70368-2](https://www.elsevier.com/books/categories-allegories/freyd/978-0-444-70368-2)

[[!redirects jointly monic]]
[[!redirects jointly injective]]
[[!redirects jointly faithful]]
[[!redirects jointly faithful functors]]
[[!redirects jointly faithful family of functors]]