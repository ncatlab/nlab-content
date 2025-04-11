
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

An **$(\infty,1)$-coproduct**  is a [[colimit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of the shape

$$
  \{A \quad B\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cocone]] $A \to A \sqcup B \leftarrow B$ which is [[universal property|universal]] among all such cocones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[coproduct]] in [[category theory]]. 

## In simplicial type theory

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. Let $\mathrm{cospan}_A(x, y)$ denote the [[type of cospans in simplicial type theory|type of cospans]], and for [[cospan in simplicial type theory|cospans]] $f:\mathrm{cospan}_A(x, y)$ and $g:\mathrm{cospan}_A(x, y)$, let $\mathrm{homcospan}_A(x, y, f, g)$ denote the [[type of morphisms of cospans in simplicial type theory|type of morphisms of cospans]] between $f$ and $g$. The **$(\infty,1)$-coproduct** of $x$ and $y$ is a cospan $c:\mathrm{cospan}_A(x, y)$ such that for all other cospans $z:\mathrm{cospan}_A(x, y)$, the type of morphisms of cospans from $c$ to $z$ is a [[contractible type]]. The type of products is given by

$$\sum_{c:\mathrm{cospan}_A(x, y)} \prod_{z:\mathrm{cospan}_A(x, y)} \mathrm{isContr}(\mathrm{homcospan}_A(x, y, c, z))$$

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of coproduct in an $(\infty,1)$-category. However, the fact that this definition works for any type $A$ implies that $(\infty,1)$-coproducts should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]]. 

## Related concepts

* [[coproduct]]

* [[(infinity,1)-product]]

* [[(infinity,1)-pushout]]

* [[(infinity,1)-colimit]]

* [[cospan]], [[cospan in simplicial type theory]]

[[!redirects (infinity,1)-coproduct]]
[[!redirects (infinity,1)-coproducts]]

[[!redirects (∞,1)-coproduct]]
[[!redirects (∞,1)-coproducts]]

[[!redirects coproduct in an (infinity,1)-category]]
[[!redirects coproducts in an (infinity,1)-category]]

[[!redirects coproduct in an (∞,1)-category]]
[[!redirects coproducts in an (∞,1)-category]]

[[!redirects coproduct in simplicial type theory]]
[[!redirects coproducts in simplicial type theory]]

[[!redirects coproduct in a type]]
[[!redirects coproducts in a type]]

[[!redirects coproduct in a Segal type]]
[[!redirects coproducts in a Segal type]]

[[!redirects coproduct in a complete Segal type]]
[[!redirects coproducts in a complete Segal type]]

[[!redirects coproduct in a Rezk type]]
[[!redirects coproducts in a Rezk type]]