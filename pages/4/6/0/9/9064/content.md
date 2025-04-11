
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

An **$(\infty,1)$-pushout**  is a [[colimit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of the shape

$$
  \{a \leftarrow c \to b\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cocone]]

$$
  \array{
    C &\to& B
    \\
    \downarrow &\cong\swArrow& \downarrow
    \\
    A &\to& A \sqcup_C B
  }
$$

which is [[universal property|universal]] among all such cocones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[pushout]] in [[category theory]]. 

## Incarnations

### In model categories

* [[homotopy pushout]]

### In simplicial type theory

#### For Segal types

In [[simplicial type theory]], the [[Segal types]] are the types that represent [[precategory objects in an (infinity,1)-category|(infinity,1)-precategories]]. Let $A$ be a [[Segal type]] in [[simplicial type theory]], and let $x:A$, $y:A$, $z:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, z)$ be two morphisms. The **$(\infty,1)$-pushout** of $f$ and $g$ is an tuple consisting of 

* an element $x \sqcup^z_{f, g} y:A$, 

* a morphism $\mathrm{inl}(f, g):\mathrm{hom}_A(y, x \sqcup^z_{f, g} y)$, 

* a morphism $\mathrm{inr}(f, g):\mathrm{hom}_A(z, x \sqcup^z_{f, g} y)$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, x \sqcup^z_{f, g} y)$ 

such that 

$$\mathrm{inl}(f, g) \circ f = \mathrm{compin}(f, g) \qquad \mathrm{and} \qquad \mathrm{inr}(f, g) \circ g = \mathrm{compin}(f, g)$$

and for any other element $w:A$ with morphisms $h:\mathrm{hom}_A(y, w)$, $j:\mathrm{hom}_A(z, w)$, and $k:\mathrm{hom}_A(x, w)$ such that $h \circ f = k$ and $j \circ g = k$, there exists a unique morphism $l(z, h, j, k):\mathrm{hom}_A(x \sqcup^z_{f, g} y, z)$ such that
$$h = l(z, h, j, k) \circ \mathrm{inl}(f, g) \qquad \mathrm{and} \qquad j = l(z, h, j, k) \circ \mathrm{inr}(f, g) \qquad \mathrm{and} \qquad k = l(z, h, j, k) \circ \mathrm{compin}(f, g)$$

#### For arbitrary types

The notion of an $(\infty,1)$-pushout can be generalised from [[Segal types]] to arbitrary types in [[simplicial type theory]], which represent [[simplicial infinity-groupoids]]. In a [[Segal type]] $A$, given morphisms $f:\mathrm{hom}_A(x, y)$, $g:\mathrm{hom}_A(y, z)$, and $h:\mathrm{hom}_A(x, z)$, $g \circ f = h$ if and only if $h$ is the [[unique composite]] of $f$ and $g$. This means that we can use the latter condition in the definition of an $(\infty,1)$-pushout in types which are not Segal and thus do not have a composition function on morphisms. 

Thus, let $A$ be a type in [[simplicial type theory]], and let $x:A$, $y:A$, $z:A$ be two elements in $A$ and let $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(x, z)$ be two morphisms. The **$(\infty,1)$-pushout** of $f$ and $g$ is an tuple consisting of 

* an element $x \sqcup^z_{f, g} y:A$, 

* a morphism $\mathrm{inl}(f, g):\mathrm{hom}_A(y, x \sqcup^z_{f, g} y)$, 

* a morphism $\mathrm{inr}(f, g):\mathrm{hom}_A(z, x \sqcup^z_{f, g} y)$, 

* and a morphism $\mathrm{compin}(f, g):\mathrm{hom}_A(x, x \sqcup^z_{f, g} y)$ 

such that 

* $\mathrm{compin}(f, g)$ is the [[unique composite]] of $\mathrm{inl}(f, g)$ and $f$ and the [[unique composite]] of $\mathrm{inr}(f, g)$ and $g$, 

* and for any other element $w:A$ with morphisms $h:\mathrm{hom}_A(y, w)$, $j:\mathrm{hom}_A(z, w)$, and $k:\mathrm{hom}_A(x, w)$ such that $k$ is the unique composite of $h$ and $f$ and the unique composite of $j$ and $g$, there exists a unique morphism $l(z, h, j, k):\mathrm{hom}_A(x \sqcup^z_{f, g} y, z)$ such that $h$ is the unique composite of $l(z, h, j, k)$ and $\mathrm{inl}(f, g)$, $j$ is the unique composite of $l(z, h, j, k)$ and $\mathrm{inr}(f, g)$, and $k$ is the unique composite of $l(z, h, j, k)$ and $\mathrm{compin}(f, g)$. 

The fact that this definition works for any type $A$ implies that $(\infty,1)$-pushouts should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]]. 

## Related concepts

* [[pushout]]

* [[(infinity,1)-pullback]]

* [[(infinity,1)-coproduct]]

* [[(infinity,1)-coequalizer]]

* [[(infinity,1)-colimit]]

## References

$(\infty,1)$-pushouts are defined in:

* [[Jacob Lurie]], section 4.4.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

* [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 5.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects (infinity,1)-pushout]]
[[!redirects (infinity,1)-pushouts]]

[[!redirects (∞,1)-pushout]]
[[!redirects (∞,1)-pushouts]]

[[!redirects (infinity,1)-pushforward]]
[[!redirects (infinity,1)-pushforwards]]

[[!redirects (∞,1)-pushforward]]
[[!redirects (∞,1)-pushforwards]]

[[!redirects (infinity,1)-cofiber coproduct]]
[[!redirects (infinity,1)-cofiber coproducts]]

[[!redirects (∞,1)-cofiber coproduct]]
[[!redirects (∞,1)-cofiber coproducts]]

[[!redirects (infinity,1)-cofibre coproduct]]
[[!redirects (infinity,1)-cofibre coproducts]]

[[!redirects (∞,1)-cofibre coproduct]]
[[!redirects (∞,1)-cofibre coproducts]]

[[!redirects pushout in an (infinity,1)-category]]
[[!redirects pushouts in an (infinity,1)-category]]

[[!redirects pushout in an (∞,1)-category]]
[[!redirects pushouts in an (∞,1)-category]]

[[!redirects pushforward in an (infinity,1)-category]]
[[!redirects pushforwards in an (infinity,1)-category]]

[[!redirects pushforward in an (∞,1)-category]]
[[!redirects pushforwards in an (∞,1)-category]]

[[!redirects cofiber coproduct in an (infinity,1)-category]]
[[!redirects cofiber coproducts in an (infinity,1)-category]]

[[!redirects cofiber coproduct in an (∞,1)-category]]
[[!redirects cofiber coproducts in an (∞,1)-category]]

[[!redirects cofibre coproduct in an (infinity,1)-category]]
[[!redirects cofibre coproducts in an (infinity,1)-category]]

[[!redirects cofibre coproduct in an (∞,1)-category]]
[[!redirects cofibre coproducts in an (∞,1)-category]]

[[!redirects pushout in simplicial type theory]]
[[!redirects pushouts in simplicial type theory]]

[[!redirects pushout in a type]]
[[!redirects pushouts in a type]]

[[!redirects pushout in a Segal type]]
[[!redirects pushouts in a Segal type]]

[[!redirects pushout in a complete Segal type]]
[[!redirects pushouts in a complete Segal type]]

[[!redirects pushout in a Rezk type]]
[[!redirects pushouts in a Rezk type]]

[[!redirects pushforward in simplicial type theory]]
[[!redirects pushforwards in simplicial type theory]]

[[!redirects pushforward in a type]]
[[!redirects pushforwards in a type]]

[[!redirects pushforward in a Segal type]]
[[!redirects pushforwards in a Segal type]]

[[!redirects pushforward in a complete Segal type]]
[[!redirects pushforwards in a complete Segal type]]

[[!redirects pushforward in a Rezk type]]
[[!redirects pushforwards in a Rezk type]]

[[!redirects cofiber coproduct in simplicial type theory]]
[[!redirects cofiber coproducts in simplicial type theory]]

[[!redirects cofiber coproduct in a type]]
[[!redirects cofiber coproducts in a type]]

[[!redirects cofiber coproduct in a Segal type]]
[[!redirects cofiber coproducts in a Segal type]]

[[!redirects cofiber coproduct in a complete Segal type]]
[[!redirects cofiber coproducts in a complete Segal type]]

[[!redirects cofiber coproduct in a Rezk type]]
[[!redirects cofiber coproducts in a Rezk type]]

[[!redirects cofibre coproduct in simplicial type theory]]
[[!redirects cofibre coproducts in simplicial type theory]]

[[!redirects cofibre coproduct in a type]]
[[!redirects cofibre coproducts in a type]]

[[!redirects cofibre coproduct in a Segal type]]
[[!redirects cofibre coproducts in a Segal type]]

[[!redirects cofibre coproduct in a complete Segal type]]
[[!redirects cofibre coproducts in a complete Segal type]]

[[!redirects cofibre coproduct in a Rezk type]]
[[!redirects cofibre coproducts in a Rezk type]]