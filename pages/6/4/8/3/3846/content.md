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

Also since the form is nondegenerate, there exists $v \in V$ such that $N(v) \neq 0$. From $N(v) = N(e v) = N(e)N(v)$, it follows that $N(e) = 1$. 

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

Observe that $\bar{v} = v$ just when $v$ is a scalar multiple of the identity. By analogy with the classical case (composition algebras over $\mathbb{R}$), such elements will be called "real". 

The next few propositions develop properties of conjugation. 

+-- {: .un_prop}
######Proposition (Adjointness)
$\langle u v, w \rangle = \langle v, \bar{u}w \rangle$ and $\langle u v, w \rangle = \langle u, w\bar{v} \rangle$
=-- 

+-- {: .proof}
######Proof
Put $x = e$ in the exchange identity to get the first equation in 

$$\langle u v, w \rangle = 2\langle u, w \rangle \langle v, e \rangle - \langle u, w v \rangle = \langle u, w(2\langle v, e\rangle e - v)\rangle = \langle u, w\bar{v} \rangle$$

The other adjointness equation is proved similarly. 
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

By the involution and anti-automorphism properties, we see that $\bar{v}v$ is fixed under conjugation: is "real". Better yet, 

+-- {: .un_prop}
######Proposition (Reality)
$\bar{u} \cdot (u v) = N(u)v$. 
=-- 

+-- {: .proof}
######Proof 
For all $w$, 

$$\langle \bar{u}\cdot (u v), w \rangle = \langle u v, u w \rangle = N(u)\langle v, w \rangle = \langle N(u)v, w \rangle$$ 

and the result follows from nondegeneracy. 
=--

This last result has several interesting corollaries. Putting $v = e$, we see that 

* $N(u) \neq 0$ implies $u$ is invertible, with $u^{-1} = \bar{u}/N(u)$. 

* $N(u) = 0$ implies $u$ is a zero divisor, with $\bar{u} u = 0$. 

In either case, we have from $\bar{u} = 2\langle u, e \rangle e - u$ the identity 

$$\bar{u} u = (2\langle u, e \rangle e - u)u = N(u)e$$ 

so that every element $u$ of a composition algebra satisfies a quadratic equation 

$$u^2 - 2\langle u, e \rangle u + N(u)e = 0.$$ 

This has as further consequence the fact that an algebra admits at most one norm making it a composition algebra (because the minimal monic polynomial of an element $u$ in a finite-dimensional algebra is uniquely determined; the norm of an element would the uniquely determined constant coefficient of its minimal polynomial). 

A final corollary of **"Reality"** is 

+-- {: .un_prop} 
######Proposition (Alternative law) 

$u \cdot (u v) = u^2 \cdot v$ and $u \cdot v^2 = (u v) \cdot v$. 
=--

+-- {: .proof} 
######Proof 
We have $w(u v) = (w u)v$ if $w$ is either $e$ or $\bar{u}$, and $u$ is a linear combination of $e$ and $\bar{u}$. The other equation is proven similarly.
=--

## Cayley-Dickson doubling construction

We begin with a simple observation: 

+-- {: .un_prop}
######Proposition
Let $V$ be a finite-dimensional vector space with a nondegenerate bilinear form, and let $W$ be a subspace such that the form on $V$ restricts to a nondegenerate form on $W$. Then 

$$V = W \oplus W^\perp$$ 

and the form on $V$ restricts to a nondegenerate form on $W^\perp$. 
=--

+-- {: .proof}
######Proof
The fact that $W \cap W^\perp = \{0\}$ is immediate from nondegeneracy of the form on $W$, and that $W + W^\perp = V$ follows from this and a simple dimension count ($dim(W^\perp) = dim((V/W)^*) = dim(V/W)$ and $dim(V) = dim(W) + dim(V/W)$). For the second assertion, we know that for $v \in W^\perp$, the map $\langle v, - \rangle |_W: W \to k$ is zero; if also $\langle v, - \rangle |_{W^\perp}: W^\perp \to k$ is zero, then $\langle v, - \rangle: V \to k$ is zero because $V = W + W^\perp$, and $v = 0$ follows from nondegeneracy of the form on $V$. 
=-- 

Thus, given a composition algebra $V$ and a composition subalgebra $W$ of $V$ (that is, a subspace closed under identity and multiplication, such that the norm on $V$ restricts to a nondegenerate form on $W$), the proposition shows there exists $\alpha \in W^\perp$ such that $N(\alpha) \neq 0$. This $\alpha$ is invertible, so $\alpha \cdot W$ has the same dimension as $W$. Moreover, for all $v, w \in W$ we have 

$$\langle \alpha v, w \rangle = \langle \alpha, w \bar{v} \rangle = 0$$ 

so that, by nondegeneracy of the form on $W$, $\alpha \cdot W \cap W = \{0\}$. Indeed, $\alpha W$ is orthogonal to $W$. It follows that $W + \alpha W$ has double the dimension of $W$. 

Now let us fix such an $\alpha$, and put $\lambda = N(\alpha)$. 

+-- {: .un_prop}
######Proposition
For elements $u, v, w, x \in W$, 

$$\langle u + \alpha v, w + \alpha x \rangle = \langle u, w \rangle + \lambda \langle v, x \rangle.$$ 
=--

+-- {: .proof}
######Proof
This follows from the identities 

$$\langle u, \alpha x \rangle = \langle u \bar{x}, \alpha \rangle = 0 \qquad \langle \alpha v, w \rangle = \langle \alpha, w \bar{v} \rangle = 0 \qquad \langle \alpha v, \alpha x \rangle = N(\alpha)\langle v, x \rangle$$ 

plus bilinearity of the form. 
=--

Consequently, if $\langle u + \alpha v, w \rangle = 0$ for all $w \in W$, we must have $u = 0$, and if $\langle u + \alpha v, \alpha x \rangle = 0$ for all $x \in W$, then $v = 0$. It follows that the form on $V$, when restricted to $W + \alpha W$, is nondegenerate. 

Now we want to show that the double $W + \alpha W$ is closed under multiplication, hence forms a composition subalgebra. It follows immediately from all this that $dim(V)$ is a power of 2, and in fact we will see later that the only possible dimensions are 1, 2, 4, and 8. Indeed, the structure of composition algebras is very tightly constrained. 

+-- {: .un_prop}
######Proposition (Conjugation on the double)
We have $\widebar{u + \alpha v} = \bar{u} - \alpha v$. Consequently, $\alpha v = - \widebar{\alpha v} = - \bar{v} \bar{\alpha} = \bar{v} \alpha$, and $\widebar{\alpha} = -\alpha$.  
=--

+-- {: .proof} 
######Proof
$\widebar{\alpha v} = 2\langle \alpha v, e \rangle e - \alpha v = -\alpha v$. 
=--

+-- {: .un_thm}
######Theorem (Closure under multiplication)
For all $u, v, w, x \in W$, $(u + \alpha v)(w + \alpha x) = (u w - \lambda x v) + \alpha (w v + \bar{u} x)$.
=--

+-- {: .proof}
######Proof
For all $y \in V$, we have the following sets of equations, using the previous proposition (Conj), the Exchange identity (Ex), and other identities frequently observed above (unlabeled as such). 

$$\langle u (\alpha x), y \rangle = \langle \alpha x, \bar{u} y \rangle \stackrel{Ex}{=} 0 - \langle \alpha y, \bar{u} x \rangle = \langle y, \alpha (\bar{u} x) \rangle = \langle \alpha (\bar{u} x), y \rangle$$ 

[ ]

$$\langle (\alpha v)w, y \rangle = \langle \alpha v, y \bar{w} \rangle \stackrel{Conj}{=} \langle \bar{v} \alpha, y \bar{w} \rangle \stackrel{Ex}{=} 0 - \langle \bar{v}\bar{w}, y \alpha \rangle = \langle (\bar{v}\bar{w})\alpha, y \rangle = \langle \widebar{w v} \alpha, y \rangle \stackrel{Conj}{=} \langle \alpha (w v), y \rangle$$

[ ] 

$$\langle (\alpha v)(\alpha x), y \rangle \stackrel{Conj}{=} -\langle \alpha v, y (\alpha x) \rangle \stackrel{Ex}{=} 0 + \langle \alpha (\alpha x), y v \rangle \stackrel{Conj}{=} -\langle \alpha x, \alpha (y v) \rangle = -\lambda \langle x, y v \rangle = \langle -\lambda x\bar{v}, y \rangle$$

These identities, combined with nondegeneracy of the form, give the result. 
=--



## References

* [wikipedia](http://en.wikipedia.org/wiki/Composition_algebra)

* Markus Rost, _On the dimension of a composition algebra_, Documenta  Mathematica __1__ (1996), 209-214, [files](http://www.math.uni-bielefeld.de/documenta/vol-01/10.html) Abstract: "The possible dimensions of a composition algebra are 1, 2, 4, or 8. We give a tensor categorical argument."

* John Baez's [comment](http://golem.ph.utexas.edu/category/2010/03/division_algebras_and_supersym.html#c032790)

* John H. Conway, Derek A. Smith, _On Quaternions and Octonions_, A.K. Peters, 2003.

Related $n$lab entries: [[alternative algebra]], [[Cayley-Dickson construction]]

Related eom entries: [Lie-admissible algebra](http://eom.springer.de/l/l058360.htm)