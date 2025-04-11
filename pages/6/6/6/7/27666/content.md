
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
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

\tableofcontents 

## Idea

An **$(\infty,1)$-equalizer**  is a [[limit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of shape

$$
  \{ a \rightrightarrows b\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cone]] 

$$
  \{\mathrm{eq}(a, b) \to a \rightrightarrows b\} \to \mathcal{C}
  \,.
$$

which is [[universal property|universal]] among all such cones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[equalizer]] in [[category theory]]. 

## Incarnations

### In model categories

* [[homotopy equalizer]]

### In simplicial type theory

#### For Segal types

In [[simplicial type theory]], the [[Segal types]] are the types that represent [[precategory objects in an (infinity,1)-category|(infinity,1)-precategories]]. Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ be two morphisms from $x$ to $y$. The **$(\infty,1)$-equalizer** of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{eq}(f, g):A$, 

* a morphism $\mathrm{out}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), x)$, 

* and a morphism $\mathrm{compout}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), y)$ 

such that 

$$f \circ \mathrm{out}(f, g) = \mathrm{compout}(f, g) \qquad \mathrm{and} \qquad g \circ \mathrm{out}(f, g) = \mathrm{compout}(f, g)$$

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(z, x)$ and $k:\mathrm{hom}_A(z, y)$ such that $f \circ h = k$ and $g \circ h = k$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(z, \mathrm{eq}(f, g))$ such that 
$$h = \mathrm{out}(f, g) \circ l(z, h, k) \qquad \mathrm{and} \qquad k = \mathrm{compout}(f, g) \circ l(z, h, k)$$

#### For arbitrary types

The notion of an $(\infty,1)$-equalizer can be generalised from [[Segal types]] to arbitrary types in [[simplicial type theory]], which represent [[simplicial infinity-groupoids]]. In a [[Segal type]] $A$, given morphisms $f:\mathrm{hom}_A(x, y)$, $g:\mathrm{hom}_A(y, z)$, and $h:\mathrm{hom}_A(x, z)$, $g \circ f = h$ if and only if $h$ is the [[unique composite]] of $f$ and $g$. This means that we can use the latter condition in the definition of an $(\infty,1)$-equalizer in types which are not Segal and thus do not have a composition function on morphisms. 

Thus, let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ be two morphisms from $x$ to $y$. The **$(\infty,1)$-equalizer** of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{eq}(f, g):A$, 

* a morphism $\mathrm{out}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), x)$, 

* and a morphism $\mathrm{compout}(f, g):\mathrm{hom}_A(\mathrm{eq}(f, g), y)$ 

such that 

* $\mathrm{compout}(f, g)$ is the [[unique composite]] of $f$ and $\mathrm{out}(f, g)$ and the [[unique composite]] of $g$ and $\mathrm{out}(f, g)$, 

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(z, x)$ and $k:\mathrm{hom}_A(z, y)$ such that $k$ is the unique composite of $f$ and $h$ and the unique composite of $g$ and $h$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(z, \mathrm{eq}(f, g))$ such that $h$ is the unique composite of $\mathrm{out}(f, g)$ and $l(z, h, k)$ and $k$ is the unique composite of $\mathrm{compout}(f, g)$ and $l(z, h, k)$.

The fact that this definition works for any type $A$ implies that $(\infty,1)$-equalizers should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]].  

## Related concepts

* [[equalizer]]

* [[(infinity,1)-coequalizer]]

* [[(infinity,1)-product]]

* [[(infinity,1)-pullback]]

* [[(infinity,1)-limit]]

## References

$(\infty,1)$-equalizers are defined in:

* [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 5.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects (infinity,1)-equalizer]]
[[!redirects (infinity,1)-equalizers]]

[[!redirects (∞,1)-equalizer]]
[[!redirects (∞,1)-equalizers]]

[[!redirects (infinity,1)-equaliser]]
[[!redirects (infinity,1)-equalisers]]

[[!redirects (∞,1)-equaliser]]
[[!redirects (∞,1)-equalisers]]

[[!redirects equalizer in an (infinity,1)-category]]
[[!redirects equalizers in an (infinity,1)-category]]

[[!redirects equalizer in an (∞,1)-category]]
[[!redirects equalizers in an (∞,1)-category]]

[[!redirects equaliser in an (infinity,1)-category]]
[[!redirects equalisers in an (infinity,1)-category]]

[[!redirects equaliser in an (∞,1)-category]]
[[!redirects equalisers in an (∞,1)-category]]

[[!redirects equalizer in simplicial type theory]]
[[!redirects equalizers in simplicial type theory]]
[[!redirects equaliser in simplicial type theory]]
[[!redirects equalisers in simplicial type theory]]

[[!redirects equalizer in a type]]
[[!redirects equalizers in a type]]
[[!redirects equaliser in a type]]
[[!redirects equalisers in a type]]

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