Classically, the **fundamental theorem of algebra** states that 

* The [[field]] of [[complex number]]s $\mathbb{C}$ is [[algebraically closed field|algebraically closed]]. In other words, every polynomial with coefficients in $\mathbb{C}$ has a root in $\mathbb{C}$. 

Many proofs of this theorem are known; some use complex analysis (the reciprocal of a polynomial cannot be bounded), some use algebraic topology (the degree of a map is invariant with respect to homotopy), and some use advanced calculus (polynomial functions on the complex numbers are open mappings). All of these proofs involve, at some level, the fact that the real numbers are [[Dedekind real number|Dedekind complete]], which has as a classical consequence the fact that the real numbers are archimedean. 

The following proof is algebraic and, unlike the proof methods cited above, applies more generally to [[real closed field]]s, which need not be archimedean. It is due to Emil Artin, and forms a basic chapter in the Artin-Schreier theory of real closed fields. (Of course, the fact that the real numbers form a real closed field uses Dedekind completeness.)

We recall that a _real closed field_ is an ordered field such that every positive element has a square root, and every polynomial of odd degree has a root. Clearly the polynomial $x^2 + 1$ has no root in a real closed field. 

+-- {: .un_thm}
######Theorem 
If $F$ is real closed, then $K = F[\sqrt{-1}]$ is algebraically closed. 
=--

+-- {: .proof} 
######Proof 
We must show that any irreducible polynomial $p$ with coefficients in $K$ has a root in $K$. 

The splitting field of $p$ is a finite Galois extension $L$ of $F$, with Galois group $G$. If $G(2)$ is the Sylow 2-group of $G$, then the fixed field of $G(2)$ is an odd degree extension of $F$, given by the splitting field of an odd degree irreducible polynomial $q$ over $F$. But since $F$ is real closed, $q$ has a root in $F$; by irreducibility, the degree must be 1, so that in fact $G = G(2)$. We have $|G| \gt 1$ since the splitting field contains $K$. 

So $G$ is a 2-group. But for any prime $p$, a finite $p$-group has nontrivial center, and is therefore solvable by an inductive argument. Therefore the extension $L/F$ arises from a tower of non-trivial quadratic extensions 

$$F \subseteq L_1 \subseteq \ldots \subseteq L_n = L$$ 

By the [[quadratic formula]], the first field $L_1$ arises by adjoining roots to $F$ of a polynomial $x^2 + a x + b$, 

$$\frac{-a \pm \sqrt{a^2 - 4b}}{2},$$ 

where $a^2 - 4b$ is negative. Since $F$ is real closed, the positive element $4b - a^2$ has a square root in $F$, so that the roots displayed above belong to $K = F[\sqrt{-1}]$. So $L_1 = K$. But $K$ has no nontrivial quadratic extensions by the lemma that follows, so in fact $L_1 = L_n = K$ and the theorem is proved. 
=-- 

+-- {: .un_lem}
######Lemma 
Every element of $K = F[\sqrt{-1}]$ has a square root in $K$. 
=-- 

+-- {: .proof} 
######Proof 
The proof is most easily apprehended by analogy with polar coordinate representations of complex numbers and half-angle formulas, where a square root of $r e^{i\theta}$ is given by $r^{1/2}e^{i\theta /2}$. Let $i$ be a fixed square root of $-1$, and let $a + b i$ be an arbitrary element of $K$, with $a, b \in F$. We must solve $(x + y i)^2 = a + b i$, i.e., find $x, y \in F$ such that 

$$x^2 - y^2 = a, \qquad 2x y = b$$ 

Since $a^2 + b^2$ has a square root in $F$, we may assume without loss of generality that $a^2 + b^2 = 1$. By interchanging $x$ and $y$ if necessary, we may assume $a \geq 0$; by replacing $y$ by $-y$ if necessary, we may also assume $b \geq 0$. Since $0 \leq a \leq 1$, we may choose nonnegative $x$ and $y$ such that 

$$x^2 = \frac{1+a}{2}, \qquad y^2 = \frac{1-a}{2}$$ 

and this provides the solution. 
=--
