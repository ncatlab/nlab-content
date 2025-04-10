
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

The concept of a [[equalizer]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, equalizers make sense for any type, not just the [[Segal types]]. 

## Definition

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ be two morphisms from $x$ to $y$. The **equalizer** of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{eq}(f, g):A$, 

* a morphism $\mathrm{out}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), x)$, 

* and a morphism $\mathrm{compout}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), y)$ 

such that 

* $\mathrm{compout}(f, g)$ is the [[unique composite]] of $f$ and $\mathrm{out}(f, g)$ and the [[unique composite]] of $g$ and $\mathrm{out}(f, g)$, 

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(z, x)$ and $k:\mathrm{hom}_A(z, y)$ such that $k$ is the unique composite of $f$ and $h$ and the unique composite of $g$ and $h$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(z, \mathrm{eq}(f, g))$ such that $h$ is the unique composite of $\mathrm{out}(f, g)$ and $l(z, h, k)$ and $k$ is the unique composite of $\mathrm{compout}(f, g)$ and $l(z, h, k)$. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of [[equalizer in an (infinity,1)-category]]: the *[[equalizer]]* of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{eq}(f, g):A$, 

* a morphism $\mathrm{out}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), x)$, 

* and a morphism $\mathrm{compout}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), y)$ 

such that 

$$f \circ \mathrm{out}(f, g) = \mathrm{compout}(f, g) \qquad \mathrm{and} \qquad g \circ \mathrm{out}(f, g) = \mathrm{compout}(f, g)$$

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(z, x)$ and $k:\mathrm{hom}_A(z, y)$ such that $f \circ h = k$ and $g \circ h = k$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(z, \mathrm{eq}(f, g))$ such that 
$$h = \mathrm{out}(f, g) \circ l(z, h, k) \qquad \mathrm{and} \qquad k = \mathrm{compout}(f, g) \circ l(z, h, k)$$

## Related concepts

* [[simplicial type theory]]

* [[equalizer]]

* [[equalizer in an (infinity,1)-category]]

* [[coequalizer in simplicial type theory]]

[[!redirects equalizer in simplicial type theory]]
[[!redirects equalizers in simplicial type theory]]
[[!redirects equaliser in simplicial type theory]]
[[!redirects equalisers in simplicial type theory]]

[[!redirects equalizer in a Segal type]]
[[!redirects equalizers in a Segal type]]
[[!redirects equaliser in a Segal type]]
[[!redirects equalisers in a Segal type]]

[[!redirects equalizer in a complete Segal type]]
[[!redirects equalizers in a complete Segal type]]
[[!redirects equaliser in a complete Segal type]]
[[!redirects equalisers in a complete Segal type]]

[[!redirects equalizer in a Rezk type]]
[[!redirects equalizers in a Rezk type]]
[[!redirects equaliser in a Rezk type]]
[[!redirects equalisers in a Rezk type]]