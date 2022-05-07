
#Contents#
* table of contents
{:toc}


## Idea

A __polygonal line__ is the union of segments $\overline{A_0 A_1}$, $\overline{A_1 A_2}, \ldots, \overline{A_{n-1} A_n}$ where
$n\in\mathbf{N}$ and $(A_0,A_1,\ldots, A_n)$ is an $(n+1)$-tuple of consecutively distinct points in an affine plane or in a $k$-dimensional [[affine space]]. A polygonal line is called 
__closed__ if $A_0 = A_n$ (regarding that consecutive points are distinct, this implies that $n\geq 2$). A closed polygonal line is __non-self-intersecting__ if for any $k \lt l$, $0\leq k\lt l \leq n-1$, $\overline{A_k A_{k+1}}\cap \overline{A_l A_{l+1}}= \emptyset$ except in the case $(k,l) = (0,n-1)$ when the intersection is $\{A_0\}$. A __simple closed (planar) polygonal line__ is a closed non-self-intersecting line which is in its entirety contained in some affine 2-plane. By Jordan's curve theorem, a complement of any simple closed polygonal line within its 2-plane has two components, one bounded and one unbounded. A __polygon__ is a set in an affine $k$-space ($k\geq 2$) which can be represented as a simple closed planar polygonal line union the bounded component of its complement within its 2-plane. The bounded and unbounded components of the complement of the corresponding polygonal line in its 2-plane are called the interior and the exterior of the polygon. For fixed $n$ we also say $n$-gon, and the points $A_1,\ldots, A_n$ are called the vertices of the polygon, the segments $\overline{A_1 A_2}, \ldots, \overline{A_{n-1} A_n}, \overline{A_n A_1}$ are called the __edges__ or the sides of the polygon. 

Often one restricts further and also requires that no 2 consecutive edges of a polygon are on the same line (equivalently, no 3 consecutive vertices are on the same line).  

A diagonal of an $n$-gon is a segment from $A_k$ to $A_l$ when $|k-l|\gt 1$.

In other geometries instead of segments we may consider segments on geodesical lines, so we can talk about $n$-gones in spherical and non-Euclidean geometries. 

For some related ideas see [[polyhedron]].

(...)

## Discussion

A 3-gon is also called a triangle and it may be alternatively defined as the smallest convex set containing 3 non-colinear points. This definition does not rely on the Jordan's curve theorem (for which anyway we just need a more elementary case of simple closed polygonal lines).  Sometimes, by a polygon one means its boundary, that is a simple closed polygonal line, then no need to consider the interior. 
$n$-gons for $n\geq 4$ an $n$-gon may be convex or nonconvex.
If it is convex there is seemingly no need for the considerations of (the polygonal case of) Jordan's curve theorem for considering the interior as we can take a convex hull. But how to make a simple criterium without consideration of interior when an $n$-gon is convex ?  In nonconvex/general case, one may resort to subdivision (of would-be interior) into triangles, what is simple in examples, but intricate in full generality. 

## Examples

Convex regular polgyons:

* [[triangle]]

* [[square]]

* [[pentagon]]

* [[hexagon]]

* ...

## Related pages

* [[tesselation]]

* [[scissors congruence]]

* [[dihedral group]]

* [[dihedron]]

## References

* Wikipedia, _[Polygon](https://en.wikipedia.org/wiki/Polygon)_

* Wikipedia, _[Regular polygon](https://en.wikipedia.org/wiki/Regular_polygon)

* Jeff Erickson, _Jordan polygon theorem_, from notes for a combinatorial topology course in 2009, [pdf](https://jeffe.cs.illinois.edu/teaching/comptop/2009/notes/jordan-polygon-theorem.pdf)
* M. Shimrat, _Algorithm 112: Position of point relative to polygon_, Commun. ACM 5(8):434, 1962 [doi](https://doi.org/10.1145/368637.368653); R. Hacker, _Certification of Algorithm 112: Position of point relative to polygon_, Commun. ACM 5(12):606, 1962


[[!redirects polygons]]

[[!redirects regular polygon]]
[[!redirects regular polygons]]
