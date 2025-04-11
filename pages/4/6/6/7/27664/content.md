
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

An **$(\infty,1)$-coequalizer**  is a [[colimit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of shape

$$
  \{ a \rightrightarrows b\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cocone]] 

$$
  \{ a \rightrightarrows b \to \mathrm{coeq}(a, b)\} \to \mathcal{C}
  \,.
$$

which is [[universal property|universal]] among all such cocones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[coequalizer]] in [[category theory]]. 

## Incarnations

### In model categories

* [[homotopy coequalizer]]

### In simplicial type theory

#### For Segal types

In [[simplicial type theory]], the [[Segal types]] are the types that represent [[precategory objects in an (infinity,1)-category|(infinity,1)-precategories]]. Let $A$ be a [[Segal type]] in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ be two morphisms from $x$ to $y$. The **$(\infty,1)$-coequalizer** of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{coeq}(f, g):A$, 

* a morphism $\mathrm{in}(f, g):\mathrm{hom}_A(y, \mathrm{coeq}(f, g))$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, \mathrm{coeq}(f, g))$ 

such that 

$$\mathrm{in}(f, g) \circ f = \mathrm{compin}(f, g) \qquad \mathrm{and} \qquad \mathrm{in}(f, g) \circ g = \mathrm{compin}(f, g)$$

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(y, z)$ and $k:\mathrm{hom}_A(x, z)$ such that $h \circ f = k$ and $j \circ g = k$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(\mathrm{coeq}(f, g), z)$ such that
$$h = l(z, h, k) \circ \mathrm{in}(f, g) \qquad \mathrm{and} \qquad k = l(z, h, k) \circ \mathrm{compin}(f, g)$$

#### For arbitrary types

The notion of an $(\infty,1)$-coequalizer can be generalised from [[Segal types]] to arbitrary types in [[simplicial type theory]], which represent [[simplicial infinity-groupoids]]. In a [[Segal type]] $A$, given morphisms $f:\mathrm{hom}_A(x, y)$, $g:\mathrm{hom}_A(y, z)$, and $h:\mathrm{hom}_A(x, z)$, $g \circ f = h$ if and only if $h$ is the [[unique composite]] of $f$ and $g$. This means that we can use the latter condition in the definition of an $(\infty,1)$-coequalizer in types which are not Segal and thus do not have a composition function on morphisms. 

Thus, let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, y)$ be two morphisms from $x$ to $y$. The **$(\infty,1)$-coequalizer** of $f$ and $g$ is an tuple consisting of 

* an element $\mathrm{coeq}(f, g):A$, 

* a morphism $\mathrm{in}(f, g):\mathrm{hom}_A(y, \mathrm{coeq}(f, g))$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, \mathrm{coeq}(f, g))$ 

such that 

* $\mathrm{compin}(f, g)$ is the [[unique composite]] of $\mathrm{in}(f, g)$ and $f$ and the [[unique composite]] of $\mathrm{in}(f, g)$ and $g$, 

* and for any other element $z:A$ with morphisms $h:\mathrm{hom}_A(y, z)$ and $k:\mathrm{hom}_A(x, z)$ such that $k$ is the unique composite of $h$ and $f$ and the unique composite of $h$ and $g$, there exists a unique morphism $l(z, h, k):\mathrm{hom}_A(\mathrm{coeq}(f, g), z)$ such that $h$ is the unique composite of $l(z, h, k)$ and $\mathrm{in}(f, g)$ and $k$ is the unique composite of  $l(z, h, k)$ and $\mathrm{compin}(f, g)$. 

The fact that this definition works for any type $A$ implies that $(\infty,1)$-coequalizers should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]]. 

## Related concepts

* [[coequalizer]]

* [[(infinity,1)-equalizer]]

* [[(infinity,1)-coproduct]]

* [[(infinity,1)-pushout]]

* [[(infinity,1)-colimit]]

## References

$(\infty,1)$-coequalizers are defined in:

* [[Jacob Lurie]], section 4.4.3 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

* [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 5.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects (infinity,1)-coequalizer]]
[[!redirects (infinity,1)-coequalizers]]

[[!redirects (∞,1)-coequalizer]]
[[!redirects (∞,1)-coequalizers]]

[[!redirects (infinity,1)-coequaliser]]
[[!redirects (infinity,1)-coequalisers]]

[[!redirects (∞,1)-coequaliser]]
[[!redirects (∞,1)-coequalisers]]

[[!redirects coequalizer in an (infinity,1)-category]]
[[!redirects coequalizers in an (infinity,1)-category]]

[[!redirects coequalizer in an (∞,1)-category]]
[[!redirects coequalizers in an (∞,1)-category]]

[[!redirects coequaliser in an (infinity,1)-category]]
[[!redirects coequalisers in an (infinity,1)-category]]

[[!redirects coequaliser in an (∞,1)-category]]
[[!redirects coequalisers in an (∞,1)-category]]

[[!redirects coequalizer in simplicial type theory]]
[[!redirects coequalizers in simplicial type theory]]
[[!redirects coequaliser in simplicial type theory]]
[[!redirects coequalisers in simplicial type theory]]

[[!redirects coequalizer in a type]]
[[!redirects coequalizers in a type]]
[[!redirects coequaliser in a type]]
[[!redirects coequalisers in a type]]

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