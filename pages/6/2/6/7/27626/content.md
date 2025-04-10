
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

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. The **coproduct** of $x$ and $y$ is an tuple consisting of an element $x \coprod y:A$, a morphism $i_x:\mathrm{hom}_A(x, x \coprod y)$, and a morphism $i_y:\mathrm{hom}_A(y, x \coprod y)$, such that for all other tuples $(z:A, f:\mathrm{hom}_A(x, z), g:\mathrm{hom}_A(y, z))$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(z, x \coprod y)$ such that $f$ is the [[unique composite]] of $h(z, f, g)$ and $i_x$ and $g$ is the [[unique composite]] of $h(z, f, g)$ and $i_y$. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[coproduct in an (infinity,1)-category]]. 

## Related concepts

* [[simplicial type theory]]

* [[coproduct]]

* [[coproduct in an (infinity,1)-category]]

* [[product in simplicial type theory]]

[[!redirects coproduct in a Segal type]]
[[!redirects coproducts in a Segal type]]

[[!redirects coproduct in a complete Segal type]]
[[!redirects coproducts in a complete Segal type]]

[[!redirects coproduct in a Rezk type]]
[[!redirects coproducts in a Rezk type]]