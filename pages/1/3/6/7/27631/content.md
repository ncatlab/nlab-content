
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

The concept of [[finitely complete]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, finitely complete makes sense for any type, not just the [[Segal types]]. 

## Definition

In [[simplicial type theory]], a type $A$ is a [[finitely complete]] if 

* $A$ has a [[terminal object in simplicial type theory|terminal object]] $1:A$

* All elements $x:A$ and $y:A$ have a [[product in simplicial type theory|product]] $x \times y:A$

* All elements $x:A$ and $y:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ have an [[equalizer in simplicial type theory|equalizer]] $\mathrm{eq}(f, g):A$

If A is a [[Segal type]] then this notion coincides with the usual notion of [[finitely complete (infinity,1)-category]]. 

## Related concepts

* [[simplicial type theory]]

* [[finitely complete]]

* [[finitely complete (infinity,1)-category]]

[[!redirects finitely complete type]]
[[!redirects finitely complete types]]