#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Suppose we inscribe a regular pentagon, a regular decagon, and a regular hexagon in circles of the same radius.  If we denote the respective edge lengths of these polygons by $P$, $D$ and $H$, then these lengths will satisfy the identity:

$$P^2=D^2+H^2$$

This means that the edges of a pentagon, decagon and hexagon of identical radii can fit together to form a right triangle.

Euclid states this beautiful but mysterious identity as [Proposition 10](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII10.html) of Book XIII of the _Elements_.  This is the last book of the _Elements_, the one which deals with properties of the Platonic solids.  He uses Proposition 10 as part of his construction of the regular icosahedron in [Proposition 13](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII13.html).  

This has led various historians to suggest that the pentagon-decagon-hexagon identity was first discovered in the course of research on the icosahedron.  However, it seems that until now there has been no _proof_ of the pentagon-decagon-hexagon identity based on properties of the icosahedron.  We present such a proof here.

We also present two other proofs: a modernized version of Euclid's original proof, and a somewhat simpler proof which (like Euclid's) uses only 2-dimensional geometry.

#Euclid's proof#

The essence of [Euclid's proof](http://aleph0.clarku.edu/~djoyce/java/elements/bookXIII/propXIII10.html) can be understood if we take for granted the numerical values of the various angles in his construction, which are easily established.  Euclid himself would not have used numerical values like this, and they are not a part of the proof; they're merely a short-hand that allows the reader to see at a glance the relationships between angles that the original proof established by routine methods.

[[!include pentagon decagon hexagon identity/Euclid]]

The line segment $A B$ is one edge of a pentagon inscribed in a circle centred at $F$, and $A K$ and $K B$ are edges of a decagon inscribed in the same circle.  Note that while $A B$ is bisected by $H$ and $A K$ is bisected by $L$, the point $N$ is _not_ a point of bisection of $A H$.

Triangle $A B F$ is similar to triangle $B F N$.  So $\frac{A B}{B F}=\frac{B F}{F N}=\frac{B F}{B N}$, with the last equality true because the triangles are isosceles with $F N = B N$.  Thus ${B F}^2={A B}\cdot{B N}$.

Triangle $B A K$ is similar to triangle $K A N$.  So $\frac{B A}{A K}=\frac{K A}{A N}$.  Thus ${A K}^2={A B}\cdot{A N}$.

Adding our two results, we have:
${B F}^2+{A K}^2={A B}\cdot(A N + B N)={A B}^2$.

$B F$ is our radius (or equivalently, the length of one side of a hexagon inscribed in the same circle), $A K$ is a decagon side, and $A B$ is a pentagon side.  So we have established the pentagon-decagon-hexagon identity.

#Another 2d proof#

Euclid's proof is quick but somewhat mysterious.  Here is another, perhaps simpler, proof that uses only 2-dimensional constructions. It relies on a lemma concerning the ratio of sides in a "golden triangle".  

##Golden triangle lemma##

[[!include pentagon decagon hexagon identity/golden triangle]]

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

[[!include pentagon decagon hexagon identity/golden ratio]]

By the golden triangle lemma for isosceles triangles with angles of 36&#176;, triangle $N O P$ gives us $r=t\Phi$.  From the same lemma, applied to triangle $N M P$ glued to its mirror image in the line $N M$, we have $2b=t/\Phi$.

From the right triangle $N M P$ we have $s^2=t^2-b^2$, hence $(2s)^2=4t^2-4b^2$.

The whole large multi-coloured rectangle has an area of $(2s)^2$, because the green square, the light blue rectangle, and each of the two red rectangles _all_ have areas of $t^2$, but then we need to subtract the light red
square where the two red rectangles overlap, and that has area $4b^2$.

Now if we subtract a single $t^2$, the light blue rectangle, then we're left with a square of side length $r$,
thanks to the fact that $\Phi=1+1/\Phi$.  So $(2s)^2-t^2=r^2$, which is the pentagon-decagon-hexagon identity.

###Alternative construction displaying right triangles###

While the construction above is straightforward, it's also possible to present an equivalent result that explicitly gives us right triangles with the pentagon edge as their hypotenuse and the hexagon and decagon edges as their other sides.

[[!include pentagon decagon hexagon identity/pythagorean identity]]

The diagram above is similar to one used in a common proof of Pythagoras's Theorem, but here we use it to establish the value of the square of the hypotenuse of a right triangle with sides $r$ and $t$, i.e. the hexagon edge and the decagon edge.

The large tilted square has a hypotenuse as its side.  Its area is $4b^2$, from the central pink square, plus $4t^2$, from the four multi-coloured $t\times t$ squares arranged around the central square, minus four times the area of the dark green triangle that needs to be excluded (the contributions from the yellow triangles inside and outside the region cancel out).  But each dark green triangle has both base and height of $2b$, and hence an area of $2b^2$, so the total area is $4t^2+4b^2-4\times 2b^2=4t^2-4b^2=(2s)^2$, the square of a pentagon edge.

##An identity in the golden ratio##

The first way of presenting the preceding proof implies the identity:

$$\Phi^2+\frac{1}{\Phi^2}=3$$

which can also be verified algebraically from the defining equation for $\Phi$.  We can see this identity a bit more clearly if we remove the leftmost rectangle from the construction, slide the rightmost one down to eliminate the overlap, and take out the overall factor of $t$ from all the sides.  We then have:

[[!include pentagon decagon hexagon identity/golden ratio identity]]

We can also construct a diagram that explicitly shows that the square of the diagonal of a rectangle of dimensions $\Phi$ by $\frac{1}{\Phi}$ is $3$.

[[!include pentagon decagon hexagon identity/golden ratio identity pythagorean]]

Here each red triangle has area $\frac{1}{2}$, so along with the light green unit square the total area is $3$.

#Proof using the icosahedron#

Suppose we take **three congruent rectangles**, and assemble them symmetrically so that their _long_ edges are all mutually orthogonal, and their _short_ edges are all mutually orthogonal.  Like this:

[[!include pentagon decagon hexagon identity/skinny duads]]

We then join up the corners to make an icosahedron, as in the diagram above.  Eight faces of this icosahedron (the ones centred on the diagonals of the eight "octants" into which the space here is divided) will _always_ be congruent and equilateral; that's guaranteed by the construction, whatever the precise ratio of the side lengths of the rectangles.  The other twelve faces will be isosceles triangles, all congruent to each other.

Now, it's clear that by making the rectangles long and skinny, we can make the isosceles triangles as long and skinny as we like.  But what about making them short and squat?  How far can we go in that direction?

[[!include pentagon decagon hexagon identity/square duads]]

If we make the three rectangles into squares, as above, the isosceles triangles have two 45&#176; angles.  So between this extreme, and the long-and-skinny extreme, it's clear that we can choose _some_ intermediate degree of skinniness for the rectangles that will turn the 12 isosceles triangles into equilateral triangles.

So, a _regular_ icosahedron must exist, and it will have six edges that form three mutually orthogonal pairs.

[[!include pentagon decagon hexagon identity/duads]]

(The argument we've just given implicity uses the [[intermediate value theorem]] and would not have been used by Euclid, although Archimedes might have attempted it.  An alternative that avoids using the intermediate value theorem is given at the end of the proof.)

We will set the short side of the rectangles to $1$, and for now we will call the corresponding value for the long side that produces a regular icosahedron $x$.

In the figure below we project everything into the plane of one of the rectangles.  Where two vertices are projected to the same point in the diagram, a circle is drawn around the point.

[[!include pentagon decagon hexagon identity/icosahedron]]

The five vertices of the icosahedron that project onto the line segment $A P R$ will form a regular pentagon, the edges of which are also edges of the icosahedron.  $A P R$ is a straight line because the pentagon is a planar figure, as it must be if it forms the base of a pentagonal pyramid with five congruent equilateral triangles as its other faces.  The point $C$ is produced by dropping a perpendicular line from the apex, $B$, of this pentagonal pyramid, to its base.

By construction, $Q R$ is parallel to $A B$, and both are orthogonal to $O P$.  Combined with the fact that $A P R$ is a straight line, that's enough to show that the triangle $A B C$ is congruent to the triangle $S P T$.

The five vertices that project onto the line segment $(-A) S Q$ will form another pentagon.  The two pentagons will be congruent, and the radius of the circles in which they're inscribed will be $A C$.  And since the triangle $A B C$ is congruent to the triangle $S P T$, the _distance_ between the pentagons, $S T$, equals their radius, $A C$.

These two pentagons are shown in the diagram below.

[[!include pentagon decagon hexagon identity/icosahedron triangles]]

If we draw a line perpendicular to the planes of the two pentagons, from a vertex in one plane, $A$, to the point directly below it on the other plane, $V$, the length of that perpendicular, $A V$, will be equal to the common radius of the pentagons, $A C$.  Now, $A V$ is one side of a right triangle whose hypotenuse is an icosahedral edge, $A Q$ (congruent to the edges of the pentagons), and whose third side, $Q V$, is one edge of a decagon inscribed in the same circle as the lower pentagon.  The decagon edge arises because the two pentagons are rotated relative to each other by an angle of 36&#176;, the angle between vertices in a decagon.

So, the triangles $A B C$ and $A Q V$ are congruent (both being right triangles with a pentagon edge as their hypotenuse and the radius as one of their sides), and both exhibit the pentagon-decagon-hexagon identity.

According to the historian Ian Mueller, Eva Sachs, in her book _Die F&#252;nf Platonischen K&#246;rper_, suggested an accurately drawn figure could let someone guess that the distance between the two pentagons equals the radius of either one.  Mueller also writes that Dijksterhuis (in 1929) and Neuenschwander (in 1975) claimed it's "intuitively evident" that the two right triangles above are congruent.   These clues led Greg Egan to the present proof.

If we want, we can now appeal to Euclid's golden triangle lemma -- which gives us the ratio between the radius and the decagon edge length as $\Phi$ -- and work backwards to show that this is also the ratio of length to width for our three orthogonal rectangles; that is, $x=\Phi$ is the value needed to produce a regular icosahedron.  This follows simply from the fact that the right triangle $O R P$ is similar to the right triangle $C A B$.

Finally, suppose we wish to avoid using the intermediate value theorem.  If we project the generic version of our icosahedron onto the plane of one of its rectangles, we get this:

[[!include pentagon decagon hexagon identity/irregular icosahedron]]

In order to make $A P R$ into a straight line -- which amounts to making the pentagon of vertices that project onto $A P R$ into a planar figure -- we need to satisfy:

$$\frac{x+1}{x}=x$$

This is just the defining equation for the golden ratio, $\Phi$.  If our icosahedron is regular, the pentagonal pyramid that sits on the pentagon will be made up of equilateral triangles, and its base will be planar.  So again we see that we can only get a regular icosahedron if we set $x=\Phi$.

Of course if we're sceptical about the very _existence_ of a regular icosahedron, we need to do a bit more work and confirm that this choice of $x$ actually makes the variable edge length in our generic icosahedron equal to the other edge length that's fixed by the short side of the rectangles (which we've set to $1$ for the sake of simplicity).

[[!include pentagon decagon hexagon identity/pythagorean icosahedron]]

If we take an edge that projects onto $A Q$ in the diagram above as our example of the variable edge length, we can easily see that the square of $A Q$ itself is $\frac{3}{4}$:  the light green square has area $\frac{1}{4}$, and each red triangle has area $\frac{1}{2} \times \frac{\Phi}{2} \times \frac{1}{2 \Phi} = \frac{1}{8}$.  By construction, both vertices that project onto $Q$ are a distance of $\frac{1}{2}$ from the plane, so the total length of either edge that projects to $A Q$ is $1$.  All the variable edges are congruent, so all $30$ edges are now shown to have a length of $1$.

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