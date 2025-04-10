
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

The concept of a [[coproduct]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, coproducts make sense for any type, not just the [[Segal types]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. Let $\mathrm{cospan}_A(x, y)$ denote the [[type of cospans in simplicial type theory|type of cospans]], and for [[cospan in simplicial type theory|cospans]] $f:\mathrm{cospan}_A(x, y)$ and $g:\mathrm{cospan}_A(x, y)$, let $\mathrm{homcospan}_A(x, y, f, g)$ denote the [[type of morphisms of cospans in simplicial type theory|type of morphisms of cospans]] between $f$ and $g$. The **coproduct** of $x$ and $y$ is a cospan $c:\mathrm{cospan}_A(x, y)$ such that for all other cospans $z:\mathrm{cospan}_A(x, y)$, the type of morphisms of cospans from $c$ to $z$ is a [[contractible type]]. The type of products is given by

$$\sum_{c:\mathrm{cospan}_A(x, y)} \prod_{z:\mathrm{cospan}_A(x, y)} \mathrm{isContr}(\mathrm{homspan}_A(x, y, c, z))$$

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[coproduct in an (infinity,1)-category]]. 

## Related concepts

* [[simplicial type theory]]

* [[coproduct]]

* [[coproduct in an (infinity,1)-category]]

* [[product in simplicial type theory]]

* [[cospan in simplicial type theory]]

[[!redirects coproduct in simplicial type theory]]
[[!redirects coproducts in simplicial type theory]]

[[!redirects coproduct in a Segal type]]
[[!redirects coproducts in a Segal type]]

[[!redirects coproduct in a complete Segal type]]
[[!redirects coproducts in a complete Segal type]]

[[!redirects coproduct in a Rezk type]]
[[!redirects coproducts in a Rezk type]]
