This is a page dedicated to helping all those who're struggling with understanding the classic book:

* B. Bakalov & A. Kirillov, _Lectures on tensor categories and modular functors_ AMS, University Lecture Series, (2000) ([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html))

The procedure is: go to the [nForum Help me! I'm trying to understand Bakalov and Kirillov](http://ncatlab.org/nlab/show/Help%20me!%20I%27m%20trying%20to%20understand%20Bakalov%20and%20Kirillov) page, or to [Math Overflow](http://mathoverflow.net/). Type in your question and get someone to answer it. Then put down the answer here in final form for future generations. 

### Errata

* pg 112, bottom of proof of Theorem 5.3.8, "the Dehn twist axiom MF7" should read MS7, I believe. [[Bruce Bartlett]]

### How does the "s" map work? ([nForum link](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1099&page=1)) 

[[Bruce Bartlett]]: I don't understand the $s$ map in Example 5.1.11 in the online version of the book. It's supposed to be the automorphism
 \[
 s : \Gamma_{1,1} \rightarrow \Gamma_{1,1}
\] 
of the torus with one boundary circle which is the analogue of a map which I _do_ understand, the automorphism
\[
 s_t : \Gamma_{1,0} \rightarrow \Gamma_{1,0}
\]
of the ordinary torus (no boundary circle) to itself, which sends 
\[
 (\theta, \phi) \mapsto (\phi, -\theta).
\]
But the map $s_t$ doesn't seem to work if there is a boundary circle involved. Because an automorphism of $\Gamma_{1,1}$ is supposed to be the identity on the boundary circle, but the map $s_t$ isn't: it rotates the boundary circle a quarter rotation (right?). The reason I say so is the following picture: we think of the torus as $\mathbb{R}^2 / \mathbb{Z}^2$, as Bakalov and Kirillov encourage us to do. Then the presence of the boundary circle can be thought of as having a little tangent vector pointing to the right at all the lattice positions (this uses their alternative Definition 5.1.10 the extended surface category). The map $(x,y) \mapsto (y, -x)$ rotates the plane by a quarter rotation and takes the lattice to itself, hence it descends to the quotient. But this map rotates the tangent vector by a quarter rotation, and we're supposed to fix the tangent vectors!

So how does the map $s$ work?

Answer: [[Domenico Fiorenza]] explained it as follows: consider the torus with one boundary circle as a square made of elastic material with with opposite sides identified, with an open disc missing in the center. Then turn the square through one quarter of a rotation, while keeping the boundary circle fixed. That's the $s$ map. 

If you picture it at the level of the plane (i.e. before we mod $R^2$ out by $Z^2$), then you need to imagine a whole bunch of circles ("knobs") located at the integer lattice points of the plane. Get a whole bunch of friends (one for each knob), and then count down "3,2,1,turn!" and turn the knobs through a quarter revolution clockwise (this distorts the elastic material from which the plane is made). Then rotate the whole thing rigidly one quarter of a revolution counterclockwise. The resultant map is the $s$-map at the level of the plane. 

category: reference