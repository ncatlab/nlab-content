
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Complete categories
* table of contents
{: toc}

## Definition

A [[category]] $C$ is **complete** if it has all [[small limit|small]] [[limit|limits]]: that is, if every [[small diagram|small]] [[diagram]]

$$ F: D \to C$$

where $D$ is a [[small category]] has a [[limit]] in $C$.

Sometimes one says that $C$ is __small-complete__ to stress that $D$ must be small; compare [[finitely complete category]].  Also compare [[complete small category]], which is different; here we see that any [[small category]] that is also small-complete must be [[thin category|thin]] (at least classically).


## Examples

Many familiar categories of mathematical structures are complete: to name just a few examples, [[Set]], [[Grp]], [[Ab]], [[Vect]] and [[Top]] are complete.

As hinted above, every [[complete lattice]] is complete as a category.

A common situation is that of a category of algebras for a [[monad]] in a complete category:  If there exists a [[monadic  functor]] $C\to D$ and $D$ is complete, then $C$ is complete (as [[monadic functor|monadic functors]] [[created limit|create limits]]).  This includes some obvious examples (such as [[Grp]], [[Ab]], and [[Vect]]), as well as some less-obvious examples, such as [[complete lattice|complete lattices]] and [[compact space|compact]] [[Hausdorff space|Hausdorff]] spaces.

The contravariant presheaf category $[C,Set]$ is complete, and the dual [[Yoneda embedding]] exhibits it as the [[free completion]] of $C$.


## Related concepts

* [[cocomplete category]]

* [[bicomplete category]]

* [[M-complete category]]

[[!redirects complete category]]
[[!redirects complete categories]]
[[!redirects small-complete category]]
[[!redirects small-complete categories]]
[[!redirects smally complete category]]
[[!redirects smally complete categories]]
