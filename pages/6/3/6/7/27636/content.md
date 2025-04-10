
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

The concept of a [[pullback]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, pullbacks make sense for any type, not just the [[Segal types]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $x:A$, $y:A$, $z:A$ be three elements in $A$ and let $f:\mathrm{hom}_A(x, z)$ and $g:\mathrm{hom}_A(y, z)$ be two morphisms. The **pullback** of $f$ and $g$ is an tuple consisting of 

* an element $x \times_z^{f,g} y:A$, 

* a morphism $\mathrm{outl}(f, g):\mathrm{hom}_A(x \times_z^{f,g} y, x)$, 

* a morphism $\mathrm{outr}(f, g):\mathrm{hom}_A(x \times_z^{f,g} y, y)$, 

* and a morphism $\mathrm{compout}(f, g):\mathrm{hom}_A(x \times_z^{f,g} y, z)$ 

such that 

* $\mathrm{compout}(f, g)$ is the [[unique composite]] of $f$ and $\mathrm{outl}(f, g)$ and the [[unique composite]] of $g$ and $\mathrm{outr}(f, g)$, 

* and for any other element $w:A$ with morphisms $h:\mathrm{hom}_A(w, x)$, $j:\mathrm{hom}_A(w, y)$ and $k:\mathrm{hom}_A(w, z)$ such that $k$ is the unique composite of $f$ and $h$ and the unique composite of $g$ and $j$, there exists a unique morphism $l(z, h, j, k):\mathrm{hom}_A(z, x \times_z^{f,g} y)$ such that $h$ is the unique composite of $\mathrm{outl}(f, g)$ and $l(z, h, j, k)$, $j$ is the unique composite of $\mathrm{outr}(f, g)$ and $l(z, h, j, k)$, and $k$ is the unique composite of $\mathrm{compout}(f, g)$ and $l(z, h, j, k)$. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[pullback in an (infinity,1)-category]]: the *pullback* of $f$ and $g$ is an tuple consisting of 

* an element $x \times_z^{f,g} y:A$, 

* a morphism $\mathrm{outl}(f, g):\mathrm{hom}_A(x \times_z^{f,g} y, x)$, 

* a morphism $\mathrm{outr}(f, g):\mathrm{hom}_A(x \times_z^{f,g} y, y)$, 

* and a morphism $\mathrm{compout}(f, g):\mathrm{hom}_A(x \times_z^{f,g} y, z)$ 

such that 

$$f \circ \mathrm{outl}(f, g) = \mathrm{compout}(f, g) \qquad \mathrm{and} \qquad g \circ \mathrm{outr}(f, g) = \mathrm{compout}(f, g)$$

* and for any other element $w:A$ with morphisms $h:\mathrm{hom}_A(w, x)$, $j:\mathrm{hom}_A(w, y)$ and $k:\mathrm{hom}_A(w, z)$ such that $k$ is the unique composite of $f$ and $h$ and the unique composite of $g$ and $j$, there exists a unique morphism $l(z, h, j, k):\mathrm{hom}_A(z, x \times_z^{f,g} y)$ such that
$$h = \mathrm{outl}(f, g) \circ l(z, h, j, k) \qquad \mathrm{and} \qquad j = \mathrm{outr}(f, g) \circ l(z, h, j, k) \qquad \mathrm{and} \qquad k = \mathrm{compout}(f, g) \circ l(z, h, j, k)$$

## Related concepts

* [[simplicial type theory]]

* [[pullback]]

* [[pullback in an (infinity,1)-category]]

* [[pushout in simplicial type theory]]

[[!redirects pullback in simplicial type theory]]
[[!redirects pullbacks in simplicial type theory]]

[[!redirects pullback in a Segal type]]
[[!redirects pullbacks in a Segal type]]

[[!redirects pullback in a complete Segal type]]
[[!redirects pullbacks in a complete Segal type]]

[[!redirects pullback in a Rezk type]]
[[!redirects pullbacks in a Rezk type]]

[[!redirects fiber product in simplicial type theory]]
[[!redirects fiber products in simplicial type theory]]

[[!redirects fiber product in a Segal type]]
[[!redirects fiber products in a Segal type]]

[[!redirects fiber product in a complete Segal type]]
[[!redirects fiber products in a complete Segal type]]

[[!redirects fiber product in a Rezk type]]
[[!redirects fiber products in a Rezk type]]

[[!redirects fibre product in simplicial type theory]]
[[!redirects fibre products in simplicial type theory]]

[[!redirects fibre product in a Segal type]]
[[!redirects fibre products in a Segal type]]

[[!redirects fibre product in a complete Segal type]]
[[!redirects fibre products in a complete Segal type]]

[[!redirects fibre product in a Rezk type]]
[[!redirects fibre products in a Rezk type]]