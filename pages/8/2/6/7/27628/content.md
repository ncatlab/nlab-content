
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The notion of [[composition]] of [[morphisms]] in [[simplicial type theory]].

## Definition

Let $A$ be a type in [[simplicial type theory]]. Recall that the [[hom-type]] is defined as 

$$\mathrm{hom}_A(x, y) \coloneqq \sum_{f:\mathbb{I} \to A} (f(0) = x) \times (f(1) = y)$$

A **pair of composable morphisms** in $A$ is a [[tuple]] consisting of elements $x:A$, $y:A$, $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(y, z)$. The type of pairs of composable morphisms is the [[dependent sum type]]

$$\sum_{x:A} \sum_{y:A} \sum_{z:A} \mathrm{hom}_A(x, y) \times \mathrm{hom}_A(y, z)$$

A **composite of morphisms** in $A$ is a [[tuple]] consisting of elements $x:A$, $y:A$, $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$, $g:\mathrm{hom}_A(y, z)$, and $h:\mathrm{hom}_A(x, z)$. The type of pairs of composable morphisms is the [[dependent sum type]]

$$\sum_{x:A} \sum_{y:A} \sum_{z:A} \mathrm{hom}_A(x, y) \times \mathrm{hom}_A(y, z) \times \mathrm{hom}_A(x, z)$$

There is a function from composites to pairs of composable morphisms

$$p:\left(\sum_{x:A} \sum_{y:A} \sum_{z:A} \mathrm{hom}_A(x, y) \times \mathrm{hom}_A(y, z) \times \mathrm{hom}_A(x, z)\right) \to \left(\sum_{x:A} \sum_{y:A} \sum_{z:A} \mathrm{hom}_A(x, y) \times \mathrm{hom}_A(y, z)\right)$$

which discards the morphism in $\mathrm{hom}_A(x, z)$ from the tuple. 

A pair of composable morphisms $(x, y, z, f, g)$ is **uniquely composable** if the [[fiber type]] of $p$ at $(x, y, z, f, g)$ is a [[contractible type]]. 

$$\mathrm{isUniquelyComposable}(x, y, z, f, g) \coloneqq\mathrm{isContr}\left(\mathrm{fiber}(p, (x, y, z, f, g))\right)$$

In this case, the unique morphism $h:\mathrm{hom}_A(x, z)$ such that $p(x, y, z, f, g, h) = (x, y, z, f, g)$ is said to be the **unique composite** of the morphisms $f$ and $g$. 

$$\mathrm{isUniqueComposite}(x, y, z, f, g, h) \coloneqq \mathrm{isUniquelyComposable}(x, y, z, f, g) \times (p(x, y, z, f, g, h) = (x, y, z, f, g))$$

## Related concepts

* [[hom-type]]

* [[Segal type]]

[[!redirects pair of composable morphisms]]
[[!redirects pairs of composable morphisms]]

[[!redirects type of pairs of composable morphisms]]
[[!redirects types of pairs of composable morphisms]]

[[!redirects composite of morphisms]]
[[!redirects composites of morphisms]]

[[!redirects composition of morphisms]]

[[!redirects type of composite of morphisms]]
[[!redirects types of composites of morphisms]]

[[!redirects uniquely composable]]

[[!redirects unique composite]]
[[!redirects unique composites]]

[[!redirects unique composition]]

[[!redirects unique composite of morphisms]]
[[!redirects unique composites of morphisms]]

[[!redirects unique composition of morphisms]]

[[!redirects composable morphisms]]