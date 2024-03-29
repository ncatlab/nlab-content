
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Characteristic polynomial and Cayley-Hamilton theorem. 

See also _[[determinant]]_.

+-- {: .num_lemma}
###### Lemma 

Let $R$ be a [[commutative ring]], and let $A$ be an $n \times n$ [[matrix]] with entries in $R$. Then there exists an $n \times n$ matrix $\tilde{A}$ with entries in $R$, called the **adjugate** of $A$, such that $A \tilde{A} = \tilde{A} A = \det(A) \cdot I_n$. 

=-- 

+-- {: .proof}
###### Proof 
We may as well take $R$ to be the [[polynomial ring]] $\mathbb{Z}[a_{i j}]_{1 \leq i, j \leq n}$, since we are then free to interpret the indeterminates $a_{i j}$ however we like along a ring map $\mathbb{Z}[a_{i j}] \to R$. Let $A = (a_{i j})$ denote the corresponding generic matrix. 

Guided by Cramer's rule (see [[determinant]]), put 

$$\tilde{A}_{j i} = \det(a_1, \ldots, e_i, \ldots a_n),$$ 

the $a_i$ being columns of $A$ and $e_i$, the column vector with $1$ in the $i^{th}$ row and $0$'s elsewhere, appearing as the $j^{th}$ column. If we pretend $A$ is invertible, then we know $A \tilde{A} = \det(A) \cdot I_n = \tilde{A} A$ by [[Cramer's rule]]. We claim this holds for general $A$. 

Indeed, we can interpret this as a [[polynomial]] equation in $\mathbb{C}[a_{i j}]$ and check it there. As an equation between polynomial functions on the space of matrices $A \in Mat_n(\mathbb{C}) = Spec(\mathbb{C}[a_{i j}])$, it holds on the dense subset $GL_n(\mathbb{C}) \hookrightarrow Mat_n(\mathbb{C})$. Therefore, by continuity, it holds on all of $Mat_n(\mathbb{C})$. But a polynomial function equation with coefficients in $\mathbb{C}$ implies the corresponding polynomial identity, and the proof is complete. 
=-- 

An alternative proof that avoids appeal to a continuity 
argument may be given in terms of [[exterior algebra]]. Start by observing that the equation $\widetilde{A} A = \det(A) \cdot 1_n$ holds over $R = \mathbb{Z}[a_{i j}]$ if it holds over a field $k$ in which $R$ embeds. If $V$ is an $n$-dimensional vector space over $k$ and $A\colon V \to V$ is $k$-linear, then the natural transformation 

$$\wedge \colon V \otimes_k \Lambda^{n-1} V \to \Lambda^n V$$ 

gives an exact pairing $V \otimes_k \Lambda^{n-1} V \to k$ which induces an isomorphism $V \cong (\Lambda^{n-1} V)^\ast$, and the adjugate $\widetilde{A}: V \to V$ is defined to be the evident composite 

$$V \cong (\Lambda^{n-1} V)^\ast \stackrel{(\Lambda^{n-1} A)^\ast}{\to} (\Lambda^{n-1} V)^\ast \cong V.$$ 

The equation $\widetilde{A} A = \det A \cdot 1_V$ holds iff the perimeter of the diagram 

\begin{tikzcd}
V \ar[r, "A"] \ar[dr, swap, "\det A \cdot 1_V"] & V \ar[r, "\sim"] \ar[d, "\widetilde{A}"] & (\Lambda^{n-1} V)^\ast \ar[d, "(\Lambda^{n-1} A)^\ast"] \\ 
& V \ar[r, "\sim"] & (\Lambda^{n-1} V)^\ast 
\end{tikzcd} 

commutes, but this is equivalent to commutativity of the naturality square 

\begin{tikzcd} 
V \otimes_k \Lambda^{n-1} V \ar[r, "\wedge"] \ar[d, swap, "A \otimes_k \Lambda^{n-1} A"] & \Lambda^n V \ar[d, "\det A \cdot Id"] \\ V \otimes_k \Lambda^{n-1} V \ar[r, "\wedge"] & \Lambda^n V
\end{tikzcd} 

and this completes the proof. 

+-- {: .num_theorem}
###### Theorem 
(**Cayley-Hamilton**) 
Let $V$ be a finitely generated free module over a commutative ring $R$, and let $f \colon V \to V$ be an $R$-module map. Let $p(t) \in R[t]$ be the **characteristic polynomial** $\det(t \cdot 1_V - f)$ of $f$, and let $\phi_f \colon R[t] \to Mod_R(V, V)$ be the unique $R$-algebra map sending $t$ to $f$. Then $p(f) \coloneqq \phi_f(p)$ is the zero map $0 \colon V \to V$. 

=-- 

+-- {: .proof} 
###### Proof 
Via $\phi_f$, regard $V$ as an $R[t]$-module, and with regard to some $R$-basis $\{v_i\}_{1 \leq i \leq n}$ of $V$, represent $f$ by a matrix $A$. Now consider $t \cdot I_n - A$ as an $n \times n$ matrix $B(t)$ with entries in $R[t]$. By definition of the module structure, this matrix $B(t)$, seen as acting on $V^n$, annihilates the length $n$ column vector $c$ whose $i^{th}$ row entry is $v_i$. 

By the previous lemma, there is $\tilde{B}(t)$ such that $\tilde{B}(t) B(t)$ is $\det(t \cdot I_n - A)$ times the identity matrix. It follows that 

$$\det(t \cdot I_n - A) c = \tilde{B}(t) B(t) c = \tilde{B}(t) 0 = 0$$ 

i.e., $\det(t \cdot I_n - A) \cdot v_i = 0$ for each $i$. Since the $v_i$ form an $R$-basis, the $R[t]$-scalar $\det(t \cdot I_n - A)$ annihilates the $R[t]$-module $V$, as was to be shown. 
=-- 

The Cayley-Hamilton theorem easily generalizes to finitely generated $R$-modules (not necessarily free) as follows. Let $f \colon V \to V$ be a module endomorphism, and suppose $\pi \colon R^n \to V$ is an epimorphism. Since $R^n$ is projective, the map $f \circ \pi$ can be lifted through $\pi$ to a map $A \colon R^n \to R^n$. Let $P(t)$ be the characteristic polynomial of $A$. 

+-- {: .num_prop #lem}
###### Proposition 
$P(f) = 0$. 
=-- 

+-- {: .proof} 
###### Proof 
Write $P(t) = \sum_i a_i t^i$. We already know $P(A) = 0$. From $f \circ \pi = \pi \circ A$, it follows that $f^i \circ \pi = \pi \circ A^i$ for any $i \geq 0$. Hence $P(f) \circ \pi = \pi \circ P(A) = 0$. Since $\pi$ is epic, $P(f) = 0$ follows. 
=-- 

We give an interesting and perhaps surprising consequence of the Cayley-Hamilton theorem below, after establishing a lemma close in spirit to [[Nakayama's lemma]]. 

+-- {: .num_lemma} 
###### Lemma 
Suppose $V$ is a finitely generated $R$-module, and $g \colon V \to V$ is a module map such that $g(V) \subseteq I V$ for some ideal $I$ of $R$. Then there is a polynomial $p(t) = t^n + a_1 t^{n-1} + \ldots + a_n$, with all $a_i \in I$, such that $p(g) = 0$. 
=-- 

+-- {: .proof} 
###### Proof 
For some finite $n \geq 0$, we have a surjective map $p: R^n \to V$. Tensoring $p$ with $I$, we obtain a surjective map $I^n \cong I \otimes_R R^n \stackrel{I \otimes_R p}{\twoheadrightarrow} I \otimes_R V \stackrel{mult}{\twoheadrightarrow} I V$, fitting in a commutative diagram 

$$\array{
 & & & & & & I^n & \hookrightarrow & R^n \\
 & & & & & & \downarrow & & \downarrow _\mathrlap{p} \\
R^n & \stackrel{p}{\to} & V & \stackrel{g}{\to} & im(g) & \stackrel{i}{\hookrightarrow} & I V & \hookrightarrow & V 
}$$

By projectivity of $R^n$, we can lift $i g p: R^n \to I V$ to a map $h: R^n \to I^n$ making the diagram commute. Let $A$ be the $R$-module map $R^n \stackrel{h}{\to} I^n \hookrightarrow R^n$, regarded as a matrix. Then the characteristic polynomial of $A$ satisfies the conclusion, by the Cayley-Hamilton theorem and Proposition \ref{lem}. 
=-- 

+-- {: .num_prop #surj}
###### Proposition 
Let $V$ be a finitely generated module over a commutative ring $R$, and let $f \colon V \to V$ be a surjective module map. Then $f$ is an isomorphism. 
=-- 

+-- {: .proof} 
###### Proof 
Regard $V$ as a finitely generated $R[t]$-module via $\phi_f \colon R[t] \to Mod_R(V, V)$. Since $f$ is assumed surjective, we have $I V = V$ for the ideal $I = (t)$ of $R[t]$. Now take $g = 1_V$ as in the preceding lemma, a module map over the ring $R' = R[t]$. By the lemma, we see that 
$g^n + a_1 g^{n-1} + \ldots + a_n = 0$ where $a_i \in (t)$, in other words the $R[t]$-scalar 

$$(1 + a_1 + \ldots + a_n)1_V = 0$$ 

as an operator on $V$. Write $a_i = b_i(t) t$ for polynomials $b_i(t) \in R[t]$. Now we may rewrite the previous displayed equation as 

$$1_V(v) = -(\sum_i b_i(t)) t \cdot v$$ 

for all $v \in V$, which translates into saying that $1_V = -\sum_i b_i(f) f$, i.e., that $-\sum_i b_i(f)$ is a retraction of $f$. Since $f$ is epic, we now see $f$ is an isomorphism. 
=-- 

## Examples

* Characteristic polynomials of [[Frobenius homomorphisms]] acting via [[Galois representations]] constitute [[Artin L-functions]].

## References

The proof of the Cayley-Hamilton theorem follows the treatment in 

* Serge Lang, _Algebra_ ($3^{rd}$ edition), Addison-Wesley, 1993. 

The proof of Proposition \ref{surj} on surjective endomorphisms of finitely generated modules was extracted from 

* Stacks Project, Commutative Algebra, section 15 ([pdf](http://math.columbia.edu/algebraic_geometry/stacks-git/algebra.pdf))


[[!redirects Cayley-Hamilton theorem]]

[[!redirects characteristic polynomials]]
