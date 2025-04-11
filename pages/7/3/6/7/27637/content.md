
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

An **$(\infty,1)$-coproduct**  is a [[colimit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of the shape

$$
  \{A \quad B\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cocone]] $A \to A \sqcup B \leftarrow B$ which is [[universal property|universal]] among all such cocones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[coproduct]] in [[category theory]]. 

## Incarnations

### In model categories

* [[homotopy coproduct]]

### In simplicial type theory

#### For Segal types

In simplicial type theory, the Segal types are the types that represent (infinity,1)-precategories. Let $A$ be a [[Segal type]] in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. The **$(\infty,1)$-coproduct** of $x$ and $y$ is an tuple consisting of 

* an element $x \sqcup y:A$, 

* a morphism $i_x:\mathrm{hom}_A(x, x \sqcup y)$, and 

* a morphism $i_y:\mathrm{hom}_A(y, x \sqcup y)$, 

such that for all $z:A$, $f:\mathrm{hom}_A(x, z)$, $g:\mathrm{hom}_A(y, z)$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(x \sqcup y, z)$ such that $f = h(z, f, g) \circ i_x$ and $g = h(z, f, g) \circ i_y$. 

#### For arbitrary types

The notion of an $(\infty,1)$-coproduct can be generalised from [[Segal types]] to arbitrary types in [[simplicial type theory]], which represent [[simplicial infinity-groupoids]]. In a [[Segal type]] $A$, given morphisms $f:\mathrm{hom}_A(x, y)$, $g:\mathrm{hom}_A(y, z)$, and $h:\mathrm{hom}_A(x, z)$, $g \circ f = h$ if and only if $h$ is the [[unique composite]] of $f$ and $g$. This means that we can use the latter condition in the definition of an $(\infty,1)$-coproduct in types which are not Segal and thus do not have a composition function on morphisms. 

Thus, let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. The **$(\infty,1)$-coproduct** of $x$ and $y$ is an tuple consisting of 

* an element $x \sqcup y:A$, 

* a morphism $i_x:\mathrm{hom}_A(x, x \sqcup y)$, and 

* a morphism $i_y:\mathrm{hom}_A(y, x \sqcup y)$, 

such that for all $z:A$, $f:\mathrm{hom}_A(x, z)$, $g:\mathrm{hom}_A(y, z)$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(x \sqcup y, z)$ such that $f$ is the [[unique composite]] of $h(z, f, g)$ and $i_x$ and $g$ is the [[unique composite]] of $h(z, f, g)$ and $i_y$. 

The fact that this definition works for any type $A$ implies that $(\infty,1)$-coproducts should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]]. 

## Related concepts

* [[coproduct]]

* [[(infinity,1)-product]]

* [[(infinity,1)-coequalizer]]

* [[(infinity,1)-pushout]]

* [[(infinity,1)-colimit]]

## References

$(\infty,1)$-coproducts are defined in: 

* [[Jacob Lurie]], section 4.4.1 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

* [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 5.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects (infinity,1)-coproduct]]
[[!redirects (infinity,1)-coproducts]]

[[!redirects (∞,1)-coproduct]]
[[!redirects (∞,1)-coproducts]]

[[!redirects coproduct in an (infinity,1)-category]]
[[!redirects coproducts in an (infinity,1)-category]]

[[!redirects coproduct in an (∞,1)-category]]
[[!redirects coproducts in an (∞,1)-category]]

[[!redirects coproduct in simplicial type theory]]
[[!redirects coproducts in simplicial type theory]]

[[!redirects coproduct in a type]]
[[!redirects coproducts in a type]]

[[!redirects coproduct in a Segal type]]
[[!redirects coproducts in a Segal type]]

[[!redirects coproduct in a complete Segal type]]
[[!redirects coproducts in a complete Segal type]]

[[!redirects coproduct in a Rezk type]]
[[!redirects coproducts in a Rezk type]]
