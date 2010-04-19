This is a page dedicated to helping all those who're struggling with understanding the classic book:

* B. Bakalov & A. Kirillov, _Lectures on tensor categories and modular functors_ AMS, University Lecture Series, (2000) ([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html))

Type up your questions and fire away! You can also alert someone you know can answer your question by email, and ask them to respond here (if they care to), so that others may also benefit. 

### Errata

* pg 112, bottom of proof of Theorem 5.3.8, "the Dehn twist axiom MF7" should read MS7, I believe. [[Bruce Bartlett]]

### How does the "s" map work?

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


category: reference