
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

#Idea#

A certain identity in [[Euclidean geometry]].

Suppose we inscribe a regular pentagon, a regular decagon, and a regular hexagon in circles of the same radius.  If we denote the respective edge lengths of these polygons by $P$, $D$ and $H$, then these lengths will satisfy the identity:

$$P^2=D^2+H^2$$

This means that the edges of a pentagon, decagon and hexagon of identical radii can fit together to form a right triangle.

Euclid states this beautiful but mysterious identity as [Proposition 10](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII10.html) of Book XIII of the _Elements_.  This is the last book of the _Elements_, the one which deals with properties of the Platonic solids.  He uses Proposition 10 as part of his construction of the regular icosahedron in [Proposition 13](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII13.html).  

This has led various historians to suggest that the pentagon-decagon-hexagon identity was first discovered in the course of research on the icosahedron.  However, it seems that until now there has been no _proof_ of the pentagon-decagon-hexagon identity based on properties of the icosahedron.  We present such a proof here.

We also present two other proofs: a modernized version of Euclid's original proof, and a somewhat simpler proof which (like Euclid's) uses only 2-dimensional geometry.

#Euclid's proof#

The essence of [Euclid's proof](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII10.html) can be understood if we take for granted the numerical values of the various angles in his construction, which are easily established.  Euclid himself would not have used numerical values like this, and they are not a part of the proof; they're merely a short-hand that allows the reader to see at a glance the relationships between angles that the original proof established by routine methods.

[[!include pentagon decagon hexagon identity > Euclid]]

The line segment $A B$ is one edge of a pentagon inscribed in a circle centred at $F$, and $A K$ and $K B$ are edges of a decagon inscribed in the same circle.  Note that while $A B$ is bisected by $H$ and $A K$ is bisected by $L$, the point $N$ is _not_ a point of bisection of $A H$.

Triangle $A B F$ is similar to triangle $B F N$.  So $\frac{A B}{B F}=\frac{B F}{F N}=\frac{B F}{B N}$, with the last equality true because the triangles are isosceles with $F N = B N$.  Thus ${B F}^2={A B}\cdot{B N}$.

Triangle $B A K$ is similar to triangle $K A N$.  So $\frac{B A}{A K}=\frac{K A}{A N}$.  Thus ${A K}^2={A B}\cdot{A N}$.

Adding our two results, we have:
${B F}^2+{A K}^2={A B}\cdot(A N + B N)={A B}^2$.

$B F$ is our radius (or equivalently, the length of one side of a hexagon inscribed in the same circle), $A K$ is a decagon side, and $A B$ is a pentagon side.  So we have established the pentagon-decagon-hexagon identity.

#Another 2d proof#

Euclid's proof is quick but somewhat mysterious.  Here is another, perhaps simpler, proof that uses only 2-dimensional constructions. It relies on a lemma concerning the ratio of sides in a "golden triangle".  

##Golden triangle lemma##

[[!include pentagon decagon hexagon identity > golden triangle]]

The lemma states that in any isosceles triangle with angles of 72&#176;, 36&#176; and 72&#176;, the ratio of the long sides of the triangle to its base is $\Phi$, the golden ratio, which is defined as the unique positive solution of the equation:

$$1+\frac{1}{\Phi}=\Phi$$

Note that some authors call "the golden ratio" the reciprocal of the number we're calling $\Phi$.  For the purpose of this article, $\Phi=\frac{\sqrt{5}+1}{2}\approx 1.61803$.

In the diagram above, triangle $B D E$ is similar to triangle $B E C$.  So:

$$\frac{B D}{B E}=\frac{B E}{B C}$$
$$\frac{r+t}{r}=\frac{r}{t}$$
$$1+\frac{t}{r}=\frac{r}{t}$$

By the definition of the golden ratio, $\frac{r}{t}=\Phi$.

This lemma was given by Euclid as [Proposition 9](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII9.html) of Book XIII.

##Proof using the golden triangle lemma##

[[!include pentagon decagon hexagon identity > golden ratio]]

By the golden triangle lemma for isosceles triangles with angles of 36&#176;, triangle $N O P$ gives us $r=t\Phi$.  From the same lemma, applied to triangle $P N Q$, we have $2b=t/\Phi$.  So the product of $r$ and $2b$ is $t^2$.

Because triangle $N Q O$ and $N Q P$ are both isosceles, $O Q = N Q = N P = t$, the decagon edge.  And we can read off the equation $r=t+2b$ just by summing the distances along $O P$.

From the right triangle $N M P$ we have $s^2=t^2-b^2$, hence $(2s)^2=4t^2-4b^2$.

The whole large multi-coloured rectangle has an area of $(2s)^2$, because the green square, the light blue rectangle, and each of the two red rectangles _all_ have areas of $t^2$, but then we need to subtract the light red
square where the two red rectangles overlap, and that has area $4b^2$.

Now if we subtract a single $t^2$, the light blue rectangle, we're left with a square of side length $r$.  So $(2s)^2-t^2=r^2$, which is the pentagon-decagon-hexagon identity.

###Alternative construction displaying right triangles###

While the construction above is straightforward, it's also possible to present an equivalent result that explicitly gives us right triangles with the pentagon edge as their hypotenuse and the hexagon and decagon edges as their other sides.

[[!include pentagon decagon hexagon identity > pythagorean identity]]

The diagram above is similar to one used in a common proof of Pythagoras's Theorem, but here we use it to establish the value of the square of the hypotenuse of a right triangle with sides $r$ and $t$, i.e. the hexagon edge and the decagon edge.

The large tilted square has a hypotenuse as its side.  Its area is $4b^2$, from the central pink square, plus $4t^2$, from the four multi-coloured $t\times t$ squares arranged around the central square, minus four times the area of the dark green triangle that needs to be excluded (the contributions from the yellow triangles inside and outside the region cancel out).  But each dark green triangle has both base and height of $2b$, and hence an area of $2b^2$, so the total area is $4t^2+4b^2-4\times 2b^2=4t^2-4b^2=(2s)^2$, the square of a pentagon edge.

At first glance it might seem as if we've only used $r=t+2b$ to derive the result here, whereas in the previous construction we needed the fact that the product of $r$ and $2b$ was $t^2$.  But we _have_ used it:  the yellow triangles that share an edge with the dark green triangles, and those that do not, are only congruent because of it.  The latter have one of their sides by construction being $r-t=2b$, whereas the former's matching side arises as a proportion of the larger $r\times t$ triangle as $\frac{t}{r}\cdot t=2b$.

##An identity in the golden ratio##

The first way of presenting the preceding proof implies the identity:

$$\Phi^2+\frac{1}{\Phi^2}=3$$

which can also be verified algebraically from the defining equation for $\Phi$.  We can see this identity a bit more clearly if we remove the leftmost rectangle from the construction, slide the rightmost one down to eliminate the overlap, and take out the overall factor of $t$ from all the sides.  We then have:

[[!include pentagon decagon hexagon identity > golden ratio identity]]

We can also construct a diagram that explicitly shows that the square of the diagonal of a rectangle of dimensions $\Phi$ by $\frac{1}{\Phi}$ is $3$.

[[!include pentagon decagon hexagon identity > golden ratio identity pythagorean]]

Here each red triangle has area $\frac{1}{2}$, so along with the light green unit square the total area is $3$.

#Proof using the icosahedron#
{. #Icosahedron}

Suppose we take **three congruent rectangles**, and assemble them symmetrically so that their _long_ edges are all mutually orthogonal, and their _short_ edges are all mutually orthogonal.  Like this:

[[!include pentagon decagon hexagon identity > skinny duads]]

We then join up the corners to make an icosahedron, as in the diagram above.  Eight faces of this icosahedron (the ones centred on the diagonals of the eight "octants" into which the space here is divided) will _always_ be congruent and equilateral; that's guaranteed by the construction, whatever the precise ratio of the side lengths of the rectangles.  The other twelve faces will be isosceles triangles, all congruent to each other.

In terms of edges, there are two congruent sets:  the six edges that correspond to short sides of our rectangles will all be congruent, and the twenty-four edges that are sides of the eight equilateral faces will all be congruent.

Now, it's clear that by making the rectangles long and skinny, we can make the isosceles triangles as long and skinny as we like.  But what about making them short and squat?  How far can we go in that direction?

[[!include pentagon decagon hexagon identity > square duads]]

If we make the three rectangles into squares, as above, the isosceles triangles have two 45&#176; angles.  So between this extreme, and the long-and-skinny extreme, it's clear that we can choose _some_ intermediate degree of skinniness for the rectangles that will turn the 12 isosceles triangles into equilateral triangles.

So, a _regular_ icosahedron must exist, and it will have six edges that form three mutually orthogonal pairs.

[[!include pentagon decagon hexagon identity > duads]]

(The argument we've just given implicity uses the [[intermediate value theorem]] and would not have been used by Euclid, although Archimedes might have attempted it.  An alternative that avoids using the intermediate value theorem is given at the end of the proof.)

We will set the short side of the rectangles to $1$, and for now we will call the corresponding value for the long side that produces a regular icosahedron $x$.

In the figure below we project everything into the plane of one of the rectangles.  Where two vertices are projected to the same point in the diagram, a circle is drawn around the point.

[[!include pentagon decagon hexagon identity > icosahedron]]

The five vertices of the icosahedron that project onto the line segment $A P R$ will form a regular pentagon, the edges of which are also edges of the icosahedron.  $A P R$ is a straight line because the pentagon is a planar figure, as it must be if it forms the base of a pentagonal pyramid with five congruent equilateral triangles as its other faces.  The point $C$ is produced by dropping a perpendicular line from the apex, $B$, of this pentagonal pyramid, to its base.

By construction, $Q R$ is parallel to $A B$, and both are orthogonal to $O P$.  Combined with the fact that $A P R$ is a straight line, that's enough to show that the triangle $A B C$ is congruent to the triangle $S P T$.

The five vertices that project onto the line segment $Z S Q$ will form another pentagon.  The two pentagons will be congruent, and the radius of the circles in which they're inscribed will be $A C$.  And since the triangle $A B C$ is congruent to the triangle $S P T$, the _distance_ between the pentagons, $S T$, equals their radius, $A C$.

These two pentagons are shown in the diagram below.

[[!include pentagon decagon hexagon identity > icosahedron triangles]]

If we draw a line perpendicular to the planes of the two pentagons, from a vertex in one plane, $A$, to the point directly below it on the other plane, $V$, the length of that perpendicular, $A V$, will be equal to the common radius of the pentagons, $A C$.  Now, $A V$ is one side of a right triangle whose hypotenuse is an icosahedral edge, $A Q$ (congruent to the edges of the pentagons), and whose third side, $Q V$, is one edge of a decagon inscribed in the same circle as the lower pentagon.  The decagon edge arises because the two pentagons are rotated relative to each other by an angle of 36&#176;, the angle between vertices in a decagon.

So, the triangles $A B C$ and $A Q V$ are congruent (both being right triangles with a pentagon edge as their hypotenuse and the radius as one of their sides), and both exhibit the pentagon-decagon-hexagon identity.

According to the historian Ian Mueller, Eva Sachs, in her book _Die F&#252;nf Platonischen K&#246;rper_, suggested an accurately drawn figure could let someone guess that the distance between the two pentagons equals the radius of either one.  Mueller also writes that Dijksterhuis (in 1929) and Neuenschwander (in 1975) claimed it's "intuitively evident" that the two right triangles above are congruent.   These clues led Greg Egan to the present proof.

If we want, we can now appeal to Euclid's golden triangle lemma -- which gives us the ratio between the radius and the decagon edge length as $\Phi$ -- and work backwards to show that this is also the ratio of length to width for our three orthogonal rectangles; that is, $x=\Phi$ is the value needed to produce a regular icosahedron.  This follows simply from the fact that the right triangle $O R P$ is similar to the right triangle $C A B$.

##Avoiding the intermediate value theorem##

Finally, suppose we wish to avoid using the intermediate value theorem.  To do this, we need to specify the length-to-width ratio, $x$, of the rectangles in our construction, and show that our choice yields a regular icosahedron.

One approach we could take is to set $x=\Phi$, and directly calculate the length of an edge of our icosahedron that doesn't lie on one of the rectangles.  If this length is $1$ -- matching the edges that _do_ lie on the rectangles -- the icosahedron will be regular.

[[!include pentagon decagon hexagon identity > pythagorean icosahedron]]

As the diagram above shows, this isn't too hard; with the help of a re-scaled version of the diagram we used to demonstrate the identity $\Phi^2+\frac{1}{\Phi^2}=3$, we can see that ${A Q}^2=\frac{3}{4}$, and, since the vertices that project to $Q$ are a distance of $\frac{1}{2}$ out of the plane, the squared length of the edge that projects to $A Q$ will be $1$.

But if this is a little too close to resorting to algebra, we can take a more geometric approach.

If we project the generic version of our icosahedron onto the plane of one of its rectangles, we get this:

[[!include pentagon decagon hexagon identity > irregular icosahedron]]

In order to make $A P R$ into a straight line -- which amounts to making the pentagon of vertices that project onto $A P R$ into a planar figure -- we need the slope of $A R$ to equal the slope of $P R$, which is equivalent to:

$$\frac{x+1}{x}=x$$

This is just the defining equation for the golden ratio, $\Phi$.  So we need to set $x=\Phi$ to have any hope of our icosahedron being regular, since in a regular icosahedron the pentagon will be the base of a pentagonal pyramid with equilateral sides, which is clearly a planar figure.

Next, we note that the golden triangle lemma can be used to establish that in the figure below, the larger of the two golden triangles here associated with a regular pentagon is $\Phi$ times larger than the smaller one (because the long edge of the smaller triangle is congruent to the small edge of the larger triangle).  This means the _height_ of a regular pentagon, measured from one edge, is $\Phi$ times the height of an adjacent vertex.

[[!include pentagon decagon hexagon identity > pentagon heights]]

The same lemma also shows that the _width_ of a regular pentagon, measured parallel to one edge, is $\Phi$ times its edge length.

[[!include pentagon decagon hexagon identity > pentagon width]]

Now, by choosing $x=\Phi$, as well as making the pentagon that projects onto $A P R$ into a planar figure, we've actually made _every_ set of five vertices that are neighbours to any given vertex in the icosahedron lie in a plane.

[[!include pentagon decagon hexagon identity > icosahedron pentagon]]

For example, the two such pentagons that project onto $B P S Z R$ must also be planar.  But since they're planar, their projection here will preserve the ratio between the perpendicular distance from $P S$ to the vertex that projects to $R$ and the perpendicular distance from $P S$ to the vertices that project to $Z$ and $B$.  The projections of these distances are just $\frac{x}{2}$ and $\frac{1}{2}$ respectively, so our choice of $x=\Phi$ makes their ratio equal to $\Phi$.

Furthermore, the lengths of the line segments projecting to $B Z$ and $P S$ will be the same in the actual pentagons as they are in the projection, and in the projection their ratio is $\frac{B Z}{P S}=x=\Phi$.

But we've established that both these ratios are $\Phi$ for a _regular_ pentagon, and the pentagons projecting to $B P S Z R$ are already so symmetrical (with at least four congruent edges, and mirror symmetry in the perpendicular bisector of the fifth edge) that if they share both ratios, they too must be regular.

[[!include pentagon decagon hexagon identity > regular pentagon]]

That's probably intuitively obvious, but we can make it a bit more explicit.  In the diagram above, the blue pentagon shares one edge with the regular, black pentagon, and has also been constrained to have the same width and height ratios.  The height ratio fixes $\frac{J K}{G H}=\Phi$ and the width ratio fixes $\frac{F L}{E F}=\Phi$, which means the two yellow triangles are similar, which in turn fixes $\frac{F K}{F H}=\Phi=\frac{F K'}{F H'}$.

If we further require that the triangle $F K H$ is isosceles (which follows from the way we've constructed the generic icosahedron), then it will be similar to $F K' H'$, and $F L K$ will be similar to $F L K'$ (since the angle of either of the two yellow triangles at $F$ is just half the supplement of the angle $K F H$).  But since $F L K$ and $F L K'$ share an edge, they will actually be _congruent_, and the blue and black pentagons will coincide exactly.

In other words, there is only one pentagon meeting all the conditions we've imposed:  the regular pentagon with edge $F L$.  This means that, given our choice of $x=\Phi$, the two kinds of congruent edges in our generic icosahedron end up being the same size, and the icosahedron itself is regular.

#A dual proof using the icosahedron#
{. #IcosahedronDual}

The pentagon-decagon-hexagon identity is usually demonstrated by exhibiting a right triangle whose sides are the edges of a regular pentagon, decagon and hexagon _with the same radii_.  However, a proof of the identity devised by Ian Agol constructs a pentagon, decagon and hexagon associated with the icosahedron that all share a common edge, and whose _radii_ (now of different lengths) correspond to the _altitudes_ of a right triangle.

If the length of the common edge of the three polygons is taken to be 1, then their radii are the _reciprocals_ of the edge lengths $P$, $D$ and $H$ of the same polygons if they had radii of 1.  But the altitudes of a right triangle obey a "reciprocal" or "dual" version of the usual Pythagorean theorem:  if the altitudes of a right triangle measured from its two perpendicular sides are $a$ and $b$, and that measured from the hypotenuse is $c$, then it is easily shown that:

$$\frac{1}{c^2} = \frac{1}{a^2} + \frac{1}{b^2}$$

It follows that the existence of a right triangle with altitudes $a=\frac{1}{D}$, $b=\frac{1}{H}$ and $c=\frac{1}{P}$ implies the pentagon-decagon-hexagon identity:

$$P^2=D^2+H^2$$

[[!include pentagon decagon hexagon identity > agol icosahedron]]

In the diagram above, we have chosen a vertex $V$ of a regular icosahedron with center $C$.  The points $M_1$ and $M_2$ are the midpoints of two edges of the icosahedron incident on $V$, and we construct three regular polygons that all have $M_1 M_2$ as a common edge.

A regular hexagon (blue) is constructed with center $V$, with $M_1 M_2$ as one of its edges, lying in the plane of one of the faces of the icosahedron.

A regular pentagon (yellow) is constructed, with its five vertices being the midpoints of the five edges of the icosahedron that are incident on $V$.  The center of this pentagon will lie on the line segment $C V$, and is named $W$ in the diagram.  The plane in which this pentagon lies is orthogonal to $C V$, so the line segment $W M_1$ meets $C V$ in a right angle.

A regular decagon (green) is constructed with center $C$, with $M_1 M_2$ as one of its edges.

Finally, a right triangle (red) is constructed, with vertices $C$, $M_1$ and $V$.  The angle at $M_1$ is a right angle, because $C M_1$ is a perpendicular bisector of the polyhedron edge of which $M_1$ is the midpoint.  The altitude $C M_1$ of this triangle is the radius of the decagon.  The altitude $V M_1$ is the radius of the hexagon.  And the altitude $W M_1$ is the radius of the pentagon.  From the dual Pythagorean theorem, this establishes the pentagon-decagon-hexagon identity.

Ian Agol's construction can also be applied to any of the other Platonic solids, and also to the four Kepler-Poinsot polyhedra.  This yields the following results:

From the tetrahedron and from the cube, $T^2=S^2+H^2$ for a triangle, square and hexagon.

From the octahedron, $S^2=H^2+H^2$, for a square and two hexagons.

From the dodecahedron, $T^2=D^2+D_3^2$, for a triangle, decagon, and a 10-pointed star polygon, $D_3$, whose ten edges subtend a total of 1080&#176;.  This star polygon arises as the analogous polygon to the blue hexagon in the icosahedral case.  Its center is a vertex $V$ of the dodecahedron, and it has as one edge the line segment joining the midpoints of two adjacent edges of a pentagonal face (both edges being incident on the vertex $V$).  Since the interior angle of a regular pentagon at each corner is 108&#176;, the corresponding polygon must be a star polygon with its edges subtending that angle, and the first multiple of 108&#176; that is also a multiple of 360&#176; is 1080&#176;, from ten edges.

[[!include pentagon decagon hexagon identity > agol dodecahedron]]

Applying the construction to the Kepler-Poinsot polyhedra, the great dodecahedron and the great icosahedron both yield $P_2^2=H^2+D_3^2$, where $P_2$ is a pentagram.  The small stellated dodecahedron yields the original identity, $P^2=D^2+H^2$, with the locations of the hexagon and decagon swapped compared to the icosahedral construction.  And the great stellated dodecahedron yields $T^2=D^2+D_3^2$, the same identity as the ordinary dodecahedron, with the decagon and the 10-pointed stars changing places.

In general, one of the polygons (the "green" one) is invariant under taking the dual of the polyhedron.  If the faces of the polyhedron are $n$-gons and the vertex figures are $v$-gons, the "yellow" polygon  (whose vertices are all the midpoints of all the edges incident on some vertex of the polyhedron) will be a $v$-gon, with each edge subtending an angle of $\frac{2\pi}{v}$, while the "blue" polygon centred on the vertex will be a $\frac{2n}{n-2}$-gon, where each edge subtends an angle of $\frac{(n-2)\pi}{n} = \pi-\frac{2\pi}{n}$ (the interior angle between the edges of an $n$-gon).

The difference of the squares of the sines of half these angles is:

$$\sin\left(\frac{\pi}{v}\right)^2 - \sin\left(\frac{(n-2)\pi}{2n}\right)^2 = -\cos\left(\pi \left(\frac{1}{n}+\frac{1}{v}\right)\right) \cos\left(\pi \left(\frac{1}{n}-\frac{1}{v}\right)\right)$$

where the RHS is now clearly invariant under an exchange of $n$ and $v$.  This quantity is the squared sine of half the angle subtended by each edge of the "green" polygon.

#References#

* John Baez, [This Week's Finds in Mathematical Physics, Week 283](http://math.ucr.edu/home/baez/week283.html)

* [n-Caf&#233; discussion of TWF 283](http://golem.ph.utexas.edu/category/2009/11/this_weeks_finds_in_mathematic_44.html)

* John Baez, [Some Thoughts on the Number 6](http://math.ucr.edu/home/baez/six.html)

* Ian Mueller, _Philosophy of Mathematics and Deductive Structure in Euclid's Elements_, MIT Press, Cambridge Massachusetts, 1981, pp. 257--258 and references therein.

* Eva Sachs, _Die F&#252;nf Platonischen K&#246;rper, zur Geschichte der Mathematik und der Elementenlehre Platons und der Pythagoreer_, Berlin, Weidmann, 1917, pp. 102--104. 
See page 102--103 [here](http://math.ucr.edu/home/baez/icosahedron_sachs_1.jpg) and page 104 [here](http://math.ucr.edu/home/baez/icosahedron_sachs_2.jpg).


[[!redirects pentagon-decagon-hexagon identity]]
[[!redirects pentagon–decagon–hexagon identity]]
[[!redirects pentagon--decagon--hexagon identity]]