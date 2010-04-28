#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Let $k$ be a field with $char(k) \neq 2$. A **composition algebra** over $k$ consists of a finite-dimensional vector space $V$ together with a 

* A nondegenerate symmetric bilinear form $\langle , \rangle: V \otimes V \to k$, 

* A multiplication map, i.e., a linear map $- \cdot -: V \otimes V \to V$, 

* A unit $e \in V$ for the multiplication, i.e., so that $e \cdot v = v = v \cdot e$, 

such that, putting $N(v) = \langle v, v \rangle$, 

* $N(u) N(v) = N(u v)$ (writing $u v$ for $u \cdot v$). 

There are no assumptions on the multiplication such as associativity, commutativity, etc. Examples of composition algebras include the real numbers, the complex numbers, the quaternions, and the octonions. 

Since $char(k) \neq 2$, we can recover the bilinear form from the norm by the formula 

$$\langle u, v \rangle = \frac{N(u + v) - N(u) - N(v)}{2}$$ 

Since the bilinear form is nondegenerate, we may infer $u = v$ whenever 

$$\langle u, w \rangle = \langle v, w \rangle$$

and this will be frequently used in the sequel. 

## Basic identities

The arrangements of the proofs below closely follow the treatment by Conway and Smith (see references below). 

+-- {: .un_prop}
######Proposition (Scaling)
$\langle u v, u w \rangle = N(u)\langle v, w \rangle$ and $\langle u w, v w \rangle = \langle u, v \rangle N(w)$
=--

+-- {: .proof}
######Proof 
The left sides, and therefore the right sides of the equations below are equal: 

$$N(u(v + w)) = N(u)N(v + w) = N(u)(N(v) + 2\langle v, w \rangle + N(w))$$

[ ]

$$N(u v + u w) = N(u v) + 2\langle u v, u w \rangle + N(u w) = N(u)N(v) + 2\langle u v, u w \rangle + N(u)N(w)$$ 

and the result follows by cancellation and division by $2$. 
=--

+-- {: .un_prop}
######Proposition (Exchange)
$\langle u v, w x \rangle = 2\langle u, w \rangle \langle v, x \rangle - \langle u x, w v \rangle$
=--

+-- {: .proof}
######Proof
From the scaling identity, we have 

$$\langle (u + w)v, (u + w)x \rangle = N(u + w)\langle v, x \rangle = N(u)\langle v, x \rangle + 2\langle u, w \rangle \langle v, x \rangle + N(w)\langle v, x \rangle = \langle u v, u x \rangle + 2\langle u, w \rangle \langle v, x \rangle + \langle w v, w x \rangle$$

but the left-hand side is equal to 

$$\langle u v + w v, u x + w x \rangle = \langle u v, u x \rangle + \langle w v, u x \rangle + \langle u v, w x \rangle + \langle w v, w x \rangle$$

and now we equate the right-hand sides and cancel to get the result. 
=--

### Conjugation identities 

In any composition algebra, we may define a **conjugation** operator by 

$$\bar{v} = 2\langle v, e \rangle e - v$$

The next few propositions develop properties of conjugation. 

+-- {: .un_prop}
######Proposition (Adjointness)
$\langle u v, w \rangle = \langle v, \bar{u}w \rangle$ and $\langle u v, w \rangle = \langle u, w\bar{v} \rangle$
=-- 

+-- {: .proof}
######Proof
Put $x = e$ in the exchange identity to get the first equation in 

$$\langle u v, w \rangle = 2\langle u, w \rangle \langle v, 1 \rangle - \langle u, w v \rangle = \langle u, w(2\langle v, e\rangle e - v)\rangle = \langle u, w\bar{v} \rangle$$
=--

+-- {: .un_prop} 
######Proposition (Involution) 
$v = \bar{\bar{v}}$ for all $v$. 
=-- 

+-- {: .proof}
######Proof 
For all $u$ we have 

$$\langle u, v \rangle = \langle u\bar{v}, e \rangle = \langle u, \bar{\bar{v}} \rangle$$ 

and the result follows from nondegeneracy. 
=-- 

+-- {: .un_prop} 
######Proposition (Unitarity) 
$\langle u, v \rangle = \langle \bar{v}, \bar{u} \rangle = \langle \bar{u}, \bar{v} \rangle$.  
=-- 

+-- {: .proof} 
######Proof 
$\langle u, v \rangle = \langle e, \bar{u}v \rangle = \langle \bar{v}, \bar{u} \rangle = \langle \bar{u}, \bar{v} \rangle$ where the last equation is symmetry of the bilinear form. 
=-- 

+-- {: .un_prop}
######Proposition (Anti-automorphism) 
$\bar{u} \bar{v} = \widebar{v u}$. 
=-- 

+-- {: .proof}
######Proof 
For all $w$ we have 

$$\langle \bar{u}\bar{v}, w \rangle = \langle \bar{v}, u w \rangle = \langle \bar{v}\bar{w}, u \rangle = \langle \bar{w}, v u \rangle = \langle \widebar{v u}, w \rangle$$

using involution and unitarity. The result follows from nondegeneracy of the form. 
=-- 

## Cayley-Dickson doubling construction

## References

* [wikipedia](http://en.wikipedia.org/wiki/Composition_algebra)

* Markus Rost, _On the dimension of a composition algebra_, Documenta  Mathematica __1__ (1996), 209-214, [files](http://www.math.uni-bielefeld.de/documenta/vol-01/10.html) Abstract: "The possible dimensions of a composition algebra are 1, 2, 4, or 8. We give a tensor categorical argument."

* John Baez's [comment](http://golem.ph.utexas.edu/category/2010/03/division_algebras_and_supersym.html#c032790)

* John H. Conway, Derek A. Smith, _On Quaternions and Octonions_, A.K. Peters, 2003.

Related $n$lab entries: [[alternative algebra]], [[Cayley-Dickson construction]]

Related eom entries: [Lie-admissible algebra](http://eom.springer.de/l/l058360.htm)