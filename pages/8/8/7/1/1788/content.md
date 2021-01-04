
#Contents#
* table of contents
{:toc}

### Cayley-Dickson doubling construction

This is essentially the same as the [[Cayley-Dickson construction]], but in this section it is applied specifically to composition algebras where we have to deal with a norm, whereas the general construction applies to general (nonassociative) algebras equipped with an anti-involution. 

We begin with a simple observation: 

+-- {: .num_prop}
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

+-- {: .num_prop}
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

+-- {: .num_prop}
######Proposition (Conjugation on the double)
We have $\widebar{u + \alpha v} = \bar{u} - \alpha v$. Consequently, $\alpha v = - \widebar{\alpha v} = - \bar{v} \bar{\alpha} = \bar{v} \alpha$, and $\widebar{\alpha} = -\alpha$.  
=--

+-- {: .proof} 
######Proof
$\widebar{\alpha v} = 2\langle \alpha v, e \rangle e - \alpha v = -\alpha v$. 
=--

+-- {: .num_theorem}
######Theorem (Closure under multiplication)
For all $u, v, w, x \in W$, $(u + \alpha v)(w + \alpha x) = (u w - \lambda x \bar{v}) + \alpha (w v + \bar{u} x)$.
=--

+-- {: .proof}
######Proof
For all $y \in V$, we have the following sets of equations, using the previous proposition (Conj), the Exchange identity (Ex), and other identities frequently observed above (unlabeled as such). 

$$\langle u (\alpha x), y \rangle = \langle \alpha x, \bar{u} y \rangle \stackrel{Ex}{=} 0 - \langle \alpha y, \bar{u} x \rangle = \langle y, \alpha (\bar{u} x) \rangle = \langle \alpha (\bar{u} x), y \rangle$$ 

$$\langle (\alpha v)w, y \rangle = \langle \alpha v, y \bar{w} \rangle \stackrel{Conj}{=} \langle \bar{v} \alpha, y \bar{w} \rangle \stackrel{Ex}{=} 0 - \langle \bar{v}\bar{w}, y \alpha \rangle = \langle (\bar{v}\bar{w})\alpha, y \rangle = \langle \widebar{w v} \alpha, y \rangle \stackrel{Conj}{=} \langle \alpha (w v), y \rangle$$

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

$$(w + \alpha x)(u + \alpha v) = (w u - \lambda v\bar{x}) + \alpha (u x + \bar{w} v)$$ 

together with commutativity and trivial conjugation in $W$, we infer commutativity in $V$. 

Hence the doubling process may be iterated three times at most.

This same result can also be proven using [[string diagram]] calculus.  See [this paper](http://math.ucr.edu/home/baez/Hurwitz.pdf) for a nice exposition of that route.



### Hurwitz's Theorem 
 {#HurwitzTheoremSection}


The classification of composition algebras over specific fields (e.g., [[number field]]s, [[local fields]]) can be a bit intricate; in this section we concentrate solely on the classical case where $k = \mathbb{R}$ is the [[real numbers]], where the results have been known for a long time, known as the _[[Hurwitz theorem]]_. 

A fundamental dichotomy is whether or not the composition algebra has zero divisors, i.e., elements $v$ such that $N(v) = 0$. If not, then the composition algebra is a division algebra (every nonzero element is invertible). If so, then the composition algebra is called a **split** composition algebra. We analyze each in turn. 

+-- {: .num_prop}
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

Thus, we have established the [[Hurwitz theorem]]

+-- {: .num_theorem}
######Theorem (Hurwitz) 

The only [[division algebra|division]] composition algebras over the [[real numbers]] $\mathbb{R}$ are the [[real numbers]], [[complex numbers]], [[quaternions]], and [[octonions]]. 

=-- 


#### Split composition algebras

Now we turn to split composition algebras $V$. It turns out that the structure of these is _not_ specific to the field $\mathbb{R}$: the classification of possible split composition algebras is the same over any field (see the text by Springer and Veldkamp), although we will continue to work over $\mathbb{R}$ as we describe them below. 

Suppose $V = W + \alpha W$, where $\alpha \in W^\perp$, $N(\alpha) \neq 0$. Put $j = \alpha/|N(\alpha)|^{1/2}$, so $|N(j)| = 1$, $V = W + j W$. In addition to the trivial 1-dimensional case, we have the following possibilities. 

* $dim(V) = 2$. In this case $N(j) = -1$ (else $V$ would be a division algebra, not a split composition algebra) and $j^2 = 1$ (we are now using $1$ to denote the identity). The elements 
$$e_1 = \frac{1 + j}{2} \qquad e_2 = \frac{1-j}{2}$$ 
are primitive idempotents, conjugate to one another, and $V \cong \mathbb{R} e_1 \oplus \mathbb{R} e_2$ as a product ring. The norm of an element $x e_1 + y e_2$ is $N(x e_1 + y e_2) = x y$. 

* $dim(V) = 4$. Let $i$ be an imaginary unit of $W$, so $\bar{i} = -i$ and $|N(i)| = 1$. Here either $N(i) = -1$ ($W$ is split), or $N(i) = 1$ ($W$ is isomorphic to $\mathbb{C}$). In the second instance, $N(j) = -1$, else $V$ would be a division algebra, and we may replace $W$ by the split algebra $W' = \mathbb{R} + \mathbb{R} i j$ and still have $V = W' + j W'$. So without loss of generality we may assume $W$ is split; therefore, there is up to isomorphism only one split composition algebra of dimension 4. This is the algebra of $2 \times 2$ matrices $A$, for which $N(A) = det(A)$ and $W$ is embedded as the subalgebra of diagonal matrices; the element $j$ may be taken to be the matrix $A$ with $a_{11} = a_{22} = 0$, $a_{12} = a_{21} = 1$. The conjugate of a matrix $A$ is $\bar{A} = Tr(A)I - A$, which leads to the familiar formula for $det(A) A^{-1}$ when $A$ is invertible. 

* $dim(V) = 8$. Again, by an argument similar to the one used for the case of dimension 4, we may assume a maximal proper composition subalgebra $W$ is split, and up to isomorphism there is only one split composition algebra of dimension 8, aka the [[split octonions]]. The multiplication may be deduced from the fundamental result on doubling multiplication above, or may be expressed as follows. Denote scalars by letters like $r, s$ and 3-vectors by letters like $x, y$. Let $\langle x, y \rangle$ denote the standard inner product 
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

