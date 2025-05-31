
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
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

$f$ and $g$ are the [[composable pair of morphisms]] of a commutative triangle, and $h$ is the **composite** or **unique composite** of the morphisms $f$ and $g$ in the commutative triangle. 

Equivalently, every **commutative triangle** in a category $C$ is represented by a [[functor]] $F:\Delta^2 \to C$ from the [[triangle category]] $\Delta^2$ to $C$. 

## Characterization

A commutative triangle is determined entirely by $f$ and $g$; therefore, a commutative triangle is equivalent to a [[composable pair]] of morphisms.

Accordingly, one rarely hears of commutative triangles on their own; instead, the concept only comes up when one already has a triangle and asks whether it commutes.  (This is different from the situation with [[commutative squares]].)

## Related concepts

* [[triangle category]]

* [[triangle]], [[2-simplex]]

* [[composable pair]]

* [[composite of morphisms]]

## References

The phrase "commutative triangle" appears in:

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.5.1 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects commutative triangle]]
[[!redirects commutative triangles]]