
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

An **$(\infty,1)$-product**  is a [[limit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of the shape

$$
  \{A \quad B\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cone]] $A \to A \sqcup B \leftarrow B$ which is [[universal property|universal]] among all such cones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[product]] in [[category theory]]. 

## Incarnations

### In model categories

* [[homotopy product]]

### In simplicial type theory

#### For Segal types

In [[simplicial type theory]], the [[Segal types]] are the types that represent [[precategory objects in an (infinity,1)-category|(infinity,1)-precategories]]. Let $A$ be a [[Segal type]] in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. The **$(\infty,1)$-product** of $x$ and $y$ is an tuple consisting of 

* an element $x \times y:A$, 

* a morphism $p_x:\mathrm{hom}_A(x \times y, x)$, 

* and a morphism $p_y:\mathrm{hom}_A(x \times y, y)$, 

such that for all $z:A$, $f:\mathrm{hom}_A(z, x)$, $g:\mathrm{hom}_A(z, y)$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(z, x \times y)$ such that $f = p_x \circ h(z, f, g)$ and $g = p_y \circ h(z, f, g)$. 

#### For arbitrary types

The notion of an $(\infty,1)$-product can be generalised from [[Segal types]] to arbitrary types in [[simplicial type theory]], which represent [[simplicial infinity-groupoids]]. In a [[Segal type]] $A$, given morphisms $f:\mathrm{hom}_A(x, y)$, $g:\mathrm{hom}_A(y, z)$, and $h:\mathrm{hom}_A(x, z)$, $g \circ f = h$ if and only if $h$ is the [[unique composite]] of $f$ and $g$. This means that we can use the latter condition in the definition of an $(\infty,1)$-product in types which are not Segal and thus do not have a composition function on morphisms. 

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. The **$(\infty,1)$-product** of $x$ and $y$ is an tuple consisting of 

* an element $x \times y:A$, 

* a morphism $p_x:\mathrm{hom}_A(x \times y, x)$, 

* and a morphism $p_y:\mathrm{hom}_A(x \times y, y)$, 

such that for all $z:A$, $f:\mathrm{hom}_A(z, x)$, $g:\mathrm{hom}_A(z, y)$, [[uniqueness quantifier|there exists a unique]] morphism $h(z, f, g):\mathrm{hom}_A(z, x \times y)$ such that $f$ is the [[unique composite]] of $p_x$ and $h(z, f, g)$ and $g$ is the [[unique composite]] of $p_y$ and $h(z, f, g)$. 

The fact that this definition works for any type $A$ implies that $(\infty,1)$-products should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]].  

## Related concepts

* [[product]]

* [[(infinity,1)-coproduct]]

* [[(infinity,1)-equalizer]]

* [[(infinity,1)-pullback]]

* [[(infinity,1)-limit]]

## References

* [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 5.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects (infinity,1)-product]]
[[!redirects (infinity,1)-products]]

[[!redirects (∞,1)-product]]
[[!redirects (∞,1)-products]]

[[!redirects product in an (infinity,1)-category]]
[[!redirects products in an (infinity,1)-category]]

[[!redirects product in an (∞,1)-category]]
[[!redirects products in an (∞,1)-category]]

[[!redirects product in simplicial type theory]]
[[!redirects products in simplicial type theory]]

[[!redirects product in a type]]
[[!redirects products in a type]]

[[!redirects product in a Segal type]]
[[!redirects products in a Segal type]]

[[!redirects product in a complete Segal type]]
[[!redirects products in a complete Segal type]]

[[!redirects product in a Rezk type]]
[[!redirects products in a Rezk type]]