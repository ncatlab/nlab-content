
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Commutative triangles
* table of contents
{: toc}

## Definition

Let $C$ be a [[category]]. A **triangle** of morphisms of $C$ consists of objects $X,Y,Z$ of $C$ and morphisms $f\colon X \to Y$, $g\colon Y \to Z$, and $h\colon X \to Z$. This is often pictured as a triangle
$$ \array {
  X & \overset{f}\rightarrow & Y \\
    & \searrow^{h}           & \downarrow^{g} \\
    &                        & Z
} $$

The triangle is **[[commutative diagram|commutative]]** if $h = g \circ f$.

## Characterisation

A commutative triangle is determined entirely by $f$ and $g$; therefore, a commutative triangle is equivalent to a [[composable pair]] of morphisms.

Accordingly, one rarely hears of commutative triangles on their own; instead, the concept only comes up when one already has a triangle and asks whether it commutes.  (This is different from the situation with [[commutative squares]].)

## The walking commutative triangle

The **[[walking]] [[commutative triangle]]** or **[[2-simplex]] category** is the category $\Delta^2$ which consists of three objects $0, 1, 2 \in \Delta^2$ and three morphisms $h_{01}:\mathrm{hom}_{\Delta^2}(0, 1)$, $h_{02}:\mathrm{hom}_{\Delta^2}(0, 2)$, $h_{12}:\mathrm{hom}_{\Delta^2}(1, 2)$, such that $h_{02} = h_{12} \circ h_{01}$.

Every commutative triangle in a category $C$ is represented by a [[functor]] $F:\Delta^2 \to C$ from the walking commutative triangle to $C$. 

## Related concepts

* [[walking structure]]

  * [[walking pair of objects]]

  * [[walking morphism]]

  * [[walking parallel pair]]

  * **walking commutative triangle**

  * [[walking isomorphism]]

  * [[walking equivalence]]

* [[2-simplex]]

## References

The phrase "walking commutative triangle" appears in:

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.5.1 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects commutative triangle]]
[[!redirects commutative triangles]]

[[!redirects walking commutative triangle]]
[[!redirects walking commutative triangles]]

[[!redirects walking commutative triangle category]]
[[!redirects walking commutative triangle categories]]

[[!redirects free-standing commutative triangle]]
[[!redirects free-standing commutative triangles]]

[[!redirects free-standing commutative triangle category]]
[[!redirects free-standing commutative triangle categories]]

[[!redirects free-living commutative triangle]]
[[!redirects free-living commutative triangles]]

[[!redirects free-living commutative triangle category]]
[[!redirects free-living commutative triangle categories]]

[[!redirects 2-simplex category]]
[[!redirects 2-simplex categories]]