
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
* table of contents
{:toc}

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
 
+-- {: .num_cor}
######Corollary

For all $u$, $v$ in a composition algebra, the third alternative law holds: $u(v u) = (u v)u$.

=-- 

See also [[Moufang loop]]. 


## Related $n$Lab entries

* [[alternative algebra]]

* [[Cayley-Dickson construction]]


## References

* {#SpringerVeltkamp00} [[Tonny Springer]], [[Ferdinand Veldkamp]], chapter 1 of _Octonions, Jordan Algebras, and Exceptional Groups_, Springer Monographs in Mathematics, 2000

* {#Rost96} Markus Rost, _On the dimension of a composition algebra_, Documenta  Mathematica __1__ (1996), 209-214, [files](http://www.math.uni-bielefeld.de/documenta/vol-01/10.html) Abstract: "The possible dimensions of a composition algebra are 1, 2, 4, or 8. We give a tensor categorical argument."

A general abstract formulation of [Rost 96](#Rost96) in terms of [[string diagrams]] in [[additive category|additive]] [[braided monoidal categories]] is in

* {#Street18} [[Ross Street]], _Vector product and composition algebras in braided monoidal additive categories_ ([arXiv:1812.04143](https://arxiv.org/abs/1812.04143))


An exposition of the [[string diagram]] proof of the [Hurwitz' theorem](HurwitzTheoremSection) on the classification of compositon algebras is given in

* [[Bruce Westbury]], _Hurwitz' theorem on composition algebras_ ([arXiv:1011.6197](http://arxiv.org/abs/1011.6197))

* [[John Baez]]'s [comment](http://golem.ph.utexas.edu/category/2010/03/division_algebras_and_supersym.html#c032790)

See also

* [[John Conway]], Derek A. Smith, _On Quaternions and Octonions_, A.K. Peters, 2003. 

* T.A. Springer, F.D. Veldkamp, _Octonions, Jordan algebras, and exceptional groups_, Springer Monographs in Mathematics, Springer-Verlag 2000. 

* [wikipedia](http://en.wikipedia.org/wiki/Composition_algebra)


* [[eom]]: [Lie-admissible algebra](http://eom.springer.de/l/l058360.htm)



