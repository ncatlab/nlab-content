
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Let $k$ be a [[field]] with [[characteristic]] $char(k) \neq 2$. A **composition algebra** over $k$ consists of a finite-dimensional [[vector space]] $V$ together with a 

* A nondegenerate symmetric bilinear form $\langle , \rangle: V \otimes V \to k$, 

* A multiplication map, i.e., a linear map $- \cdot -: V \otimes V \to V$, 

* A unit $e \in V$ for the multiplication, i.e., so that $e \cdot v = v = v \cdot e$, 

such that, putting $N(v) = \langle v, v \rangle$, 

* $N(u) N(v) = N(u v)$ (writing $u v$ for $u \cdot v$). 

There are no assumptions on the multiplication such as associativity, commutativity, etc. Examples of composition algebras include the real numbers, the complex numbers, the quaternions, the octonions, and the algebra of $2 \times 2$ matrices over a field. 

Since $char(k) \neq 2$, we can recover the bilinear form from the norm by the formula 

$$\langle u, v \rangle = \frac{N(u + v) - N(u) - N(v)}{2}$$ 

Since the bilinear form is nondegenerate, we may infer $u = v$ whenever 

$$\langle u, w \rangle = \langle v, w \rangle$$

and this will be frequently used in the sequel. 

Also since the form is nondegenerate, there exists $v \in V$ such that $N(v) \neq 0$. From $N(v) = N(e v) = N(e)N(v)$, it follows that $N(e) = 1$. 

## Properties

### Basic identities

The arrangements of the proofs below are based in part on the treatments by Conway and Smith, and by Springer and Veldkamp (see references below). 

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

#### Conjugation identities 

In any composition algebra, we may define a **conjugation** operator by 

$$\bar{v} = 2\langle v, e \rangle e - v$$

Observe that $\bar{v} = v$ just when $v$ is a scalar multiple of the identity. By analogy with the classical case (composition algebras over $\mathbb{R}$), such elements will be called **real**. 

The next few propositions develop properties of conjugation. 

+-- {: .un_prop}
######Proposition (Adjointness)
$\langle u v, w \rangle = \langle v, \bar{u}w \rangle$ and $\langle u v, w \rangle = \langle u, w\bar{v} \rangle$. $\langle w, u v \rangle = \langle \bar{u} w, v \rangle$ and $\langle w, u v \rangle = \langle w\bar{v}. u \rangle$. 
=-- 

+-- {: .proof}
######Proof
Put $x = e$ in the exchange identity to get the first equation in 

$$\langle u v, w \rangle = 2\langle u, w \rangle \langle v, e \rangle - \langle u, w v \rangle = \langle u, w(2\langle v, e\rangle e - v)\rangle = \langle u, w\bar{v} \rangle$$

The second adjointness equation is proved similarly; the final two come from symmetry of the form.  
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

A final corollary of **Reality** is 

+-- {: .un_prop} 
######Proposition (Alternative law) 

$u \cdot (u v) = u^2 \cdot v$ and $u \cdot v^2 = (u v) \cdot v$. 
=--

+-- {: .proof} 
######Proof 
We have $w(u v) = (w u)v$ if $w$ is either $e$ or $\bar{u}$, and $u$ is a linear combination of $e$ and $\bar{u}$. The other equation is proven similarly.
=--

These are the two axioms as given in [[alternative algebra]], but we remark that often a third alternative law is considered: $u (v u) = (u v) u$. For discussion of this in composition algebras, see the section on Moufang identities below. 

### Cayley-Dickson doubling construction

This is essentially the same as the [[Cayley-Dickson construction]], but in this section it is applied specifically to composition algebras where we have to deal with a norm, whereas the general construction applies to general (nonassociative) algebras equipped with an anti-involution. 

We begin with a simple observation: 

+-- {: .un_prop}
######Proposition
Let $V$ be a finite-dimensional vector space with a nondegenerate bilinear form, and let $W$ be a subspace such that the form on $V$ restricts to a nondegenerate form on $W$. Then 

$$V = W \oplus W^\perp$$ 

and the form on $V$ restricts to a nondegenerate form on $W^\perp$. 
=--

+-- {: .proof}
######Proof
The fact that $W \cap W^\perp = \{0\}$ is immediate from nondegeneracy of the form on $W$, and that $W + W^\perp = V$ follows from this and the fact that $dim(W) + dim(W^\perp) = dim(V)$ (use $dim(W^\perp) = dim((V/W)^*) = dim(V/W)$ and $dim(V) = dim(W) + dim(V/W)$). For the second assertion, we know that for $v \in W^\perp$, the map $\langle v, - \rangle |_W: W \to k$ is zero; if also $\langle v, - \rangle |_{W^\perp}: W^\perp \to k$ is zero, then $\langle v, - \rangle: V \to k$ is zero because $V = W + W^\perp$, and $v = 0$ follows from nondegeneracy of the form on $V$. 
=-- 

Thus, given a composition algebra $V$ and a composition subalgebra $W$ of $V$ (that is, a subspace closed under identity and multiplication, such that the norm on $V$ restricts to a nondegenerate form on $W$), the proposition shows there exists $\alpha \in W^\perp$ such that $N(\alpha) \neq 0$. This $\alpha$ is invertible, so $\alpha \cdot W$ has the same dimension as $W$. Moreover, for all $v, w \in W$ we have 

$$\langle \alpha v, w \rangle = \langle \alpha, w \bar{v} \rangle = 0$$ 

so that, by nondegeneracy of the form on $W$, $\alpha W \cap W = \{0\}$. Indeed, $\alpha W$ is orthogonal to $W$. It follows that $W + \alpha W$ has double the dimension of $W$. 

Now let us fix such an $\alpha$, and put $\lambda = N(\alpha)$. 

+-- {: .un_prop}
######Proposition
For elements $u, v, w, x \in W$, 

$$\langle u + \alpha v, w + \alpha x \rangle = \langle u, w \rangle + \lambda \langle v, x \rangle.$$ 
=--

+-- {: .proof}
######Proof
This follows from the equations 

$$\langle u, \alpha x \rangle = \langle u \bar{x}, \alpha \rangle = 0 \qquad \langle \alpha v, w \rangle = \langle \alpha, w \bar{v} \rangle = 0 \qquad \langle \alpha v, \alpha x \rangle = N(\alpha)\langle v, x \rangle$$ 

plus bilinearity of the form. 
=--

Consequently, if $\langle u + \alpha v, w \rangle = 0$ for all $w \in W$, we must have $u = 0$, and if $\langle u + \alpha v, \alpha x \rangle = 0$ for all $x \in W$, then $v = 0$. It follows that the form on $V$, when restricted to $W + \alpha W$, is nondegenerate. 

Now we want to show that the double $W + \alpha W$ is closed under multiplication, hence forms a composition subalgebra. It follows immediately from all this that, starting from the trivial composition subalgebra $k \cdot e$ of dimension 1, $dim(V)$ must be a power of 2, and in fact we will see later that the only possible dimensions are 1, 2, 4, and 8. Indeed, the possible structures of composition algebras are very tightly constrained. 

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
For all $u, v, w, x \in W$, $(u + \alpha v)(w + \alpha x) = (u w - \lambda x \bar{v}) + \alpha (w v + \bar{u} x)$.
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

#### Possible dimensions are 1, 2, 4, and 8. 

The calculation expressed by the fundamental theorem just stated has some remarkable consequences: 

* Suppose $V = W + \alpha W$. Then $W$ is an _associative_ composition algebra. 

For, by starting from the identity 

$$N(u + \alpha v)N(w + \alpha x) = N((u w - \lambda x \bar{v}) + \alpha (w v + \bar{u} x))$$ 

and expanding, one obtains 

$$(N(u) + \lambda N(v))(N(w) + \lambda N(x)) = N(u w) - 2\lambda \langle u w, x\bar{v} \rangle + \lambda^2 N(x\bar{v}) + \lambda (N(w v) + 2\langle w v, \bar{u} x \rangle + N(\bar{u}x))$$ 

Using the fact that $N$ is a homomorphism, plus unitarity $N(u) = N(\bar{u})$, further expansions and cancellations yield 

$$0 = -2\lambda \langle u w, x\bar{v} \rangle + 2\lambda \langle w v, \bar{u}x \rangle$$

which, by adjointness, yields 

$$\langle (u w)v, x \rangle = \langle u(w v), x \rangle$$ 

which by nondegeneracy on $W$, yields associativity $(u w)v = u(w v)$. 

* Suppose $V = W + \alpha W$ is an associative composition algebra. Then $W$ is a _commutative, associative_ composition algebra. 

For clearly the subalgebra $W$ must be associative; it is also commutative via the following string of equations (using conjugation of the double): 

$$\alpha(v w) = (\alpha v)w = (\bar{v}\alpha)w = \bar{v}(\alpha w) = \bar{v}(\bar{w} \alpha) = (\bar{v}\bar{w})\alpha = \widebar{w v}\alpha = \alpha (w v)$$

and cancelling out $\alpha$. 

Conversely, a lengthy but straightforward calculation shows that if $W$ is commutative and associative, then $V$ is associative. 

* Suppose $V = W + \alpha W$ is a commutative associative composition algebra. Then $W$ is purely real, i.e., is the trivial 1-dimensional associative commutative algebra $k \cdot e$. 

This results from 

$$\alpha w \stackrel{Conj}{=} \bar{w}\alpha \stackrel{comm}{=} \alpha \bar{w}$$ 

so that $w = \bar{w}$ for every $w \in W$, so that $w$ is real. Conversely, from 

$$(u + \alpha v)(w + \alpha x) = (u w - \lambda x\bar{v}) + \alpha (w v + \bar{u} x)$$

[ ] 

$$(w + \alpha x)(u + \alpha v) = (w u - \lambda v\bar{x}) + \alpha (u x + \bar{w} v)$$ 

together with commutativity and trivial conjugation in $W$, we infer commutativity in $V$. 

Hence the doubling process may be iterated three times at most.

This same result can also be proven using [[string diagram]] calculus.  See [this paper](http://math.ucr.edu/home/baez/Hurwitz.pdf) for a nice exposition of that route.

### Hurwitz's Theorem

The classification of composition algebras over specific fields (e.g., [[number field]]s, [[local field]]s) can be a bit intricate; in this section we concentrate solely on the classical case where $k = \mathbb{R}$, where the results have been known for a long time. 

A fundamental dichotomy is whether or not the composition algebra has zero divisors, i.e., elements $v$ such that $N(v) = 0$. If not, then the composition algebra is a division algebra (every nonzero element is invertible). If so, then the composition algebra is called a **split** composition algebra. We analyze each in turn. 

+-- {: .un_prop}
######Proposition
In a division composition algebra, all nonzero elements have positive norm. 
=--

+-- {: .proof} 
######Proof
If all elements $v$ orthogonal to the identity $e$ have positive norm, the result is immediate since 

$$N(r v + s e) = r^2 N(v) + s^2 \geq 0$$ 

Otherwise, if some such element $v$ has $N(v) = \lambda \lt 0$, we may put $u = v/|\lambda|^{1/2}$ so that $N(u) = -1$. Then $u$ is orthogonal to $e$ and 

$$N(u + e) = N(u) + N(e) = -1 + 1 = 0$$ 

which contradicts the assumption that all nonzero elements are invertible.
=--

In particular, any division composition algebra is a [[normed division algebra]].

Now let $V$ be a division composition algebra, with $V = W + \alpha W$, where $0 \neq \alpha \in W^\perp$. Put $j = \alpha/N(\alpha)^{1/2}$, so that $N(j) = 1$, $j \perp W$, and $V = W + j W$. We have the following possibilities. 

* $dim(V) = 2$. In that case $W$ is purely real and $V$ is a commutative field over $\mathbb{R}$ with $-j^2 = j\bar{j} = N(j) = 1$. This is of course the complex numbers, with 
$$N(s + j t) = s^2 + t^2$$ 
the usual norm. The conjugate of $s + j t$ is $s - j t$. 

* $dim(V) = 4$. In that case $W$ is a 2-dimensional division composition algebra, hence isomorphic to $\mathbb{C}$, and $V$ is an associative division algebra over $\mathbb{R}$ given by $V = \mathbb{C} + j\mathbb{C}$, where again $j^2 = -1$. (Evidently $V$ is not commutative because $W$ is not purely real.) By conjugation of the double, we have 
$$j i = -i j$$ 
where $i$ is an imaginary unit of $\mathbb{C}$, and we arrive at the algebra of quaternions $\mathbb{H}$ over $\mathbb{R}$, with orthonormal basis provided by $1, i, j, k = i j$. Conjugation is given by the usual operation
$$a + b i + c j + d k \mapsto a - b i - c j - d k$$

* $dim(V) = 8$. In that case $W$ is a 4-dimensional division composition algebra, hence isomorphic to $\mathbb{H}$, and $V$ is an alternative division algebra over $\mathbb{R}$ given by $V = \mathbb{H} + j\mathbb{H}$, with $j^2 = -1$. ($V$ is not associative because $W$ is not commutative.) The structure of multiplication is given by the theorem above and the resulting algebra is the algebra of octonions, with the standard norm and conjugation. 

Thus, we have established 

+-- {: .un_thm}
######Theorem (Hurwitz) 
The only division composition algebras over $\mathbb{R}$ are the reals, complexes, quaternions, and octonions. 
=-- 

#### Split composition algebras

Now we turn to split composition algebras $V$. It turns out that the structure of these is _not_ specific to the field $\mathbb{R}$: the classification of possible split composition algebras is the same over any field (see the text by Springer and Veldkamp), although we will continue to work over $\mathbb{R}$ as we describe them below. 

Suppose $V = W + \alpha W$, where $\alpha \in W^\perp$, $N(\alpha) \neq 0$. Put $j = \alpha/|N(\alpha)|^{1/2}$, so $|N(j)| = 1$, $V = W + j W$. In addition to the trivial 1-dimensional case, we have the following possibilities. 

* $dim(V) = 2$. In this case $N(j) = -1$ (else $V$ would be a division algebra, not a split composition algebra) and $j^2 = 1$ (we are now using $1$ to denote the identity). The elements 
$$e_1 = \frac{1 + j}{2} \qquad e_2 = \frac{1-j}{2}$$ 
are primitive idempotents, conjugate to one another, and $V \cong \mathbb{R} e_1 \oplus \mathbb{R} e_2$ as a product ring. The norm of an element $x e_1 + y e_2$ is $N(x e_1 + y e_2) = x y$. 

* $dim(V) = 4$. Let $i$ be an imaginary unit of $W$, so $\bar{i} = -i$ and $|N(i)| = 1$. Here either $N(i) = -1$ ($W$ is split), or $N(i) = 1$ ($W$ is isomorphic to $\mathbb{C}$). In the second instance, $N(j) = -1$, else $V$ would be a division algebra, and we may replace $W$ by the split algebra $W' = \mathbb{R} + \mathbb{R} i j$ and still have $V = W' + j W'$. So without loss of generality we may assume $W$ is split; therefore, there is up to isomorphism only one split composition algebra of dimension 4. This is the algebra of $2 \times 2$ matrices $A$, for which $N(A) = det(A)$ and $W$ is embedded as the subalgebra of diagonal matrices; the element $j$ may be taken to be the matrix $A$ with $a_{11} = a_{22} = 0$, $a_{12} = a_{21} = 1$. The conjugate of a matrix $A$ is $\bar{A} = Tr(A)I - A$, which leads to the familiar formula for $det(A) A^{-1}$ when $A$ is invertible. 

* $dim(V) = 8$. Again, by an argument similar to the one used for the case of dimension 4, we may assume a maximal proper composition subalgebra $W$ is split, and up to isomorphism there is only one split composition algebra of dimension 8, aka the **split octonions**. The multiplication may be deduced from the fundamental result on doubling multiplication above, or may be expressed as follows. Denote scalars by letters like $r, s$ and 3-vectors by letters like $x, y$. Let $\langle x, y \rangle$ denote the standard inner product 
$$x_1 y_1 + x_2 y_2 + x_3 y_3$$ 
and let $x \wedge y$ denote the standard cross-product, so that $\langle x \wedge y, z \rangle = det(x, y, z)$. Elements of $V$ are represented by $2 \times 2$ arrays 
$$\left( 
\begin{aligned}
r & x\\
y & s
\end{aligned}
\right)$$
and multiplication is given by the following formula, highly reminiscent of matrix multiplication but with some cross-product cross terms: 
$$\left(
\begin{aligned}
r & x\\
y & s
\end{aligned}
\right) 
\cdot
\left(
\begin{aligned}
r' & x'\\
y' & s'
\end{aligned}
\right) = 
\left(
\begin{aligned}
r r' + \langle x, y' \rangle & r x' + s' x + y \wedge y'\\ 
r' y + s y' + x \wedge x' & \langle y, x' \rangle + s s'
\end{aligned}
\right)
$$
The norm is given by a kind of determinant formula 
$$N\left(
\begin{aligned}
r & x\\
y & s
\end{aligned}
\right) = r s - \langle x, y \rangle
$$

### Moufang identities

Further consequences of the composition algebra axioms include the Moufang laws which are important in the study of octonions. 

**Moufang identities** 

* $(u v)(w u) = (u(v w))u) = u((v w)u)$ 

* $((u v)u)w = u(v(u w))$

* $((u v)w)v = u(v(w v))$

We will prove the first of these; the others are proven in similar style (see Springer-Veldkamp for details). (It may be tricky to remember how the bracketings go, but one thing to remember is that the bracketings shouldn't lead to proofs of general associativity when interpreted in a division algebra!) 

+-- {: .proof}
######Proof 
We have

$$\array{
\langle (u v)(w u), x \rangle & = & \langle u v, x(\bar{u}\bar{w})\rangle\\ & \stackrel{Ex}{=} & 2\langle u, x\rangle\langle v, \bar{u}\bar{w} \rangle - \langle u(\bar{u}\bar{w}), x v \rangle \\ 
 & = & 2\langle u, x\rangle\langle v w, \bar{u} \rangle - \langle \bar{u}\bar{w}, \bar{u}(x v) \rangle \\
 & = & 2\langle v w, \bar{u} \rangle\langle u, x\rangle - N(u)\langle \bar{w}\bar{v}, x \rangle \\ 
 & = & 2\langle v w, \bar{u} \rangle\langle u, x\rangle - N(u)\langle \widebar{v w}, x \rangle
}$$ 

which makes it plain that $(u v)(w u)$ depends on $u$ and $v w$ only. Hence we get the same result if we replace $v$ and $w$ and any two elements whose product is $v w$, say $v w$ and $e$. In other words, 

$$(u v)(w u) = (u(v w))(e u) = (u(v w))u, \qquad (u v)(w u) = (u e)((v w)u) = u((v w)u)$$ 

which completes the proof. 
=--
 
+-- {: .un_cor}
######Corollary
For all $u$, $v$ in a composition algebra, the third alternative law holds: $u(v u) = (u v)u$.
=--

## References

* Markus Rost, _On the dimension of a composition algebra_, Documenta  Mathematica __1__ (1996), 209-214, [files](http://www.math.uni-bielefeld.de/documenta/vol-01/10.html) Abstract: "The possible dimensions of a composition algebra are 1, 2, 4, or 8. We give a tensor categorical argument."

* [[John Baez]]'s [comment](http://golem.ph.utexas.edu/category/2010/03/division_algebras_and_supersym.html#c032790)

* [[Bruce Westbury]], _[Hurwitz's Theorem](http://math.ucr.edu/home/baez/Hurwitz.pdf)_

* [[John Conway]], Derek A. Smith, _On Quaternions and Octonions_, A.K. Peters, 2003. 

* T.A. Springer, F.D. Veldkamp, _Octonions, Jordan algebras, and exceptional groups_, Springer Monographs in Mathematics, Springer-Verlag 2000. 

* [wikipedia](http://en.wikipedia.org/wiki/Composition_algebra)


Related $n$lab entries: [[alternative algebra]], [[Cayley-Dickson construction]]

Related eom entries: [Lie-admissible algebra](http://eom.springer.de/l/l058360.htm)
