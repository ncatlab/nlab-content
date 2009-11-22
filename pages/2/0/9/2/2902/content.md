#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Suppose we inscribe a regular pentagon, a regular decagon, and a regular hexagon in circles of the same radius.  If we denote the respective edge lengths of these polygons by $P$, $D$ and $H$, then these lengths will satisfy the identity:

$$P^2=D^2+H^2$$

This means that the edges of a pentagon, decagon and hexagon of identical radii can fit together to form a right triangle.

#Euclid's proof#

Euclid gave a proof of this identity in his <i>Elements</i>, as Euclid as [Proposition 10](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII10.html) of Book XIII.  The essence of this proof can be understood if we take for granted the numerical values of the various angles in his construction, which are easily established.

[[!include pentagon decagon hexagon identity/Euclid]]

The line segment $A B$ is one edge of a pentagon inscribed in a circle centred at $F$, and $A K$ and $K B$ are edges of a decagon inscribed in the same circle.  Note that while $A B$ is bisected by $H$ and $A K$ is bisected by $L$, the point $N$ is _not_ a point of bisection of $A H$.

Triangle $A B F$ is similar to triangle $B F N$.  So $\frac{A B}{B F}=\frac{B F}{F N}=\frac{B F}{B N}$, with the last equality true because the triangles are isosceles with $F N = B N$.  Thus ${B F}^2={A B}\cdot{B N}$.

Triangle $B A K$ is similar to triangle $K A N$.  So $\frac{B A}{A K}=\frac{K A}{A N}$.  Thus ${A K}^2={A B}\cdot{A N}$.

Adding our two results, we have:
${B F}^2+{A K}^2={A B}\cdot(A N + B N)={A B}^2$.

$B F$ is our radius (or equivalently, the length of one side of a hexagon inscribed in the same circle), $A K$ is a decagon side, and $A B$ is a pentagon side.  So we have established the pentagon-decagon-hexagon identity.

#Other proofs#

We present two other proofs of the identity.  Both of these rely on a lemma concerning the ratio of sides in a "golden triangle".

##Golden triangle lemma##

[[!include pentagon decagon hexagon identity/golden triangle]]

The lemma states that in any isosceles triangle with angles of 72&deg;, 36&deg; and 72&deg;, the ratio of the long sides of the triangle to its base is $\Phi$, the golden ratio, which is defined as the unique positive solution of the equation:

$$1+\frac{1}{\Phi}=\Phi$$

Note that some authors call "the golden ratio" the reciprocal of the number we're calling $\Phi$.  For the purpose of this article, $\Phi=\frac{\sqrt{5}+1}{2}\approx 1.61803$.

In the diagram above, triangle $B D E$ is similar to triangle $B E C$.  So:

$$\frac{B D}{B E}=\frac{B E}{B C}$$
$$\frac{r+t}{r}=\frac{r}{t}$$
$$1+\frac{t}{r}=\frac{r}{t}$$

By the definition of the golden ratio, $\frac{r}{t}=\Phi$.

This lemma was given by Euclid as [Proposition 9](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII9.html).

##Proof from an identity for the golden ratio##

[[!include pentagon decagon hexagon identity/golden ratio]]

By the golden triangle lemma for isosceles triangles with angles of 36&deg;, triangle $N O P$ gives us $r=t\Phi$.  From the same rule for triangle $N M P$ glued to its mirror image in the line $N M$ we have $2b=t/\Phi$.

From the right triangle $N M P$ we have $s^2=t^2-b^2$, hence $(2s)^2=4t^2-4b^2$.

The whole large multi-coloured rectangle has an area of $(2s)^2$, because the green square, the light blue rectangle, and each of the two red rectangles <i>all</i> have areas of $t^2$, but then we need to subtract the light red
square where the two red rectangles overlap, and that has area $4b^2$.

Now if we subtract a single $t^2$, the light blue rectangle, then we're left with a square of side length $r$,
thanks to the fact that $\Phi=1+1/\Phi$.  So $(2s)^2-t^2=r^2$, which is the pentagon-decagon-hexagon identity.

The middle section of this proof is essentially a diagrammatic proof of the identity:

$$\Phi^2+\frac{1}{\Phi^2}=3$$

which can also be verified algebraically from the defining equation for $\Phi$.

##Proof from a construction on the icosahedron##


[[!include pentagon decagon hexagon identity/duads]]

Suppose we construct a regular icosahedron based on three orthogonal "duads".  These are rectangles in the golden ratio, with vertices of the icosahedron at their corners.

[[!include pentagon decagon hexagon identity/icosahedron]]

In the diagram above, everything is projected into the plane of one duad, which has the vertices $A$, $B$, $-A$ and $-B$ as its corners.  Where two vertices are projected to the same point in the diagram, there is a circle drawn around the point.

By construction, all vertices will be equidistant from the centre of symmetry.  To establish that we really do have a _regular_ icosahedron here, we need to prove that all the edge lengths are equal.  The 6 edges that lie along the short side of some duad are all of length 1, by construction.  The 24 other edges can be shown to be of the same length by essentially just one calculation; in each case, the difference in the coordinates of the relevant vertices are $\frac{\Phi}{2}$, $\frac{1}{2}$ and $\frac{\Phi-1}{2}$.  So four times the sum of the squares of these coordinate differences will be:

$$(\Phi-1)^2+\Phi^2+1=\frac{1}{\Phi^2}+\Phi^2+1=4$$

where we've used the fact that $\Phi-1=\frac{1}{\Phi}$, which follows directly from the defining equation for $\Phi$, and then the identity:

$$\frac{1}{\Phi^2}+\Phi^2=3$$

So the edge lengths will all equal 1.  We also need to prove that $A P R$ is actually a straight line, as we've drawn it!  This amounts to proving that the ratio of vertical to horizontal displacement from $R$ of the points $A$ and $P$ are the same:

$$\frac{\frac{\Phi}{2}}{\frac{\Phi}{2}+\frac{1}{2}}=\frac{\frac{1}{2}}{\frac{\Phi}{2}}$$

or equivalently:

$$\Phi^2=\Phi+1$$

which follows directly from the defining equation for $\Phi$.

The right triangle $O R P$ is similar to the right triangle $C A B$.  So $\frac{C A}{C B}=\frac{O R}{O P}=\Phi$, with the last equality true by construction.  It follows from the golden triangle lemma that $C B$ is the edge length of a decagon inscribed in a circle of radius $C A$.

But the five vertices that project onto the line $A P R$ form a regular pentagon inscribed in a circle of radius $C A$, and the edge length of that pentagon is $A B$.  So the right triangle $C A B$ constitutes a proof of the pentagon-decagon-hexagon identity.

#References#

* John Baez, [This Week's Finds in Mathematical Physics, Week 283](http://math.ucr.edu/home/baez/week283.html)

* [n-Caf&eacute; discussion of TWF 283](http://golem.ph.utexas.edu/category/2009/11/this_weeks_finds_in_mathematic_44.html)

* John Baez, [Some thoughts on the Number 6](http://math.ucr.edu/home/baez/six.html)


[[!redirects pentagon-decagon-hexagon identity]]
[[!redirects pentagon–decagon–hexagon identity]]
[[!redirects pentagon--decagon--hexagon identity]]