## Using cross ratio

A quadruple of points $(A,B,C,D)$ is called [[harmonic ratio|harmonic]] if the [[cross ratio]] $(A,B;C,D) = -1$; points $C$ and $D$ are then called harmonic conjugates and $(A,B;D,C) = -1$ as well. We say that this ratio is harmonic and that the quadruple $(A,B,C,D)$ is harmonic. For this reason, the cross ratio in general is often called the anharmonic ratio as it measures the difference from the harmonic special case. 

## In synthetic terms

Harmonic conjugates can be characterized in geometric terms, as usually done in axiomatic approaches. 

To formulate this, recall that a [[complete quadrangle]] consists has 4 coplanar points called vertices no 3 of which are colinear and all 6 lines called sides which are incident with pairs of vertices. Two sides are opposite if they do not contain a common vertex. The three intersections of opposite sides are called diagonal points and the lines of the triangle incident with pairs of diagonal points are called the diagonal sides.

The following characterizations of harmonic quadruple of points are often cited ([Palman 1984](#Palman1984)).

1. If $A$ and $B$ are distinct vertices of a complete quadrangle, $C$ a diagonal point on the line $A B$ and $D$ the intersection of $A B$ with the line through other two diagonal points.

2. $A$ and $B$ are are the diagonal points of a complete rectangle, and $C$ and $D$ are the intersections of the line $A B$ with those mutually opposite sides of the complete rectangle which pass through the third diagonal point. 

$A B U V$ is a complete rectangle, $C,W,O$ are its diagonal points and hence $(A, B, C, D)$ is a harmonic quadruple, the [[cross ratio]] is $(A,B;C,D)=-1$.

[[!include harmonic svg1]]

For the second criterium, consider the complete quadrangle $O V W U$, then $A, B$ are two out of 3 diagonal points, the third pair of the mutually opposite sides in the criterium are $O W$ and $V U$ (their intersection is the third diagonal point).

Now, one has to prove that if one takes $A,B,C$ distinct points that there is a unique $D$ with above properties, that is the construction does not depend on the choice of the points $V$ and $O$ (or equivalently, $U$ and $V$). In the synthetic approach this means that the choice of points $U,V$ with $U,V,C$ colinear (or equivalently, the  choice of points $U, O$) does not affect the position of $D$ in the construction. This however uses the fact that the plane is [[Desarguesian]]. For the projective planes over a commutative field this is hence automatic. 

### A degenerate case of 6 intersection points of a quadrangle

Given any [[complete quadrangle]] and a line in the same projective plane, one can consider the 6 points of intersection of a line with sides of quadrangle and name it in this order: first 3 points, say $A,B,C$, are intersections with the 3 sides passing through a single vertex of the quadrangle, then $E,F,E$ are intersections of the 3 remaining sides opposite to the first 3 sides in the same order. The fact that the 6 points are obtained this way is denoted by $Q(A B C, D E F)$. If $A,B,C,D,E$ are fixed than $F$ can be determined uniquely (it does not depend on a choice of the quadrangle giving the first 5 points). There is a [[projective involution]] sending each of the 6 intersections of the line with a side of the quadrangle to the intersection of the line with the opposite side ([[Pappus' involution theorem]]).

If the line on which the 6-tuple is standing is one of the diagonals of the quadrangle, then two pairs of points coincide by the definition of the diagonal (e.g. $A=D$ and $B = E$) and the 6-tuple becomes 4-tuple which is moreover harmonic.

## Harmonic pencil

Dually, we can consider a pencil of lines through a fixed point. 4 lines in this pencil are in a harmonic ratio if
they by duality correspond to a harmonic 4-tuple of points in the dual projective plane of lines, but it can be characterized in many different ways including that the intersections of the 4 lines with one, and then automatically any other line not in the pencil are a harmonic 4-tuple of points. Thus to be harmonic is also an invariant under perspectivities. 

## Literature

Modern treatment is in Chapter 6 of 

* [[Marcel Berger]], _Géométrie_, Cassini (Engl. transl. Geometry I, Springer)

A synthetic treatment is for example in 

* {#Palman1984} Dominik Palman, _Projektivna geometrija_, Školska knjiga, Zagreb 1984.


category: geometry

[[!redirects harmonic conjugate]]
[[!redirects harmonic conjugates]]
[[!redirects harmonic quadruple]]
