
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

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. The **product** of $x$ and $y$ is an tuple consisting of 

* an element $x \times y:A$, 

* a morphism $p_x:\mathrm{hom}_A(x \times y, x)$, 

* and a morphism $p_y:\mathrm{hom}_A(x \times y, y)$, 

such that for all $z:A$, $f:\mathrm{hom}_A(z, x)$, $g:\mathrm{hom}_A(z, y)$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(z, x \times y)$ such that $f$ is the [[unique composite]] of $p_x$ and $h(z, f, g)$ and $g$ is the [[unique composite]] of $p_y$ and $h(z, f, g)$. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[product in an (infinity,1)-category]]: the *product* of $x$ and $y$ is an tuple consisting of 

* an element $x \times y:A$, 

* a morphism $p_x:\mathrm{hom}_A(x \times y, x)$, 

* and a morphism $p_y:\mathrm{hom}_A(x \times y, y)$, 

such that for all $z:A$, $f:\mathrm{hom}_A(z, x)$, $g:\mathrm{hom}_A(z, y)$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(z, x \times y)$ such that $f = p_x \circ h(z, f, g)$ and $g = p_y \circ h(z, f, g)$. 

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