
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

In [[Euclidean geometry]], a **regular polygon** is a (simple, non self-intersecting) [[polygon]] in a [[Euclidean space]] $\mathbb{R}^n$ such that every [[segment]] of the [[boundary]] of the polygon has the same [[length]] and every [[angle]] between two segments of the boundary of the polygon has the same angle [[measure]]. (The boundary of a regular polygon is sometimes called called a **regular polygonal line**)

## Perimeter and area ##

We are using the [[circle constant]] $\tau = 2 \pi$. 

Every regular polygon is the union of $n$ congruent [[triangles]] each with segments of length $r$ and $r$ respectively and an angle of $\frac{\tau}{n}$ between the two segments of length $r$. As a result, the triangles are isosceles and the altitude from the center of the regular polygon to the third segment of the triangles bisects the angle: such that the angles between the [[circumradius]] and the altitude is $\frac{\tau}{2n}$. The length of the third segment is thus given by 

$$b \coloneqq r \sin\left(\frac{\tau}{2n}\right) + r \sin\left(\frac{\tau}{2n}\right) = 2 r \sin\left(\frac{\tau}{2n}\right)$$

The perimeter of a regular polygon $\mathcal{P}_n$ (strictly speaking, a regular polygonal line) with $n$ sides and [[circumradius]] $r$ is given by the sequence of functions $P_\mathcal{P}:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$

$$P_\mathcal{P}(n)(r) = n b = r (2 n) \sin\left(\frac{\tau}{2n}\right)$$

The area of a regular polygon $\mathcal{P}_n$ with $n$ sides and [[circumradius]] $r$ is given by the sequence of functions $P:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$

$$A_\mathcal{P}(n)(r) = n \left(\frac{1}{2} r b\right) = n \frac{1}{2} r (2 r) \sin\left(\frac{\tau}{2n}\right) = \frac{1}{2} r^2 (2 n) \sin\left(\frac{\tau}{2n}\right)$$

## See also ##

* [[polygon]]

* [[center of a regular polygon]]

* [[circumference of a circle]]

* [[area of a circle]]

## References 

* Wikipedia, _[Regular polygon](https://en.wikipedia.org/wiki/Regular_polygon)

[[!redirects regular polygons]]

[[!redirects regular polygonal line]]
[[!redirects regular polygonal lines]]
