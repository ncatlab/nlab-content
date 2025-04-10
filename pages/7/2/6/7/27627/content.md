
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

## Idea

The concept of a categorical [[product]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, categorical products make sense for any type, not just the [[Segal types]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. Let $\mathrm{span}_A(x, y)$ denote the [[type of spans in simplicial type theory|type of spans]], and for [[span in simplicial type theory|spans]] $f:\mathrm{span}_A(x, y)$ and $g:\mathrm{span}_A(x, y)$, let $\mathrm{homspan}_A(x, y, f, g)$ denote the [[type of morphisms of spans in simplicial type theory|type of morphisms of spans]] between $f$ and $g$. The **product** of $x$ and $y$ is a span $p:\mathrm{span}_A(x, y)$ such that for all other spans $z:\mathrm{span}_A(x, y)$, the type of morphisms of spans from $z$ to $p$ is a [[contractible type]]. The type of products is given by

$$\sum_{p:\mathrm{span}_A(x, y)} \prod_{z:\mathrm{span}_A(x, y)} \mathrm{isContr}(\mathrm{homspan}_A(x, y, z, p))$$

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[product in an (infinity,1)-category]]. 

## Related concepts

* [[simplicial type theory]]

* [[product]]

* [[product in an (infinity,1)-category]]

* [[coproduct in simplicial type theory]]

* [[span in simplicial type theory]]

[[!redirects product in simplicial type theory]]
[[!redirects products in simplicial type theory]]

[[!redirects product in a Segal type]]
[[!redirects products in a Segal type]]

[[!redirects product in a complete Segal type]]
[[!redirects products in a complete Segal type]]

[[!redirects product in a Rezk type]]
[[!redirects products in a Rezk type]]