
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

The concept of a [[coequalizer]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, coequalizers make sense for any type, not just the [[Segal types]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ be two morphisms from $x$ to $y$. The **coequalizer** of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{coeq}(f, g):A$, 

* a morphism $\mathrm{in}(f, g):\mathrm{hom}_A(y, \mathrm{coeq}(f, g))$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, \mathrm{coeq}(f, g))$ 

such that 

* $\mathrm{compin}(f, g)$ is the [[unique composite]] of $\mathrm{in}(f, g)$ and $f$ and the [[unique composite]] of $\mathrm{in}(f, g)$ and $g$, 

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(y, z)$ and $k:\mathrm{hom}_A(x, z)$ such that $k$ is the unique composite of $h$ and $f$ and the unique composite of $h$ and $g$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(\mathrm{coeq}(f, g), z)$ such that $h$ is the unique composite of $l(z, h, k)$ and $\mathrm{in}(f, g)$ and $k$ is the unique composite of  $l(z, h, k)$ and $\mathrm{compin}(f, g)$. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[coequalizer in an (infinity,1)-category]]: the *[[coequalizer]]* of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{coeq}(f, g):A$, 

* a morphism $\mathrm{in}(f, g):\mathrm{hom}_A(y, \mathrm{coeq}(f, g))$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, \mathrm{coeq}(f, g))$ 

such that 

$$\mathrm{in}(f, g) \circ f = \mathrm{compin}(f, g) \qquad \mathrm{and} \qquad \mathrm{in}(f, g) \circ g = \mathrm{compin}(f, g)$$

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(y, z)$ and $k:\mathrm{hom}_A(x, z)$ such that $k$ is the unique composite of $h$ and $f$ and the unique composite of $h$ and $g$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(\mathrm{coeq}(f, g), z)$ such that
$$h = l(z, h, k) \circ \mathrm{in}(f, g) \qquad \mathrm{and} \qquad k = l(z, h, k) \circ \mathrm{compin}(f, g)$$

## Related concepts

* [[simplicial type theory]]

* [[coequalizer]]

* [[coequalizer in an (infinity,1)-category]]

* [[equalizer in simplicial type theory]]

[[!redirects coequalizer in simplicial type theory]]
[[!redirects coequalizers in simplicial type theory]]
[[!redirects coequaliser in simplicial type theory]]
[[!redirects coequalisers in simplicial type theory]]

[[!redirects coequalizer in a Segal type]]
[[!redirects coequalizers in a Segal type]]
[[!redirects coequaliser in a Segal type]]
[[!redirects coequalisers in a Segal type]]

[[!redirects coequalizer in a complete Segal type]]
[[!redirects coequalizers in a complete Segal type]]
[[!redirects coequaliser in a complete Segal type]]
[[!redirects coequalisers in a complete Segal type]]

[[!redirects coequalizer in a Rezk type]]
[[!redirects coequalizers in a Rezk type]]
[[!redirects coequaliser in a Rezk type]]
[[!redirects coequalisers in a Rezk type]]