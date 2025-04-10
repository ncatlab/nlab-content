
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

The concept of a [[pushout]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, pushouts make sense for any type, not just the [[Segal types]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $x:A$, $y:A$, $z:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, z)$ be two morphisms. The **pushout** of $f$ and $g$ is an tuple consisting of 

* an element $x \sqcup^z_{f, g} y:A$, 

* a morphism $\mathrm{inl}(f, g):\mathrm{hom}_A(y, x \sqcup^z_{f, g} y)$, 

* a morphism $\mathrm{inr}(f, g):\mathrm{hom}_A(z, x \sqcup^z_{f, g} y)$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, x \sqcup^z_{f, g} y)$ 

such that 

* $\mathrm{compin}(f, g)$ is the [[unique composite]] of $\mathrm{inl}(f, g)$ and $f$ and the [[unique composite]] of $\mathrm{inr}(f, g)$ and $g$, 

* and for any other element $w:A$ with morphisms $h:\mathrm{hom}_A(y, w)$, $j:\mathrm{hom}_A(z, w)$, and $k:\mathrm{hom}_A(x, w)$ such that $k$ is the unique composite of $h$ and $f$ and the unique composite of $j$ and $g$, there exists a unique morphism $l(z, h, j, k):\mathrm{hom}_A(x \sqcup^z_{f, g} y, z)$ such that $h$ is the unique composite of $l(z, h, j, k)$ and $\mathrm{inl}(f, g)$, $j$ is the unique composite of $l(z, h, j, k)$ and $\mathrm{inr}(f, g)$, and $k$ is the unique composite of $l(z, h, j, k)$ and $\mathrm{compin}(f, g)$. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[pushout in an (infinity,1)-category]]: the *[[pushout]]* of $f$ and $g$ is an tuple consisting of 

* an element $x \sqcup^z_{f, g} y:A$, 

* a morphism $\mathrm{inl}(f, g):\mathrm{hom}_A(y, x \sqcup^z_{f, g} y)$, 

* a morphism $\mathrm{inr}(f, g):\mathrm{hom}_A(z, x \sqcup^z_{f, g} y)$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, x \sqcup^z_{f, g} y)$ 

such that 

$$\mathrm{inl}(f, g) \circ f = \mathrm{compin}(f, g) \qquad \mathrm{and} \qquad \mathrm{inr}(f, g) \circ g = \mathrm{compin}(f, g)$$

and for any other element $w:A$ with morphisms $h:\mathrm{hom}_A(y, w)$, $j:\mathrm{hom}_A(z, w)$, and $k:\mathrm{hom}_A(x, w)$ such that $k$ is the unique composite of $h$ and $f$ and the unique composite of $j$ and $g$, there exists a unique morphism $l(z, h, j, k):\mathrm{hom}_A(x \sqcup^z_{f, g} y, z)$ such that
$$h = l(z, h, j, k) \circ \mathrm{inl}(f, g) \qquad \mathrm{and} \qquad j = l(z, h, j, k) \circ \mathrm{inr}(f, g) \qquad \mathrm{and} \qquad k = l(z, h, j, k) \circ \mathrm{compin}(f, g)$$

## Related concepts

* [[simplicial type theory]]

* [[pushout]]

* [[pushout in an (infinity,1)-category]]

* [[pullback in simplicial type theory]]

[[!redirects pushout in simplicial type theory]]
[[!redirects pushouts in simplicial type theory]]

[[!redirects pushout in a Segal type]]
[[!redirects pushouts in a Segal type]]

[[!redirects pushout in a complete Segal type]]
[[!redirects pushouts in a complete Segal type]]

[[!redirects pushout in a Rezk type]]
[[!redirects pushouts in a Rezk type]]

[[!redirects pushforward in simplicial type theory]]
[[!redirects pushforwards in simplicial type theory]]

[[!redirects pushforward in a Segal type]]
[[!redirects pushforwards in a Segal type]]

[[!redirects pushforward in a complete Segal type]]
[[!redirects pushforwards in a complete Segal type]]

[[!redirects pushforward in a Rezk type]]
[[!redirects pushforwards in a Rezk type]]

[[!redirects cofiber coproduct in simplicial type theory]]
[[!redirects cofiber coproducts in simplicial type theory]]

[[!redirects cofiber coproduct in a Segal type]]
[[!redirects cofiber coproducts in a Segal type]]

[[!redirects cofiber coproduct in a complete Segal type]]
[[!redirects cofiber coproducts in a complete Segal type]]

[[!redirects cofiber coproduct in a Rezk type]]
[[!redirects cofiber coproducts in a Rezk type]]

[[!redirects cofibre coproduct in simplicial type theory]]
[[!redirects cofibre coproducts in simplicial type theory]]

[[!redirects cofibre coproduct in a Segal type]]
[[!redirects cofibre coproducts in a Segal type]]

[[!redirects cofibre coproduct in a complete Segal type]]
[[!redirects cofibre coproducts in a complete Segal type]]

[[!redirects cofibre coproduct in a Rezk type]]
[[!redirects cofibre coproducts in a Rezk type]]