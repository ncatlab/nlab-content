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


[[!redirects commutative triangle]]
[[!redirects commutative triangles]]
