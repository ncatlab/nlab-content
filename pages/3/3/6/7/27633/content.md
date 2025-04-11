
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

The concept of [[finitely cocomplete]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, finitely cocomplete makes sense for any type, not just the [[Segal types]]. 

## Definition

In [[simplicial type theory]], a type $A$ is **finitely cocomplete** if 

* $A$ has an [[initial object in simplicial type theory|initial object]] $0:A$

* There is a [[(infinity,1)-pushout|pushout]] $x \sqcup^z_{f, g} y:A$ for all elements $x:A$, $y:A$, $z:A$ and morphisms $f:\mathrm{hom}_A(z, x)$ and $g:\mathrm{hom}_A(z, y)$. 

Equivalently, type $A$ is **finitely cocomplete** if 

* $A$ has an [[initial object in simplicial type theory|initial object]] $0:A$

* There is a [[(infinity,1)-coproduct|coproduct]] $x \sqcup y:A$ for all elements $x:A$ and $y:A$

* There is a [[(infinity,1)-coequalizer|coequalizer]] $\mathrm{coeq}(f, g):A$ for all elements $x:A$ and $y:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$

If A is a [[Rezk type]] then this notion coincides with the usual notion of [[finitely cocomplete (infinity,1)-category]]. 

## Related concepts

* [[simplicial type theory]]

* [[finitely cocomplete]]

* [[finitely cocomplete (infinity,1)-category]]

* [[finitely complete type]]

[[!redirects finitely cocomplete type]]
[[!redirects finitely cocomplete types]]

[[!redirects finitely cocomplete Segal type]]
[[!redirects finitely cocomplete Segal types]]

[[!redirects finitely cocomplete complete Segal type]]
[[!redirects finitely cocomplete complete Segal types]]

[[!redirects finitely cocomplete Rezk type]]
[[!redirects finitely cocomplete Rezk types]]