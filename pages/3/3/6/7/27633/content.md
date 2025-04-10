
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

* $A$ has an [[initial object in simplicial type theory|terminal object]] $0:A$

* All elements $x:A$ and $y:A$ have a [[coproduct in simplicial type theory|coproduct]] $x \coprod y:A$

* All elements $x:A$ and $y:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ have an [[coequalizer in simplicial type theory|coequalizer]] $\mathrm{coeq}(f, g):A$

If A is a [[Segal type]] then this notion coincides with the usual notion of [[finitely cocomplete (infinity,1)-category]]. 

## Related concepts

* [[simplicial type theory]]

* [[finitely cocomplete]]

* [[finitely cocomplete (infinity,1)-category]]

* [[finitely complete type]]

[[!redirects finitely cocomplete type]]
[[!redirects finitely cocomplete types]]